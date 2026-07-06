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

## Phase 3 — Agents: a minimal team, not a cast of thirty

For a single Go repo with strong CI, most of the suggested 9-agent roster is overhead.
Three subagent definitions in `.claude/agents/`, each with a strict contract
(mission, scope, output format, required evidence):

- **builder** — implements a bounded change in one module; contract requires naming the
  files touched and the exact verification commands run with their output tails.
- **qa-verifier** — read-only + test-execution; re-runs the verification matrix for the
  diff and returns PASS/FAIL per gate with command output as evidence. Never edits.
- **critic** — adversarial review of a diff against the repo's own bars: coverage
  delta, race safety, redaction false-positive/negative risk (this is a security tool —
  a "passing" change that weakens redaction is the worst failure mode), doc drift
  (README/CONFIGURATION/KNOWN_LIMITATIONS claims vs. behavior).

Explicitly not created: chief-operator (that is the main session's job; the harness
already provides orchestration), system-fixer / eval-designer / improvement-analyst /
context-librarian / research-scout (folded into normal sessions until recurring need is
demonstrated in the log — see Phase 5).

Model routing rule of thumb, recorded in `CLAUDE.md`: strongest available model for
main-session orchestration and critic passes; mid-tier for builder tasks; small/fast
for mechanical sweeps (gofmt fixes, doc greps). Never hardcode model IDs in agent
frontmatter beyond tier hints — availability changes.

*Enforced tomorrow by:* `.claude/agents/*.md` frontmatter (tools, model tier) is applied
by the harness; contracts live in the agent prompt files, not in chat.

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
| 4 | Phase 3 agents | ~1 session | Clean delegation with evidence |
| 5 | Phase 5 evals + log | ongoing | Failures compound into system patches |

Definition of done for the upgrade: a fresh session, given "change X in pkg/scanner and
ship it", reaches a green-CI-equivalent state using only committed files — no chat-borne
tribal knowledge required.
