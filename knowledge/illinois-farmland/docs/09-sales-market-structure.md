# How Illinois Farmland Trades: Sales Market Structure

How Illinois farmland actually changes hands — sale channels, buyer/seller composition, turnover rate, the records that document each transfer, and the (still minority) role of institutional capital.

**Data current as of:** ISPFMRA 2026 *Land Values and Lease Trends* report (2025 sales year, released ~April 2026); farmdoc daily turnover study (2003–2025 data, published April 2026); NCREIF Farmland Index (Q2 2025); Farmland Partners Inc. and Gladstone Land FY2025 annual reports (as of 12/31/2025); Illinois real estate transfer tax rate effective 7/1/2026.
**Built/verified:** 2026-07-12

## 1. Sale channels: auction, private treaty, sealed bid

Illinois farmland moves through three principal channels — public auction (single-tract or multi-parcel), private treaty (negotiated sale, typically broker-listed), and sealed bid — and the mix between them shifts with the cycle. During the 2021–2023 boom, weekly Class-A auctions became the norm as competitive bidding produced headline prices; by 2024, auction activity had cooled enough that "no-sale" outcomes (bid not meeting reserve) in the trailing six months exceeded the combined total for 2021–2023 [not confirmed against a primary source at build time] (ISPFMRA-sourced secondary commentary, [ispfmra.org/land-values-archive](https://ispfmra.org/land-values-archive/), 2024).

| Report (sales year covered) | Public/single-tract auction | Multi-parcel auction | Private treaty | Sealed bid / other |
|---|---|---|---|---|
| ISPFMRA archive commentary (2019 sales) | ~33% (combined auction) [not confirmed against a primary source at build time] | n/a | Majority (>50%, "more common" than auction) [not confirmed against a primary source at build time] | n/a |
| ISPFMRA 2025 report (2024 sales) | 53% | 17% | 27% | ~3% (residual; not directly quoted in any source reviewed) |
| ISPFMRA 2026 report (2025 sales) | Not quantified in sources reviewed | n/a | Secondary commentary describes private treaty as "regaining primacy" over auction [not confirmed against a primary source at build time] | n/a |

*Source: ISPFMRA, 2025 Land Values and Lease Trends Report (covering 2024 sales, released March 27, 2025), [ispfmra.org/download/2025-land-values-report](https://ispfmra.org/download/2025-land-values-report/) — the 53%/17%/27% split is independently corroborated across secondary summaries and treated as confirmed. The 2019 baseline and the 2025-sales "private treaty regaining primacy" description are directional secondary-source claims that could not be checked against the primary report text in this build; treat them as illustrative of cyclicality, not as precise shares. See [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md) for the underlying ISPFMRA survey methodology.*

The auction/private-treaty split is a leading indicator worth tracking alongside price levels: a rising auction share generally signals a seller's market (sellers choose the channel expected to maximize competitive tension), while a swing back toward private treaty — as described for 2025 sales — is consistent with the broader 2025 softening in Class A land values discussed in [02-land-values-and-price-history.md](02-land-values-and-price-history.md).

## 2. Buyer composition: farmers vs. investors vs. institutions

| Sales year (report vintage) | Farmer buyers (total) | Local investor | Non-local / individual investor | Institutional buyer | Confirmed? |
|---|---|---|---|---|---|
| 2023 sales (2024 report) | 59% (57% local + relocating) | 17% | 13% | not separately broken out | [not confirmed against a primary source at build time] |
| 2024 sales (2025 report) | ~57–59% (57% local farmers) | 17% | 13% | not separately broken out | [not confirmed against a primary source at build time] |
| 2025 sales (2026 report) | 58% (56% local + 2% relocating) | — | 34% (individual investors, local+non-local combined) | 8% | Confirmed |

*Source: ISPFMRA 2026 report, "Farmland Prices at Plateau?" (2025 sales year, published April 1, 2026), [ispfmra.org/2026/04/01/farmland-prices-at-plateau](https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/) — the 58%/34%/8% breakdown for 2025 sales is corroborated by multiple independent secondary write-ups reproducing it verbatim and is treated as confirmed. The 2023-sales and 2024-sales rows come from ISPFMRA 2024/2025 report secondary coverage ([ispfmra.org/2024/03/21/land-prices-holding-steady-to-up-survey-results](https://ispfmra.org/2024/03/21/land-prices-holding-steady-to-up-survey-results/); [farmprogress.com](https://www.farmprogress.com/farm-business/illinois-farmland-values-soften-cash-rents-follow-suit-in-2025-report)) but were not independently re-verified in the build-time check pass, so are flagged accordingly.*

Farmers have been the modal buyer in every ISPFMRA survey year reviewed (57–59% of purchases), but the combined investor share (individual plus, from 2025 sales onward, institutional) has held at roughly a third of transactions — a materially larger investor presence than the "family farm to family farm" model implies. The 2026 report is the first to break out institutional buyers (8%) as a distinct category rather than folding them into "investor."

## 3. Seller composition: estates dominate

| Category | Share of sellers | Confirmed? |
|---|---|---|
| Estate | ~59% | [not confirmed against a primary source at build time] |
| Retired farmer | ~13% | [not confirmed against a primary source at build time] |
| Active farmer | ~6% | [not confirmed against a primary source at build time] |
| Individual investor | ~12% | [not confirmed against a primary source at build time] |
| Institution | ~9% | [not confirmed against a primary source at build time] |

*Source: ISPFMRA Land Values Report seller-composition data, secondary coverage of the 2025 report ([ispfmra.org/download/2025-land-values-report](https://ispfmra.org/download/2025-land-values-report/)). Two independent secondary summaries attributed the same ~59% estate-seller figure to different survey years (2023 vs. 2024 sales) without reconciling; the exact sales year is not confirmed and the full table should be checked against the primary ISPFMRA PDF before being cited precisely. Directionally, the figures are internally consistent: active farmers selling out (6%) are a small minority of sellers, while estates plus retired farmers (~72%) account for most supply — i.e., most Illinois farmland reaches the market through generational transfer or retirement, not active-operator downsizing.*

## 4. Annual turnover rate

Physical turnover of Illinois farmland is slow relative to the pace of price discussion in the market. farmdoc's county-level study, built from Illinois PTAX-203 transfer-declaration records aggregated over 2003–2025, found:

- **Statewide average annual turnover: ~1.56%** of farmland acres per year (Confirmed — corroborated by an independent Illinois Extension summary quoting the same figure).
- Only three years in the 23-year window — **2003, 2004, and 2021** — exceeded a 2% statewide turnover rate.
- Implied average holding period: **~64 years** per parcel/ownership spell.

*Source: farmdoc daily, "Illinois Farmland Turnover Rates: 2003–2025" (University of Illinois, published April 2026), [farmdocdaily.illinois.edu/2026/04/illinois-farmland-turnover-rates-2003-2025.html](https://farmdocdaily.illinois.edu/2026/04/illinois-farmland-turnover-rates-2003-2025.html).*

### County extremes (2003–2025 average annual turnover rate)

| Rank | County | Average annual turnover rate |
|---|---|---|
| Highest 1 | Hardin | 3.4% |
| Highest 2 | Pope | 3.2% |
| Highest 3 | Alexander | 3.1% |
| **Statewide average** | — | **1.56%** |
| Lowest 3 | White | 0.6% |
| Lowest 2 | Richland | 0.5% |
| Lowest 1 | DuPage | 0.2% |

*Source: farmdoc daily, "Illinois Farmland Turnover Rates: 2003–2025," April 2026 (same URL as above). Confirmed — independently reproduced with matching figures, including secondary detail (Champaign and Pike at 3%, Brown at 2.8%, Cook at 2.7% on the high end). High-turnover counties cluster in southern Illinois near the Ohio/Mississippi confluence (Hardin, Pope, Alexander); the lowest-turnover county, DuPage, reflects Chicago-metro urban-fringe land-use pressure suppressing agricultural-land transactions rather than a "sticky ownership" farm-economics effect.*

### Formulas

**Annual turnover rate**

```
Turnover_rate (%) = (Acres of farmland transferred in arm's-length sales during year Y / Total farmland acres in the geography) × 100
```
- *Acres transferred* = sum of qualifying (arm's-length, non-family, non-exempt) farmland transactions recorded via PTAX-203 declarations at the county recorder during year Y.
- *Total farmland acres* = base denominator (county or statewide farmland acreage, e.g., from the USDA Census of Agriculture or county assessor records).
- Worked example: a county with 400,000 farmland acres and 6,000 acres transacted in qualifying sales in one year has turnover = 6,000/400,000 × 100 = **1.5%**, consistent with the statewide 2003–2025 average of ~1.56%.
- Source: methodology implied by farmdoc daily, "Illinois Farmland Turnover Rates: 2003–2025" (as above).

**Implied average holding period**

```
Average_holding_period (years) = 1 / Turnover_rate (as a decimal)
```
- *Turnover_rate* = annual fraction of farmland acreage that transacts (e.g., 0.0156 for 1.56%). Standard inverse relationship between a flow rate and average tenure under a roughly steady-state turnover process.
- Worked example: at the statewide 1.56% average annual turnover rate, holding period = 1/0.0156 ≈ **64.1 years**, matching farmdoc's reported figure.
- Source: standard turnover/tenure identity, as applied in the farmdoc daily analysis above.

## 5. Transaction-data sources

The raw record behind essentially every Illinois farmland transaction-level dataset is the **PTAX-203 Real Estate Transfer Declaration**, required by the Real Estate Transfer Tax Law (35 ILCS 200/31-1 et seq.) to accompany every deed filed with a county recorder (35 ILCS 200/31-25); exemptions are listed at 35 ILCS 200/31-45. PTAX-203 captures sale price, buyer/seller identity, and property characteristics, and county assessors use it for sales-ratio (assessment-equalization) studies; the state's MyDec system is the e-filing front end.

**Correction to the transfer-tax rate:** the state real estate transfer tax rate is **$0.75 per $500 of value** (equivalently $1.50/$1,000), effective **July 1, 2026** — not the $0.50/$500 rate that applied previously and that is still widely quoted in older secondary summaries. This was confirmed at build time by four independent secondary/industry sources (e.g., [listwithclever.com](https://listwithclever.com/real-estate-blog/illinois-real-estate-transfer-taxes-an-in-depth-guide/)) but the exact Public Act number amending 35 ILCS 200/31-10 could not be pulled directly from ilga.gov in this build [not confirmed against a primary source at build time — verify the Public Act citation directly against ilga.gov before relying on this for a legal filing]. See [10-tax-and-assessment.md](10-tax-and-assessment.md) for the full transfer-tax and assessment treatment.

**Transfer tax due (state-level)**
```
State_transfer_tax = ROUNDUP(Sale_price / 500) × $0.75
```
- *Sale_price* = full actual consideration for the transfer, as declared on Form PTAX-203.
- Counties (and some municipalities) may layer on additional local transfer tax; certain transfers are exempt under 35 ILCS 200/31-45 (e.g., interspousal transfers, no-consideration transfers into a revocable trust, government transfers).
- Worked example: a $2,000,000 farmland sale: 2,000,000/500 = 4,000; tax = 4,000 × $0.75 = **$3,000** in state transfer tax (at the post-7/1/2026 rate), before any county-level transfer tax.
- Source: 35 ILCS 200/31-10, rate as corrected above; filing mechanics per Illinois Department of Revenue PTAX-203 instructions, [tax.illinois.gov/localgovernments/property/general-information/ptax-203_instructions.html](https://tax.illinois.gov/localgovernments/property/general-information/ptax-203_instructions.html).

Beyond the statutory record, several practitioner tools aggregate PTAX-203-derived comp data for market use:

- **Farm Credit Illinois's Farmland Trends Tracker** — a comp-sales tool classifying tracked sales into land classes using the University of Illinois Bulletin 811 Productivity Index (PI) bands (Excellent 133+, Good 117–132, Average 100–116, Fair <100); see [www.farmcreditil.com/Tools/Farmland-Trends-Tracker](https://www.farmcreditil.com/Tools/Farmland-Trends-Tracker) [not confirmed against a primary source at build time — full sourcing methodology not independently verified]. PI classification detail is covered in [06-soil-productivity.md](06-soil-productivity.md).
- **AcreValue** and **FarmlandFinder** — commercial platforms surfacing county-record-derived comps and, in FarmlandFinder's case, a digital marketplace for landowners to solicit and manage buy/sell offers directly ([www.farmprogress.com/management/farmlandfinder-launches-platform-for-seller-buyer-offers](https://www.farmprogress.com/management/farmlandfinder-launches-platform-for-seller-buyer-offers)) [not confirmed against a primary source at build time; no data found on the share of overall Illinois transaction volume these platforms represent].
- **Auction-company trackers** (e.g., DreamDirt's monthly market reports) — see Section 8 below; these are a selected sample of auction outcomes, not a transaction census.

Consult [12-data-source-directory.md](12-data-source-directory.md) for the full inventory of primary and secondary data sources used across this knowledge base.

## 6. Institutional capital: NCREIF, farmland REITs, 1031 exchanges

Institutional ownership remains a minority channel in Illinois but is trackable through a small number of benchmarks:

- **NCREIF Farmland Index** — covers only properties held on behalf of qualified tax-exempt institutional investors (predominantly pension funds), and is the standard institutional-segment benchmark, not a measure of the broader Illinois market. It posted its **first-ever negative annual total return, −1.0%, for full-year 2024** (since the index's 1991 inception), followed by a modest **+0.33% total return in Q2 2025** (income +0.59%, appreciation −0.26%); the row-crop segment (most relevant to Illinois corn/soybean ground) returned +0.98% over that period, and the Corn Belt region returned +1.71% for full-year 2024. Confirmed via multiple independent outlets (Global AG Investing, FarmTogether, Scythe & Spade). Source: NCREIF Farmland Property Index, [user.ncreif.org/data-products/farmland](https://user.ncreif.org/data-products/farmland/); coverage at [globalaginvesting.com/ncreifs-total-farmland-index-generates-negative-return](https://globalaginvesting.com/ncreifs-total-farmland-index-generates-negative-return/).
- **Publicly traded farmland REITs** — the two main vehicles with some Illinois exposure are **Farmland Partners Inc.** (NYSE: FPI, ~71,600 acres across 11 states, as of December 31, 2025) and **Gladstone Land Corporation** (Nasdaq: LAND, 144 farms totaling ~98,688 acres across 14 states, as of December 31, 2025, more specialty-crop/fruit-and-vegetable weighted than Corn Belt row crops). Both figures are confirmed against the companies' FY2025 SEC Form ARS filings. Neither company's public filings disaggregate Illinois-specific acreage or value — Illinois is a minority holding within a diversified national portfolio for both, and the Illinois-specific share of either company's acreage was not available in sources reviewed at build time. Source: Farmland Partners Inc. / Gladstone Land Corp FY2025 Annual Report to Shareholders (SEC EDGAR, filed 2026), [www.sec.gov/Archives/edgar/data/1591670/000110465926029563/tm263935d3_ars.pdf](https://www.sec.gov/Archives/edgar/data/1591670/000110465926029563/tm263935d3_ars.pdf).
- **1031 like-kind exchanges** — industry (brokerage-side) commentary describes 1031 exchanges as a meaningful demand driver from high-net-worth and out-of-state buyers repositioning capital from other real estate into farmland, but no Illinois-specific share-of-transactions statistic exists in ISPFMRA, NASS, or farmdoc data reviewed. [not confirmed against a primary source at build time — directional/anecdotal industry claim only]. Source: FarmTogether, "Leveraging 1031 Exchanges in Farmland," [farmtogether.com/learn/blog/1031-exchanges-in-farmland](https://farmtogether.com/learn/blog/1031-exchanges-in-farmland).
- **National institutional AUM growth** — secondary commentary describes U.S. institutional farmland assets under management roughly doubling from 2020 to 2023 to approximately $16 billion nationally (not Illinois-specific, and not independently re-verified at build time). [not confirmed against a primary source at build time].

## 7. Seasonality

Fall (post-harvest) is described by industry practitioners as the heaviest season for Illinois farmland auctions and new listings — sellers and buyers gain yield and price certainty, and harvest proceeds provide bidder liquidity — though some brokers note spring/summer listings can face less competing inventory even at lower volume. No NASS or ISPFMRA month-by-month transaction-count series was located to quantify the seasonal split precisely; treat this as a qualitative, practitioner-sourced pattern only. [not confirmed against a primary source at build time]. Source: industry commentary, e.g., DreamDirt Q1 2026 Illinois farmland market report, [dreamdirt.com/illinois-farmland-prices-sales-trends-q1-2026-market-report](https://dreamdirt.com/illinois-farmland-prices-sales-trends-q1-2026-market-report/).

## 8. Top-end 2025 auction results (selected sample)

Per the SOURCING.md known limitations, auction results are a **selected sample** — sellers choose the auction channel when they expect strong competition, so tracked results skew high relative to all transactions and should not be read as representative of the average sale. The figures below are individual transactions, not market averages, and were not independently re-verified against a primary auction-house filing at build time.

| Month (2025) | County | Acres | Price/acre | Productivity Index (PI) | Notes |
|---|---|---|---|---|---|
| February | Douglas | not specified | $21,000 | not specified | Highest price cited for the month |
| March 5 | Shelby | 41.58 | $18,500 | 144 | |
| March 5 | Grundy | 120 | $17,100 | 126.1 | |
| May | Ford | 47.94 | $18,200 | 131.8 (96% tillable) | Highest-selling farm cited for the month |
| June | Livingston (near Ancona) | 69.63 | $17,100 | 137.1 | ~$124.70 per PI point |
| July | Sangamon | not specified | $19,100 | 138 | Highest sale cited for the month |

*Source: DreamDirt monthly Illinois farmland price/auction reports, February–July 2025 editions, [dreamdirt.com/unlocking-the-value-of-illinois-farmland-a-comprehensive-guide-to-current-land-prices-and-expert-insights-june-2025-report](https://dreamdirt.com/unlocking-the-value-of-illinois-farmland-a-comprehensive-guide-to-current-land-prices-and-expert-insights-june-2025-report/). [not confirmed against a primary source at build time — treat as a selected sample of high-end auction outcomes per SOURCING.md's "Auction results" limitation, not a market-average benchmark.] For statewide average land-class values (which softened for Class A/Excellent land even as these top-end tracts sold strongly), see [02-land-values-and-price-history.md](02-land-values-and-price-history.md) and [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md). Productivity Index methodology is covered in [06-soil-productivity.md](06-soil-productivity.md).*

## Sources

- ISPFMRA, *2025 Land Values and Lease Trends Report* (2024 sales year), released March 27, 2025 — [ispfmra.org/download/2025-land-values-report](https://ispfmra.org/download/2025-land-values-report/)
- ISPFMRA, *"Farmland Prices at Plateau?"* (2026 report, 2025 sales year), published April 1, 2026 — [ispfmra.org/2026/04/01/farmland-prices-at-plateau](https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/)
- ISPFMRA, *2024 Land Values Report* coverage (2023 sales year), March 21, 2024 — [ispfmra.org/2024/03/21/land-prices-holding-steady-to-up-survey-results](https://ispfmra.org/2024/03/21/land-prices-holding-steady-to-up-survey-results/)
- ISPFMRA Land Values Archive — [ispfmra.org/land-values-archive](https://ispfmra.org/land-values-archive/)
- farmdoc daily, *"Illinois Farmland Turnover Rates: 2003–2025,"* University of Illinois, April 2026 — [farmdocdaily.illinois.edu/2026/04/illinois-farmland-turnover-rates-2003-2025.html](https://farmdocdaily.illinois.edu/2026/04/illinois-farmland-turnover-rates-2003-2025.html)
- Illinois Compiled Statutes, 35 ILCS 200, Article 31 (Real Estate Transfer Tax Law) — rate at 31-10, filing requirement at 31-25, exemptions at 31-45; text at ilga.gov [not independently re-fetched at build time]
- Illinois Department of Revenue, PTAX-203 instructions — [tax.illinois.gov/localgovernments/property/general-information/ptax-203_instructions.html](https://tax.illinois.gov/localgovernments/property/general-information/ptax-203_instructions.html)
- Secondary corroboration of the July 1, 2026 transfer-tax rate increase to $0.75/$500 — [listwithclever.com/real-estate-blog/illinois-real-estate-transfer-taxes-an-in-depth-guide](https://listwithclever.com/real-estate-blog/illinois-real-estate-transfer-taxes-an-in-depth-guide/)
- Farm Credit Illinois, Farmland Trends Tracker — [www.farmcreditil.com/Tools/Farmland-Trends-Tracker](https://www.farmcreditil.com/Tools/Farmland-Trends-Tracker)
- Farm Progress, *"FarmlandFinder launches platform for seller-buyer offers"* — [www.farmprogress.com/management/farmlandfinder-launches-platform-for-seller-buyer-offers](https://www.farmprogress.com/management/farmlandfinder-launches-platform-for-seller-buyer-offers)
- NCREIF, Farmland Property Index — [user.ncreif.org/data-products/farmland](https://user.ncreif.org/data-products/farmland/)
- Global AG Investing, *"NCREIF's Total Farmland Index Generates Negative Return"* — [globalaginvesting.com/ncreifs-total-farmland-index-generates-negative-return](https://globalaginvesting.com/ncreifs-total-farmland-index-generates-negative-return/)
- Farmland Partners Inc. / Gladstone Land Corp, FY2025 Annual Report to Shareholders (SEC EDGAR, filed 2026) — [www.sec.gov/Archives/edgar/data/1591670/000110465926029563/tm263935d3_ars.pdf](https://www.sec.gov/Archives/edgar/data/1591670/000110465926029563/tm263935d3_ars.pdf)
- FarmTogether, *"Leveraging 1031 Exchanges in Farmland"* — [farmtogether.com/learn/blog/1031-exchanges-in-farmland](https://farmtogether.com/learn/blog/1031-exchanges-in-farmland)
- DreamDirt, monthly Illinois farmland price/auction reports, February–July 2025 and Q1 2026 editions — [dreamdirt.com](https://dreamdirt.com/)

See also: [02-land-values-and-price-history.md](02-land-values-and-price-history.md), [06-soil-productivity.md](06-soil-productivity.md), [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md), [10-tax-and-assessment.md](10-tax-and-assessment.md), [12-data-source-directory.md](12-data-source-directory.md), [../SOURCING.md](../SOURCING.md).
