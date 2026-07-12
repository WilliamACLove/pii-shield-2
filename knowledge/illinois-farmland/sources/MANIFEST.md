# Source Manifest — Illinois Farmland Pricing, Sales, and Rent

Retrieved (attempted): 2026-07-12

## IMPORTANT: No files were downloaded in this session

Every attempt to fetch a document — via `curl` (Bash) and via the `WebFetch` tool —
failed with an organization-level egress-policy denial (`gateway answered 403 to
CONNECT (policy denial or upstream failure)`), not a site-specific block. This was
confirmed by testing unrelated control domains: `https://www.google.com` and
`https://en.wikipedia.org` were **also** denied, while the two egress-allowlisted
package registries (`https://pypi.org`, `https://registry.npmjs.org`) succeeded
(HTTP 200). Per `/root/.ccr/README.md`, 403/407 responses from the proxy are
policy denials that should be reported, not retried or routed around.

Consequently **every row below is "not archived"** for this reason (labeled
`NETWORK BLOCKED`), separate from the one item that is intentionally manifest-only
under the copyright rule (`COPYRIGHT — not archived by design`). All URLs were
identified via the `WebSearch` tool (a hosted search service, not a direct fetch
from this sandbox) and are believed correct as of the search date, but have **not**
been byte-verified against the live document (no `file`/`pdftotext` check was
possible). Titles, dates, and figures quoted below come from search-result
snippets, not from directly opened PDFs — treat as provisional until an
environment with outbound web access can download and verify them.

To complete this archive: re-run in a session whose egress policy allows
`nass.usda.gov`, `downloads.usda.library.cornell.edu`, `esmis.nal.usda.gov`,
`ilga.gov`, `tax.illinois.gov`, `chicagofed.org`, `farmdoc.illinois.edu`,
`farmdocdaily.illinois.edu`, `soilproductivity.nres.illinois.edu`, `ers.usda.gov`,
and `ispfmra.org` (for citation-checking only, per the copyright rule).

