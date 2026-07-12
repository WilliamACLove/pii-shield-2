# Illinois Cash Rents

Reference on USDA NASS's state- and county-level cash rent survey for Illinois cropland and pasture, the historical rent series, the rent-to-value relationship, and how NASS's survey average relates to professionally-managed rent benchmarks.

**Data current as of:** 2025 state and county cash rents (USDA NASS, released August 2025); 2025 ISPFMRA land values/lease survey (March 2025); Federal Reserve Bank of Chicago AgLetter, February and May 2026 issues.
**Built/verified:** 2026-07-12

## 1. Latest NASS state average cash rent

USDA NASS's 2025 *Land Values and Cash Rents* Highlights report puts the Illinois statewide average cash rent for **non-irrigated cropland at $264/acre in 2025**, down $5 from a record **$269/acre in 2024** — the first year-over-year statewide decline since 2020. Rent reductions were concentrated on higher-productivity soils; lower-productivity soils reportedly saw a slight increase (USDA NASS, *Land Values and Cash Rents (2025 Highlights)*, released August 2025, describing 2025 values, [PDF](https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf)). This figure is corroborated across multiple independent secondary write-ups of the same NASS release (FarmWeek Now, an AgUpdate/farmdoc reprint, and DTN), all citing identical $264 (2025) vs. $269 (2024) figures.

A $265/acre figure for 2025 also appears in at least one secondary source. This could not be traced to a primary-source table and may reflect a different cut of the data (e.g., a "top cash-rent states" ranking) rather than the same non-irrigated-cropland statewide average — **[not confirmed against a primary source at build time]**. Treat $264/acre as the better-supported figure for the statewide non-irrigated cropland average.

Illinois cropland value averaged **$9,850/acre in 2025** in the same release. An initial pass characterized this as the 8th-highest state value nationally; a re-check found the ranking is more likely **9th** (behind Rhode Island, Massachusetts, Connecticut, California, New Jersey, Florida, Iowa, and New Hampshire at $9,900/acre, and just above Ohio at $9,750/acre). This corrected ranking rests on a search-engine reconstruction of the NASS state list rather than a direct read of the primary table, so treat the exact rank as reasonably confident but not primary-verified (USDA NASS, *Land Values and Cash Rents (2025 Highlights)*, August 2025). See [02-land-values-and-price-history.md](02-land-values-and-price-history.md) for the land-value series in full.

