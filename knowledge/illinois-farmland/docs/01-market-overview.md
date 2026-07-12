# Illinois Farmland Market: Overview and Orientation

The synthesis document for this knowledge base — the state of the Illinois farmland market as of mid-2026, the measurement systems that describe it, and how the other eleven documents fit together. Detailed citations live in the linked documents; this overview cites only its headline figures.

**Data current as of:** mid-2026 (latest releases: USDA NASS *Land Values 2025 Summary*, Aug. 2025; ISPFMRA 2026 *Land Values and Lease Trends* report, Apr. 2026; Chicago Fed *AgLetter*, May 2026; farmdoc daily through July 2026)
**Built/verified:** 2026-07-12

## 1. The market in one paragraph

Illinois has some of the most valuable row-crop farmland in the United States — roughly 26–27 million acres of farmland anchored by deep prairie Mollisols in the central and east-central "cash grain belt." As of the latest data, USDA NASS puts average Illinois farm real estate at **$8,930/acre** and cropland at **$9,850/acre** (2025, +2.6% and +3.1% y/y), while ISPFMRA's professional survey puts top-quality (Excellent, PI 133+) land at roughly **$15,800–$16,400/acre**, down about 3% from its 2023 peak. Statewide average cash rent is **$264/acre** (2025, down $5 — the first decline since 2020), with professionally managed Excellent-class ground renting in the **$315–$404/acre** range. The market since 2023 is best described as a **high plateau with quality-dependent softening**: blended statewide averages still inch up, top-quality land has drifted down modestly, and independent surveys (ISPFMRA, Chicago Fed) agree rents and values are flat-to-lower even as farm incomes have weakened much more sharply — the classic pattern of farmland's stickiness relative to its income fundamentals. (Sources and vintages: [02-land-values-and-price-history.md](02-land-values-and-price-history.md), [03-cash-rents.md](03-cash-rents.md), [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md), [11-macro-drivers-and-outlook.md](11-macro-drivers-and-outlook.md).)

## 2. The three measurement systems — never mix them silently

The single most common error in discussing Illinois farmland prices is treating numbers from different measurement systems as interchangeable. They are not (see [SOURCING.md](../SOURCING.md) rule 4):

| System | What it measures | Headline current figure | Doc |
|---|---|---|---|
| **USDA NASS surveys** | Operator-reported opinion of value/rent, statistically sampled, blended across all quality levels | $8,930/acre farm real estate; $9,850/acre cropland; $264/acre cash rent (2025) | [02](02-land-values-and-price-history.md), [03](03-cash-rents.md) |
| **ISPFMRA expert panel** | Farm managers'/appraisers' compilation of observed sales and leases, segmented by soil-productivity class and 10 regions | Excellent class ≈ $15,846/acre (CY2025); class-segmented rent ranges | [07](07-ispfmra-benchmarks.md) |
| **Actual transactions** (auctions, brokered sales, PTAX-203 records) | Real closing prices — but a *selected, quality-skewed sample* | top central-IL auctions well above survey averages | [09](09-sales-market-structure.md) |

A statement like "Illinois farmland is worth about $9,000/acre" and a statement like "good central Illinois farms bring $15,000+" are **both correct** — they describe different populations measured differently. Any grounded answer about Illinois land prices must say *which system* it is quoting.

## 3. The valuation spine

Almost everything in Illinois farmland pricing hangs off one identity (full treatment with worked examples in [05-valuation-math.md](05-valuation-math.md)):

```
V = NOI / r
```

- **NOI** for farmland is cash rent net of landlord costs (property tax, insurance, management) — see [03](03-cash-rents.md) for rents, [10](10-tax-and-assessment.md) for the property-tax component.
- **r**, the capitalization rate, is observed at roughly **2.7%** for Illinois farmland in 2025 (gross rent ÷ price), compressed from 4–5% in the 1990s. Its long decline — not rent growth alone — drove much of the post-2000 price appreciation, and its relationship to the 10-year Treasury (≈4.3% average in 2025) is the standard framework for the current outlook debate ([05](05-valuation-math.md) §3, §5; [11](11-macro-drivers-and-outlook.md)).
- Land quality enters through the **Productivity Index (PI)**, Bulletin 811's 47–147 scale — the basis of ISPFMRA's Excellent/Good/Average/Fair classes and of the farmdoc rent-vs-PI regression ([06-soil-productivity.md](06-soil-productivity.md)). PI is Illinois-specific; it is **not** Iowa's CSR2.