| # | Filename (or "not archived") | Title | Publisher | Vintage/edition | Source URL | Retrieved | SHA256 (first 16) | Notes |
|---|---|---|---|---|---|---|---|---|
| 1a | not archived | Land Values 2025 Summary | USDA NASS | 2025 (released Aug 1, 2025) | https://downloads.usda.library.cornell.edu/usda-esmis/files/pn89d6567/2n49w148w/m039n441h/land0825.pdf (mirror: https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0825.pdf) | 2026-07-12 | — | NETWORK BLOCKED. Per search snippets: US farm real estate avg $4,350/acre (+4.3%), cropland $5,830/acre (+4.7%), pasture $1,920/acre (+4.9%) vs 2024. |
| 1b | not archived | Land Values 2024 Summary | USDA NASS | 2024 (released Aug 2, 2024) | https://esmis.nal.usda.gov/sites/default/release-files/pn89d6567/vh53zm770/1c18g799h/land0824.PDF (mirror: https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0824.pdf) | 2026-07-12 | — | NETWORK BLOCKED. Per search snippets: US farm real estate avg $4,170/acre (+5.0%), cropland $5,570/acre (+4.7%) vs 2023. |
| 1c | not archived | Land Values and Cash Rents (Highlights) | USDA NASS | 2025 | https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf | 2026-07-12 | — | NETWORK BLOCKED. National highlights 2-pager combining land values and cash rents; supplementary to item 1a. |
| 2a | not archived | Illinois 2025 Cash Rents (news release) | USDA NASS, Illinois field office | dated file name "20250128" — vintage year unconfirmed, likely describes 2024 or preliminary 2025 data | https://www.nass.usda.gov/Statistics_by_State/Illinois/Publications/Current_News_Release/2025/20250128-IL-2025-Cash-Rents-News-Release.pdf | 2026-07-12 | — | NETWORK BLOCKED. Filename date (Jan 28) is inconsistent with NASS's normal Aug/Sept cash-rent release cadence — needs verification once reachable; do not cite vintage year without opening the PDF. |
| 2b | not archived | Illinois Cash Rent by County (August 2025 county estimates) | USDA NASS, Illinois field office | 2025 (county estimates normally published late August) | Expected under https://www.nass.usda.gov/Statistics_by_State/Illinois/Publications/County_Estimates/2025/ — exact 2025 filename not confirmed; 2024 analog was https://www.nass.usda.gov/Statistics_by_State/Illinois/Publications/County_Estimates/2024/20240823-IL-Cash-Rent-by-County.pdf | 2026-07-12 | — | NETWORK BLOCKED. Per press coverage: 2025 IL county cash rents ranged $92/acre (Pope Co.) to $372/acre (Sangamon Co.); 95 of 102 counties reported. |
| 2c | not archived | QuickStats — Illinois cash rents by land use (state & county) | USDA NASS QuickStats | 2025 | https://quickstats.nass.usda.gov/ (interactive query tool; no static export URL identified without direct access to build/test the query) | 2026-07-12 | — | NETWORK BLOCKED (and QuickStats requires interactive query-building that could not be exercised at all in this session). |
| 3 | not archived | Bulletin 811: Optimum Crop Productivity Ratings for Illinois Soils | University of Illinois, College of ACES (Office of Research) | Published August 2000 (most recent revision found; distributed via soilproductivity.nres.illinois.edu) | http://soilproductivity.nres.illinois.edu/Bulletin811ALL.pdf (also archived at IDEALS: https://www.ideals.illinois.edu/items/1070, handle 2142/1027) | 2026-07-12 | — | NETWORK BLOCKED. No evidence found of a revision newer than the 2000 edition; confirm on retrieval. |
| 4 | not archived | 735 ILCS 5/9-206 — Notice to terminate tenancy of farm land | State of Illinois (Illinois General Assembly, ilga.gov) | Current codification (Code of Civil Procedure, Illinois Compiled Statutes) | https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-206 (alt permalink: https://ilga.gov/Documents/legislation/ilcs/documents/073500050K9-206.htm) | 2026-07-12 | — | NETWORK BLOCKED. Per search snippet, statute requires written notice to quit not less than 4 months prior to end of the lease year for year-to-year farm tenancies (crop share, livestock share, cash rent, or other basis); waiver by verbal lease is barred. Full text must be re-pulled and saved verbatim once reachable, with retrieval-date header, per task instructions. |
| 5 | not archived | 35 ILCS 200/10-110 through 10-147 — Farmland Assessment (Property Tax Code, Div. 6) | State of Illinois (ilga.gov) | Current codification | Section index: https://www.ilga.gov/legislation/ilcs/ilcs4.asp?DocName=003502000HArt.+10+Div.+6&ActID=596&ChapterID=8&SeqStart=20200000&SeqEnd=22200000 ; individual sections e.g. https://ilga.gov/Documents/legislation/ilcs/documents/003502000K10-110.htm , https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=003502000K10-115 | 2026-07-12 | — | NETWORK BLOCKED. 10-110 last amended by P.A. 92-301, eff. Jan 1, 2002 per snippet; sections 10-115 through 10-147 not individually confirmed — must pull each section (or the Div. 6 index page, which may render all sections on one page) once reachable. |
| 6a | not archived | Certified Values for Assessment Year 2026 ($ per acre) | Illinois Department of Revenue | Assessment year 2026 | https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2026-farmland-certified-values.pdf | 2026-07-12 | — | NETWORK BLOCKED. Per snippet: 5-year capitalization rate of 5.27%; EAV/acre = 33.33% of debased agricultural economic value by soil Productivity Index (PI), capped at ±10% year-over-year change per PI. |
| 6b | not archived | Certified Values for Assessment Year 2025 ($ per acre) | Illinois Department of Revenue | Assessment year 2025 | https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2025-farmland-certified-values.pdf | 2026-07-12 | — | NETWORK BLOCKED. Per snippet: 5-year capitalization rate of 4.83%. |
| 6c | not archived | Illinois Department of Revenue Publication 122 (farmland assessment guidance) | Illinois Department of Revenue | January 2026 edition | https://tax.illinois.gov/content/dam/soi/en/web/tax/research/publications/pubs/documents/pub-122.pdf | 2026-07-12 | — | NETWORK BLOCKED. Supplementary methodology publication accompanying items 6a/6b. |
| 7a | not archived | AgLetter — "Midwest Farmland Values Ended 2025 with Solid Growth" | Federal Reserve Bank of Chicago | February 2026 (No. 2011), describing Q4 2025 | Web page: https://www.chicagofed.org/publications/agletter/2025-2029/february-2026 ; PDF (pattern-inferred from prior years' naming convention, e.g. .../february-2025.pdf — NOT confirmed): https://www.chicagofed.org/-/media/publications/agletter/2025-2029/february-2026.pdf?sc_lang=en | 2026-07-12 | — | NETWORK BLOCKED. Per snippets: District farmland values +6% y/y in 2025 (reversing a modest 2024 decline); Q4-2025 "good" farmland values +2% q/q; credit conditions weakening (5.6% of loans with major/severe repayment problems, highest since mid-2020). |
| 7b | not archived | AgLetter — "First Quarter Midwest Farmland Values Up Some from a Year Ago" | Federal Reserve Bank of Chicago | May 2026, describing Q1 2026 | Web page: https://www.chicagofed.org/publications/agletter/2025-2029/may-2026 ; PDF (pattern-inferred, NOT confirmed): https://www.chicagofed.org/-/media/publications/agletter/2025-2029/may-2026.pdf?sc_lang=en | 2026-07-12 | — | NETWORK BLOCKED. Per snippets: District farmland values +3% y/y in Q1 2026 but "good" farmland dipped 1% q/q; 2026 annual cash rental rates down 3% (second consecutive annual decrease); farmland demand and sales activity down y/y. |
| 8 | not archived | Farmland Values and Rental Agreements in Illinois for 2026 (Nick Paulson) | University of Illinois farmdoc | September 18, 2025 handout, describing 2026 leasing outlook | https://farmdoc.illinois.edu/wp-content/uploads/2025/09/2025-09-18-Farmland-and-Leases-in-2026-Handout.pdf | 2026-07-12 | — | NETWORK BLOCKED. Freely distributed extension handout; current edition of the "leasing facts" series. Prior-year analog also found: https://farmdoc.illinois.edu/wp-content/uploads/2023/10/2023-10-17-Farmland-Lease-Handout.pdf |
| 9 | not archived (topic page, not a single downloadable report) | Farmland Value — Land Use, Land Value & Tenure | USDA ERS | Ongoing topic page; cites 2025 data (US farm real estate avg $4,350/acre, +4.3% nominal / +1.9% real) | https://www.ers.usda.gov/topics/farm-economy/land-use-land-value-tenure/farmland-value | 2026-07-12 | — | NETWORK BLOCKED. This is a maintained webpage aggregating charts/data rather than one static PDF; related standalone ERS report "Trends in U.S. Farmland Values and Ownership" at https://www.ers.usda.gov/publications/44660 if a PDF version exists — not confirmed. |
| 10a | not archived (COPYRIGHT — manifest-only by design, per task instructions) | Illinois Farmland Values and Lease Trends — 2026 edition | Illinois Society of Professional Farm Managers and Rural Appraisers (ISPFMRA) | 2026 (survey results describing year-ahead 2026/2027 outlook) | Archive index: https://ispfmra.org/land-values-archive/ ; 2026 report page: https://ispfmra.org/download/2026-land-values-report/ | 2026-07-12 | — | Do not archive full book regardless of network access — member-organization survey publication, per copyright rule. Note: some search snippets suggest ISPFMRA has offered recent editions as free downloads (e.g., 2025 edition "available early and at no cost"); this does not override the task's explicit instruction to treat this title as not-archived. |
| 10b | not archived (COPYRIGHT — manifest-only by design) | Illinois Farmland Values and Lease Trends — 2025 edition | ISPFMRA | 2025 | Archive index: https://ispfmra.org/land-values-archive/ ; 2025 report page: https://ispfmra.org/download/2025-land-values-report/ ; announcement: https://ispfmra.org/2025/03/27/download-now-our-2025-land-values-lease-trends-report/ | 2026-07-12 | — | Same as 10a. |
| 10c | not archived (COPYRIGHT — manifest-only; farmdoc summary is secondary commentary, not the book itself) | farmdoc daily summary of March 2025 ISPFMRA survey | University of Illinois farmdoc daily | March–April 2025 | https://extension.illinois.edu/blogs/farm-focus/2025-04-11-2025-illinois-farmland-values-statewide-and-local-perspectives-part-one and part two: https://extension.illinois.edu/blogs/farm-focus/2025-04-18-2025-illinois-farmland-values-statewide-and-local-perspectives-part-two | 2026-07-12 | — | NETWORK BLOCKED for the extension-blog copies themselves (these would be fine to archive as U. of I. extension material if a farmdocdaily.illinois.edu-hosted twin exists — none confirmed via search; the URLs found are on extension.illinois.edu, a U of I domain, but exact article was not located under farmdocdaily.illinois.edu). |
| 10d | not archived (COPYRIGHT — manifest-only; same caveat) | farmdoc/Extension summary of March 2026 ISPFMRA survey | University of Illinois farmdoc daily / Illinois Extension | April–June 2026 | https://extension.illinois.edu/blogs/farm-coach/2026-05-21-illinois-farmland-values-2026-volatile-signals and https://extension.illinois.edu/blogs/farm-coach/2026-05-22-illinois-farm-cash-rent-trends-2026 ; farmdoc daily companion: https://farmdocdaily.illinois.edu/2026/04/illinois-cash-rents-and-leasing-expectations-through-2027.html | 2026-07-12 | — | NETWORK BLOCKED. |

## Why this manifest has no archived files

This task requires downloading primary-source PDFs/HTML and verifying them with
`file` and `pdftotext`/`strings`. In this session:

1. `Bash` `curl` to every target host (nass.usda.gov, downloads.usda.library.cornell.edu,
   esmis.nal.usda.gov, ilga.gov, tax.illinois.gov, chicagofed.org, farmdoc.illinois.edu,
   farmdocdaily.illinois.edu, soilproductivity.nres.illinois.edu, ers.usda.gov,
   ispfmra.org) failed with `CONNECT tunnel failed, response 403`.
2. The proxy status endpoint (`$HTTPS_PROXY/__agentproxy/status`) logged these as
   `connect_rejected` / "gateway answered 403 to CONNECT (policy denial or upstream
   failure)" for every one of them.
3. As a control, `https://www.google.com` and `https://en.wikipedia.org` were tried
   through both `curl` and the `WebFetch` tool — both denied identically — while
   `https://pypi.org` and `https://registry.npmjs.org` (on the proxy's explicit
   `noProxy` allowlist) succeeded with HTTP 200. This isolates the failure to a
   session-wide egress policy, not a problem with any specific target site, and
   per `/root/.ccr/README.md` such denials should be reported rather than retried
   or worked around.

All bibliographic data above comes from `WebSearch` result snippets (a hosted
search service that does not share this sandbox's blocked egress path), not from
opening the documents directly. Nothing was fabricated as a placeholder file.
