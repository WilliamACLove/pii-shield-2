# Farmland Valuation Mathematics (Illinois)

Reference on the formulas used to value Illinois farmland: income capitalization, the Gordon-growth/present-value model, interest-rate sensitivity, price-to-rent multiples, per-tillable-acre normalization, the three appraisal approaches, and Illinois's statutory capitalization formula for property-tax assessment.

**Data current as of:** NASS 2025 Land Values Summary (August 2025); ISPFMRA 2025 Illinois Land Values and Lease Trends (March 2025); Chicago Fed AgLetter, February and May 2026 issues; Illinois Dept. of Revenue certified farmland values, assessment year 2026; farmdoc daily through July 2026.
**Built/verified:** 2026-07-12

## 1. The core identity: V = NOI / r

Every valuation method in this document is a variant of one identity, borrowed from general income-property appraisal and applied to farmland by University of Illinois farmdoc economists (notably Schnitkey and Sherrick):

```
V = NOI / r

V   = value of the farmland (per acre, or in total)
NOI = net operating income attributable to the land
r   = capitalization rate ("current return" in farmdoc usage)
```

For farmland, NOI is **not** gross cash rent — it is rent net of landlord-borne carrying costs:

```
NOI = CashRent − PropertyTax − Insurance − Management

CashRent   = market-level cash rent per acre
PropertyTax = landlord's property tax liability per acre
Insurance   = landlord's liability/hazard insurance per acre
Management  = an allowance or fee for landlord oversight, if applicable
```

