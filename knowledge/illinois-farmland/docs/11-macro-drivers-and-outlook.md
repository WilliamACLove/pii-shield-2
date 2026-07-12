# What Moves Illinois Farmland Prices: Drivers, Cycles, and Outlook

A framework for the forces that set Illinois farmland values — commodity income, interest rates, government payments, and inflation expectations — plus the leading survey instruments that track them and the state of the bull/bear debate as of mid-2026.

**Data current as of:** USDA NASS *Land Values 2025 Summary* (August 2025, describing 2025 values); Chicago Fed *AgLetter* May 2026 (Q1 2026 survey) and February 2026 (Q4/full-year 2025); ISPFMRA *2025 Illinois Land Values and Lease Trends* (March 2025) and its Q1 2026 "Farmland Prices at Plateau?" update (April 2026); farmdoc daily through July 2026; NCREIF Farmland Index through year-end 2025.
**Built/verified:** 2026-07-12

> **Build-environment disclosure:** per [`../SOURCING.md`](../SOURCING.md), this knowledge base was assembled in a session where direct fetching of primary-source PDFs/pages was blocked at the network level; figures below were sourced via a hosted web-search service and independently re-checked by a second verification pass. Claims the verification pass could not confirm are flagged inline as such. See [`../sources/MANIFEST.md`](../sources/MANIFEST.md) for the full source list and its own network-access caveat.

For the full historical price-level tables (nominal $/acre by year, county-level detail), see [02-land-values-and-price-history.md](02-land-values-and-price-history.md). This document covers *why* prices move, not the levels themselves.

## 1. The valuation framework: land as capitalized income

Academic and Federal Reserve treatments of farmland value converge on a single organizing idea: land value is the present value of the future net income stream it can generate, i.e. a capitalized-income (Gordon-growth-style) model:

```
V = R / (i − g)          [or, with no assumed growth: V = R / i]
```

- **V** = farmland value per acre
- **R** = net income per acre (proxied by cash rent net of property taxes/ownership costs, or net farm operating return)
- **i** = discount/capitalization rate (proxied by long-term interest rates plus a risk premium)
- **g** = expected growth rate of net income (from inflation or productivity gains)

