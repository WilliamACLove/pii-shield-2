# Handoff: Completing the Illinois Farmland Knowledge Base

Instructions for a follow-up session (any model) to finish the items this build could not complete. The original build session (2026-07-12) ran in an environment whose network policy **blocked all direct fetches** — only a hosted web-search service worked — so everything below reduces to "fetch the primary document, verify, and update."

**Prerequisites for the follow-up session:**
- Network access to: `nass.usda.gov`, `downloads.usda.library.cornell.edu`, `ers.usda.gov`, `ilga.gov`, `tax.illinois.gov`, `chicagofed.org`, `farmdoc.illinois.edu`, `farmdocdaily.illinois.edu`, `extension.illinois.edu`, `soilproductivity.nres.illinois.edu`, `ispfmra.org`, `ptab.illinois.gov` (or a browser tool such as Kapture that can reach them).
- Write access to this repo/branch (or its successor if migrated to a private repo).
- Read `SOURCING.md` first and follow its rules for any edit.

## Task 1 — Archive the primary documents (highest value)

`sources/MANIFEST.md` lists every core document with its exact URL, publisher, and vintage. For each row not marked "not archived (copyrighted/member-only)":

1. Download to `sources/` with a descriptive kebab-case filename including the vintage year.
2. Verify it is the intended document (`file`, `pdftotext | head`), reject error pages and files under 10KB (except plain-text statutes).
3. Record SHA256 (first 16 hex chars) and retrieval date in the manifest; flip its status to archived.

Do **not** archive the ISPFMRA report books (member publications, copyrighted) — manifest-only, by design.

## Task 2 — Resolve the flagged open items

Each is flagged inline in the docs with `[not confirmed against a primary source at build time]` or an "Unresolved" callout. In priority order:

| # | Open item | Where | How to resolve |
|---|---|---|---|
| 1 | **P.A. 104-0468 cap-rate "guardrails"** (published rate + 3pp, 8% floor / 10% ceiling) vs. IDOR certified rates (4.83% AY2025, 5.27% AY2026) — which divisor actually produces AEV, and from which assessment year? | `docs/05-valuation-math.md` §8, `docs/10-tax-and-assessment.md` §5 | Read 35 ILCS 200/10-115 current text at ilga.gov + the act text of P.A. 104-0468 + IDOR Pub. 122 (Jan 2026). Rewrite both callouts with the resolved mechanic. |
| 2 | Verbatim statutory text: 735 ILCS 5/9-206, 9-206.1, 9-316; 740 ILCS 80/2; 35 ILCS 200/10-110–10-147 | `docs/04-lease-structures-and-law.md`, `docs/10-tax-and-assessment.md` | Fetch from ilga.gov, save to `sources/`, confirm the quoted language matches, remove the "corroborated via secondary legal databases" caveats where confirmed. |
| 3 | 2025-vintage farmdoc rent-vs-PI regression coefficients | `docs/06-soil-productivity.md` §5 | farmdoc daily 15:184 (Oct 7, 2025). |
| 4 | Revised variable-cash-lease rent factors replacing 33%/40% | `docs/04-lease-structures-and-law.md` §3a | farmdoc daily 15:179 (Sept 30, 2025). |
| 5 | Certified EAV-per-PI table (current year) + the dropped PI-130 figures | `docs/10-tax-and-assessment.md` §5 | IDOR 2026-farmland-certified-values.pdf / Pub. 122 Table 1. |
| 6 | FBM-0321 index: 2005 value (173 flagged anomalous), exact base construction | `docs/02` §3.3, `docs/05` §10 | FBM-0321 PDF. |
| 7 | ISPFMRA Excellent-class PI cutoff (133 vs. 127 variant), full 10-region county map, Fair-land rent direction | `docs/07-ispfmra-benchmarks.md` | ISPFMRA report or its region map page. |
| 8 | NASS gaps: 2021 IL farm real estate value, 2007/08/09/13 state cash rents, IL pasture rent, district-level values | `docs/02`, `docs/03` | NASS QuickStats (Survey → Economics → Farms & Land & Assets → Ag Land / Rent, State = Illinois). |
| 9 | The unresolved 1971–1995 "0.54" price-rent ratio figure | `docs/05-valuation-math.md` §6 | farmdocdaily.illinois.edu/wp-content/uploads/2022/03/fdd032322.pdf. |

After each resolution: update the doc text, remove or amend the flag, and note the change in the doc's Sources section if a new source was used.

## Task 3 — Housekeeping (as directed by the owner)

- **Private-repo migration**: if the owner creates a private repo, move `knowledge/illinois-farmland/` there wholesale (history optional); this content is self-contained.
- **Annual refresh**: next scheduled data events are the NASS Land Values Summary (early Aug 2026) and Cash Rents (late Aug/Sept 2026) — refresh `docs/02`/`docs/03` headline figures and vintages when they land. Full calendar in `SOURCING.md`.

## What NOT to redo

The research, verification, writing, and consistency review are complete. Do not re-derive figures from memory or re-run broad research; the only legitimate changes are (a) primary-document confirmations/corrections per the tasks above, (b) new data releases, (c) owner-directed restructuring. Every edit must keep citations + vintages per `SOURCING.md`.
