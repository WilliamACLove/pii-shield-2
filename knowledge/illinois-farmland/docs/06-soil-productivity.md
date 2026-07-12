# Illinois Soil Productivity: the PI System

How Illinois rates cropland productivity on the Bulletin 811 Productivity Index (PI), how PI ties to sale price and cash rent, which soil series anchor the state's best ground, and why PI must never be treated as interchangeable with Iowa's CSR2.

**Data current as of:** Bulletin 811 core table (Table S2, Revised 1/2/2012); ISPFMRA 2025/2026 *Illinois Farmland Values and Lease Trends*; farmdoc daily cash-rent regression through 2024 (14:159) with a 2025 update (15:184) whose coefficients were not confirmable at build time; USDA NASS *Land Values 2025 Summary* (August 2025).
**Built/verified:** 2026-07-12

## 1. What PI measures

The Illinois **Productivity Index (PI)** is a single-number rating of a soil map unit's inherent capacity for crop production, published by the University of Illinois in **Bulletin 811, "Optimum Crop Productivity Ratings for Illinois Soils"** (Olson and Lang, College of ACES Office of Research, August 2000). It rates roughly 800+ Illinois soil map units on a scale of about **47 (low) to 147 (high)** under an *optimum* level of management — defined as the yield performance achieved by the top 16% of Illinois farmers as of the 1990s baseline — combining expected yields across corn, soybeans, wheat, oats, sorghum, and hay into one composite index ([Bulletin 811, Olson and Lang, 2000, IDEALS repository](https://www.ideals.illinois.edu/items/1070); scale and class breakpoints corroborated via [soilproductivity.nres.illinois.edu, Bulletin811ALL.pdf](http://soilproductivity.nres.illinois.edu/Bulletin811ALL.pdf)).

PI is built from a soil's:
- organic matter content
- subsoil / rooting and permeability characteristics
- natural drainage class
- slope and degree of erosion
- northern-vs-southern Illinois climate region

