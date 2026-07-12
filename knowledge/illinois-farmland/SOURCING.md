# Sourcing Standards for This Knowledge Base

Every document in this knowledge base follows these rules. If you extend the knowledge base, follow them too.

## Rules

1. **Every quantitative claim carries a citation.** A dollar figure, percentage, acreage, or date without a source and vintage is not allowed. Citations include the publisher, document title, URL, and the *data vintage* (the period the data describes), which is often different from the publication date.
2. **Primary sources outrank secondary sources.** The hierarchy, from strongest to weakest:
   - Statutes and regulations as published by the State of Illinois (ilga.gov) or federal government
   - Official statistical series: USDA NASS, USDA ERS, Illinois Department of Revenue, Federal Reserve Bank of Chicago
   - Survey-of-experts reports from professional bodies: ISPFMRA *Illinois Land Values and Lease Trends*
   - University research and extension publications: University of Illinois farmdoc / farmdoc daily
   - Industry and press reports (brokerages, auction companies, farm media) — used only to corroborate or when primary data is unavailable, and flagged as such
3. **Data vintages are stated explicitly.** Example: "Illinois average cropland value was $X/acre (USDA NASS *Land Values 2025 Summary*, August 2025, describing 2025 values)." Never present a number as "current" without anchoring it in time.
4. **Different measurement systems are never mixed silently.** NASS survey values, ISPFMRA expert-opinion values by land class, and actual transaction prices measure different things and diverge systematically. Documents state which system a number comes from.
5. **Formulas state every variable.** A formula is only included with definitions for each term, its source, and (where useful) a worked example using realistic Illinois numbers.
6. **Disagreements between sources are reported, not resolved silently.** When NASS and ISPFMRA (or two other sources) disagree, both numbers appear with an explanation of why they differ.
7. **Verification status.** Claims in this knowledge base were independently re-checked by a second research pass at build time. Where a claim could not be verified, it is marked as such in the text.

## Build-environment disclosure

This knowledge base was assembled in an environment whose network policy **blocked direct fetching of source pages and PDFs**; research and verification relied on a hosted web-search service (which returns page content in results) rather than opening each primary document directly. Consequences:

- `sources/MANIFEST.md` lists every primary document with its exact URL, publisher, and vintage, but **archival copies could not be downloaded**. A follow-up session with network access to the domains listed in the manifest should fetch, verify (`file`/`pdftotext`), and checksum each document to complete the archive.
- Numbers herein should be treated as *well-sourced but not document-confirmed* until that archival pass runs. Claims that the verification pass could not confirm are flagged inline.

## Known limitations of the underlying sources

- **USDA NASS land values** come from the June Area Survey — operator-reported estimates of what land *would* sell for, not transactions. They smooth turning points and sit below top-tier transaction prices for high-quality land.
- **ISPFMRA values** are expert opinion by land class and region from practicing farm managers and appraisers — closer to the professional market view, but not a census of sales.
- **NASS county cash rents** have sampling noise in counties with few responses; year-over-year county moves should be read cautiously.
- **Auction results** are a selected sample (sellers choose auctions when they expect competition) and skew high relative to all transactions.

## Freshness

This knowledge base was built and verified on **2026-07-12**. Sections note the latest data release available at that time. Key annual refresh points:

| Release | Publisher | Typical timing |
|---|---|---|
| Land Values Summary | USDA NASS | early August |
| Cash Rents (state & county) | USDA NASS | September (county detail follows) |
| Illinois Land Values and Lease Trends | ISPFMRA | late March |
| Certified farmland EAV values | Illinois Dept. of Revenue | certified in spring for following assessment year |
| AgLetter (7th District land values) | Federal Reserve Bank of Chicago | quarterly (Feb/May/Aug/Nov) |
| Crop budgets, operator & land returns | U. of I. farmdoc | summer/fall updates |