*Source: standard income-approach formulation; applied to Illinois cash-rented farmland in Gary Schnitkey and Bruce Sherrick, "Income and Capitalization Rate Risk in Agricultural Real Estate Markets," *Choices Magazine*, 2011 Q2 ([link](https://www.choicesmagazine.org/choices-magazine/theme-articles/farmland-values/income-and-capitalization-rate-risk-in-agricultural-real-estate-markets)); corroborated across ag-lending secondary sources. Verified: confirmed as an internally consistent identity and as the framing used by farmdoc/Choices; the underlying farmdocdaily.illinois.edu page could not be directly fetched in this build (network policy), but multiple independent search snippets reproduced the formulation verbatim.*

**Worked example (central Illinois, illustrative).** Market cash rent $300/acre; property tax $35/acre; insurance $5/acre; management allowance $10/acre:

```
NOI = 300 − 35 − 5 − 10 = $250/acre
```

At a market capitalization rate of 3.0% (close to the ~2.7% current return farmdoc reported for Illinois in 2025 — see §3):

```
V = 250 / 0.030 = $8,333/acre
```

This sits just below NASS's reported 2025 Illinois average farm real estate value of $8,930/acre and below the $9,850/acre cropland average (USDA NASS, *2025 Land Values Summary*, August 2025, describing 2025 values — see [02-land-values-and-price-history.md](02-land-values-and-price-history.md)) — consistent with cropland-quality tracts commanding above-average per-acre NOI, or trading at a somewhat lower observed cap rate than the round 3.0% used here for illustration. **This worked example uses assumed, not published, expense figures; recompute with local tax and insurance data before relying on it.**

## 2. Implied (observed) capitalization rate

Because V = NOI/r, the cap rate can be read backward out of any observed rent/price pair — this is how "the" Illinois cap rate is actually measured in practice; there is no single published survey of r itself.

```
r = Rent / Price          (gross form)
r = NOI  / Price          (net form, expenses removed)
```

*Source: farmdoc daily's "current return to farmland" framing; treated as the empirical counterpart of the theoretical discount rate in Oscar Burt's and Featherstone & Baker's present-value models (§4).*

**Worked example, Illinois 2025.** Statewide average non-irrigated cropland cash rent was **$264/acre in 2025**, down $5 from a record $269/acre in 2024 (USDA NASS, *2025 Land Values and Cash Rents Highlights*, August 2025 — this is the corrected figure; an initial pass had used a $4 decline, corrected against the primary release description reproduced verbatim by DTN and FarmWeek Now; see [03-cash-rents.md](03-cash-rents.md) §1). Illinois cropland value was $9,850/acre in the same release:

```
r = 264 / 9,850 = 0.0268 ≈ 2.7%
```

This is a gross-rent cap rate (it does not net out property tax/insurance/management), yet it lands almost exactly on the ~2.7% "current return" figure farmdoc separately reports for Illinois farmland in 2025 (§3) — a useful internal consistency check, though the two are not derived from identical inputs and the match should be read as corroborative rather than exact. **Caution on measurement systems:** the $264/acre figure is NASS's statewide average *cropland* cash rent (a survey of what operators report actually paying), while the $9,850/acre figure is NASS's *cropland value* (what operators report land would sell for) — both come from the same NASS release but are different survey questions, not a matched paired sample of the same parcels (per `../SOURCING.md` rule 4).

## 3. Illinois cap-rate levels and history

Farmdoc daily reports that **Illinois farmland cap rates compressed from roughly 4-5% in the 1990s to about 2-3% by 2022**, with the **2025 current return to Illinois farmland at approximately 2.7%**, against a 10-year Treasury Constant Maturity (CMT) rate averaging **4.3%** over the same year (farmdoc daily, "Farmland Prices and Government Programs," July 7, 2026, [link](https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html); the 2.7%/4.3% figures also appear in the lineage "Outlook for Farmland Values in 2025," November 26, 2024, [link](https://farmdocdaily.illinois.edu/2024/11/outlook-for-farmland-values-in-2025.html)).

*Verification note:* the 2.7%/4.3% figure for 2025 was independently reproduced verbatim across multiple search passes (verdict: confirmed). The 1990s-to-2022 compression range (4-5% → 2-3%) is corroborated by secondary aggregation of farmdoc's long-run rent/price series but was **not independently recomputed from the raw farmdoc data table** in this build — treat the decade-level range as well-supported but not document-confirmed at the level of individual years. A full year-by-year series should be pulled from farmdoc's "Farmland Values and Returns by State Through Time" tool; see [08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md).

This multi-decade compression — a falling denominator in V = NOI/r — is a primary driver of Illinois land-value appreciation independent of any growth in rents themselves; see §5 for the interest-rate transmission mechanism and [02-land-values-and-price-history.md](02-land-values-and-price-history.md) for the resulting price series.

## 4. Gordon growth / present-value model

When cash flows are expected to grow at a constant rate rather than stay flat, the simple capitalization formula generalizes to the Gordon growth (constant-growth perpetuity) model:

```
V = CF1 / (r − g)

V   = current value of the farmland
CF1 = expected net cash flow (NOI) in the next period
r   = required rate of return / discount rate
g   = expected constant perpetual growth rate of NOI

Note: setting g = 0 collapses this to V = NOI / r (§1).
```

*Source: standard finance formulation, applied to farmland by Oscar R. Burt, "Econometric Modeling of the Capitalization Formula for Farmland Prices," *American Journal of Agricultural Economics*, Vol. 68 (1986), pp. 10-26 (a second-order rational distributed lag on net crop-share rents; [journal link](https://academic.oup.com/ajae/article/68/1/10/62057)), and Allen Featherstone and Timothy Baker, "An Examination of Farm Sector Real Asset Dynamics: 1910-85," *American Journal of Agricultural Economics*, 1987 (land value as the discounted sum of expected future rents). Barry Falk formally tested the present-value model with cointegration methods, building on Campbell & Shiller (1987), in "Formally Testing the Present Value Model of Farmland Prices," *AJAE* 73(1) (1991), pp. 1-10 — using 1921-86 Iowa data, he found real farmland prices deviate systematically from fundamentals, i.e., evidence against the pure constant-expected-returns present-value model ([citation record](https://ideas.repec.org/p/isu/genstf/199006010700001213.html)). Schnitkey and Sherrick's 2011 *Choices* article (§1) is the direct applied descendant of this line at farmdoc. *Verified: Burt and Falk citation details (journal, volume, pages, and abstract content) confirmed via Oxford Academic/Wiley listings; the Featherstone & Baker (1987) citation rests on a secondary academic-search aggregation only.*

**Worked example (illustrative, not a farmdoc point estimate).** Central-Illinois FBFM data show cash rent on cash-rented grain farms rising from $132/acre (2000) to $336/acre (2024) — an average annual growth rate of:

```
g = (336 / 132)^(1/24) − 1 = 2.545^(0.04167) − 1 ≈ 0.0397 ≈ 4.0%/year
```

(farmdoc daily, "Comparing Returns to Owned vs. Cash-Rented Farmland," August 26, 2025, describing FBFM-enrolled central-Illinois grain farms through 2024, [link](https://farmdocdaily.illinois.edu/2025/08/comparing-returns-to-owned-vs-cash-rented-farmland.html)). This is *rent* growth, not NOI-net-of-expenses growth, and is used here only as an illustrative proxy for g. If next-period NOI is projected at $250/acre and the required unlevered total return r is assumed at 6.5%:

```
V = 250 / (0.065 − 0.040) = 250 / 0.025 = $10,000/acre
```

This example exists to show the model's core weakness in practice: the **(r − g) spread is small and the result is extremely sensitive to it** — an 0.5-point change in either r or g moves V by roughly 20%. Neither r=6.5% nor g=4.0% (as an NOI proxy) is a farmdoc-published point estimate; they are assumed for demonstration only.

## 5. Interest-rate relationship

Because r is a required rate of return, it competes with yields available on other assets. Farmdoc daily uses the spread between the current farmland return and the 10-year Treasury CMT as an equilibrium check:

```
Spread = r_10yr − r_farmland

If Spread > 0 and widening: downward pressure on V is implied — since V = NOI/r,
either r must rise toward competing-asset yields, or NOI must rise, to close the gap.
```

*Source: farmdoc daily's "Outlook for Farmland Values"/"Farmland Prices and Government Programs" series (§3); conceptually descends from the Burt/Featherstone-Baker discount-rate framework, using the risk-free Treasury rate as a benchmark component of r.*

**Worked example.** 2025: Illinois current farmland return ≈ 2.7% vs. 10-year CMT average ≈ 4.3%:

```
Spread = 4.3% − 2.7% = 1.6 percentage points
```

Farmdoc reads this as a signal of mild, not severe, downward pressure on Illinois values — consistent with the plateau/softening reported by ISPFMRA and the Chicago Fed's AgLetter through 2025-2026 (§7 in [03-cash-rents.md](03-cash-rents.md); see also [11-macro-drivers-and-outlook.md](11-macro-drivers-and-outlook.md)). As of July 10, 2026 the 10-year Treasury yield stood at approximately 4.56% per secondary reporting (Forbes Advisor, citing Treasury.gov; industry/press-tier source, used only to corroborate — **[not confirmed against the Treasury.gov primary release at build time]**). Note this mixes vintages: pairing a July 2026 Treasury quote against the 2025 farmland-return estimate is illustrative of the mechanism, not a recomputed 2026 spread.

## 6. Price-to-rent multiples

The reciprocal of the cap rate is a price-to-rent multiple — analogous to a price/earnings ratio, expressing how many years of current rent are needed to "pay back" the purchase price:

```
Multiple = Price / Rent = 1 / r
```

*Source: Carl Zulauf and Bruce Sherrick, "The Dramatic Change in US Ag Land Price-Rent Ratio," farmdoc daily, January 9, 2026 ([link](https://farmdocdaily.illinois.edu/2026/01/the-dramatic-change-in-us-ag-land-price-rent-ratio.html)).*

Zulauf and Sherrick document that the **US cropland price-to-rent multiple nearly doubled since 1998, rising from about 20x to about 36x by 2025-2026**, with no statistically significant explanatory factor yet identified for the rise. A related 2022 farmdoc daily piece ties the ratio inversely to interest rates: for a given rent, land price rises as interest rates fall (farmdoc daily, "Land Price-to-Rent Ratio and Interest Rates," March 23, 2022 — cited for the qualitative interest-rate mechanism only; the article's own reported numeric ratio for 1971-1995 could not be reconciled with the 20x-36x figures during verification and is **omitted here as unresolved** — see the note at the end of this section).

**Worked example.** At the 2025 US average cropland price of $5,830/acre and the reported 36x multiple:

```
Implied rent = 5,830 / 36 ≈ $161.9/acre
```

This closely matches the separately reported 2025 US average cropland cash rent of $161/acre — an internal-consistency check that held up under independent re-verification (USDA NASS 2025 Land Values Summary, as cited in Zulauf & Sherrick 2026).

Running the ratio the other direction: if the multiple had stayed at 1998's ~20x instead of rising to 36x, 2025's average US cropland price would imply:

```
Price_at_20x = 5,830 × (20/36) ≈ $3,239/acre
```

Zulauf and Sherrick report this hypothetical figure as **$3,244/acre, a 44% reduction**. Recomputing directly from the stated 20x/36x ratio and $5,830/acre price yields $3,239/acre (a $5, ~0.15% variance) — immaterial, and most likely explained by the source using more precise (unrounded) ratio values than the round "20" and "36" quoted in the prose. The 44% decline figure checks out against the source's own $3,244 figure: (5,830 − 3,244)/5,830 = 44.4% ≈ 44%.

*Note on an unresolved older figure:* research notes for this document surfaced a claim that the price-to-rent ratio "averaged 0.54" over 1971-1995 in a 2022 farmdoc daily piece — apparently a differently-normalized ratio (possibly rent/price rather than price/rent) that could not be reconciled with the 20x-36x multiples above during verification, and the primary PDF could not be fetched in this build to resolve the discrepancy. **[Not confirmed against a primary source at build time — omitted as a numeric claim; treat as an open item for a follow-up pass with access to `farmdocdaily.illinois.edu/wp-content/uploads/2022/03/fdd032322.pdf`.]**

## 7. Per-tillable-acre vs. gross-acre valuation

Farmland appraisal and Illinois's own assessment system both distinguish valuation **per gross acre** (total deeded acreage) from valuation **per tillable acre** (acreage actually croppable), because gross acreage often includes non-productive waterways, roads, farmstead, timber, or CRP ground that dilutes a simple average:

```
Price_per_gross_acre    = TotalPrice / GrossAcres
Price_per_tillable_acre = TotalPrice / TillableAcres          (TillableAcres ≤ GrossAcres)
$_per_PI_point           = Price_per_tillable_acre / PI
```

where **PI** is the University of Illinois Soil Productivity Index (also called ILPI), a per-soil-type rating documented in University of Illinois Bulletin 811, covering 800+ Illinois soil types. The market/agronomic PI scale runs from **47 to 147**; Class A soils are PI 133-147, Class B is PI 117-132, Class C is PI 100-116, and PI ≤ 99 is classified as "other agricultural land," not prime farmland. This is a **distinct scale** from the Illinois Department of Revenue's own 82-132 PI convention used specifically for property-tax assessment (§8) — the two should not be conflated.

*Source: "What is a Soil Productivity Index (PI)?" (Big Farms, [link](https://www.bigfarms.com/prop/faqdetail/32/what_is_a_soil_productivity_index_(pi))); University of Illinois Bulletin 811, *Optimum Crop Productivity Ratings for Illinois Soils* (soilproductivity.nres.illinois.edu). Verified: the 47-147 scale and A/B/C class boundaries, and the separate 82-132 IDOR assessment scale, were both independently reproduced verbatim across search passes (verdict: confirmed). See [06-soil-productivity.md](06-soil-productivity.md) for the full PI system and its use in cropland ratings.*

**Worked example (illustrative, hypothetical tract — not a reported transaction).** A 160 gross-acre tract with 145 tillable acres, average PI 133, sells for $1,500,000:

```
Price_per_gross_acre    = 1,500,000 / 160 = $9,375/acre
Price_per_tillable_acre = 1,500,000 / 145 = $10,345/acre  (rounded)
$_per_PI_point           = 10,345 / 133   = $77.78/PI point
```

The $970/acre gap between the gross- and tillable-acre prices ($10,345 − $9,375) is entirely a function of the 15 non-tillable acres; comparing this tract to another of different tillable-percentage using only the gross-acre figure would understate or overstate relative land quality. Normalizing to $/PI point is what allows appraisers and lenders to compare tracts of different soil quality on a common basis. **Figures in this example are constructed for illustration and do not describe an actual sale.**

## 8. Illinois statutory formula: Agricultural Economic Value (property-tax assessment)

Illinois farmland property-tax assessment is not based on market sales comparison — it is a *statutorily codified* V = NOI/r calculation, distinct from (and generally far below) market value:

```
AEV_i           = NetIncome5yr_i / CapRate5yr
AssessedValue_i = 0.3333 × AEV_i

i              = soil productivity index (PI) class, on the Dept. of Revenue's 82-132 assessment scale
NetIncome5yr_i = 5-year average certified net income to land for soil PI class i,
                 certified by the Farmland Assessment Technical Advisory Board (FATAB)
CapRate5yr     = 5-year moving average of the Federal Land Bank (Farm Credit) farmland
                 mortgage interest rate (the certified published rate: 4.83% AY2025, 5.27% AY2026)
AssessedValue_i = equalized assessed value per acre for property-tax purposes
                  (33.33% is Illinois's general assessment ratio), subject to a
                  statutory cap limiting year-over-year change to 10% of the prior-year
                  median-cropped-soil (PI 111) certified value (P.A. 98-0109)
```

**Unresolved: the P.A. 104-0468 cap-rate "guardrails."** Secondary coverage (farmweeknow.com) of Public Act 104-0468 describes new guardrails on the capitalization rate — "three percentage points added to the published rate, with a floor of 8% and a ceiling of 10%." Read together with the certified published rates, that would imply an *effective* divisor of 8.00% for a 4.83% published rate (7.83% floored to 8%) and 8.27% for a 5.27% published rate — materially lowering AEVs relative to dividing by the raw published rate. However, the act's text, its effective assessment year, and how it interacts with the IDOR certified-values documents (which state the 4.83%/5.27% figures without an adjusted rate) could **not** be reconciled against a primary source at build time — the two readings are reported side by side here per `../SOURCING.md` rule 6, and the worked example below uses the certified published rate as stated in the IDOR document. Resolve against the statute and the current IDOR Publication 122 before relying on either mechanic. See [10-tax-and-assessment.md](10-tax-and-assessment.md) for the full assessment procedure.

*Source: 35 ILCS 200/10-115 et seq. (Illinois Compiled Statutes, Property Tax Code); Illinois Department of Revenue, "Glossaries and Formulas" ([PDF](https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/glossayformulas.pdf)); capitalization-rate floor/ceiling added by Public Act 104-0468. Verified: the AEV/cap-rate structure and the P.A. 104-0468 guardrails (base rate + 3 points, floor 8%, ceiling 10%) were independently confirmed via multiple search passes; the certified 5-year capitalization rate for assessment year 2026 is **5.27%**, up from **4.83%** for assessment year 2025 (Illinois Dept. of Revenue, *Certified Values for Assessment Year 2026*, [PDF](https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2026-farmland-certified-values.pdf); *Certified Values for Assessment Year 2025*, [PDF](https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2025-farmland-certified-values.pdf)). The exact statutory text of 35 ILCS 200/10-115 and FATAB's net-income certification methodology could not be read directly from ilga.gov in this build — full statutory language should be pulled and quoted verbatim in a follow-up pass. See [10-tax-and-assessment.md](10-tax-and-assessment.md) for the full property-tax assessment procedure and the 10%-per-PI change cap in context.*

**Worked example (hypothetical soil PI class).** Assessment year 2026 certified 5-year capitalization rate: 5.27%. Assume a certified 5-year average net income to land of $220/acre for a given PI class:

```
AEV = 220 / 0.0527 ≈ $4,175/acre
AssessedValue = 0.3333 × 4,175 ≈ $1,391/acre
```

This illustrates why statutory ag-use assessed values run far below market sale values — e.g., against NASS's $9,850/acre 2025 Illinois cropland market value (§1) — by design: the statutory formula capitalizes farming income potential, not speculative market price. **The $220/acre net-income input is hypothetical; actual FATAB-certified net income by PI class was not retrieved in this research pass.**

## 9. The three appraisal approaches applied to farmland

Certified appraisal of Illinois farmland (governed by USPAP, the Uniform Standards of Professional Appraisal Practice) conventionally applies three approaches:

| Approach | How it's applied to farmland | When it dominates |
|---|---|---|
| **Sales comparison** | Comparable recent sales of similar tracts, adjusted for soil quality (PI, §7), location, tillable percentage, and improvements | Primary method for typical unimproved row-crop tracts |
| **Income (direct capitalization)** | Estimate market rent from comparable-farm rent data, subtract typical landlord expenses (property tax, insurance, management) to reach NOI, then divide by a market-derived cap rate — i.e., the same V = NOI/r formula from §1, applied at the individual-parcel level | Rent-driven valuation of income-producing/leased tracts |
| **Cost** | Reproduction/replacement cost of improvements, less depreciation, plus land value | Reserved mainly for parcels where building improvements (grain systems, livestock facilities, homesteads) are a significant share of value |

*Source: general appraisal-industry description, corroborated across ag-lending/appraisal secondary sources — e.g., Compeer Financial, "Cracking the Code: How to Appraise Farmland," November 2023 ([link](https://www.compeer.com/articles/2023/november-2023/cracking-the-code-mastering-agricultural-land-appraisals)); People's Company and FCS Financial secondary explainers. Per `../SOURCING.md` rule 2, industry/press sources are the lowest tier in the hierarchy and are used here only to corroborate a standard, non-controversial methodological description — this section was not independently re-verified against a USPAP text or a farmdoc-specific appraisal methodology document in this build.*

## 10. Data tables

### USDA NASS Illinois farm real estate, cropland, and pasture values, 2024-2025 ($/acre)

| Year | Farm real estate (all land & buildings) | Cropland | Pasture | YoY change (farm real estate) |
|---|---|---|---|---|
| 2024 | $8,700 | ~$9,554* | ~$3,970* | — |
| 2025 | $8,930 | $9,850 | $4,200 | +2.6% |

\* 2024 cropland and pasture values are derived here by reversing the reported 2025 YoY changes (+3.1% cropland, +5.8% pasture) rather than taken directly from a primary 2024 table row; treat as arithmetic reconstructions, consistent with but not identical to any directly-published 2024 figure.

*Source: USDA NASS, *2025 Land Values Summary*, released August 1, 2025, describing 2025 values, as reported in farmdoc daily, "Illinois Farm Real Estate Values Hold Strong in 2025, Even with Lower Farm Incomes," August 8, 2025 ([link](https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html)). Verified: the 2025 figures ($8,930 / $9,850 / $4,200 and their YoY percentages) were independently reproduced verbatim across search passes (confirmed). See [02-land-values-and-price-history.md](02-land-values-and-price-history.md) for the full multi-year series.*

### ISPFMRA 2025 Illinois Land Values & Lease Trends — sales prices and cash rents by quality class

| Quality class | 2025 avg sale price/acre | Change vs. 2024 | 2025 cash rent range/acre | 2024 cash rent range/acre |
|---|---|---|---|---|
| Excellent | $15,846 (median $15,984) | −3.2% | $315–$404 | $350–$425 |
| Good | ~$13,268 (Region 6 example only; range $8,000–$18,105) | n/a (regional example, not a statewide figure) | n/a | n/a |
| Average | $9,933 (median $9,436) | −0.6% | $260–$342 | $283–$355 |

**[Not confirmed against a primary source at build time — these ISPFMRA figures were not independently re-checked in the verification pass behind this document; ISPFMRA's report itself is a member-survey publication under copyright and was not archived (see `../sources/MANIFEST.md` item 10b).]** 49% of surveyed ISPFMRA members expected 2025 values to fall up to 5%; 31% expected flat; 13% expected a 5-10% decline; 5% expected an increase.

*Source: ISPFMRA, *2025 Illinois Land Values and Lease Trends Report*, survey conducted among ISPFMRA members covering sales through year-end 2024/early 2025, released March 27, 2025 ([announcement link](https://ispfmra.org/2025/03/27/download-now-our-2025-land-values-lease-trends-report/)). See [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md) for the full ISPFMRA regional benchmark series.*

### Index numbers of Illinois farmland values (farmdoc FBM-0321), selected years

| Year | Index |
|---|---|
| 1970 | 26.4 |
| 1980 | 110 |
| 1990 | 76 |
| 2000 | 122 |
| 2010 | 254 |
| 2020 | 383 |
| 2025 | 481 |

**[Not confirmed against a primary source at build time — the index's exact base year and construction methodology should be confirmed against the primary FBM-0321 document before citing individual index values in analysis.]**

*Source: farmdoc, *Index Numbers of Illinois Farmland Values* (FBM-0321), updated 2025, Illinois FBFM data ([PDF](https://farmdoc.illinois.edu/assets/management/farmland-values/FBM-0321landvalueindex_2025.pdf)).*

### Central Illinois farmer returns and ownership costs on cash-rented farmland (FBFM data)

| Year | Avg. cash rent/acre | Farmer return to cash-rented land | Economic (imputed) ownership cost/owned acre |
|---|---|---|---|
| 2000 | $132 | n/a | $108 |
| 2023 | n/a | −$47 | n/a |
| 2024 | $336 | −$35 | ~$270 |
| 2025 | n/a | −$6 | n/a |
| 2026 (projected) | n/a | +$11 | n/a |

Cash rent on FBFM-enrolled central-Illinois grain farms rose from $132/acre (2000) to $336/acre (2024), an average ~4%/year increase (recomputed and confirmed in §4). Imputed ownership cost per owned acre — computed as farmland value × a capitalization rate based on a rolling average of net farmer returns — rose from $108 (2000) to over $270 (2024), an average ~3.9%/year increase.

*Source: farmdoc daily, "Comparing Returns to Owned vs. Cash-Rented Farmland," August 26, 2025, FBFM enrolled-farm data through 2024 with 2025-2026 projections ([link](https://farmdocdaily.illinois.edu/2025/08/comparing-returns-to-owned-vs-cash-rented-farmland.html)). See [08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md) for the full farmer-returns series and methodology.*

## Sources

- Gary Schnitkey and Bruce Sherrick, "Income and Capitalization Rate Risk in Agricultural Real Estate Markets," *Choices Magazine*, 2011 Q2. https://www.choicesmagazine.org/choices-magazine/theme-articles/farmland-values/income-and-capitalization-rate-risk-in-agricultural-real-estate-markets
- farmdoc daily, "Farmland Prices and Government Programs," July 7, 2026. https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html
- farmdoc daily, "Outlook for Farmland Values in 2025," November 26, 2024. https://farmdocdaily.illinois.edu/2024/11/outlook-for-farmland-values-in-2025.html
- Oscar R. Burt, "Econometric Modeling of the Capitalization Formula for Farmland Prices," *American Journal of Agricultural Economics*, Vol. 68 (1986), pp. 10-26. https://academic.oup.com/ajae/article/68/1/10/62057
- Allen Featherstone and Timothy Baker, "An Examination of Farm Sector Real Asset Dynamics: 1910-85," *American Journal of Agricultural Economics*, 1987 (cited via secondary academic aggregation). https://www.semanticscholar.org/paper/FARMLAND-VALUATION:-A-NET-PRESENT-VALUE-APPROACH-Westergard/cd5b3fcbb59771fa534940325121d755050716cd
- Barry Falk, "Formally Testing the Present Value Model of Farmland Prices," *American Journal of Agricultural Economics*, 73(1) (1991), pp. 1-10. https://ideas.repec.org/p/isu/genstf/199006010700001213.html
- farmdoc daily, "The Dramatic Change in US Ag Land Price-Rent Ratio" (Carl Zulauf and Bruce Sherrick), January 9, 2026. https://farmdocdaily.illinois.edu/2026/01/the-dramatic-change-in-us-ag-land-price-rent-ratio.html
- farmdoc daily, "Land Price-to-Rent Ratio and Interest Rates," March 23, 2022 (cited for qualitative mechanism only; numeric ratio unresolved — see §6). https://farmdocdaily.illinois.edu/wp-content/uploads/2022/03/fdd032322.pdf
- 35 ILCS 200/10-115 et seq., Illinois Compiled Statutes, Property Tax Code (ilga.gov).
- Illinois Department of Revenue, "Glossaries and Formulas." https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/glossayformulas.pdf
- Illinois Department of Revenue, *Certified Values for Assessment Year 2026*. https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2026-farmland-certified-values.pdf
- Illinois Department of Revenue, *Certified Values for Assessment Year 2025*. https://tax.illinois.gov/content/dam/soi/en/web/tax/localgovernments/property/documents/2025-farmland-certified-values.pdf
- USDA NASS, *2025 Land Values Summary*, released August 1, 2025. https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf
- farmdoc daily, "Illinois Farm Real Estate Values Hold Strong in 2025, Even with Lower Farm Incomes," August 8, 2025. https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html
- ISPFMRA, *2025 Illinois Land Values and Lease Trends Report*, March 27, 2025. https://ispfmra.org/2025/03/27/download-now-our-2025-land-values-lease-trends-report/
- farmdoc, *Index Numbers of Illinois Farmland Values* (FBM-0321), updated 2025. https://farmdoc.illinois.edu/assets/management/farmland-values/FBM-0321landvalueindex_2025.pdf
- farmdoc daily, "Comparing Returns to Owned vs. Cash-Rented Farmland," August 26, 2025. https://farmdocdaily.illinois.edu/2025/08/comparing-returns-to-owned-vs-cash-rented-farmland.html
- Federal Reserve Bank of Chicago, AgLetter, February 2026 and May 2026 issues. https://www.chicagofed.org/publications/agletter/2025-2029/february-2026
- Big Farms, "What is a Soil Productivity Index (PI)?" https://www.bigfarms.com/prop/faqdetail/32/what_is_a_soil_productivity_index_(pi)
- University of Illinois Bulletin 811, *Optimum Crop Productivity Ratings for Illinois Soils*. http://soilproductivity.nres.illinois.edu/
- Compeer Financial, "Cracking the Code: How to Appraise Farmland," November 2023. https://www.compeer.com/articles/2023/november-2023/cracking-the-code-mastering-agricultural-land-appraisals
- DTN/Progressive Farmer, "Illinois Dominates Top 10 List of Highest County Cash Rents in Corn Belt," August 23, 2025 (cash-rent correction source). https://www.dtnpf.com/agriculture/web/ag/news/business-inputs/article/2025/08/23/illinois-dominates-top-10-list-cash
