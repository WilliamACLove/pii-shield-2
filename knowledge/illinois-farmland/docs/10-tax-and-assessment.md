# Illinois Farmland Property Tax and Use-Value Assessment

Reference material only — not tax, legal, or accounting advice. Consult a qualified Illinois property tax attorney, assessor, or CPA for parcel-specific determinations.

**Data current as of:** Assessment Year (AY) 2025 and AY2026 certified values (Illinois Dept. of Revenue); FBFM actual-tax data through 2024; Chicago Fed AgLetter through Q4 2025.
**Built/verified:** 2026-07-12

## 1. The Farmland Assessment Law: use value, not market value

Since the Farmland Assessment Law took effect in 1977, Illinois has assessed qualifying farmland on its **agricultural use value** rather than its fair-cash (market) value — a deliberate departure from the general property-tax rule that all other real estate is assessed at market value. The law was driven by Illinois Farm Bureau advocacy to insulate working farmland from being taxed on speculative or development-driven market prices (University of Illinois farmdoc daily, "Illinois Farmland Assessments – Current Issues and Considerations," March 2013, describing the 1977-origin law: https://farmdocdaily.illinois.edu/2013/03/illinois-farmland-assessments.html).

The statutory basis is **35 ILCS 200/10-110 through 10-147**, Property Tax Code, Article 10, Division 6 (State of Illinois, ilga.gov, current codification: https://ilga.gov/legislation/ilcs/ilcs4.asp?DocName=003502000HArt.+10+Div.+6&ActID=596&ChapterID=8&SeqStart=20200000&SeqEnd=22200000).

**Eligibility.** Section 10-110 requires that a parcel have been "used as a farm" for the two immediately preceding years to qualify for use-value assessment, with EAV then determined under Sections 10-115 through 10-140. "Farm" is defined broadly (crops, livestock, dairy, horticulture, fur farming, bees, fish/wildlife farming) (35 ILCS 200/10-110, ilga.gov: https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=003502000K10-110). Practical guidance generally requires 50%-or-more of contiguous acreage to be in active farm use; consult a local assessor for parcel-specific determinations.

See [01-market-overview.md](01-market-overview.md) for how this regime shapes overall Illinois farmland economics, and [09-sales-market-structure.md](09-sales-market-structure.md) for how buyers underwrite tax liability in a purchase.

## 2. The income-capitalization mechanics: from soil PI to certified EAV

### 2.1 Agricultural Economic Value per Productivity Index (PI)

Each parcel's cropland is rated on the University of Illinois' **Bulletin 810** soil Productivity Index (PI) system, which all Illinois counties were mandated to adopt for farmland assessment starting in **2006**; Bulletin 810's Table 2 was last updated in **2012** (State of Illinois Property Tax Appeal Board, "Farm Appeal Information" brochure: https://www.ptab.illinois.gov/PDF/brochures/ptab-8.pdf). PI 111 is defined by statute as the state's "median cropped soil" and serves as the anchor for the annual change cap described in §3.

For each PI, the Illinois Department of Revenue — advised by the **Farmland Assessment Technical Advisory Board (FATAB)** — certifies an **Agricultural Economic Value** using a straightforward income-capitalization formula set out in **35 ILCS 200/10-115(d)** (ilga.gov: https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=003502000K10-115):

```
Agricultural Economic Value(PI) =
    [5-yr avg. Gross Income per acre(PI) − 5-yr avg. Production Costs per acre(PI)]
    ÷ 5-yr avg. Federal Land Bank / Farm Credit farmland mortgage interest rate
```

- **Gross Income and Production Costs** are certified annually by FATAB per soil PI, based on statewide average-level farm management assumptions — not any individual farm's actual results.
- **The interest rate** is the 5-year moving average of the Federal Land Bank (now Farm Credit System) farmland mortgage rate.

> **Primary-source confirmation (regulation text, read directly):** the Illinois Administrative Code's farmland-assessment review rule confirms this structure from the primary text — county Farmland Assessment Review Committees may object to "the base data (i.e., productivity indices or agricultural economic values (AEV)) provided by the Farmland Assessment Technical Advisory Board and utilized by the Department," and any challenge "must be based upon the same procedures and time frames (e.g., same 5 year period for farmland mortgage interest rate) as the base data" (86 Ill. Adm. Code 110.165, "Farmland Assessment Review Procedures," implementing Property Tax Code §10-120; retrieved via the Descrybe legal database, 2026-07-12: https://www.ilga.gov/commission/jcar/admincode/086/086001100001650R.html). This is the one element of the assessment mechanics in this document verified against primary legal text rather than convergent secondary evidence.
- This is structurally the same NOI ÷ cap-rate logic used in market valuation (see [05-valuation-math.md](05-valuation-math.md)), but with statutorily fixed, statewide-averaged inputs rather than a specific parcel's rent and expenses.

*Worked example (illustrative — inputs not independently confirmed against the primary PDF table):* if a PI's 5-year average net income to land is $200/acre and the certified 5-year average Farm Credit mortgage rate is 4.83% (the cited AY2025 rate, §3 below), Agricultural Economic Value ≈ $200 ÷ 0.0483 ≈ $4,141/acre.

### 2.2 The 33⅓% assessment level

The certified **Equalized Assessed Value (EAV) per acre** of cropland for each PI equals **33⅓% (one-third) of that PI's Agricultural Economic Value** (35 ILCS 200/10-115; Illinois Dept. of Revenue, Publication 122, January 2026 edition: https://tax.illinois.gov/content/dam/soi/en/web/tax/research/publications/pubs/documents/pub-122.pdf). This mirrors the general 1/3-of-value assessment level applied to most other Illinois property classes outside Cook County, keeping farmland's *ratio* consistent with the rest of the tax base even though its *value base* (capitalized farm income, not market sale price) is entirely different.

Continuing the worked example: EAV ≈ 33.33% × $4,141 ≈ $1,380/acre, before applying the annual change cap described next.

## 3. The 10% annual change cap (PA 98-0109) and its cumulative effect

**Public Act 98-0109** amended 35 ILCS 200/10-115(e), effective assessment year 2015 forward, to cap the year-over-year change in each PI's certified EAV:

> "...any increase or decrease in the equalized assessed value per acre by soil productivity index shall not exceed 10% from the immediate preceding year's soil productivity index certified assessed value of the median cropped soil [PI 111]; in tax year 2015 only, that 10% limitation shall be reduced by $5 per acre." (35 ILCS 200/10-115(e), as amended by P.A. 98-0109; ilga.gov: https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=003502000K10-115)

Key mechanics:

- The cap is calculated as **10% of the prior year's PI 111 (median cropped soil) certified value**, producing a single **dollar** ceiling that is then applied **uniformly across all PI levels** — it is not a percentage-of-each-PI's-own-value cap.
- It dampens both increases *and* decreases, smoothing farmland tax bills even when the raw income-capitalization formula would imply a larger swing.
- Combined with the underlying 5-year income/rate averaging, the cap means certified values (and ultimately tax bills) lag actual farm economic conditions by roughly **5–7 years**. Illinois Extension states plainly that "2025 property taxes will be paid on 2024 calculations, accounting for 2023 farm income, ... it takes seven years to fully adjust to ever-changing farm economic conditions" (Illinois Extension, Farm Coach blog, "Farmland Owner Series: Understanding Illinois Farmland Property Taxes," May 23, 2025: https://extension.illinois.edu/blogs/farm-coach/2025-05-23-farmland-owner-series-understanding-illinois-farmland-property-taxes).

**Formula:**

```
EAV per acre(PI, year t) = 33.33% × Agricultural Economic Value(PI, year t),
  subject to: |EAV(PI, year t) − EAV(PI, year t−1)| ≤ 10% × EAV(PI 111, year t−1)
```

*Worked example, AY2026:* 10% of the AY2025 PI 111 certified value = **$56.71/acre** (see Table 1 below), so no PI's AY2026 certified EAV could move by more than $56.71/acre from its AY2025 value, regardless of what 33.33% × Agricultural Economic Value at the AY2026 5.27% cap rate would otherwise produce (Illinois Dept. of Revenue, "Certified Values for Assessment Year 2026 ($ per acre)": https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2026-farmland-certified-values.pdf).

## 4. Assessment level by farmland classification

Only bare cropland, pasture, "other farmland," and wasteland get use-value treatment. Farm buildings and homesites are carved out and assessed conventionally.

| Land Classification | Assessment Basis |
|---|---|
| Cropland | 100% of certified EAV/acre for its (debased) Productivity Index |
| Permanent pasture | 1/3 of the EAV/acre the same PI would receive as cropland; floor = 1/3 of the EAV/acre of the lowest certified cropland PI |
| Other farmland (non-cropland, non-pasture, non-homesite, non-wasteland) | 1/6 of the EAV/acre the same PI would receive as cropland; floor = 1/6 of the EAV/acre of the lowest certified cropland PI |
| Wasteland | Assessed at its contributory value to the farm parcel (minimal) |
| Farm dwelling, appurtenant structures, and underlying site | 33⅓% of fair cash (market) value — assessed like ordinary residential property, **not** at ag-use value |
| Other farm buildings (machine sheds, grain bins, livestock buildings, roadside stands) | 33⅓% of value based on current use and contribution to farm productivity |

*Source: 35 ILCS 200/10-125, 10-140, 10-145, Illinois Property Tax Code (https://ilga.gov/legislation/ilcs/ilcs4.asp?DocName=003502000HArt.+10+Div.+6&ActID=596&ChapterID=8&SeqStart=20200000&SeqEnd=22200000); corroborated by Illinois Dept. of Revenue Publication 122, January 2026 (https://tax.illinois.gov/content/dam/soi/en/web/tax/research/publications/pubs/documents/pub-122.pdf) and county assessor summaries (e.g., Henry County: https://www.henrycty.com/320/Farmland-Assessment).*

```
EAV(permanent pasture, PI) = (1/3) × EAV(cropland, same PI)   [floor: (1/3) × EAV(cropland, lowest certified PI)]
EAV(other farmland, PI)    = (1/6) × EAV(cropland, same PI)   [floor: (1/6) × EAV(cropland, lowest certified PI)]
EAV(wasteland)             = contributory value to the farm parcel (case-by-case, minimal)
```

*Worked example:* if a given PI's cropland EAV is $600/acre, permanent-pasture EAV = $600 × 1/3 = $200/acre, and "other farmland" EAV = $600 × 1/6 = $100/acre (35 ILCS 200/10-125).

## 5. Current certified values (AY2025 / AY2026)

| Assessment Year (taxes payable) | 5-Year Capitalization Rate | Max Allowed Increase at PI 111 (10% cap, PA 98-0109) |
|---|---|---|
| 2025 (taxes payable 2026) | 4.83% | $51.56/acre over the 2024 PI 111 certified value |
| 2026 (taxes payable 2027) | 5.27% | $56.71/acre over the 2025 PI 111 certified value |

*Source: Illinois Department of Revenue, "Certified Values for Assessment Year 2025 ($ per acre)" (https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2025-farmland-certified-values.pdf) and "Certified Values for Assessment Year 2026 ($ per acre)" (https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2026-farmland-certified-values.pdf); see also Publication 122 (January 2026), Table 1.*

An internal consistency check supports these two figures: the AY2025 cap ($51.56) implies a 2024 PI-111 base of ≈$515.60, and the AY2026 cap ($56.71) implies a 2025 PI-111 base of ≈$567.10; $515.60 + $51.56 ≈ $567.16, matching the implied 2025 base almost exactly — evidence the cap was binding in AY2025 and that both figures are internally coherent.

**Unresolved: reported P.A. 104-0468 cap-rate "guardrails."** Separate secondary coverage (farmweeknow.com) describes Public Act 104-0468 as adding guardrails to the capitalization rate — three percentage points added to the published rate, with an 8% floor and a 10% ceiling — which would make the *effective* AEV divisor 8.00% against a 4.83% published rate and 8.27% against a 5.27% published rate. The rates in the table above are the published certified rates as stated in the IDOR documents; whether and from which assessment year the 104-0468 adjustment applies could not be reconciled against the statute or IDOR publications at build time. Both readings are reported per `../SOURCING.md` rule 6; resolve against 35 ILCS 200/10-115 (current codification) and the current Publication 122 before computing AEVs from these rates. The same open item is flagged in [05-valuation-math.md](05-valuation-math.md) §8.

**Figures not confirmed against a primary source at build time, and omitted or flagged accordingly:**

- A statewide-average certified cropland EAV/acre of **$575.46** was attached to *both* AY2025 and AY2026 in different research passes — almost certainly a search-summarization artifact rather than two identical annual values. **[not confirmed against a primary source at build time — omitted from this table pending direct PDF/Table 1 reconciliation]**
- PI-130 (top-of-scale) AY2026 certified EAV figures ($897.38/acre cropland, $608.01/acre permanent pasture, $289.37/acre other farmland) failed verification: applying the 1/3 and 1/6 ratios from §4 to $897.38 implies pasture ≈ $299.13 and other farmland ≈ $149.56 — neither matches the $608.01 or $289.37 figures reported. The verification pass also found the search-summary layer gave self-contradictory explanations for the same numbers. **These three figures are dropped from this document per the verifier's corrected verdict; treat any PI-by-PI dollar table as unconfirmed until read directly from the primary PDF (2026-farmland-certified-values.pdf or Pub. 122 Table 1).**
- The complete PI-by-PI certified value schedule (PI 33 through 130+) was not retrievable in this research pass and is not reproduced here.
- A "Certification of Assessment Year 2027 Farmland Values" document was found posted by Marion County (dated April 20, 2026) ahead of the normal certification cycle, separately citing a $302.55 PI-111 cap figure for AY2027 — this is a different (later) assessment year, not a contradiction of the AY2026 figures above, but its early posting is unexplained and unconfirmed.

## 6. What actually gets paid: property tax bills vs. certified EAV

Certified EAV (§§2–5) is only the *assessment* input. The actual **tax bill** = certified EAV (after any local equalization/multiplier) × the local aggregate tax rate (county, township, school district, and other taxing bodies) — a rate that varies by taxing jurisdiction and is outside the scope of the state-level farmland formula.

The most reliable real-world benchmark for actual dollars paid comes from the Illinois Farm Business Farm Management (FBFM) association's records for central-Illinois grain farms:

| Year | Real Estate Tax Paid ($/owned acre) |
|---|---|
| 2000 | $33 |
| 2024 | ~$76 |

*Source: University of Illinois farmdoc daily, "Cash Requirements of Owned Farmland: 2025 vs. 2005" (October 2025): https://farmdocdaily.illinois.edu/2025/10/cash-requirements-of-owned-farmland-2025-vs-2005.html; companion article "Comparing Returns to Owned vs Cash Rented Farmland" (farmdoc daily 15:155, August 26, 2025): https://farmdocdaily.illinois.edu/2025/08/comparing-returns-to-owned-vs-cash-rented-farmland.html. Figures describe high-productivity central-Illinois FBFM grain farms — not a statewide or regional-comparison average.*

This is a compound annual growth rate of roughly **3.5%/year** from 2000 to 2024 (check: (76/33)^(1/24) − 1 ≈ 3.5%), modestly slower than the ~4%/year growth in cash rents and total ownership costs over the same period (farmdoc daily, same source).

**A separate FBFM-sourced figure of $27/acre for 2005** appears in a different farmdoc daily comparison article; this conflicts with straight-line interpolation from the $33 (2000) / $76 (2024) series above (which would imply roughly $38–40/acre by 2005) and the two figures come from different articles/samples. Per SOURCING.md rule 6, both are reported here rather than silently reconciled: treat the $33→$76 (2000→2024) series as the primary trend line, and the $27 (2005) figure as a secondary data point requiring reconciliation against the underlying FBFM summary tables.

**Regional ($/acre tax) breakdown across northern, central, and southern Illinois was not located in this research pass.** The ISPFMRA *Illinois Farmland Values and Lease Trends* report (organized by the state's 10 regions; see [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md)) likely contains this breakdown but its content was not independently confirmed here. **[not confirmed against a primary source at build time]**

**Caution on generic "effective tax rate" estimates.** Illinois's overall effective property-tax rate is sometimes cited (from a secondary, non-primary source) at roughly 1.88% — among the highest in the U.S. — and applied to market cropland values (e.g., USDA NASS's 2025 national average of ~$5,830/acre) to produce a back-of-envelope estimate near $110/acre in tax on a hypothetical 50-acre parcel. **This approach is methodologically inconsistent with how Illinois actually taxes farmland**, because — per §1 — farmland is explicitly assessed on agricultural use value, not market value. The FBFM actual-tax figure (~$76/acre in 2024, above) is the economically correct benchmark for Illinois cropland; the market-value-based 1.88% estimate is presented here only as illustrative contrast, per SOURCING.md's rule on flagging low-confidence secondary figures (source: LegalClarity, "Average Land Tax Per Acre by Region and Land Type," 2025, exact publication date not confirmed: https://legalclarity.org/average-land-tax-per-acre-by-region-and-land-type/ — low confidence, secondary source).

## 7. Property tax in the NOI / net-rent framework

Property tax is a real, recurring cash outflow to the landowner and belongs in the net-operating-income calculation used for market valuation (see [05-valuation-math.md](05-valuation-math.md) for the full derivation) — a wholly separate calculation from the statutory Agricultural Economic Value used only for the tax assessment itself:

```
NOI (owner's net cash return) = Gross Cash Rent (or crop-share equivalent)
                                 − Property Tax − Insurance − Management/Other Ownership Costs

Farmland Value (income approach) = NOI ÷ Market Capitalization Rate
```

*Source: farmdoc / Illinois Extension income-approach and cash-rent literature, e.g. https://peoplescompany.com/blog/the-income-approach-what-earnings-tell-us-about-land-value and farmdoc daily cash-rent/returns articles.*

*Worked example:* gross cash rent $300/acre, property tax $76/acre (2024 FBFM central-Illinois average, §6), insurance/management $10/acre → NOI = $300 − $76 − $10 = $214/acre. At a 3% market cap rate (farmdoc-observed market cap rates compressed from roughly 4–5% in the 1990s to about 2–3% by 2022), implied value ≈ $214 ÷ 0.03 ≈ $7,133/acre. This is illustrative only — actual cap rates, rents, and tax bills vary materially by region and land quality; see [03-cash-rents.md](03-cash-rents.md) and [08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md).

Because certified EAV (§§2–3) responds to farm income and interest rates with a 5–7 year lag while market land values and cash rents respond to current conditions in near-real time (see [11-macro-drivers-and-outlook.md](11-macro-drivers-and-outlook.md) for the current cycle, including Chicago Fed AgLetter data showing District farmland values up in 2025 alongside weakening agricultural credit conditions — 5.6% of the Seventh District's farm loan portfolio rated "major" or "severe" repayment risk in Q4 2025, the highest since Q2 2020: Federal Reserve Bank of Chicago, AgLetter, "Midwest Farmland Values Ended 2025 with Solid Growth," February 2026: https://www.chicagofed.org/publications/agletter/2025-2029/february-2026), property tax as a *share* of NOI can swing meaningfully across a rent or land-value cycle even while the underlying EAV barely moves.

## 8. Appeals

Assessment disputes (e.g., soil PI misclassification, flooding-related productivity loss) proceed through the local Board of Review and then, if unresolved, the **Illinois Property Tax Appeal Board (PTAB)**. Farm-specific appeals require the farm appeal form and evidence of the affected PI/soil types; flooding claims require a ten-year yield-loss history for the affected acreage. Appeals must generally be filed within 30 days of the Board of Review's decision (or within 30 days of a favorable prior-year PTAB decision) (State of Illinois PTAB, "Farm Appeal Information" brochure: https://www.ptab.illinois.gov/PDF/brochures/ptab-8.pdf; PTAB Practice and Procedures: https://www.ptab.illinois.gov/PractProc.html).

## 9. Development-conversion implications

Two distinct mechanisms govern farmland leaving the use-value regime:

1. **Loss of ordinary use-value eligibility.** If a parcel simply stops meeting the "used as a farm" test of §10-110 (e.g., sold and taken out of agricultural production), it loses eligibility for use-value assessment going forward and reverts to conventional fair-cash-value assessment. The sources reviewed in this research pass did **not** surface any punitive back-tax or "rollback tax" recapture mechanism — comparable to schemes used in some other states' agricultural preferential-assessment statutes — attached to this transition. **[This "no rollback tax" conclusion is a low-confidence synthesis across secondary summaries, not a directly verified statutory reading, and should be independently confirmed before being relied upon.]**
2. **The Developer's Exemption (35 ILCS 200/10-30, Publication 134).** A separate, narrower provision offers a reduced "preferential/transitional assessment" for platted, subdivided land held for future residential, commercial, or industrial development but not yet built on or sold. The preferential treatment ends — and assessed value is prorated from the completion date (or January 1 of the next assessment year, if completion follows the close of the assessment books) — once a habitable structure is completed, the lot is sold, or the land is put to residential/business/commercial use (Illinois Dept. of Revenue, Publication 134, "Developer's Exemption," July 2021 edition — most recent version identified; statute current as of July 2026: https://tax.illinois.gov/content/dam/soi/en/web/tax/research/publications/pubs/documents/pub-134.pdf). **[This synthesis is flagged low-confidence per the underlying research notes and should be independently re-checked against the statute and current edition of Pub. 134 before publication-grade reliance.]**

For the market and pricing side of conversion decisions, see [02-land-values-and-price-history.md](02-land-values-and-price-history.md) and [09-sales-market-structure.md](09-sales-market-structure.md).

## Sources

- 35 ILCS 200/10-110 through 10-147, Illinois Property Tax Code, Article 10, Division 6 (State of Illinois, ilga.gov, current codification): https://ilga.gov/legislation/ilcs/ilcs4.asp?DocName=003502000HArt.+10+Div.+6&ActID=596&ChapterID=8&SeqStart=20200000&SeqEnd=22200000
- 35 ILCS 200/10-115 (Agricultural Economic Value formula; 33⅓% assessment level; PA 98-0109 10% cap): https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=003502000K10-115
- 35 ILCS 200/10-110 (use-as-a-farm eligibility): https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=003502000K10-110
- 35 ILCS 200/10-125 (assessment level by farmland classification): https://ilga.gov/legislation/ilcs/documents/003502000K10-125.htm
- 35 ILCS 200/10-140, 10-145 (farm buildings and homesites assessed conventionally): https://ilga.gov/legislation/ilcs/documents/003502000K10-145.htm
- 35 ILCS 200/10-30 and Illinois Dept. of Revenue Publication 134, "Developer's Exemption," July 2021 edition: https://tax.illinois.gov/content/dam/soi/en/web/tax/research/publications/pubs/documents/pub-134.pdf
- Illinois Department of Revenue, "Certified Values for Assessment Year 2025 ($ per acre)": https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2025-farmland-certified-values.pdf
- Illinois Department of Revenue, "Certified Values for Assessment Year 2026 ($ per acre)": https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2026-farmland-certified-values.pdf
- Illinois Department of Revenue, Publication 122 (farmland assessment guidance), January 2026 edition: https://tax.illinois.gov/content/dam/soi/en/web/tax/research/publications/pubs/documents/pub-122.pdf
- State of Illinois Property Tax Appeal Board, "Farm Appeal Information" brochure: https://www.ptab.illinois.gov/PDF/brochures/ptab-8.pdf
- State of Illinois Property Tax Appeal Board, Practice and Procedures: https://www.ptab.illinois.gov/PractProc.html
- University of Illinois, Bulletin 810 (soil Productivity Index methodology): http://soilproductivity.nres.illinois.edu/Bulletin810ALL.pdf
- University of Illinois farmdoc daily, "Illinois Farmland Assessments – Current Issues and Considerations," March 2013: https://farmdocdaily.illinois.edu/2013/03/illinois-farmland-assessments.html
- University of Illinois farmdoc daily, "Cash Requirements of Owned Farmland: 2025 vs. 2005," October 2025: https://farmdocdaily.illinois.edu/2025/10/cash-requirements-of-owned-farmland-2025-vs-2005.html
- University of Illinois farmdoc daily, "Comparing Returns to Owned vs Cash Rented Farmland," farmdoc daily 15:155, August 26, 2025: https://farmdocdaily.illinois.edu/2025/08/comparing-returns-to-owned-vs-cash-rented-farmland.html
- Illinois Extension, Farm Coach blog, "Farmland Owner Series: Understanding Illinois Farmland Property Taxes," May 23, 2025: https://extension.illinois.edu/blogs/farm-coach/2025-05-23-farmland-owner-series-understanding-illinois-farmland-property-taxes
- Federal Reserve Bank of Chicago, AgLetter, "Midwest Farmland Values Ended 2025 with Solid Growth," February 2026: https://www.chicagofed.org/publications/agletter/2025-2029/february-2026
- Henry County, Illinois, Assessor, "Farmland Assessment" summary: https://www.henrycty.com/320/Farmland-Assessment
- LegalClarity, "Average Land Tax Per Acre by Region and Land Type," 2025 (secondary source, low confidence, illustrative context only): https://legalclarity.org/average-land-tax-per-acre-by-region-and-land-type/
- ISPFMRA, "2025 Land Values Report" (referenced for regional detail not independently confirmed in this pass): https://ispfmra.org/download/2025-land-values-report/

**Build-environment disclosure:** per `../SOURCING.md`, this knowledge base was assembled in an environment where direct fetching of source pages/PDFs was blocked; the figures above rest on a hosted web-search service's summaries of primary documents, cross-checked internally (ratio and arithmetic consistency checks) and against `../sources/MANIFEST.md`, rather than on direct reads of the underlying PDFs/statute pages. A follow-up session with working direct access should fetch and checksum each document in the manifest, and in particular should pull the complete PI-by-PI certified value table (Publication 122, Table 1, or the standalone certified-values PDFs) to resolve the flagged PI-130 and statewide-average-EAV discrepancies in §5.