Illinois's property-tax system runs the *same identity with statutory inputs*: certified farmland EAV is capitalized use-value income, not market value — which is why assessed values sit far below sale prices ([10](10-tax-and-assessment.md)).

## 4. How the market functions

- **Leases:** roughly a third to two-fifths of arrangements are fixed cash rent, with variable/flexible cash rent (~26–34%) and crop share (~21%+) making up most of the rest; the exact mix varies by survey wave. The legal spine is 735 ILCS 5/9-206 — terminating a year-to-year farm tenancy requires **written notice at least 4 months before the end of the lease year** (customarily March 1) — plus the statutory landlord's crop lien. Formulas for every lease type: [04-lease-structures-and-law.md](04-lease-structures-and-law.md).
- **Sales:** a thin market — well under 2% of Illinois farmland trades in a typical year — dominated by estate/trust sellers, with farmers the majority buyers and public auction the price-discovery mechanism for quality ground. Channel shares, buyer/seller composition, and transaction-data infrastructure: [09-sales-market-structure.md](09-sales-market-structure.md).
- **Returns benchmark:** University of Illinois farmdoc's operator-and-land-returns series and crop budgets for central Illinois are the standard for testing whether rents and prices square with farm economics ([08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md)).

## 5. Using this knowledge base for grounding

1. **Start from the doc, not from memory.** Each document carries current figures with vintages; quote the vintage with the number.
2. **Respect the flags.** Anything marked *[not confirmed against a primary source at build time]* converged across secondary sources but was never read from the primary document — this build ran in an environment that blocked direct fetches (full disclosure in [SOURCING.md](../SOURCING.md)). Treat flagged numbers as directionally reliable, not citation-grade.
3. **Check the calendar.** NASS land values refresh each August, cash rents in late August/September, ISPFMRA each spring, IDOR certified values each spring, AgLetter quarterly. A "current" number from this build is stale after the next release; the refresh schedule is in [SOURCING.md](../SOURCING.md) and the source list in [12-data-source-directory.md](12-data-source-directory.md).
4. **Terms of art** are defined in the [glossary](glossary.md).

## Document map

| Doc | Contents |
|---|---|
| [02-land-values-and-price-history.md](02-land-values-and-price-history.md) | NASS value levels, 1970–2025 series, boom/bust history, Census-benchmark revisions, methodology |
| [03-cash-rents.md](03-cash-rents.md) | State and county cash rents, historical series, survey methodology, rent-to-value ratio |
| [04-lease-structures-and-law.md](04-lease-structures-and-law.md) | Lease types and prevalence, flexible-rent formulas, 735 ILCS 5/9-206, crop lien, oral leases |
| [05-valuation-math.md](05-valuation-math.md) | V = NOI/r, cap rates, Gordon growth/DCF, price-to-rent, per-tillable-acre math, appraisal approaches |
| [06-soil-productivity.md](06-soil-productivity.md) | Bulletin 811 PI system, PI-to-value and PI-to-rent, marquee soils, PI ≠ CSR2, parcel lookup |
| [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md) | ISPFMRA classes, regions, value and rent benchmarks by class, lease-type mix |
| [08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md) | Operator/land returns, crop budgets, leasing tools, rent stickiness |
| [09-sales-market-structure.md](09-sales-market-structure.md) | Sale channels, buyer/seller composition, turnover, transaction data, 1031/institutional capital |
| [10-tax-and-assessment.md](10-tax-and-assessment.md) | Farmland Assessment Law, certified EAV mechanics, 10% cap, actual tax levels, NOI treatment |
| [11-macro-drivers-and-outlook.md](11-macro-drivers-and-outlook.md) | Drivers, cycles, Chicago Fed AgLetter, returns decomposition, asset-class comparison, outlook |
| [12-data-source-directory.md](12-data-source-directory.md) | Annotated directory of every data source, grouped, with refresh cadences |
| [glossary.md](glossary.md) | 45+ terms of art defined with Illinois context |
