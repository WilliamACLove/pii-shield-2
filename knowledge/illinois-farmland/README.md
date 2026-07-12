# Illinois Farmland Knowledge Base

A rigorously sourced reference on **Illinois farmland pricing, sales, and rent**, built to ground future analysis and writing. Every quantitative claim carries a citation with an explicit data vintage; load-bearing claims were independently re-verified by a second research pass at build time.

**Built/verified:** 2026-07-12

## Start here

- **[docs/01-market-overview.md](docs/01-market-overview.md)** — the synthesis: state of the market, the three measurement systems, the valuation spine, and a map of every document.
- **[SOURCING.md](SOURCING.md)** — the sourcing standards every document follows, known limitations of the underlying sources, the annual refresh calendar, and the build-environment disclosure (read this before treating any figure as citation-grade).

## Contents

| Path | What it is |
|---|---|
| `docs/01-market-overview.md` | Market synthesis and orientation |
| `docs/02` – `docs/11` | Topic references: land values & history, cash rents, leases & law, valuation math, soil PI, ISPFMRA benchmarks, farmdoc returns, sales market structure, tax & assessment, macro drivers & outlook |
| `docs/12-data-source-directory.md` | Annotated directory of every data source with refresh cadences |
| `docs/glossary.md` | Terms of art, defined with Illinois-specific context |
| `SOURCING.md` | Sourcing standards, source limitations, refresh calendar |
| `sources/MANIFEST.md` | Primary-document manifest: exact URLs, publishers, vintages, archival status |

## How this was built

A multi-agent pipeline on 2026-07-12: ten research agents fanned out across the knowledge pillars (USDA NASS, ISPFMRA, University of Illinois farmdoc, Illinois statutes, Illinois Dept. of Revenue, Federal Reserve Bank of Chicago); ten adversarial verification agents independently re-checked the ~96 most load-bearing claims (81 confirmed, 12 corrected — corrections applied, several silently-wrong figures caught and dropped, 3 unverifiable — flagged inline); twelve writer agents drafted the documents from the verified notes; a final review pass checked cross-document consistency, re-derived worked-example arithmetic by hand, and reconciled or explicitly surfaced the remaining conflicts.

## Known limitations (read before relying on figures)

1. **No primary-document archive yet.** The build environment blocked direct fetching of source pages/PDFs; all figures rest on convergent web-search evidence rather than opened primary documents. `sources/MANIFEST.md` lists every document with its exact URL so a session with normal network access can fetch, verify, and checksum the archive. Claims that could not be confirmed even by convergence are flagged inline: *[not confirmed against a primary source at build time]*.
2. **Data ages on a known calendar.** NASS land values (August), NASS cash rents (late Aug/Sept), ISPFMRA report (spring), IDOR certified values (spring), Chicago Fed AgLetter (quarterly). Figures here are current to the releases available as of 2026-07-12.
3. **Open items** are flagged in place — notably the P.A. 104-0468 assessment cap-rate guardrails (docs 05/10), the 2025-vintage farmdoc rent-regression coefficients (doc 06), and the exact revised variable-lease rent factors (doc 04).

Not legal, tax, or investment advice.
