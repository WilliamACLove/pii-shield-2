# Illinois Farmland Values and Price History

Reference on USDA NASS's Illinois farm real estate/cropland/pasture value levels, the annual historical series back to 1970, the 2024 Census-benchmark revision, and how NASS's survey-based figures relate to actual transaction prices and ISPFMRA's land-class values.

**Data current as of:** NASS *Land Values 2025 Summary* (Aug. 1, 2025, describing 2025 values); ISPFMRA *2026 Land Values and Lease Trends Report* (~Apr. 1, 2026, describing CY2025 sales); Federal Reserve Bank of Chicago *AgLetter*, May 2026 issue (Q1 2026 data)
**Built/verified:** 2026-07-12

> **Build-environment note:** This knowledge base was assembled in a session where direct fetching of primary PDFs/pages (nass.usda.gov, farmdoc(daily).illinois.edu, ispfmra.org, chicagofed.org) was blocked at the network level; figures below come from a hosted web-search service's excerpts of those documents, cross-checked across independent secondary sources at a second verification pass, rather than from an opened primary document. See `../SOURCING.md` and `../sources/MANIFEST.md` for the full disclosure. Points that a second pass could not corroborate are flagged inline as **[not confirmed against a primary source at build time]**.

## 1. Latest NASS Illinois land values (2025)

USDA NASS's *Land Values Summary*, released each August from the June Area Survey (see [§5](#5-nass-methodology-and-limitations)), is the primary official series for Illinois farmland value levels.

| Measure | Illinois 2025 | Illinois 2024 | % change | U.S. 2025 | U.S. % change |
|---|---|---|---|---|---|
| Farm real estate (land + buildings), $/acre | $8,930 | $8,700 | +2.6% | $4,350 | +4.3% |
| Cropland value, $/acre | $9,850 | $9,555 (implied by % change, not separately published for 2024 in sources reviewed) | +3.1% | $5,830 | +4.7% |
| Pasture value, $/acre | $4,200 | $3,970 (implied by % change) | +5.8% | $1,920 | +4.9% |

*Source: USDA NASS, "Land Values 2025 Summary" (Aug. 1, 2025), describing 2025 values ([nass.usda.gov/Publications/Todays_Reports/reports/land0825.pdf](https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0825.pdf)); corroborated by University of Illinois farmdoc daily, "Illinois Farm Real Estate Values Hold Strong in 2025 Even with Lower Farm Incomes" (Aug. 8, 2025), [farmdocdaily.illinois.edu/2025/08](https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html). 2025 was Illinois's fifth consecutive year of farm real estate gains of at least 2.4%.*

**Corn Belt ranking (farm real estate, 2025):** Iowa $9,790/acre (highest in the Corn Belt) > Ohio $9,350/acre > Illinois $8,930/acre. Illinois has been surpassed by Ohio within the last five years. (farmdoc daily, Aug. 8, 2025, as above — this ordering, not an alternative "Illinois ranks above Iowa/Ohio" framing that appeared in one lower-quality secondary snippet during research, is the one confirmed at verification.)

## 2. The 2023 Census-benchmark revision

NASS performs a formal **"final historic revision"** after each five-year Census of Agriculture to re-benchmark its survey-based annual estimates to Census levels. The most recent revision, incorporating the **2022 Census of Agriculture**, appeared in the *Land Values 2024 Summary* (Aug. 2, 2024) and revised Illinois figures for 2019–2023 downward by 1.9%–9.5% (average –5.8%, roughly –$490/acre/year across the revised span).

| Year | Illinois farm real estate, as originally published | Illinois farm real estate, after 2024 Census-benchmark revision | Revision |
|---|---|---|---|
| 2023 | $9,300/acre (farmdoc daily, Aug. 2023, +4.5% vs. 2022) | $8,420/acre | –9.46% (≈ the –9.5% upper bound NASS cited) |
| 2019–2022 | (not individually re-stated with exact revised dollar figures in sources reviewed) | (revised downward within the same 1.9%–9.5% band; exact per-year revised levels not confirmed at build time) | avg. –5.8% across 2019–2023 |

