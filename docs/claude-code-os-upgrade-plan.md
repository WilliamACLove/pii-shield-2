# Claude Code OS Upgrade Plan for PII-Shield

Status: proposed
Scope: repo-level agent infrastructure (`CLAUDE.md`, `.claude/`, hooks, agents, evals) — no product code changes.

The organizing question for every item below is: **"Which file enforces this tomorrow?"**
If the answer is "nowhere", the item is wishful thinking and is either given an enforcing
file or dropped.

---

## Phase 0 — Audit: what actually exists today

An outside-in audit of the repo as an agent sees it on session start:

| Asset | Reality |
| --- | --- |
| `CLAUDE.md` | **Does not exist.** Every session rediscovers build/test commands from scratch. |
| `.claude/` (settings, agents, skills, hooks) | **Does not exist.** No permissions allowlist, no hooks, no subagent definitions. |
| `operator/AGENTS.md` | Exists, but is ~320 lines of generic kubebuilder scaffolding documentation. Only discovered if an agent happens to enter `operator/`. Contains almost nothing PII-Shield-specific. |
| Verification knowledge | Scattered across `CONTRIBUTING.md`, `.github/workflows/ci.yml`, `scripts/*.sh`, `MANUAL_TESTING.md`, `operator/Makefile`. No single machine-readable source. |
| Memory / decision log | `notes/` exists but has no operational log format. |

Cracks found during the audit (these become eval cases in Phase 5):

1. **Broken documented command.** `CONTRIBUTING.md` says `go test ./... -v -fuzz=Fuzz`.
   Go rejects `-fuzz` with multiple packages; the working invocation is what CI uses:
   `go test -fuzz=FuzzScanner -fuzztime=15s ./pkg/scanner`. An agent following the
   contributing guide fails on its first verification attempt.
2. **Two Go modules, easy to half-test.** The repo root and `operator/` are separate
   modules. `go test ./...` from the root does **not** test the operator. CI runs both;
   `scripts/test-unit.sh` runs only the root module (and excludes `cmd/wasm`). Nothing
   tells an agent this except reading the CI YAML.
3. **Hidden merge gates.** CI enforces ≥70% total coverage, `-race`, golangci-lint
   v2.12.2 (`only-new-issues`), actionlint, a Helm runtime check, and a multi-arch
   image build. None of this is surfaced anywhere an agent reads by default, so "tests
   pass locally" routinely diverges from "CI is green".
4. **`operator/AGENTS.md` is boilerplate.** The genuinely load-bearing rules (never
   edit `zz_generated.*`, run `make manifests generate` after touching `*_types.go`,
   keep `+kubebuilder:scaffold` markers) are buried in generic CLI tutorials.

## Phase 1 — Foundation: CLAUDE.md + settings (highest value, do first)

**1a. Root `CLAUDE.md` (~60 lines, verified commands only).** Contents:

- One-paragraph orientation: log-sanitization sidecar; three deliverables (CLI
  `cmd/cleaner`, operator in `operator/` — *separate Go module*, WASM SDKs in `sdks/`).
- Verification matrix (each command test-run before being written down):

  | You changed | Run |
  | --- | --- |
  | `pkg/`, `cmd/` | `go test -race ./...` (root) |
  | `pkg/scanner` | + `go test -fuzz=FuzzScanner -fuzztime=15s ./pkg/scanner`; perf-sensitive: `go test -bench=. -benchmem ./pkg/scanner` |
  | `operator/` | `cd operator && make lint-fix test`; after `*_types.go`: `make manifests generate` |
  | `charts/` | `scripts/verify-helm-runtime.sh` |
  | Dockerfiles/agent image | `scripts/verify-agent-multiarch-build.sh` |
  | `.github/workflows/` | actionlint |

- Hard gates that CI will enforce anyway: coverage ≥70% total, race detector, golangci
  v2.12.2, gofmt.
- Pointers, not copies: `docs/threat-model.md`, `KNOWN_LIMITATIONS.md`,
  `operator/AGENTS.md`. Keep the root file short; deep content stays where it lives.

**1b. `.claude/settings.json`** with a permissions allowlist for the commands above
(`go test`, `go build`, `gofmt`, `make` in operator, the `scripts/*.sh` verifiers), so
routine verification never stalls on prompts.