**Pasture cash rent:** a statewide Illinois average pasture (non-cropland) cash rent for 2024/2025 could not be isolated from the underlying research pass — **[not confirmed against a primary source at build time]**. The NASS Highlights and county-level cash-rent products break out pasture rents separately from cropland; pull directly from the NASS 2025 Highlights PDF or [QuickStats](https://quickstats.usda.gov) to fill this gap.

## 2. County-level rents, 2025

2025 county cash rents were available for 95 of Illinois's 102 counties from direct survey responses; the remaining 7 (DuPage, Clinton, Hardin, Henry, Iroquois, Livingston, and Union) were produced via NASS's small-area (model-based) estimation because direct sample sizes were insufficient (farmdoc daily, *Considerations for Setting 2026 Cash Rents*, September 2025, [link](https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html)).

The statewide range ran from **$92/acre (Pope County, southeastern IL)** — the state low — to **$372/acre (Sangamon County, central IL)** — the state high, up $3 from Sangamon's 2024 average of $369/acre. Central and northern Illinois counties generally sit above the statewide average; most southern Illinois counties sit below it.

| Corn Belt rank | County | State | 2025 cash rent ($/acre) | Note |
|---|---|---|---|---|
| 1 | Sangamon | IL | 372 | State's highest; +$3 vs. 2024 ($369) |
| 2 | Macon | IL | 361 | +$9 vs. 2024 |
| 3 | Logan | IL | 352 | Up 5 spots from 8th in 2024 |
| 4 | Moultrie | IL | 350 | State's highest county in 2019 (was $297 then) |
| 5 | De Witt | IL | 330 | |
| 6 | Benton | IN | 327 | +$28 vs. 2024 ($299) |
| 7 (tie) | Ida | IA | 322 | +$2 vs. 2024 |
| 7 (tie) | Butler | IA | 322 | New to the top-10 list; +$14 vs. 2024 |
| 9 | Kendall | IL | 321 | +$30 vs. 2024 |
| 10 | Bureau | IL | n/a | +$18 vs. 2024; exact 2025 dollar figure not captured in sourcing pass |
| — | Pope | IL | 92 | State's lowest county in 2025 |

*Source: NASS 2025 Cash Rents by county, as reported in DTN/Progressive Farmer, "Illinois Dominates Top 10 List of Highest County Cash Rents in Corn Belt," August 23, 2025 ([link](https://www.dtnpf.com/agriculture/web/ag/news/business-inputs/article/2025/08/23/illinois-dominates-top-10-list-cash)); farmdoc daily, September 2025 ([link](https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html)). Illinois held at least 6 of the Corn Belt's top-10 highest-cash-rent counties in 2025 (7 if Bureau is counted alongside Sangamon, Macon, Logan, Moultrie, De Witt, and Kendall).*

For historical comparison, in **2019** Illinois county rents ranged from **$57/acre (Johnson County)** to **$297/acre (Moultrie County)**, with a state average of $224/acre (up $1 from $223 in 2018) (farmdoc daily, *2019 Illinois County and State Cash Rents*, September 2019, [link](https://farmdocdaily.illinois.edu/2019/09/2019-illinois-county-and-state-cash-rents.html)). The roughly 4x low-to-high county spread in 2025 ($92–$372) is wider in absolute dollars than the 2019 spread ($57–$297) but similar in relative terms, and in both years reflects the underlying soil-productivity gradient described in [06-soil-productivity.md](06-soil-productivity.md).

## 3. Historical state series (2006–2025)

| Year | Avg. non-irrigated cropland cash rent ($/acre) | Note |
|---|---|---|
| 2006 | ~132 | Start of the 2006–2013 commodity-boom rent runup |
| 2007 | n/a | Not confirmed at build time — pull from NASS QuickStats |
| 2008 | n/a | US (not IL) average was $85.50/acre this year |
| 2009 | n/a | US (not IL) average was $90.00/acre; first year of the 2008 Farm Bill's county-level mandate |
| 2010 | 169 | |
| 2011 | 183 | |
| 2012 | 212 | |
| 2013 | n/a | See peak-year discrepancy below |
| 2014 | 234 | Record high per farmdoc's 2017 retrospective |
| 2015 | 228 | −6 vs. 2014 |
| 2016 | 221 | −7 vs. 2015 |
| 2017 | 218 | −3 vs. 2016 |
| 2018 | 223 | +5 vs. 2017 |
| 2019 | 224 | +1 vs. 2018 |
| 2020 | 222 | Little change vs. 2019 |
| 2021 | 227 | |
| 2022 | 243 | +16 vs. 2021 |
| 2023 | 259 | +16 vs. 2022; a record at the time |
| 2024 | 269 | +10 vs. 2023; record high |
| 2025 | 264 | −5 vs. 2024; first statewide decline since 2020 |

*Source: compiled from multiple farmdoc daily annual "Setting/Considerations for Cash Rents" articles (2011–2025 vintages) and "Illinois Farmland Rents: 2017 State Values and 2018 Outlook" (August 2017, [link](https://farmdocdaily.illinois.edu/2017/08/illinois-farmland-rents-2017-state-values.html)), cross-checked against the 2025 NASS Highlights release for the 2024/2025 values. 2007, 2008, 2009, and 2013 Illinois-specific figures were not confirmed at build time — the 2008/2009 rows show U.S. (not Illinois) averages for context only. Fill gaps from [NASS QuickStats](https://quickstats.usda.gov) in a future revision.*

**Peak-year discrepancy:** sources disagree on which year the state cash-rent (and land-price) cycle actually peaked. farmdoc daily's 2017 retrospective attributes the $234/acre record to **2014**, describing it as following "high returns from 2006 through 2013." A Purdue Center for Commercial Agriculture analysis, by contrast, states that Illinois cash rents and farmland prices (on a state-survey basis) peaked in **2013**, with rents falling about 12.3% and farmland prices about 17.1% from the 2013 peak to 2015 — the largest such declines among Iowa, Illinois, and Indiana (Purdue Center for Commercial Agriculture, *Trends in Land Prices, Cash Rents, and Price to Rent Ratios for Iowa, Illinois, and Indiana*, [link](https://ag.purdue.edu/commercialag/home/paer-article/trends-in-land-prices-cash-rents-and-price-to-rent-ratios-for-iowa-illinois-and-indiana/)). Per the disagreement-reporting rule, both are presented here; the discrepancy should be resolved against the original 2013 and 2014 NASS annual releases.

For long-run pre-2006 context: Illinois cash rents and farmland prices fell roughly 25% and 55% respectively from peak through 1987 during the 1980s farm crisis — a far larger decline than any seen since — **[not confirmed against a primary source at build time]**. Similarly, the claim that Illinois gross farm returns and cash rents rose slowly and in tandem from 1994–2004, then diverged (returns rising faster than rents) into the 2006–2013/2014 boom, is directional context only and **[not confirmed against a primary source at build time]** (farmdoc daily, July 2026, [link](https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html)).

## 4. NASS Cash Rents survey: methodology and limitations

- **Legal basis and scope.** The county-level Cash Rents survey was mandated by the 2008 Farm Bill (as amended by the Agricultural Act of 2018), which directs NASS to provide mean rental rates for all counties with at least 20,000 acres of cropland plus pasture. NASS conducts the survey annually in every state except Alaska (USDA NASS, *Cash Rents Methodology and Quality Measures*, August 29, 2025, [link](https://www.nass.usda.gov/Publications/Methodology_and_Data_Quality/Cash_Rents/08_2025/crntqm25.pdf); USDA NASS, *Guide to NASS Surveys — Cash Rents by County*, [link](https://www.nass.usda.gov/Surveys/Guide_to_NASS_Surveys/Cash_Rents_by_County/)).
- **Coverage and exclusions.** The survey targets farms/ranches with $1,000+ in agricultural sales and a history of cash-renting land. It excludes: land rented with buildings/barns, share-rent arrangements, per-head/per-pound-of-gain/per-animal-unit-month livestock arrangements, and land rented for free. Because of these exclusions, the NASS average describes straight cash-rent-per-acre arrangements only, not the full universe of leasing structures — see [04-lease-structures-and-law.md](04-lease-structures-and-law.md) for how NASS's cash-rent figure fits alongside crop-share and flexible-cash leases.
- **US and state estimates** are released each August as part of the annual Land Values Summary; **county-level estimates** follow to QuickStats in late August.
- **Small-area (model-based) estimation.** Since roughly the 2021 estimate year, NASS has used Bayesian small-area estimation for county-level rented-acreage totals and rental rates in counties where direct survey samples are too thin to support reliable estimates — blending current-year survey expansions/standard errors with prior-year official statistics. In 2025 this applied to 7 of Illinois's 102 counties (listed in §2 above) (methodology introduced/refined circa 2011–2021; see *Small Area Estimation for County-Level Farmland Cash Rental Rates*, Journal of Survey Statistics and Methodology, [link](https://academic.oup.com/jssam/article-abstract/2/1/1/912838)).
- **Sampling noise.** Even directly-surveyed counties can have thin response counts; year-over-year county-level moves should be read cautiously rather than as precise point estimates (see `../SOURCING.md`, "Known limitations of the underlying sources").
- **What the survey measures.** NASS cash rents are operator-reported per-acre rates actually being paid, not appraised or expert-opinion values — a different measurement basis than the ISPFMRA ranges discussed in §6, and one that should not be mixed silently with them.

## 5. Rent-to-value ratio over time

**Current return (cash-on-cash yield) formula:**

```
Current Return (%) = (Average Cash Rent per Acre / Average Land Value per Acre) × 100
```

- *Average Cash Rent per Acre* = NASS state-average non-irrigated cropland cash rent for the year.
- *Average Land Value per Acre* = NASS state-average cropland value for the same year.

**Worked example (2025, Illinois):** Cash rent = $264/acre; cropland value = $9,850/acre. Current return = 264 / 9,850 × 100 ≈ **2.68% (≈2.7%)**. This self-consistency check — the headline cash-rent, land-value, and current-return figures all reconcile arithmetically — is itself a useful cross-check on the three underlying NASS figures (USDA NASS, 2025 Highlights; farmdoc daily, *Considerations for Setting 2026 Cash Rents*, September 2025, [link](https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html)).

**Correction to the "gap" framing:** farmdoc daily's discussion of this 2.7% current return is sometimes summarized as comparing it to farmland's own historical average current return of "about 4.3%." That is a mischaracterization: the 4.3% figure in farmdoc's framing is the **10-Year Treasury Constant Maturity Rate**, not a historical average of farmland's own rent-to-value ratio. The actual comparison is farmland's current cash yield against the risk-free bond rate (an opportunity-cost/relative-valuation argument), not farmland's yield against its own past self. This distinction matters: it says farmland is priced rich relative to bonds, not necessarily rich relative to its own history (farmdoc daily, *Considerations for Setting 2026 Cash Rents*, September 2025, [link](https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html)).

**Price-to-rent (P/rent) ratio:**

```
P/rent = Average Land Value per Acre / Average Cash Rent per Acre
```

the reciprocal of current return, expressed as a multiple. P/rent10 uses a trailing 10-year average rent in the denominator to smooth short-term rent volatility.

**Worked example (2025, Illinois):** P/rent = 9,850 / 264 ≈ **37.3x**.

| Series | Value | Status |
|---|---|---|
| Long-run average P/rent, 1973–2015 (Iowa) | 20.3 | Confirmed |
| Long-run average P/rent, 1973–2015 (Illinois) | 21.2 | Confirmed |
| Long-run average P/rent, 1973–2015 (Indiana) | 21.2 | Confirmed |
| P/rent10 peak (2013, regional IA/IL/IN) | 47.5 | Confirmed (single-year P/rent10 range 41.2–47.5 over 2012–2015) |
| Single-year P/rent peak, Iowa (2014) | 33.7 | Confirmed (search-derived reconstruction) |
| Single-year P/rent peak, Illinois (2015) | 33.6 | Confirmed (search-derived reconstruction) |
| Single-year P/rent peak, Indiana (2014) | 36.2 | Confirmed (search-derived reconstruction) |
| P/rent10, 2016–2021 range | ~30–36 | Confirmed (search-derived reconstruction) |
| P/rent10 "bottomed at 30.2 in 2019" and "converged to 38.1–39.2" (most recent years) | — | **[not confirmed against a primary source at build time]** — attributed to a 2025-vintage Purdue update that could not be directly fetched |

*Source: Purdue Center for Commercial Agriculture, "Trends in Land Prices, Cash Rents, and Price to Rent Ratios for Iowa, Illinois, and Indiana," vintage referencing data through 2025 ([link](https://ag.purdue.edu/commercialag/home/paer-article/trends-in-land-prices-cash-rents-and-price-to-rent-ratios-for-iowa-illinois-and-indiana/)).*

At the national level, farmdoc daily separately reports that the **US cropland price-to-cash-rent ratio has nearly doubled since 1998**, from about 20x to about 36x — directionally consistent with the Illinois/regional figures above, though a US (not Illinois-specific) framing (farmdoc daily, *The Dramatic Change in US Ag Land Price-Rent Ratio*, January 2026, [link](https://farmdocdaily.illinois.edu/2026/01/the-dramatic-change-in-us-ag-land-price-rent-ratio.html)).

See [05-valuation-math.md](05-valuation-math.md) for the full derivation of capitalized-value and current-return methods and how they combine with these ratios in appraisal practice.

## 6. How NASS averages relate to professionally-managed rents

NASS's statewide average ($264/acre in 2025) is a population-wide operator-reported mean across all cash-rented non-irrigated cropland — it is pulled down by lower-productivity ground and does not distinguish landlord/tenant sophistication. Two other data sources measure a narrower, typically higher-quality slice of the market:

- **ISPFMRA (Illinois Society of Professional Farm Managers and Rural Appraisers).** The 2025 *Land Values Report* (its 30th annual edition) gives cash-rent ranges by land-quality class from an opinion survey of practicing farm managers and appraisers — not a population census. For 2025: "excellent" farmland $315–$404/acre (down from $350–$425 in 2024); "average" farmland $260–$342/acre (down from $283–$355 in 2024). No manager surveyed expected 2026 rents to increase (50% expected flat, 50% expected further declines). These ranges run well above the NASS statewide mean because ISPFMRA's classifications describe professionally managed, often higher-quality farmland, not a full-population average (ISPFMRA, *2025 Land Values Report*, published ~March 2025, [link](https://ispfmra.org/download/2025-land-values-report/)). See [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md) for the full ISPFMRA series and methodology.
- **Federal Reserve Bank of Chicago AgLetter.** A quarterly survey of Seventh District agricultural bankers (covering Illinois, Iowa, Indiana, Wisconsin, and Michigan) — a distinct bank-lender-based methodology, not a producer survey. It reported District cash rental rates down about 2% in 2025 (the first such decline since 2020) and a further ~3% decline for 2026. This directional finding corroborates the NASS-reported Illinois $269→$264 decline, even though the two series measure different populations (Chicago Fed, *AgLetter*, February 2026 and May 2026 issues, [Feb. 2026 link](https://www.chicagofed.org/publications/agletter/2025-2029/february-2026)).

For how these NASS, ISPFMRA, and farmdoc figures feed into land-return and budgeting tools, see [08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md). Per SOURCING.md rule 4, NASS survey averages, ISPFMRA expert-opinion ranges, and bank-reported AgLetter rates are three different measurement systems and should not be averaged or substituted for one another.

## Sources

- USDA NASS, *Land Values and Cash Rents (2025 Highlights)*, released August 2025, describing 2025 values — https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf
- USDA NASS, *Cash Rents Methodology and Quality Measures*, August 29, 2025 — https://www.nass.usda.gov/Publications/Methodology_and_Data_Quality/Cash_Rents/08_2025/crntqm25.pdf
- USDA NASS, *Guide to NASS Surveys — Cash Rents by County* — https://www.nass.usda.gov/Surveys/Guide_to_NASS_Surveys/Cash_Rents_by_County/
- USDA NASS QuickStats (interactive) — https://quickstats.usda.gov
- farmdoc daily, *Considerations for Setting 2026 Cash Rents*, September 2025 — https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html
- farmdoc daily, *2019 Illinois County and State Cash Rents*, September 2019 — https://farmdocdaily.illinois.edu/2019/09/2019-illinois-county-and-state-cash-rents.html
- farmdoc daily, *Illinois Farmland Rents: 2017 State Values and 2018 Outlook*, August 2017 — https://farmdocdaily.illinois.edu/2017/08/illinois-farmland-rents-2017-state-values.html
- farmdoc daily, *The Dramatic Change in US Ag Land Price-Rent Ratio*, January 2026 — https://farmdocdaily.illinois.edu/2026/01/the-dramatic-change-in-us-ag-land-price-rent-ratio.html
- farmdoc daily, *Farmland Prices and Government Programs*, July 2026 — https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html
- DTN/Progressive Farmer, *Illinois Dominates Top 10 List of Highest County Cash Rents in Corn Belt*, August 23, 2025 — https://www.dtnpf.com/agriculture/web/ag/news/business-inputs/article/2025/08/23/illinois-dominates-top-10-list-cash
- Purdue Center for Commercial Agriculture, *Trends in Land Prices, Cash Rents, and Price to Rent Ratios for Iowa, Illinois, and Indiana* — https://ag.purdue.edu/commercialag/home/paer-article/trends-in-land-prices-cash-rents-and-price-to-rent-ratios-for-iowa-illinois-and-indiana/
- Journal of Survey Statistics and Methodology, *Small Area Estimation for County-Level Farmland Cash Rental Rates* — https://academic.oup.com/jssam/article-abstract/2/1/1/912838
- ISPFMRA, *2025 Land Values Report* (30th annual edition), ~March 2025 — https://ispfmra.org/download/2025-land-values-report/
- Federal Reserve Bank of Chicago, *AgLetter*, February 2026 and May 2026 issues — https://www.chicagofed.org/publications/agletter/2025-2029/february-2026
- opensiuc.lib.siu.edu, *An Analysis of Historical Illinois Farmland Valuations* (1980s farm crisis context; not confirmed at build time) — https://opensiuc.lib.siu.edu/cgi/viewcontent.cgi?article=2014&context=gs_rp
- `../SOURCING.md` and `../sources/MANIFEST.md` for build-environment disclosures affecting this document's verification status