*Source: USDA NASS, "Land Values 2024 Summary" (Aug. 2, 2024), [nass.usda.gov/Publications/Todays_Reports/reports/land0824.pdf](https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0824.pdf); original 2023 figure per farmdoc daily, "Illinois Farm Real Estate Value Continues Increase…for 2023" (Aug. 2023), [farmdocdaily.illinois.edu/2023/08](https://farmdocdaily.illinois.edu/2023/08/illinois-farm-real-estate-values-continues-increase-per-acre-for-2023.html).*

**Why this matters for readers of this series:** the revision is a *level shift in the estimation methodology*, not a market decline — Illinois cropland did not actually fall ~9.5% in one year. Consequently, year-over-year percentage changes published in different years' NASS reports are not always calculated on a consistent base, and apparent "declines" appearing when you naively difference two vintages of the series can be artifacts of rebenchmarking. Always check which vintage of a prior-year figure a percent change was computed against (see the worked formula below).

**Formula — NASS annual percent change:**

```
% change = (Current year value − Prior year value) / Prior year value × 100
```
- *Current/prior year value* = NASS-published average farm real estate (or cropland, or pasture) value per acre for Illinois.
- *Prior-year value used* = the **adjusted** figure from the current report if a Census-of-Agriculture benchmarking revision occurred since the prior report was published.

*Worked example:* 2025: ($8,930 − $8,700) / $8,700 × 100 = 2.64% ≈ 2.6% as published. 2024: ($8,700 − $8,420) / $8,420 × 100 = 3.33% ≈ 3.3% as published — using the Census-revised 2023 base of $8,420, **not** the originally published $9,300.
*Source: NASS Land Values Summary methodology, applied consistently 2020–2025 editions.*

## 3. Annual historical series

### 3.1 Recent series, 2013–2025 (nominal $/acre, NASS farm real estate value)

| Year | Illinois farm real estate ($/acre) | % change (as reported at the time) | Note |
|---|---|---|---|
| 2013 | $7,100 | — | Cited in 2022 farmdoc daily coverage as the "10-year" comparison base |
| 2016 | $7,300 | decline in several years 2015–2017, 2019–2020 per farmdoc daily | |
| 2019 | $7,280 | — | |
| 2020 | $7,400 | +1.6% vs. 2019 | Third straight year without a decline |
| 2021 | ~$7,900 | — | **[not confirmed against a primary source at build time]** — algebraically implied from the 2022 report's stated +12.7% change to reach $8,900; no 2021-dated primary source was independently located in this pass |
| 2022 | $8,900 | +12.7% vs. 2021 | First double-digit annual increase since 2013 (farmdoc daily, Aug. 8, 2022); as originally published — not separately confirmed whether this was later touched by the 2024 benchmark revision |
| 2023 (as originally published) | $9,300 | +4.5% vs. 2022 | farmdoc daily, Aug. 2023 |
| 2023 (revised) | $8,420 | revised down ~9.5% from $9,300 | NASS *Land Values 2024 Summary* (§2, above) |
| 2024 | $8,700 | +3.3% vs. adjusted 2023 ($8,420) | NASS *Land Values 2024 Summary* |
| 2025 | $8,930 | +2.6% vs. 2024 | NASS *Land Values 2025 Summary*; fifth straight year of ≥2.4% growth since 2020 |

*Source: Compiled from NASS Land Values Summaries 2020–2025 (August releases) and farmdoc daily commentary 2020–2025, [farmdocdaily.illinois.edu/2025/08](https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html).*

### 3.2 The 1970s boom and 1980s bust (nominal $/acre)

| Year | Illinois farm real estate ($/acre) |
|---|---|
| 1970 | $490 |
| 1975 | $952 |
| 1980 | $2,041 |
| 1981 | $2,188 (peak, per this series) |
| 1982 | $2,023 |
| 1985 | $1,314 |
| 1986 | $1,232 |

*Source: "An Analysis of Historical Illinois Farmland Valuations," Southern Illinois University Carbondale (OpenSIUC graduate research paper), sourcing NASS historical data, [opensiuc.lib.siu.edu](https://opensiuc.lib.siu.edu/cgi/viewcontent.cgi?article=2014&context=gs_rp). Cross-referenced narrative: prices rose ~370% (≈17.6%/yr average) from 1973–1981 — **confirmed** at verification — driven by grain-export demand (notably the 1972 U.S.–Soviet grain deal), inflation running 6%–13%, and negative real interest rates that made leveraged land purchases an attractive inflation hedge.*

**A note on conflicting figures for the 1981 peak and the bust's depth.** A second, independently sourced series — University of Illinois farmdoc daily, "A Historical Perspective on Illinois Farmland Sales" (May 2013), [farmdocdaily.illinois.edu/2013/05](https://farmdocdaily.illinois.edu/2013/05/historical-illinois-farmland-sales.html) — states the **1981 value was $2,023/acre**, falling at a compounded **8.7%/year** through a **1987** trough of **$1,149/acre**, a cumulative decline of **~43%** (verification corrected the commonly cited "42%" figure to ~43.2%, since $2,023 → $1,149 over six years computes to that number; the two framings are only approximately, not exactly, consistent with each other). This disagrees with the SIU-sourced table above, which places $2,023 in **1982** (not 1981) and does not extend past 1986 ($1,232/acre). Per this knowledge base's sourcing rule on disagreements, both are reported here rather than silently reconciled: the exact dollar level and year of the 1981 peak vary by source, though both agree the peak was materially north of $2,000/acre and the trough of the 1980s farm crisis fell to roughly $1,150–$1,230/acre by 1986–1987, a decline of 42%–50% depending on the source and endpoint. Comparison figures once cited alongside this claim (Iowa –49%, Nebraska –46% over the same crash) could not be corroborated by any source in this pass and are omitted here — **[not confirmed against a primary source at build time]**.

The proximate trigger for the bust: the Federal Reserve under Paul Volcker raised short-term interest rates to nearly 20% between 1979 and 1981 to fight double-digit inflation, reversing the negative-real-rate conditions that had made leveraged farmland purchases attractive; once real rates turned sharply positive, the bubble unwound into a wave of farm bankruptcies and foreclosures (thebubblebubble.com, "The 1970s U.S. Farmland Bubble," undated retrospective; framing consistent with FDIC's history of the 1980s banking/farm crisis).

### 3.3 Index Numbers of Illinois Farmland Values (farmdoc FBM-0321), 1979 = 100

| Year | Index (1979 = 100) |
|---|---|
| 1990 | 76 |
| 1991 | 79 |
| 1992 | 83 |
| 1993 | 83 |
| 1994 | 90 |
| 1995 | 98 |
| 1996 | 102 |
| 1997 | 107 |
| 1998 | 115 |
| 1999 | 119 |
| 2000 | 122 |
| 2001 | 123 |
| 2002 | 126 |
| 2003 | 131 |
| 2004 | 138 |
| 2005 | 173 — **FLAGGED: this jump from 138 (2004) looks anomalous relative to surrounding years and was not confirmed against the primary FBM-0321 PDF at build time; treat with caution** |
| 2010 | 254 |
| 2011 | 290 |
| 2012 | 334 |
| 2013 | 382 |
| 2014 | 403 |
| 2017 | 385 |
| 2018 | 392 |
| 2019 | 384 |

*Source: farmdoc, "Index Numbers of Illinois Farmland Values" (FBM-0321), University of Illinois, 2025 edition, built from NASS annual farm real estate values, [farmdoc.illinois.edu/assets/management/farmland-values/FBM-0321landvalueindex_2025.pdf](https://farmdoc.illinois.edu/assets/management/farmland-values/FBM-0321landvalueindex_2025.pdf). The 2010, 2013, and 2014 index points (254, 382, 403) were independently corroborated at verification across multiple secondary citations; other individual years in the table were not separately re-checked and, per this knowledge base's build-environment disclosure, should be treated as medium-confidence pending a direct primary-document read.*

**Formula — index construction:**
```
Index_t = (Farm real estate value_t / Farm real estate value_1979) × 100
```
- *Farm real estate value_t* = NASS average Illinois farm real estate value per acre in year *t*.
- *Farm real estate value_1979* = NASS average Illinois farm real estate value per acre in the 1979 base year.

*Worked example:* the 2013 index of 382 combined with the independently sourced 2013 dollar value of $7,100/acre implies a 1979 base value of $7,100 / 3.82 ≈ **$1,859/acre** — broadly consistent with the $2,041–$2,188/acre range documented for 1980–1981 in §3.2 above. This back-calculation was not independently confirmed against a primary-source 1979 dollar figure and should be read as an approximation, not an independently published number — **[not confirmed against a primary source at build time]**. Growth-rate context from the index: 1995–1999 saw annual increases of 4.2%–9%; 2000–2004 saw 1.3%–5.3%; and the 2010–2014 run-up (index 254 → 403, +58.7% ≈ "+59% in 4 years") reflects the row-crop commodity price boom of that period.
*Source: farmdoc FBM-0321, as above.*

### 3.4 The eras since 1987, summarized

| Era | Change | Notes |
|---|---|---|
| 1987–2004 (recovery) | Slow, steady increases for roughly a decade and a half after the 1987 trough | farmdoc daily, "A Historical Perspective on Illinois Farmland Sales" (2013) |
| 2004–2014 (ethanol/commodity boom) | ~+290% over 10 years (≈9%/yr); roughly $2,650/acre (2004) to a ~$7,700/acre peak (2014) | **[not confirmed against a primary source at build time]** — these two anchor dollar figures could not be independently corroborated in this research pass and should be checked against the primary farmdoc index-number series before being relied upon; the associated cash-rent figures below were corroborated |
| Cash rent, 2006–2013 | $150/acre → $293/acre, +95% | Corroborated; farmdoc daily, "Farmland Prices and Government Programs" (July 7, 2026), [farmdocdaily.illinois.edu/2026/07](https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html). See `03-cash-rents.md` for the full rent series |
| 2015–2018 (plateau/decline) | –1.51%, –6.34%, –4.17%, –3.53% (year-over-year, respective years) | **Farm Credit Illinois Farmland Value Benchmark Study** — a distinct, lender-based proprietary benchmark, not the NASS or ISPFMRA series; [farmcreditil.com](https://www.farmcreditil.com/knowledge-center/Newsroom/2019/August/farmland-values-relatively-stable) (Aug. 2019 release) |
| 2019 | +0.17% to +0.2% (~flat) | Farm Credit Illinois, as above |
| 2020 | +2.07% | Farm Credit Illinois Benchmark Study |
| 2021 | +8.54% (Farm Credit Illinois); a separate FBN (Farmers Business Network) Illinois survey reported +5% for the same year — the two disagree because they sample different transaction sets | Farm Credit Illinois, Aug. 2022 release, [farmcreditil.com](https://www.farmcreditil.com/knowledge-center/newsroom/2022/08-aug/copy%20of%20farmland-value-benchmark-study-results) |
| 2022 | +27.88% (Farm Credit Illinois); other industry trackers cite ~+25% YoY, crossing $10,300/acre | Farm Credit Illinois, as above — confirmed at verification |

Both the 2015–2018 decline and the 2020–2022 surge (+2.07%, +8.54%, +27.88%) come from the **Farm Credit Illinois Farmland Value Benchmark Study**, a lender's own proprietary benchmark distinct from both the NASS survey and the ISPFMRA expert-opinion survey discussed in §4 — its levels and year-over-year moves are not directly comparable to the NASS series in §3.1 without adjustment, per this knowledge base's rule against silently mixing measurement systems. Drivers of the 2020–2022 surge: corn and soybean prices roughly doubled 2019–2022; near-zero interest rates through 2021 compressed capitalization rates; cash rents rose from $279/acre (2020) to $358/acre (2022), +18%; and 2022 saw the highest volume of Illinois farmland sales on record to that point, exceeding 2021's prior record.

**Since 2023, the market has cooled and diverged by data series and by land quality:**
- NASS's blended statewide figure still shows modest nominal gains: +4.5% (2023, pre-revision), +3.3% (2024, on the revised base), +2.6% (2025) — see §3.1.
- Quality-segmented data (ISPFMRA/farmdoc-cited county figures) shows top-quality land actually declining: Illinois Excellent-class farmland fell 3.29% from $16,906/acre (2023) to $16,359/acre (2024), and Good-class fell 0.79% from $12,726 to $12,626/acre (AgriNews coverage of the ISPFMRA 2025 report, confirmed at verification, [agrinews-pubs.com](https://www.agrinews-pubs.com/business/2025/04/08/year-of-transition-survey-finds-farmland-values-softening/)). See §4 for the full ISPFMRA class table.
- The Federal Reserve Bank of Chicago's *AgLetter* for Q1 2026 (published May 2026) shows Illinois specifically down 2% year-over-year (April 2025 to April 2026) even as the broader Seventh Federal Reserve District ("good" farmland) rose 3% YoY — Indiana +8%, Wisconsin +7%, Iowa +2%, Illinois –2% — with Illinois 2026 average cash rents down about 1% (vs. Indiana +2%, Iowa –4%, Wisconsin –1%). 56% of surveyed agricultural lenders considered farmland overvalued relative to fundamentals as of Q1 2026, versus 1% undervalued. ([chicagofed.org/publications/agletter/2025-2029/may-2026](https://www.chicagofed.org/publications/agletter/2025-2029/may-2026), confirmed at verification.) A fuller macro/outlook discussion, including the farm-income and government-payment context behind "sticky" prices amid falling farmer returns, belongs in `11-macro-drivers-and-outlook.md`.

## 4. How NASS relates to transaction prices and ISPFMRA class values

These are three different measurement systems and should never be treated as interchangeable:

1. **NASS farm real estate/cropland/pasture values** (§1–§3) are **self-reported, opinion-based estimates**, not transaction prices — see §5. They are a single statewide figure blending all cropland quality levels.
2. **ISPFMRA (Illinois Society of Professional Farm Managers and Rural Appraisers)** publishes a twice-yearly *Illinois Land Values and Lease Trends* survey in which professional farm managers and appraisers report observed **actual recorded sales**, segmented by soil-productivity class (Excellent/Good/Average/Fair/Poor) and by region — closer to a professional market view of realized transactions than NASS's opinion survey, though still not a full census of all sales. Full class-by-region detail, methodology, and the complete current benchmark table live in `07-ispfmra-benchmarks.md`; only headline figures are reproduced here for context.
3. **Actual transaction prices** (individual recorded sales, e.g., from auctions or brokered deals) are the ground truth both of the above are estimating, but a raw average of transactions is itself a biased sample: auctions in particular are a selected sample (sellers choose auctions when they expect competition) and skew high relative to the full market (see `../SOURCING.md`, "Known limitations"; full discussion in `09-sales-market-structure.md`).

**ISPFMRA headline figures, by report vintage (note: the *report year* and the *sales year it covers* are different — a recurring source of confusion in secondary coverage):**

| ISPFMRA report | Released | Sales year covered | Excellent-class statewide avg. | Average-class statewide avg. |
|---|---|---|---|---|
| 2025 Land Values and Lease Trends Report | Mar. 27, 2025 | CY2024 | $16,359/acre (down 3.29% from $16,906/acre in 2023) | not separately located in sources reviewed |
| 2026 Land Values and Lease Trends Report ("Farmland Prices at Plateau?") | ~Apr. 1, 2026 | CY2025 | $15,846/acre (median $15,984), down ~3.27%/reported as "down 3%" for Class A | $9,933/acre (median $9,436) |

*Source: ISPFMRA 2025 and 2026 Land Values and Lease Trends Reports (member publications — manifest-only per copyright policy, see `../sources/MANIFEST.md`, items 10a–10b); secondary corroboration via AgriNews (Apr. 8, 2025) and Shaw Local (Apr. 11, 2026), [shawlocal.com](https://www.shawlocal.com/news/2026/04/11/farmland-prices-continued-to-soften-in-2025/). **Correction applied at verification:** an earlier research draft of this figure attributed the $15,846/$9,933 numbers to the 2025 report; they in fact belong to the 2026 report (CY2025 sales) — corrected here.*

Selected regional detail from the 2025 report (CY2024 sales), confirmed at verification:

| Region | Productivity class | # sales (2024) | Price range, $/acre | Average, $/acre |
|---|---|---|---|---|
| Region 6 | Excellent | 100+ | $11,000–$22,508 | $17,210 |
| Region 6 | Good | 37 | $8,000–$18,105 | $13,268 |
| Region 7 | Excellent | — | $15,750–$19,800 | $17,046 |
| Region 7 | Good | 23 | $7,950–$20,000 | $13,302 |

*Source: ISPFMRA 2025 Land Values and Lease Trends Report (released March 27, 2025); see `07-ispfmra-benchmarks.md` for the complete regional table and methodology.*

**Reconciling NASS and ISPFMRA:** NASS's single 2025 blended cropland figure ($9,850/acre) sits close to ISPFMRA's 2026-report **Average**-class statewide figure ($9,933/acre) — consistent with NASS's number being a population-wide blend rather than a top-quality figure — while ISPFMRA's **Excellent**-class figure ($15,846–$16,359/acre depending on vintage) is roughly 60%–70% above the NASS blended average, reflecting both a quality premium and ISPFMRA's skew toward actively traded, professionally managed central-Illinois cropland. Document `05-valuation-math.md` covers how to translate between soil-productivity-index-based valuation and these class figures.

## 5. NASS methodology and limitations

**Data collection.** NASS land-value estimates rest primarily on the **June Area Survey**, an area-sampling frame of roughly 9,000 one-square-mile segments covering the lower 48 states. Enumerators contact all agricultural operators within sampled segments and record self-reported cropland value, pasture value, and an estimated total land-and-buildings value for the operator's entire farming operation, along with an estimated percent change from the prior year. NASS defines **"farm real estate value"** as the price at which the property "could be sold... under current market conditions" if allowed to remain on the market for a reasonable time — a self-reported, hypothetical-market-value construct, **not** an actual transaction or closing price and not a third-party appraisal. **[not confirmed against a primary source at build time]:** one search result referenced a possible shift of the collection instrument to a separately named "Agricultural Land Values and Technology Use" survey conducted in August; the exact nature and timing of that transition was not independently confirmed and should be checked against NASS's own methodology report before being cited as fact.
*Source: NASS, "Guide to NASS Surveys — June Area / Land Values Methodology and Quality Measures" (methodology document dated September 2025), [nass.usda.gov/Surveys/Guide_to_NASS_Surveys/June_Area/](https://www.nass.usda.gov/Surveys/Guide_to_NASS_Surveys/June_Area/).*

**Key limitations for anyone using this series:**
- **Self-reported, not transaction-based.** Kansas State's AgManager.info explicitly flags NASS land values as "a broad indicator of changes in land values" that is "not derived from sale prices," and cautions against using them directly for farm-management decisions requiring transaction-price accuracy. Source: "Using USDA NASS Farmland Values for Farm Management Decision Making," AgManager.info (Kansas State University), [agmanager.info/land-leasing/land-buying-valuing/using-usda-nass-farmland-values-farm-management-decision-making](https://agmanager.info/land-leasing/land-buying-valuing/using-usda-nass-farmland-values-farm-management-decision-making).
- **Smooths turning points.** Because it averages self-reported operator opinion across a wide sample, the series tends to lag and smooth market turning points and sits below top-tier transaction prices for the highest-quality land (see `../SOURCING.md`, "Known limitations of the underlying sources").
- **Periodic re-benchmarking creates level shifts.** As detailed in §2, the post-Census "final historic revision" (most recently the 2022 Census of Agriculture, applied in the August 2024 report) can shift several prior years' published levels by mid-single to high-single digits, unrelated to actual market movement in those years.
- **Thin markets and sampling noise.** At sub-state resolution (county, agricultural district), few actual sales per period make transaction-based comparisons volatile; NASS's own survey-based county cash-rent estimates likewise carry sampling noise in low-response counties, and year-over-year county-level moves should be read cautiously (see `../SOURCING.md`).
- **District/county detail not covered here.** NASS does publish Agricultural Statistics District-level breakdowns of Illinois farm real estate, cropland, and pasture values in the full *Land Values Summary* and via QuickStats, but district-level figures were not obtained in the research pass behind this document. See `12-data-source-directory.md` for how to query NASS QuickStats directly (Program = Survey, Sector = Economics, Group = Farms & Land & Assets, Commodity = Ag Land, Category = Asset Value, State = Illinois, geographic level = Agricultural District).

## Sources

- USDA NASS, "Land Values 2025 Summary" (Aug. 1, 2025, describing 2025 values). https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0825.pdf
- USDA NASS, "Land Values 2024 Summary" (Aug. 2, 2024, describing 2024 values and the 2022-Census benchmark revision). https://www.nass.usda.gov/Publications/Todays_Reports/reports/land0824.pdf
- USDA NASS, "Land Values and Cash Rents" Highlights, 2025. https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf
- USDA NASS, "Guide to NASS Surveys — June Area / Land Values Methodology and Quality Measures" (methodology document, Sept. 2025). https://www.nass.usda.gov/Surveys/Guide_to_NASS_Surveys/June_Area/
- University of Illinois farmdoc daily, "Illinois Farm Real Estate Values Hold Strong in 2025 Even with Lower Farm Incomes" (Aug. 8, 2025). https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html
- University of Illinois farmdoc daily, "Illinois Farm Real Estate Value Continues Increase…for 2023" (Aug. 2023). https://farmdocdaily.illinois.edu/2023/08/illinois-farm-real-estate-values-continues-increase-per-acre-for-2023.html
- University of Illinois farmdoc daily, "A Historical Perspective on Illinois Farmland Sales" (May 2013). https://farmdocdaily.illinois.edu/2013/05/historical-illinois-farmland-sales.html
- University of Illinois farmdoc daily, "Farmland Prices and Government Programs" (July 7, 2026). https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html
- University of Illinois farmdoc, "Index Numbers of Illinois Farmland Values" (FBM-0321), 2025 edition. https://farmdoc.illinois.edu/assets/management/farmland-values/FBM-0321landvalueindex_2025.pdf
- "An Analysis of Historical Illinois Farmland Valuations," Southern Illinois University Carbondale (OpenSIUC). https://opensiuc.lib.siu.edu/cgi/viewcontent.cgi?article=2014&context=gs_rp
- "The 1970s U.S. Farmland Bubble," thebubblebubble.com (undated retrospective). https://www.thebubblebubble.com/farmland-bubble/
- ISPFMRA, 2025 Illinois Land Values and Lease Trends Report (released Mar. 27, 2025; member publication, manifest-only). https://ispfmra.org/download/2025-land-values-report/
- ISPFMRA, 2026 Illinois Land Values and Lease Trends Report, "Farmland Prices at Plateau?" (released ~Apr. 1, 2026; member publication, manifest-only). https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/
- AgriNews, "Year of Transition: Survey Finds Farmland Values Softening" (Apr. 8, 2025), covering the ISPFMRA 2025 report. https://www.agrinews-pubs.com/business/2025/04/08/year-of-transition-survey-finds-farmland-values-softening/
- Shaw Local, "Farmland Prices Continued to Soften in 2025" (Apr. 11, 2026), covering the ISPFMRA 2026 report. https://www.shawlocal.com/news/2026/04/11/farmland-prices-continued-to-soften-in-2025/
- Federal Reserve Bank of Chicago, AgLetter, "First Quarter Midwest Farmland Values Up Some from a Year Ago" (May 2026, describing Q1 2026). https://www.chicagofed.org/publications/agletter/2025-2029/may-2026
- Farm Credit Illinois, Farmland Value Benchmark Study Results (Aug. 2019 release, covering 2015–2019). https://www.farmcreditil.com/knowledge-center/Newsroom/2019/August/farmland-values-relatively-stable
- Farm Credit Illinois, Farmland Value Benchmark Study Results (Aug. 2022 release, covering 2020–2022). https://www.farmcreditil.com/knowledge-center/newsroom/2022/08-aug/copy%20of%20farmland-value-benchmark-study-results
- AgManager.info (Kansas State University), "Using USDA NASS Farmland Values for Farm Management Decision Making." https://agmanager.info/land-leasing/land-buying-valuing/using-usda-nass-farmland-values-farm-management-decision-making
- `../SOURCING.md` — sourcing standards and known limitations of underlying sources for this knowledge base.
- `../sources/MANIFEST.md` — full source manifest, including archival status.