**1c. Slim `operator/AGENTS.md`** to the ~40 repo-specific lines (never-edit list,
regen commands, envtest/Ginkgo notes, kind-cluster warning for e2e) and link it from
root `CLAUDE.md`. Move nothing new in; delete generic kubebuilder tutorial content —
the Kubebuilder Book link covers it.

**1d. Fix the broken command in `CONTRIBUTING.md`** (audit crack #1) — humans hit it too.

*Enforced tomorrow by:* `CLAUDE.md` and `operator/AGENTS.md` are auto-loaded context;
`settings.json` is applied by the harness. Correctness of the matrix is enforced by the
Phase 2 delivery-gate hook actually running those commands.

## Phase 2 — Hooks: enforcement instead of instructions

Small, deterministic, high-value only. All live in `.claude/hooks/` + `settings.json`.

| Hook | Event | What it does |
| --- | --- | --- |
| `gofmt-gate` | PostToolUse (Edit/Write on `*.go`) | `gofmt -l` the touched file; non-empty output → blocking feedback. Kills the #1 CI-failure class at edit time. |
| `generated-file-guard` | PreToolUse (Edit/Write) | Reject edits to `zz_generated.*`, `config/crd/bases/*`, `config/rbac/role.yaml`, `config/webhook/manifests.yaml`, `PROJECT`. Turns AGENTS.md's "never edit" prose into a hard stop. |
| `delivery-gate` | Stop (or pre-`git push` PreToolUse) | If `*.go` changed in root module → `go test ./...` must pass; if under `operator/` → `cd operator && go test ./...`. Blocks "done" without evidence. |
| `session-start` | SessionStart | Warm `go mod download` for both modules; print the verification matrix as a reminder. Use the `session-start-hook` skill to scaffold for web sessions. |
| `handoff-writer` | PreCompact | Append current task state (branch, changed files, failing/passing checks, next step) to `notes/agent-log.md` so compaction never loses the thread. |

Deliberately skipped: budget governors, evidence loggers for every tool call, model
auditors — logging-only hooks that nobody reads are the hook-shaped version of bloat.

*Enforced tomorrow by:* the harness executes hooks mechanically; no model discretion involved.

## Phase 3 — Agents: full roster, three-agent core first

All agents live in `.claude/agents/`, each with a strict contract (mission, scope,
output format, required evidence). The core three are built first because every task
flows through them; the rest of the roster is defined alongside so it is available on
demand instead of being reinvented in chat.

**Core (build first):**

- **builder** — implements a bounded change in one module; contract requires naming the
  files touched and the exact verification commands run with their output tails.
- **qa-verifier** — read-only + test-execution; re-runs the verification matrix for the
  diff and returns PASS/FAIL per gate with command output as evidence. Never edits.
- **critic** — adversarial review of a diff against the repo's own bars: coverage
  delta, race safety, redaction false-positive/negative risk (this is a security tool —
  a "passing" change that weakens redaction is the worst failure mode), doc drift
  (README/CONFIGURATION/KNOWN_LIMITATIONS claims vs. behavior).

**Extended roster (defined in the same pass, invoked as needed):**

- **chief-operator** — main-session operator profile for long orchestration runs
  (`claude --agent chief-operator`). Short core prompt: understand intent, split into
  microtasks, dispatch to the agents below, decide from digests, write handoffs.
  Explicit model-routing and memory rules; no instruction museum.
- **system-fixer** — bounded repairs to the `.claude/` system itself (agents, skills,
  hooks, settings). Must commit the pre-repair state before touching anything (see
  Backups below) and re-run the affected hook/agent as evidence of the fix.
- **eval-designer** — converts a recurring `notes/agent-log.md` entry into an eval
  fixture in `.claude/evals/`.
- **improvement-analyst** — reads the operational log and proposes the next system
  patch, always naming the enforcing file.
- **context-librarian** — prunes and refreshes `CLAUDE.md`, `operator/AGENTS.md`, and
  doc pointers; keeps loaded context lean and current.
- **research-scout** — read-only research (Go/k8s/golangci releases, CVEs affecting
  dependencies) returning short cited digests, never raw dumps.

**Model routing with backup routing.** Claude Code has no built-in automatic model
selection, and a subagent cannot switch its own model mid-run — the model is fixed at
dispatch. The "smart choice" therefore lives in exactly two files:

- *Frontmatter defaults* (`.claude/agents/*.md` `model:` field — accepts aliases like
  `sonnet`/`opus`/`haiku` or `inherit`): the safe per-agent default when nobody decides
  otherwise. Use aliases, never hardcoded model IDs — availability changes.
- *Dispatch-time overrides by the orchestrator*: the Agent tool takes a per-invocation
  `model` parameter that beats frontmatter. The chief-operator prompt carries the
  routing table — strongest available model for orchestration and critic passes;
  mid-tier for builder tasks; small/fast for mechanical sweeps (gofmt fixes, doc
  greps) — plus an **escalation ladder**: if a cheap tier's output fails qa-verifier,
  redispatch the same task one tier up instead of retrying at the same tier; if the
  preferred tier is unavailable, fall back one tier down (e.g. critic: strongest →
  mid-tier; builder: mid-tier → small) rather than stalling.

One footgun to document in `CLAUDE.md`: the `CLAUDE_CODE_SUBAGENT_MODEL` env var
silently outranks both frontmatter and per-dispatch overrides — keep it unset in this
repo's environments or all routing rules become dead letters.

**Backups** — two rules, both enforced by files, so no repair or risky change is
unrecoverable:

- *Working-state backups:* git is the backup medium. A `checkpoint` hook (extends
  Phase 2) requires a WIP commit on the working branch before multi-file refactors,
  generated-file regeneration (`make manifests generate`), or any scripted bulk edit —
  rollback is then `git reset`, not archaeology.
- *System backups:* `.claude/` is committed to the repo, so the agent system itself is
  versioned and revertible; the system-fixer contract requires a commit before and
  after each repair, and the pre-compact handoff writer (Phase 2) snapshots session
  state to `notes/agent-log.md` so a compaction or dropped session never loses the
  thread.

*Enforced tomorrow by:* `.claude/agents/*.md` frontmatter (tools, model tier, fallback
tier) is applied by the harness; contracts live in the agent prompt files, not in chat;
the checkpoint rule is a hook, not a habit.

## Phase 4 — Skills: encode the workflows that repeat

Two on-demand skills in `.claude/skills/` (no preloading beyond what's already global):

- **/verify-shield** — runs the right slice of the verification matrix for the current
  diff and prints a PASS/FAIL table. This is the single file that makes Phase 1's
  matrix executable instead of aspirational.
- **/bench-compare** — wraps `BASE_REF=origin/main RUNS=7 LINES=500000
  ./benchmark/run_benchmarks.sh` + scanner microbenchmarks; required for any change
  touching `pkg/scanner` hot paths, and states the acceptance rule (no regression
  beyond noise vs. base).

Everything else waits until the operational log shows a third repetition of a workflow.

## Phase 5 — Evals and memory: turn recurring failures into fixtures

- **Eval seed set** from the audit cracks: (1) agent asked to "run the tests" must run
  both modules; (2) agent editing `*_types.go` must regenerate manifests; (3) agent
  told "make fuzz pass" must use the single-package invocation. Each eval is a short
  scripted scenario + expected commands, stored in `.claude/evals/` as markdown
  checklists that the critic agent can execute.
- **Operational log** `notes/agent-log.md`, one line per incident, fixed format:
  `date | failure | root cause | system patch (file) | eval added? | next`.
  No narrative. A recurring entry with no "system patch" file after two occurrences is
  the trigger to add a hook, skill, or agent — that is the improvement loop, and the
  log is the file that enforces it.

## Sequencing and effort

| Order | Work | Size | Payoff |
| --- | --- | --- | --- |
| 1 | Phase 1 (CLAUDE.md, settings, AGENTS.md slim, CONTRIBUTING fix) | ~1 session | Every future session starts oriented |
| 2 | Phase 2 hooks (gofmt-gate, generated-file-guard, delivery-gate first) | ~1 session | CI failures caught at edit time |
| 3 | Phase 4 `/verify-shield` | small | Matrix becomes executable |
| 4 | Phase 3 agents (core three, then extended roster + checkpoint hook) | 1–2 sessions | Clean delegation with evidence, recoverable by design |
| 5 | Phase 5 evals + log | ongoing | Failures compound into system patches |

Definition of done for the upgrade: a fresh session, given "change X in pkg/scanner and
ship it", reaches a green-CI-equivalent state using only committed files — no chat-borne
tribal knowledge required.