Slope and erosion adjustment factors are applied to a base "Table S2" optimum-management value via factor tables (Table S3 in Bulletin 811); these same factors are what commercial soil-mapping software (see §7) uses to compute a site-specific PI from the base rating ([NRCS eFOTG, "Factors for Estimating Productivity and Yield Indices of Illinois Soils"](https://efotg.sc.egov.usda.gov/references/public/IL/Calculating_productivity_and_yield_indices_in_Illinois_with_adjustment_factors_for_crop_productivity.pdf), undated NRCS reference; source content relayed via search synthesis, not independently opened at build time).

### Revisions

The core productivity table — **"Table S2 (Revised): Productivity of Illinois Soils Under an Optimum Level of Management, Slightly Eroded, 0 to 2 Percent Slopes"** — was last revised **1/2/2012** (Olson and Lang) ([NRCS, "University of Illinois Base Yield Indices (for use in IL only)"](https://www.nrcs.usda.gov/publications/University%20of%20Illinois%20Base%20Yield%20Indices%20(for%20use%20in%20IL%20only)%20-Query%20By%20Soil%20Survey%20Area.html), revision confirmed at build time). No revision to the core table more recent than 2012 was found or could be confirmed; whether soilproductivity.nres.illinois.edu (the maintained host site) has posted a newer edition **[not confirmed against a primary source at build time]**.

## 2. Bulletin 810: the other Illinois PI system, used for tax assessment

Illinois maintains a second, related but distinct productivity rating: **Bulletin 810, "Average Crop, Pasture, and Forestry Productivity Ratings for Illinois Soils"** (2000), which rates the same soils under *average* management — the performance of the typical (50th-percentile) Illinois farmer in the 1990s, rather than the top-16% optimum-management basis used in Bulletin 811.

**This distinction matters because the two bulletins serve different purposes and are frequently conflated:**
- **Bulletin 811** (optimum management) is the PI generally quoted in real-estate listings, ISPFMRA reports, farmdoc rent formulas, and commercial soil-mapping software.
- **Bulletin 810** (average management) is the PI Illinois counties have been statutorily mandated to use for **farmland property-tax assessment since the 2006 assessment year** ([Illinois county assessment officials, il-ccao.org, "Farm Assessment"](http://www.il-ccao.org/what-is-assessment/farm-assessment/), confirmed at build time via multiple concordant county-government sources).

Because Bulletin 811 uses a higher (optimum) management standard than Bulletin 810, the same soil generally carries a *higher* PI under 811 than under 810. One estimate holds this gap at roughly 13% — **that specific percentage could not be verified against a primary source at build time and should be treated as indicative only [not confirmed against a primary source at build time]**. The underlying direction (811 > 810 for the same soil) is well corroborated; see the Flanagan silt loam example in §6, where a Bulletin 811 optimum-management figure (144, McLean Co., 0–2% slope) is cited against a lower average-management figure (127) for the same series.

**A PI quoted from a tax bill (Bulletin 810 basis) and a PI quoted in a farm listing or appraisal (Bulletin 811 basis) are not the same number for the same soil — never treat them as interchangeable.**

The property-tax formula built on the Bulletin 810 PI, in brief:

> **Equalized Assessed Value ($/acre, for a given soil PI) = 33.33% × Certified Agricultural Economic Value ($/acre for that PI)**, where the certified value is a 5-year moving average of gross income minus production costs (net return to land), computed and certified annually by the Illinois Department of Revenue for each Bulletin-810-based PI (35 ILCS 200/10-110 et seq.), subject to a **±10% year-over-year cap** on the change in the certified value for the median-productivity soil.
> **Debased Assessed Value = Equalized Assessed Value × debasement adjustment** (for slope, drainage, ponding/flooding, field size/shape).
> **Permanent pasture assessed value = 1/3 × debased cropland-equivalent value; "other farmland" = 1/6 × debased cropland-equivalent value.**

— corroborated across multiple Illinois county-government and IDOR sources at build time ([Illinois Dept. of Revenue, farmland assessment guidance](https://tax.illinois.gov/localgovernments/property/farmland.html); statutory basis [35 ILCS 200/ Art. 10, Div. 6](https://www.ilga.gov/legislation/ilcs/ilcs4.asp?DocName=003502000HArt.+10+Div.+6&ActID=596&ChapterID=8&SeqStart=21100000&SeqEnd=23100000)).

The exact current-year certified $/acre-by-PI table, and a worked numeric example, belong in **[10-tax-and-assessment.md](10-tax-and-assessment.md)**, which should pull the table directly from IDOR Publication 122 — it was not retrievable at build time in this session.

## 3. PI classification (market classes)

ISPFMRA and farmdoc group Bulletin 811 PI values into four market classes, which underpin the productivity-class breakouts used throughout the ISPFMRA *Illinois Farmland Values and Lease Trends* report (see **[07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md)** for the full regional breakout by class):

| Class | PI Range | Common Market Label |
|---|---|---|
| A | 133–147 | Excellent |
| B | 117–132 | Good |
| C | 100–116 | Average |
| Other agricultural land | ≤ 99 | Fair / not prime |

Source: scale and class breakpoints defined in Bulletin 811 (Olson and Lang, 2000, revised 2012); confirmed via concordant secondary summaries at build time — [Bulletin811ALL.pdf](http://soilproductivity.nres.illinois.edu/Bulletin811ALL.pdf); classes as used in the [2025/2026 ISPFMRA Land Values Report](https://ispfmra.org/land-values-archive/).

## 4. PI-to-value relationship

The 2025 ISPFMRA report breaks out per-acre sale prices by productivity class within each of its 10 regions. Region Six (east-central Illinois — Logan, Christian, DeWitt, Macon, Moultrie, Piatt, Shelby Counties per the region's county list) illustrates the gradient:

| Productivity Class | Avg. PI | Price/acre range | Avg. price/acre |
|---|---|---|---|
| Excellent (133+) | 139.7 | $11,000–$22,508 | $17,210 |
| Good (117–132) | 127.7 | $8,000–$18,105 | $13,268 |
| Average (100–116) | n/a (24 sales, 2024 data cited) | $7,333–$13,046 | $9,386 |

Source: [2025 ISPFMRA Illinois Farmland Values & Lease Trends Report](https://ispfmra.org/download/2025-land-values-report/) (relayed via search-service summary at build time; ispfmra.org returned an HTTP 403 to direct fetch in this session, so this table is **corroborated via secondary synthesis, not independently opened from the primary PDF — [not confirmed against a primary source at build time]**).

From this table, the implied marginal value of a PI point between the Excellent and Good classes is roughly **($17,210 − $13,268) ÷ (139.7 − 127.7) ≈ $328/PI point** (author-calculated from the table above; treat as regional/vintage-specific, not a statewide constant — sale-price-per-PI-point varies by region and year and is not separately published by ISPFMRA as a single statewide figure).

For statewide land-value benchmarks independent of PI (which contextualize the $/acre figures above), see **[02-land-values-and-price-history.md](02-land-values-and-price-history.md)**: USDA NASS's *Land Values 2025 Summary* (released August 1, 2025) reported Illinois farm real estate value at **$8,930/acre** (+2.6% y/y from $8,700 in 2024) and Illinois cropland value at **$9,850/acre** (+3.1% y/y) ([USDA NASS, Land Values 2025 Summary](https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0825.pdf), describing 2025 values; confirmed at build time via concordant secondary reporting — direct fetch of nass.usda.gov was blocked by proxy policy in this session).

## 5. PI-to-rent relationship ($/PI point)

University of Illinois farmdoc daily publishes a periodically re-fit linear regression converting a farm's PI directly into an estimated average county cash rent:

> **Average Cash Rent ($/acre) = a × PI + b + CRD adjustment**

where PI is the Bulletin 811 optimum-management Productivity Index (≈47–147 scale), *a* is the marginal $/PI-point coefficient, *b* is the regression intercept, and the CRD adjustment is a fixed dollar term specific to the farm's Illinois Crop Reporting District, capturing regional cash-rent-market effects not explained by PI alone.

Published coefficient sets:

| Vintage | a ($/PI point) | b | Fit | Source |
|---|---|---|---|---|
| 2017 (original) | 2.79 | −147 | R² ≈ 0.91 against 2017 USDA county cash rents | [farmdoc daily 7:205, Schnitkey, Nov. 7, 2017](https://farmdocdaily.illinois.edu/2017/11/determining-average-cash-rent-productivity-index.html) |
| 2024 ("Setting 2025 Cash Rents") | 3.76 | −202 | Fit to then-current county rents | farmdoc daily 14:159, Schnitkey/Paulson/Zulauf/Baltz, Sept. 3, 2024 |
| 2025 update | not confirmed | not confirmed | Re-fit to 2025 NASS county cash rents (95 of 102 IL counties reported; remaining counties estimated by the regression) | [farmdoc daily 15:184, "Relationships between Average Cash Rents and Soil Productivity," Oct. 7, 2025](https://farmdocdaily.illinois.edu/2025/10/relationships-between-average-cash-rents-and-soil-productivity.html) — **exact 2025-vintage coefficients [not confirmed against a primary source at build time]**; farmdocdaily.illinois.edu returned a proxy-level policy denial on every fetch attempt in this session. |

**Worked example** (2024 coefficients): a Champaign County farm with PI = 134 and a CRD adjustment of +$25 →
Average Cash Rent = (3.76 × 134) − 202 + 25 = 503.84 − 202 + 25 ≈ **$326.84/acre** (source cites ≈$326/acre; arithmetic checked and confirmed at build time).

Cross-reference **[03-cash-rents.md](03-cash-rents.md)** for county-level NASS cash-rent series this regression is fit against, and **[07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md)** for ISPFMRA's own class-based statewide cash-rent figures:

| Class | Cash rent, $/acre |
|---|---|
| Excellent | $375 |
| Good | $325 |
| Average | $273 |
| Fair | $200 |

Source: [ISPFMRA 2025-2026 Illinois Farmland Values and Lease Trends Report](https://ispfmra.org/land-values-archive/) (relayed via search-service summary at build time — **[not confirmed against a primary source at build time]**, ispfmra.org blocked direct fetch in this session).

Note the two systems roughly agree in direction: the ISPFMRA class table implies about ($375 − $325) ÷ (average PI gap between Excellent and Good, ~12 points per §3) ≈ $4/PI point at the class-average level, versus farmdoc's $2.79–$3.76/PI-point marginal coefficient fit across individual counties — these are different measurement methods (expert-opinion class averages vs. a county-level regression) and should not be expected to match exactly; per sourcing rule, both are reported rather than reconciled.

## 6. Marquee Illinois soil series and where the best soils are

Illinois's highest-value farmland is anchored by a handful of dark, loess- or till-derived, poorly-to-somewhat-poorly-drained prairie Mollisols:

| Soil series | Typical PI (average mgmt., Bulletin 810 basis unless noted) | Note |
|---|---|---|
| Drummer silty clay loam (map symbol 152) | **127** | Illinois's official State Soil; poorly drained. A stale PI of 150 also circulates in some secondary sources — **127 is the figure corroborated against current usage at build time**; cite management basis and vintage whenever quoting a bare PI number for this or any series ([Illinois Soil Classifiers Association, "Drummer"](https://illinoissoils.org/drummer/), confirmed at build time). |
| Drummer scl, gravelly substratum (map symbol 350) | 122 | Variant |
| Drummer scl, till substratum (map symbol 552) | 120 | Variant |
| Flanagan silt loam | 127 (average mgmt.); 144 cited under Bulletin 811 optimum mgmt., 0–2% slope, McLean Co. | Prairie soil, McLean/Livingston Co. area; illustrates the 810-vs-811 gap discussed in §2 |
| Ipava silt loam | 126 | Somewhat poorly drained; Fulton/McDonough Co. |
| Muscatune silt loam | 130 | Somewhat poorly drained; NRCS type location in Warren Co., IL |
| Sable silty clay loam | not confirmed — among the top loess prairie soils by reputation, but no specific PI value could be independently confirmed at build time **[not confirmed against a primary source at build time]** | Formed entirely in loess, on moraine/terrace summits |

Sources: [Bulletin811ALL.pdf](http://soilproductivity.nres.illinois.edu/Bulletin811ALL.pdf); [IDOR Bulletin 810 table](https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/bulletin810table2.pdf); NRCS Official Series Descriptions for [Ipava](https://soilseries.sc.egov.usda.gov/OSD_Docs/I/Ipava.html), [Muscatune](https://soilseries.sc.egov.usda.gov/OSD_Docs/M/MUSCATUNE.html), and [Sable](https://soilseries.sc.egov.usda.gov/OSD_Docs/S/SABLE.html) — all relayed via search-service synthesis at build time; direct fetch of these hosts was blocked in this session, so treat the Flanagan/Ipava/Muscatune figures above as well-sourced but **not independently document-confirmed at build time**, distinct from the explicitly re-verified Drummer figure.

**Geographic concentration:** the state's highest-PI counties cluster in the east-central "cash grain belt," commonly cited as Piatt (~138), Macon (~137), Champaign (~136), Logan (~135), and DeKalb (~135), against a statewide average PI cited around 113, with McLean, Livingston, and DeWitt Counties also frequently cited among the most productive (McLean County has repeatedly led the nation in corn and soybean production — [WGLT, June 2023](https://www.wglt.org/local-news/2023-06-06/corn-and-soybean-king-mclean-county-farmers-led-state-nation-in-2022-production)). **These specific county-average PI figures could not be traced to a single primary Bulletin 811 county table at build time and should be treated as directionally correct but numerically unconfirmed [not confirmed against a primary source at build time].** The qualitative pattern — that the east-central and central Illinois prairie counties, dominated by Drummer/Flanagan/Ipava/Muscatune-type soils, carry the state's highest PIs — is well corroborated across sources.

For the ISPFMRA regional map these counties fall into, see **[07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md)**.

## 7. Illinois PI is not Iowa CSR2 — do not equate them

**Illinois PI (Bulletin 811) and Iowa's CSR2 (Corn Suitability Rating 2) are different, non-interchangeable scales.** A PI of, say, 130 in Illinois has no defined numerical equivalence to a CSR2 of 130 in Iowa (and in fact 130 is near the top of the Illinois scale but only mid-range on Iowa's).

| | Illinois PI (Bulletin 811) | Iowa CSR2 |
|---|---|---|
| Scale | ~47–147 | 5–100 |
| Basis | Multi-crop (corn, soybean, wheat, oats, sorghum, hay) optimum-management yield potential, plus soil physical/chemical factors (organic matter, subsoil, drainage, slope, region) | Corn-suitability index built from historical corn-yield records combined with soil characteristics |
| Maintained by | University of Illinois (Olson and Lang, Bulletin 811) | Iowa State University |

Commercial soil-mapping platforms (e.g., Surety/AgriData) explicitly carry PI and CSR2 as **separate, state-specific data layers** for exactly this reason ([DreamDirt, "CSR2 & PI: What They Mean for Your Farm's Land Value"](https://dreamdirt.com/soil-productivity-ratings-explained-csr2-pi-and-what-they-mean-for-farmland-value/); [AgriData/Surety Illinois Bulletin 811 documentation](https://support.agridatainc.com/IllinoisBulletin811.ashx); confirmed via multiple concordant farmland-brokerage explainer sources at build time). **Never convert a PI figure to a CSR2 figure (or vice versa) for cross-border land comparisons.**

## 8. Where to look up PI for a parcel

- **Surety/AgriData mapping software** — the standard trade tool used by farm managers, appraisers, and lenders; overlays Bulletin 811 PI onto NRCS soil-map units per parcel, drawing underlying soil-map and productivity-factor data from the USDA NRCS eFOTG database. As of a November 2023 AgriData data update, displayed PI values include a ponding/flooding adjustment that can lower some ratings ([AgriData Illinois Bulletin 811 documentation](https://support.agridatainc.com/IllinoisBulletin811.ashx), relayed via search synthesis; direct fetch blocked at build time).
- **University of Illinois soil productivity site** ([soilproductivity.nres.illinois.edu](http://soilproductivity.nres.illinois.edu/)) — hosts the Bulletin 810/811 source PDFs and county soil-type PI tables.
- **USDA Web Soil Survey / SoilWeb** ([websoilsurvey.nrcs.usda.gov](https://websoilsurvey.nrcs.usda.gov/app/)) — gives the underlying soil map units for a parcel; PI itself is an Illinois-specific overlay, not a standard Web Soil Survey attribute.
- **County Soil and Water Conservation District offices** and the original county Soil Surveys.
- **County Assessor's office** for the Bulletin-810-basis PI used on the property-tax bill (see §2 and [10-tax-and-assessment.md](10-tax-and-assessment.md)) — this will generally differ from the Bulletin 811 figure quoted on a sale listing for the same soil.

A tract's "PI" as quoted in a sale listing or legal description is normally an **acreage-weighted average across all soil map units within the parcel boundary**, not a single soil-series number — PI ratings are assigned per map unit (soil type), not per whole farm. Source: aggregated from AgriData documentation and Bulletin 811 usage conventions, relayed via search synthesis at build time.

## Cross-references

- **[07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md)** — full ISPFMRA regional/class breakout of sale prices and cash rents (the productivity classes defined here in §3 are the backbone of that report's tables).
- **[10-tax-and-assessment.md](10-tax-and-assessment.md)** — the Bulletin 810 tax-assessment mechanics and the certified EAV-per-PI table (§2 above gives the formula only; the current-year $/acre-by-PI figures belong there).
- **[02-land-values-and-price-history.md](02-land-values-and-price-history.md)** — statewide/NASS land-value benchmarks referenced in §4.
- **[03-cash-rents.md](03-cash-rents.md)** — county-level NASS cash rent series the farmdoc PI regression (§5) is fit against.
- **[05-valuation-math.md](05-valuation-math.md)** — capitalization and value-per-acre mechanics that pair with the PI-to-value relationship in §4.
- **[glossary.md](glossary.md)** — PI, CRD, EAV, and related terms.

## Sources

- Olson, K.R. and Lang, J.M., *Bulletin 811: Optimum Crop Productivity Ratings for Illinois Soils*, University of Illinois College of ACES Office of Research, August 2000 (Table S2 revised 1/2/2012). https://www.ideals.illinois.edu/items/1070 ; http://soilproductivity.nres.illinois.edu/Bulletin811ALL.pdf
- NRCS, *University of Illinois Base Yield Indices (for use in IL only)*. https://www.nrcs.usda.gov/publications/University%20of%20Illinois%20Base%20Yield%20Indices%20(for%20use%20in%20IL%20only)%20-Query%20By%20Soil%20Survey%20Area.html
- NRCS eFOTG, *Factors for Estimating Productivity and Yield Indices of Illinois Soils*. https://efotg.sc.egov.usda.gov/references/public/IL/Calculating_productivity_and_yield_indices_in_Illinois_with_adjustment_factors_for_crop_productivity.pdf
- Illinois County Assessing Officials, "Farm Assessment." http://www.il-ccao.org/what-is-assessment/farm-assessment/
- Illinois Department of Revenue, farmland assessment guidance. https://tax.illinois.gov/localgovernments/property/farmland.html
- Illinois Compiled Statutes, 35 ILCS 200/ Article 10, Division 6 (Farmland Assessment). https://www.ilga.gov/legislation/ilcs/ilcs4.asp?DocName=003502000HArt.+10+Div.+6&ActID=596&ChapterID=8&SeqStart=21100000&SeqEnd=23100000
- ISPFMRA, *Illinois Farmland Values and Lease Trends*, 2025/2026 edition. https://ispfmra.org/land-values-archive/ ; https://ispfmra.org/download/2025-land-values-report/
- Schnitkey, G., "Determining the Average Cash Rent Based on Productivity Index," farmdoc daily 7:205, Nov. 7, 2017. https://farmdocdaily.illinois.edu/2017/11/determining-average-cash-rent-productivity-index.html
- Schnitkey, Paulson, Zulauf, Baltz, "Setting 2025 Cash Rents," farmdoc daily 14:159, Sept. 3, 2024.
- farmdoc daily 15:184, "Relationships between Average Cash Rents and Soil Productivity," Oct. 7, 2025. https://farmdocdaily.illinois.edu/2025/10/relationships-between-average-cash-rents-and-soil-productivity.html
- USDA NASS, *Land Values 2025 Summary*, released August 1, 2025. https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0825.pdf
- Illinois Soil Classifiers Association, "Drummer" (State Soil). https://illinoissoils.org/drummer/
- NRCS Official Series Descriptions: Ipava (https://soilseries.sc.egov.usda.gov/OSD_Docs/I/Ipava.html), Muscatune (https://soilseries.sc.egov.usda.gov/OSD_Docs/M/MUSCATUNE.html), Sable (https://soilseries.sc.egov.usda.gov/OSD_Docs/S/SABLE.html)
- DreamDirt, "CSR2 & PI: What They Mean for Your Farm's Land Value." https://dreamdirt.com/soil-productivity-ratings-explained-csr2-pi-and-what-they-mean-for-farmland-value/
- AgriData Inc., Illinois Bulletin 811 documentation. https://support.agridatainc.com/IllinoisBulletin811.ashx
- USDA Web Soil Survey. https://websoilsurvey.nrcs.usda.gov/app/
- University of Illinois soil productivity site. http://soilproductivity.nres.illinois.edu/
- WGLT, "Corn and soybean king: McLean County farmers led state, nation in 2022 production," June 2023. https://www.wglt.org/local-news/2023-06-06/corn-and-soybean-king-mclean-county-farmers-led-state-nation-in-2022-production

**Build-environment note:** per [../SOURCING.md](../SOURCING.md), this session's network policy blocked direct fetching of nearly every primary-source host above (proxy-level 403 on farmdocdaily.illinois.edu, ideals.illinois.edu, nass.usda.gov, ilga.gov, tax.illinois.gov, ispfmra.org, agridatainc.com, soilproductivity.nres.illinois.edu, and others). All figures above were corroborated via a hosted web-search service's result synthesis and cross-checked across multiple independent secondary sources at build time, not read directly from the primary PDFs. See [../sources/MANIFEST.md](../sources/MANIFEST.md) for the full archive status. A follow-up session with working access to these hosts should fetch and checksum the primary documents, and in particular should resolve: (1) the exact 2025-vintage farmdoc cash-rent regression coefficients, (2) the current IDOR Publication 122 certified $/acre-by-PI table, (3) Sable's precise Bulletin 811 PI value, and (4) a full 102-county PI table.