*(Iowa State CARD, Agricultural Policy Review, "Land Values, Interest Rates, and the Federal Reserve's Expectations," Spring 2024: "Land value is the net present value of all discounted future income flows, which can be thought of as net income divided by interest (discount) rate." [link](https://agpolicyreview.card.iastate.edu/spring-2024/land-values-interest-rates-and-federal-reserves-expectations))*

This single equation explains most of what follows: anything that raises expected **R** (commodity prices, government payments, productivity) or lowers **i** (falling interest rates, falling risk premia) mechanically raises **V**, and vice versa. Farm income is generally cited as the dominant driver, with interest rates next in importance (same CARD source). For detailed per-parcel valuation mechanics (soil-adjusted cap rates, income vs. market approaches), see [05-valuation-math.md](05-valuation-math.md); this document uses the model only to explain aggregate macro movements.

**Worked example — the current-return (capitalization) rate:**

```
Cap rate = Cash rent per acre / Farmland value per acre
```

farmdoc daily reports Illinois's average *current return* (cash rent ÷ land value) was 2.8% for 2024, averaging just over 2.8% since 2020 (farmdoc daily, "Outlook for Farmland Values in 2025," November 26, 2024 [link](https://farmdocdaily.illinois.edu/2024/11/outlook-for-farmland-values-in-2025.html)). Checking the arithmetic against farmdoc's own companion figures for that year: $269/acre average cash rent ÷ $9,550/acre average farmland value ≈ 2.82%, consistent with the reported 2.8%. Using 2025's USDA NASS figures instead ($264/acre cash rent ÷ $9,850/acre cropland value) gives ≈ 2.7% — a slightly lower cap rate year over year, meaning the same rent dollar now supports a somewhat higher land value than it did the year before, all else equal. This is the mechanism by which falling cap rates (from falling interest rates or falling required risk premia) mechanically inflate implied land values for an unchanged income stream.

*Note on measurement systems:* the NASS figure ($9,850/acre cropland, 2025) is a national-survey (June Area Survey) estimate; farmdoc's own Illinois-specific series (~$9,550/acre for 2024) is a different index built from a different sample. Per [`../SOURCING.md`](../SOURCING.md) rule 4, these are not directly comparable single time series — treat each as internally consistent but methodologically distinct. See [02-land-values-and-price-history.md](02-land-values-and-price-history.md) for how the two series are reconciled.

## 2. Era-by-era narrative (brief — see doc 02 for full tables)

| Era | Approx. move | Dominant driver | Citation |
|---|---|---|---|
| 1973–1981 boom | Illinois +370% total, ~17.6%/yr | 1972 US-Soviet grain deal, 6–13% inflation, negative real interest rates made leveraged land an inflation hedge | SIU OpenSIUC, "An Analysis of Historical Illinois Farmland Valuations" [link](https://opensiuc.lib.siu.edu/cgi/viewcontent.cgi?article=2014&context=gs_rp); cross-cited via farmdoc daily (2013) |
| 1981–1987 crash | Illinois ≈ −43% cumulative (compounded ≈ −8.7%/yr) | Volcker-era Fed tightening pushed short rates near 20% (1979–81) to fight double-digit inflation; land had been priced for continued inflation | farmdoc daily, "A Historical Perspective on Illinois Farmland Sales," May 2013 [link](https://farmdocdaily.illinois.edu/2013/05/historical-illinois-farmland-sales.html) |
| 1987–2004 recovery | Slow, steady gains for ~1.5 decades | Gradual normalization after the farm-debt crisis | farmdoc daily (2013), same source |
| 2004–2014 ethanol/commodity boom | Cash rents +95% ($150→$293/acre, 2006–2013); statewide value roughly $2,650→$7,700/acre (+290%, ~9%/yr) *[dollar-level anchor figures not confirmed against a primary source at build time — cash-rent figures are independently corroborated, but the $2,650/$7,700 statewide levels could not be]* | Renewable Fuel Standard-driven corn demand; a peer-reviewed county study finds farmland values in high-corn-suitability counties rose $1,147/acre (+44%) after 2005 attributable to the RFS, which is estimated to explain ~30% of the 2006–2014 corn price increase | farmdoc/SIU retrospective figures; Wiley AEPP, "Biofuel Growth: The Unintended Effects of the Ethanol Boom on Farmland Values" (2026) [link](https://onlinelibrary.wiley.com/doi/abs/10.1002/aepp.70071) |
| 2015–2019 plateau | −1.5% to −6.3%/yr (2015–18), then +0.2% (2019) | Ethanol-boom-era commodity prices cooled from 2012–13 highs | Farm Credit Illinois Farmland Value Benchmark Study, August 2019 [link](https://www.farmcreditil.com/knowledge-center/Newsroom/2019/August/farmland-values-relatively-stable) |
| 2020–2022 surge | +2.07%, +8.54%, +27.88% (Farm Credit IL benchmark, by year) | Corn/soybean prices roughly doubled 2019–2022; near-zero interest rates compressed cap rates; Russia-Ukraine war grain-supply disruption; record sales volume | Farm Credit Illinois Farmland Value Benchmark Study, August 2022 [link](https://www.farmcreditil.com/knowledge-center/newsroom/2022/08-aug/copy%20of%20farmland-value-benchmark-study-results) |
| 2023–2026 cooling / divergence | NASS statewide blended figure still +2.6% (2025, to $8,930/acre); but quality-class series show top land down 3–5% from 2023 peaks, and Chicago Fed shows Illinois specifically −2% YoY in Q1 2026 even as neighboring states rose | Falling corn/soybean prices from 2H-2023 cutting net farm income; rate-hike cycle; regional divergence within the Corn Belt | See Section 4 (AgLetter) and Section 7 (outlook) below |

*(The 1981–1987 decline figure above reflects a verification correction: the original ~42% figure and comparative Iowa/Nebraska decline percentages could not be corroborated against any accessible source at build time and have been dropped; farmdoc's own index-number data — $2,023/acre in 1981 to $1,149/acre in 1987 — computes to ~43.2%, which is used here instead.)*

## 3. Driver deep dives

### 3.1 Commodity prices and net farm income

Corn and soybean prices are the proximate driver of net cash-rent income, and their swings map closely onto the price cycles above. In the most recent downswing: 2023 U.S. marketing-year-average (MYA) prices were corn $4.65/bu and soybeans $12.50/bu; 2024 projected MYA prices fell to corn $4.35/bu and soybeans $10.10/bu, with commodity prices beginning to decline in the second half of 2023 (farmdoc daily, "What a Farm's 2024 Financial Performance Indicates about 2025," February 2025 [link](https://farmdocdaily.illinois.edu/2025/02/what-a-farms-2024-financial-performance-indicates-about-2025.html); Univ. of Missouri RAFF, Fall 2024 Illinois Farm Income Outlook, October 2024).

The income effect has been large: Illinois net farm income per farm fell from a 2022 peak of roughly $506,000/farm (high commodity prices) to about $72,000/farm in 2023 and an estimated ~$30,000/farm in 2024 — levels comparable to the unprosperous 2015–2019 years. Statewide, Illinois net farm income was projected to fall 31% in 2024 to $5.4 billion (farm receipts down $4.83B on lower crop receipts, production expenses down $1.26B, government payments up $0.30B) (farmdoc daily, February 2025, same source).

### 3.2 Interest rates and the discount rate

Per the capitalized-income model (Section 1), interest rates set the discount rate **i**. Two regime shifts illustrate the mechanism at opposite extremes:

- **1979–1981:** the Volcker Fed raised short-term rates to near 20% to fight inflation running 11% (1979) and 13% (1980), the proximate trigger that unwound the 1970s farmland bubble once negative real rates turned sharply positive (thebubblebubble.com, "The 1970s U.S. Farmland Bubble" [link](https://www.thebubblebubble.com/farmland-bubble/); consistent with FDIC's history of the 1980s farm crisis).
- **2020–2021 vs. 2023–2024:** near-zero pandemic-era rates compressed cap rates and helped drive the 2020–2022 surge (Section 2). By contrast, the March 2024 FOMC "dot plot" signaling rates holding in a 4.5–5.5% range (rather than the steep cuts markets had priced in) was cited as a headwind on land values, consistent with Iowa Realtors Land Institute data showing roughly a 3% Iowa land-value decline between September 2023 and March 2024 (Iowa State CARD, Spring 2024, cited in Section 1 [link](https://agpolicyreview.card.iastate.edu/spring-2024/land-values-interest-rates-and-federal-reserves-expectations)).

The CARD piece frames interest rates as "after farm income, ... the most important" determinant of farmland value — i.e., a secondary but material lever relative to the income numerator.

### 3.3 Cash rent growth

Cash rent is the **R** term that translates commodity-price and productivity trends into land value. See [03-cash-rents.md](03-cash-rents.md) for the full county-level series; at the macro level, the statewide average cropland cash rent fell from $269/acre (2024) to $264/acre (2025), about −1.9% (USDA NASS Cash Rents 2025 release, covered by DTN, August 23, 2025 [link](https://www.dtnpf.com/agriculture/web/ag/news/business-inputs/article/2025/08/23/illinois-dominates-top-10-list-cash)). Sangamon County was the state's highest-rent county at $372/acre in 2025 (up from $369 in 2024), per the same release.

### 3.4 Inflation-hedging demand

Farmland's status as a hard, income-producing, inflation-linked asset was the central driver of the 1970s boom (Section 2) and remains part of the long-run investment thesis discussed in Section 6. The mechanism: in a negative-real-rate environment, borrowing to buy an appreciating, income-producing hard asset is attractive; the 1970s and, to a lesser extent, the 2020–2022 cycle both fit this pattern.

### 3.5 Government payments and price "stickiness"

A defining feature of the 2023–2026 cycle is a growing wedge between falling/negative farmer operating returns and farmland prices/cash rents that have not fallen proportionally. farmdoc's July 2026 analysis (Schnitkey, Zulauf, Paulson, Tsay) finds negative average returns are expected for a **fourth straight crop year** on Illinois cash-rented corn-soybean land across all regions of the state, even as land prices and rents have stayed comparatively "sticky." The authors attribute this to federal support — crop insurance, ARC/PLC Commodity Title payments, and repeated ad hoc disaster/market assistance, further reinforced by the One Big Beautiful Bill Act (OBBBA) — cushioning realized cash flow to land even when market-based operating returns are negative (farmdoc daily, "Farmland Prices and Government Programs," July 7, 2026 [link](https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html)).

In terms of the Section 1 model, government payments raise realized **R** (or reduce its downside variance) independent of market commodity prices, which helps explain why **V** has not fallen in step with farm operating income.

## 4. Chicago Fed AgLetter: methodology and latest Illinois readings

The *AgLetter* is a quarterly Seventh Federal Reserve District publication (covering Illinois, Iowa, Indiana, Michigan, and Wisconsin) tracking farmland values and credit conditions via a survey of agricultural lenders. The publication has run in some form since the 1940s and is one of the longest-running survey-based measures of Midwest farmland values. Its index values are computed by subtracting the percentage of respondents reporting "lower" values from the percentage reporting "higher," adding 100, and benchmarking against the year-earlier quarter. Starting with the Q1 2026 survey, the respondent panel was broadened to include Farm Credit System institutions in addition to commercial banks (previously banks only) (Federal Reserve Bank of Chicago, *AgLetter*, May 2026 [link](https://www.chicagofed.org/publications/agletter/2025-2029/may-2026)).

**Latest two readings:**

| Report | Covers | Seventh District | Illinois | Notes |
|---|---|---|---|---|
| February 2026 *AgLetter* | Q4 2025 / full-year 2025 | Solid growth for full-year 2025; District "good" farmland +2% in Q4 2025 vs. Q3 2025 | Not separately reported in this issue | "Midwest Farmland Values Ended 2025 with Solid Growth" |
| May 2026 *AgLetter* | Q1 2026 | +3% YoY; "good" farmland −1% vs. Q4 2025 (QoQ) | −2% YoY (April 1, 2025 to April 1, 2026); 2026 average cash rents down 1% | By state: Indiana +8%, Wisconsin +7%, Iowa +2%, Illinois −2% YoY — Illinois was the only state in the District to post a year-over-year decline; survey panel broadened to include Farm Credit System institutions starting this issue |

*Source: Federal Reserve Bank of Chicago, AgLetter, February 2026 and May 2026 issues.* [link](https://www.chicagofed.org/publications/agletter/2025-2029/may-2026)

The May 2026 issue also flagged weakening ag credit conditions: non-real-estate farm loan repayment rates were reported lower for January–March 2026 versus a year earlier (same source).

## 5. Academic decomposition: returns vs. discount rates

The Section 1 capitalized-income model is the standard framework used to decompose farmland-price movements into (a) changes in expected future income/returns and (b) changes in the discount/capitalization rate. Under this framework:

- A rising numerator (**R**) — from higher commodity prices, higher realized cash rents, or higher government payments — raises **V** even with a constant discount rate.
- A falling denominator (**i − g**) — from falling interest rates, a falling risk premium, or higher expected inflation/growth (**g**) — also raises **V**, independent of any change in current income.

The practical difficulty (and the live academic/Fed debate) is separating these two effects empirically in real time, since interest-rate cycles and commodity-price cycles have often moved together (e.g., the 2020–2022 surge combined both a commodity-price boom *and* near-zero rates; the 2023–2026 cooling combines both falling commodity income *and* a higher-rate regime, making it hard to attribute the slowdown to either factor alone from public data). The literature synthesized in the research pass for this document (Iowa State CARD, Spring 2024, Section 3.2) frames farm income as the primary driver, with interest rates as the next most important lever — but the exact quantitative split (how many percentage points of a given year's move come from each channel) is a matter of ongoing econometric work at outlets like the Kansas City Fed and the peer-reviewed agricultural-economics journals (AJAE, AEPP) rather than a single settled figure; no single primary citation with an exact attribution split could be confirmed against a primary source at build time, so no such split is asserted here. Readers wanting the underlying identification strategies should consult the Federal Reserve Bank working-paper series and AJAE/AEPP directly.

## 6. Farmland vs. other assets: long-run total returns

The NCREIF Farmland Index is the standard institutional benchmark for total returns (income + capital appreciation) on U.S. farmland held by institutional investors.

| Period | Total return | Capital return | Income return | Notes |
|---|---|---|---|---|
| 2024 | −1.03% | −3.46% | +2.49% | First negative annual total return in well over a decade (secondary sources vary on the exact prior-negative-year count; treat "decades of positive returns" framing as approximate, not an exact historical superlative) |
| 2024 (Corn Belt Annual Cropland sub-index) | +1.7% | −0.5% | +2.2% (a record low) | Corn Belt cropland capital index was up 52.6% cumulatively over the prior 4 years; its income index rose only 11.9% over the same span |
| 2025 | +0.20% | −2.80% | +3.05% | NCREIF Total Farmland Index, full year |

*Source: NCREIF Farmland Index data through year-end 2025, as reported via secondary coverage (FarmTogether, GlobalAgInvesting, AgIS Capital) of NCREIF's releases; NCREIF's own site was not directly fetchable at build time.* [link](https://user.ncreif.org/data-products/farmland/)

Over a longer window, secondary aggregators summarizing NCREIF data report farmland total returns of roughly **10.15% annualized (6.82% standard deviation)** over a trailing ~32-year window, versus the **S&P 500's ~10.49% annualized return but with a much higher 17.59% standard deviation** — the core of the institutional case for farmland as a diversifier: comparable long-run return with roughly a third of the volatility, and historically low/negative correlation to equities and bonds (FarmTogether/mooloo.net summaries of NCREIF data; not independently confirmed against NCREIF's primary release at build time). 2024's negative print and 2025's marginal recovery indicate this historically low-volatility asset class is not immune to the post-2022 rate-hike cycle and falling crop prices — see [08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md) for Illinois-specific farm-level operator and land return series that complement this institutional-index view.

## 7. The outlook debate, mid-2026

As of this writing, professional and academic commentary is split, with a cautious/bearish tilt dominating recent survey data:

**Case for further softening / caution:**
- ISPFMRA's Q1 2026 update ("Farmland Prices at Plateau?", April 2026) found 56% of respondents considered Illinois farmland overvalued (vs. 1% undervalued), and 61% expected a 2026 price decline [link](https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/). *(These percentages come from a single search-derived secondary account and were not independently re-confirmed by the verification pass at build time — treat as well-sourced but not document-confirmed.)*
- The Chicago Fed's Q1 2026 AgLetter shows Illinois as the only Seventh District state posting a year-over-year value decline (−2%), with 2026 average cash rents down 1% (Section 4).
- farmdoc's July 2026 analysis projects a fourth consecutive year of negative average returns on cash-rented corn-soybean land (Section 3.5), and net farm income remains far below its 2022 peak (Section 3.1).
- ISPFMRA's earlier 2025 report found 49% of surveyed managers/appraisers expected 2025 values to fall (up to 5%), 31% expected flat, and only 5% expected an increase — with cash-rent ranges for both excellent land ($350–425/acre in 2024 to $315–404/acre in 2025) and average land ($283–355/acre to $260–342/acre) softening year over year (ISPFMRA 2025 Land Values and Lease Trends Report, released March 27, 2025, as covered by Farm Progress [link](https://www.farmprogress.com/farm-business/illinois-farmland-values-soften-cash-rents-follow-suit-in-2025-report); *these specific percentage splits were not independently re-confirmed by the verification pass at build time*). Looking to 2026, half of ISPFMRA members surveyed expected cash rents to stay flat and half expected a decrease, with none expecting an increase.

**Case for resilience:**
- Despite the majority expecting a near-term (2026) decline, ISPFMRA's own survey commentary notes a majority of respondents still expect price *increases* over a longer, 5-year horizon — consistent with the "sticky" pattern where cyclical softening has not (yet) translated into a repeat of the 1980s-style crash.
- Government payment programs (crop insurance, ARC/PLC, OBBBA-related support) are actively cushioning realized farm cash flow even as market-based operating returns run negative (Section 3.5), which historically has supported land values against income shocks that would otherwise force distressed selling.
- Farmland's long-run total-return and volatility profile versus equities (Section 6) continues to support structural institutional and generational-wealth demand independent of any single crop-price or rate cycle.
- Illinois's NASS-survey blended real-estate value still posted a nominal gain in 2025 (+2.6% to $8,930/acre) even as quality-class and Chicago Fed series showed softening — illustrating that "the market" is not moving uniformly and blended statewide averages can mask real weakness concentrated in top-quality land and specific regions.

On balance, the weight of the most recent (2026) survey and Federal Reserve evidence points toward a plateau-to-mild-decline regime for Illinois specifically — a divergence from some neighboring Corn Belt states — driven by the combination of a higher-for-longer interest-rate regime and multi-year weak commodity income, partially offset by government-payment-supported price stickiness. Whether that stickiness persists or gives way to a larger correction is the central open question in current practitioner commentary; readers should track the next ISPFMRA release (expected ~March 2027) and Chicago Fed *AgLetter* issues (quarterly) as the leading indicators.

## Sources

- USDA NASS, *2025 Land Values and Cash Rents Highlights*, August 1, 2025. [link](https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf)
- farmdoc daily, "Illinois Farm Real Estate Values Hold Strong in 2025, Even with Lower Farm Incomes," August 8, 2025. [link](https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html)
- USDA NASS Cash Rents 2025 release, as covered by DTN, August 23, 2025. [link](https://www.dtnpf.com/agriculture/web/ag/news/business-inputs/article/2025/08/23/illinois-dominates-top-10-list-cash)
- SIU OpenSIUC, "An Analysis of Historical Illinois Farmland Valuations." [link](https://opensiuc.lib.siu.edu/cgi/viewcontent.cgi?article=2014&context=gs_rp)
- farmdoc daily, "A Historical Perspective on Illinois Farmland Sales," May 2013. [link](https://farmdocdaily.illinois.edu/2013/05/historical-illinois-farmland-sales.html)
- thebubblebubble.com, "The 1970s U.S. Farmland Bubble." [link](https://www.thebubblebubble.com/farmland-bubble/)
- Wiley, Applied Economic Perspectives and Policy, "Biofuel Growth: The Unintended Effects of the Ethanol Boom on Farmland Values," 2026. [link](https://onlinelibrary.wiley.com/doi/abs/10.1002/aepp.70071)
- Farm Credit Illinois, Farmland Value Benchmark Study Results, August 2019. [link](https://www.farmcreditil.com/knowledge-center/Newsroom/2019/August/farmland-values-relatively-stable)
- Farm Credit Illinois, Farmland Value Benchmark Study Results, August 2022. [link](https://www.farmcreditil.com/knowledge-center/newsroom/2022/08-aug/copy%20of%20farmland-value-benchmark-study-results)
- farmdoc daily, "What a Farm's 2024 Financial Performance Indicates about 2025," February 2025. [link](https://farmdocdaily.illinois.edu/2025/02/what-a-farms-2024-financial-performance-indicates-about-2025.html)
- Iowa State CARD, Agricultural Policy Review, "Land Values, Interest Rates, and the Federal Reserve's Expectations," Spring 2024. [link](https://agpolicyreview.card.iastate.edu/spring-2024/land-values-interest-rates-and-federal-reserves-expectations)
- farmdoc daily, "Farmland Prices and Government Programs," July 7, 2026. [link](https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html)
- farmdoc daily, "Outlook for Farmland Values in 2025," November 26, 2024. [link](https://farmdocdaily.illinois.edu/2024/11/outlook-for-farmland-values-in-2025.html)
- Federal Reserve Bank of Chicago, *AgLetter*, February 2026 and May 2026 issues. [link](https://www.chicagofed.org/publications/agletter/2025-2029/may-2026)
- NCREIF Farmland Index data (secondary coverage via FarmTogether, GlobalAgInvesting, AgIS Capital). [link](https://user.ncreif.org/data-products/farmland/)
- ISPFMRA, "Farmland Prices at Plateau?," April 1, 2026. [link](https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/)
- Farm Progress, coverage of ISPFMRA 2025 Land Values and Lease Trends Report, March 27, 2025. [link](https://www.farmprogress.com/farm-business/illinois-farmland-values-soften-cash-rents-follow-suit-in-2025-report)
- [`../SOURCING.md`](../SOURCING.md) — sourcing standards and build-environment disclosure for this knowledge base.
- [`../sources/MANIFEST.md`](../sources/MANIFEST.md) — full primary-source manifest with URLs and archival status.
