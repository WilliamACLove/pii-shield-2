# farmdoc: Returns, Budgets, and Leasing Tools

University of Illinois farmdoc / farmdoc daily as the primary grounding source for Illinois crop-budget returns, cash-rent guidance, and leasing decision tools — with the exact URLs to pull current numbers from.

**Data current as of:** initial 2026 crop budgets (Aug 19, 2025) and Jan 13, 2026 revision; cash-rent guidance (Sept. 9, 2025); historical corn/soybean returns update (June 2, 2026); farmland-price/government-programs outlook (July 7, 2026); 2026 ISPFMRA survey as cross-posted by farmdoc (~Mar/Apr 2026); USDA NASS *Land Values 2025 Summary* (Aug 1, 2025, describing 2025 values).

**Built/verified:** 2026-07-12

> **Build-environment note:** per [`../SOURCING.md`](../SOURCING.md), this session's outbound fetches to farmdoc.illinois.edu, farmdocdaily.illinois.edu, and nass.usda.gov were blocked at the network-policy level; the figures below come from a hosted web-search service's snippets, independently re-checked by a second verification pass, rather than from directly opened primary pages. Verification verdicts (confirmed / corrected / unverifiable) are noted inline. Treat every number as well-sourced but not document-confirmed until a follow-up session with direct access re-pulls the primary PDFs/HTML.

## 1. The farmdoc Operator/Land Return Framework

farmdoc's recurring crop-budget series (Illinois Crop Budgets and Historic Returns) defines returns as:

```
Land Return per acre        = Gross Revenue per acre − Non-Land Production Costs per acre
Farmer/Operator Return       = Land Return per acre − Cash Rent per acre
  (cash-rented ground)
```

- **Gross Revenue** = (Yield × Price) + government/insurance payments (ARC/PLC, crop insurance indemnities, ad hoc assistance such as Farmer Bridge Assistance).
- **Yield** = expected bu/acre for corn or soybeans by region and productivity class (e.g., central Illinois, high-productivity soils).
- **Price** = farmdoc's assumed marketing-year average price per bushel for the budget vintage.
- **Non-Land Production Costs** = seed, fertilizer, chemicals, crop insurance premiums, fuel/power, machinery repair/depreciation/lease, labor, interest, and other overhead — everything except land cost/rent.
- **Cash Rent** = the assumed or survey-based per-acre cash rent for the region/class.

Source: farmdoc daily crop-budget methodology, described across *2026 Illinois Crop Budgets* (Aug. 19, 2025) — [farmdocdaily.illinois.edu/2025/08/2026-illinois-crop-budgets.html](https://farmdocdaily.illinois.edu/2025/08/2026-illinois-crop-budgets.html). Verification verdict: **confirmed** (algebraic consistency check passed; formula is a direct rearrangement, and spot-checks against confirmed cash-rent and return figures below are directionally consistent).

A companion identity used in the cash-rent-setting literature (Section 4):

```
Breakeven Rent Reduction Needed = Current (or projected) Cash Rent per acre − Land Return per acre
```

i.e., the rent cut required so Land Return equals Cash Rent (zero operator return). Source: farmdoc daily, *Considerations for Setting 2026 Cash Rents* (Sept. 9, 2025) — [farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html](https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html).

## 2. Operator/Land Return History — Central Illinois High-Productivity Farmland

**[Not confirmed against a primary source at build time.]** The verification pass could not confirm this specific year-by-year sequence and found it inconsistent with other search-derived figures for what should be the same farmdoc chart (one search described 2021–2022 "operator and land return" — a pre-cash-rent-deduction measure — as "more than $600/acre," falling to $266/acre in 2023; another described a 2026 projected "operator and land return" of $312/acre with ARC/PLC paid in "Oct. 2027," a date that itself conflicts with the Oct. 2026 payment date used elsewhere in these notes). The table below reproduces the original research draft for reference, flagged as unverified; do not cite it as fact without pulling the primary chart (likely in `crop_budgets_2026.pdf` or the historic-returns handbook section, Section 7 below).

| Crop Year | Farmer/Operator Return per acre | Note |
|---|---|---|
| 2021 | +$314 | Grain-price spike |
| 2022 | +$269 | Ukraine-Russia war grain disruption |
| 2023 | −$47 | First negative year of current downturn |
| 2024 | −$35 | Second consecutive negative year |
| 2025 | ~−$6 | Per one farmdoc release; other releases show larger negatives depending on vintage |
| 2026 (projected) | ~+$11 in one release, OR still framed as a "fourth straight negative year" in others | Estimates revised repeatedly through 2026 as price/ARC-PLC assumptions changed |

*Source (unverified): farmdoc daily, cross-referenced from [2026-illinois-crop-budgets.html](https://farmdocdaily.illinois.edu/2025/08/2026-illinois-crop-budgets.html), [revised-illinois-crop-budgets-for-2026.html](https://farmdocdaily.illinois.edu/2026/01/revised-illinois-crop-budgets-for-2026.html), and [historical-corn-versus-soybean-returns-in-illinois.html](https://farmdocdaily.illinois.edu/2026/06/historical-corn-versus-soybean-returns-in-illinois.html). Verification verdict: **unverifiable**.*

What *is* independently confirmed (Section 3 below) is the directional narrative: 2021–2022 were sharply positive years on cash-rented ground, followed by a multi-year negative-return stretch for corn-soybean rotations that farmdoc's July 2026 outlook (Section 6) still describes as ongoing.

## 3. 2026 Illinois Crop Budgets — Central Illinois

### 3.1 Initial release (Aug. 19, 2025) vs. revised release (Jan. 13, 2026)

The verification pass found that the original research notes had **conflated figures from two different budget vintages** — the corrected table below separates them.

| Item | Initial Aug. 2025 budget | Jan. 13, 2026 revision |
|---|---|---|
| Corn yield, central IL | 241 bu/acre | 241 bu/acre |
| Soybean yield, central IL | 76 bu/acre | 76 bu/acre |
| Corn price | **$4.15/bu** *(corrected — see note)* | $4.25/bu |
| Soybean price | **$10.30/bu** *(corrected — see note)* | $10.40/bu |
| ARC/PLC assumption, central IL | **~$50/acre** *(corrected — see note)* | included, plus Farmer Bridge Assistance |
| Corn gross revenue | not independently confirmed at initial-release prices | ~$1,080/acre |
| Soybean gross revenue | not independently confirmed at initial-release prices | ~$846/acre |
| Farmer/operator return, corn (by region) | −$72/acre (northern IL) to −$111/acre (southern IL) | same range restated |
| Farmer/operator return, soybeans (by region) | not separately reported | −$8/acre (southern IL) to +$18/acre (central IL) |
| Farmer Bridge Assistance added to 2025 returns | — | +$44/acre (corn), +$31/acre (soybeans), +$39/acre (wheat) |

*Source: farmdoc daily, [2026 Illinois Crop Budgets](https://farmdocdaily.illinois.edu/2025/08/2026-illinois-crop-budgets.html) (Aug. 19, 2025) and [Revised Illinois Crop Budgets for 2026](https://farmdocdaily.illinois.edu/2026/01/revised-illinois-crop-budgets-for-2026.html) (Jan. 13, 2026).*

**Correction note:** the original research draft attributed corn/soybean prices of $4.25/$10.40 per bu, ARC/PLC of ~$56/acre, and gross revenues of ~$1,080 (corn)/~$846 (soybeans) to the *initial* Aug. 2025 release. Independent re-verification against multiple secondary sources (FarmWeekNow and a syndicated mirror of the same farmdoc article) found the initial release instead used corn at $4.15/bu, soybeans at $10.30/bu, and ARC/PLC at ~$50/acre — a 10-cent-per-bushel increase distinguishes the initial numbers from the *revised* Jan. 2026 figures, and the $1,080/$846 gross-revenue figures are explicitly the revised-budget numbers. Yields (241/76 bu/acre) and the −$72 to −$111/acre corn-return range check out consistently across both vintages. Verification verdict: **corrected**.

A separate, later estimate cited "~$65/acre" as expected ARC/PLC support for central Illinois high-productivity ground (not paid until October 2026); this appears to be a distinct actual-payment-rate estimate rather than either budget's initial assumption, and its date/vintage was not independently pinned down — **[not confirmed against a primary source at build time]**.

Non-land costs were reported as rising slightly 2025→2026 (higher nitrogen costs for corn, lower potash costs for soybeans, stable power costs, overhead rising on labor and interest), marking what farmdoc describes as the fourth consecutive year of negative average returns for cash-rented corn-soybean rotations across all Illinois regions.

## 4. Cash Rents and the "Stickiness" Thesis

### 4.1 Illinois average cash rent, USDA NASS (as cited by farmdoc)

| Year | Illinois average cash rent, all cropland | Note |
|---|---|---|
| 2024 | $269/acre | USDA NASS figure as cited by farmdoc |
| 2025 | $264/acre | Larger declines on higher-productivity soil; slight increase on lower-productivity soil |
| 2026 (expectation) | Further reductions expected, but not enough to reach breakeven | farmdoc's calculation: rents would need to fall **more than $30/acre further** for cash-rented returns to reach breakeven |

*Source: farmdoc daily, [Considerations for Setting 2026 Cash Rents](https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html) (Paulson, Schnitkey, Zulauf, Baltz; Sept. 9, 2025). This was the first year-over-year statewide cash-rent decline since 2020 (when rent fell from $224 to $222/acre). Verification verdict: **confirmed** (independently re-derived via WebSearch synthesis and matched precisely, including the >$30/acre breakeven-shortfall figure).*

### 4.2 The stickiness argument

Applying the Section 1 identity: with Illinois average cash rent at $264/acre (2025) and farmdoc's own crop-budget Land Return implying a shortfall of **>$30/acre**, actual/expected rent adjustment ($269→$264, i.e. $5/acre) has been roughly one-sixth of what the negative Land Return implies would be needed to restore breakeven. farmdoc daily's July 7, 2026 article *Farmland Prices and Government Programs* argues that federal Commodity Title programs (ARC/PLC) plus ad hoc assistance (MFP, CFAP, ECAP, Farmer Bridge Assistance under the OBBBA) have propped up farm income and slowed the downward adjustment of both cash rents and land prices — i.e., government payments are identified by farmdoc as the primary mechanism behind the stickiness, not a claim that rents/prices are mispriced absent that support. Illinois farmland prices rose sharply 2020–2023, then flattened/declined only slightly since, even as operator returns on cash-rented ground turned negative for four straight crop years.

*Source: farmdoc daily, [Farmland Prices and Government Programs](https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html) (July 7, 2026). Verification verdict: **confirmed** as a described farmdoc analytical argument (attribute as farmdoc's interpretation, not raw statistical fact).*

See [`04-lease-structures-and-law.md`](04-lease-structures-and-law.md) for the legal mechanics of cash-rent adjustment (notice periods, lease-year timing) that also contribute to observed stickiness, and [`03-cash-rents.md`](03-cash-rents.md) for the full county-level NASS cash-rent series.

## 5. Corn vs. Soybean Return Reversal (2013–2025)

farmdoc daily's *Historical Corn versus Soybean Returns in Illinois* (June 2, 2026; Paulson, Schnitkey, Zulauf) — based on Illinois FBFM (Farm Business Farm Management) data for central Illinois high-productivity grain farms — finds soybean per-acre returns exceeded corn returns in **10 of 13 crop years, 2013–2025**, reversing the 2000–2012 pattern in which corn was more often the more profitable crop. The average soybean-over-corn return advantage across that period was **$53/acre**, with the largest single-year gap of **$237/acre in 2023**. Illinois farmers have shifted acreage from corn toward soybeans in response.

*Source: farmdoc daily, [Historical Corn versus Soybean Returns in Illinois](https://farmdocdaily.illinois.edu/2026/06/historical-corn-versus-soybean-returns-in-illinois.html), vol. 16, issue 96 (June 2, 2026). Verification verdict: **confirmed** (independently re-derived via WebSearch synthesis; the $53/acre average and $237/acre 2023 peak were additional detail found during verification, not present in the original draft).*

## 6. farmdoc Daily Outlook — Current Read on Farmland Prices

- **April 7, 2026** — *2026 Illinois Farmland Price Expectations: Navigating a Stable Yet Softening Market* (Tsay & Schnitkey; farmdoc daily vol. 16, issue 59), framing the 2026 ISPFMRA survey: after strong early-2020s appreciation, the Illinois farmland market is stabilizing on tighter crop margins and higher expected input costs (69% of survey respondents expect input costs to rise in 2026), while long-term (5-year) optimism among market professionals remains strong. [farmdocdaily.illinois.edu/2026/04/2026-illinois-farmland-price-expectations-navigating-a-stable-yet-softening-market.html](https://farmdocdaily.illinois.edu/2026/04/2026-illinois-farmland-price-expectations-navigating-a-stable-yet-softening-market.html). Verdict: **confirmed**.
- **July 7, 2026** — *Farmland Prices and Government Programs* — the stickiness thesis; see Section 4.2. [farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html](https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html). Verdict: **confirmed** (as described analytical argument).
- **November 2024** — *Outlook for Farmland Values in 2025* (Paulson & Schnitkey) predicted roughly a **3% decline** in Illinois farmland values for 2025. Actual USDA NASS 2025 data instead showed a **+2.6% increase** to $8,930/acre (Section 7.1) — a documented forecast miss, useful for calibrating confidence in farmdoc's forward-looking price calls (frame as "forecast vs. actual," not a general reliability critique). [farmdocdaily.illinois.edu/2024/11/outlook-for-farmland-values-in-2025.html](https://farmdocdaily.illinois.edu/2024/11/outlook-for-farmland-values-in-2025.html). Verdict: **confirmed**.
- **2026 ISPFMRA survey** (cross-posted to farmdoc daily as *Farmland Prices at Plateau?*, ~April 1, 2026): **61%** of Illinois professional farm managers expect further 2026 price softening (50% expecting 0–5% declines, 11% expecting 5–10%), 25% expect flat prices, 14% expect a slight increase — while most still expect appreciation over a 5-year horizon. See Section 7.2 for the class-level detail and [`07-ispfmra-benchmarks.md`](07-ispfmra-benchmarks.md) for the full ISPFMRA regional breakdown. Verdict: **confirmed** (triangulated across three independent search queries).

## 7. Land Values Context (NASS and ISPFMRA, for cross-reference)

### 7.1 USDA NASS land values, 2025

| Metric | 2025 value | Change from 2024 |
|---|---|---|
| U.S. average farm real estate | $4,350/acre | +4.3% |
| U.S. average cropland | $5,830/acre | +$260 (+4.7%) |
| U.S. average pasture | $1,920/acre | +$90 (+4.9%) |
| Illinois average farm real estate | $8,930/acre | +2.6% (from $8,700/acre in 2024) |

*Source: USDA NASS, Land Values 2025 Summary, released Aug. 1, 2025, describing 2025 values — **[esmis.nal.usda.gov/.../land0825.pdf](https://esmis.nal.usda.gov/sites/default/release-files/pn89d6567/2n49w148w/m039n441h/land0825.pdf)** (mirror: [downloads.usda.library.cornell.edu](https://downloads.usda.library.cornell.edu/usda-esmis/files/pn89d6567/2n49w148w/m039n441h/land0825.pdf)); cited via farmdoc daily, [Illinois Farm Real Estate Values Hold Strong in 2025, Even with Lower Farm Incomes](https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html) (Zwilling, Aug. 8, 2025). Illinois's $8,930/acre figure represents the fifth consecutive year (since 2020) of at least a 2.4% annual gain (averaging 4.7%/year) and is 22% above the 2016 level ($7,300/acre); among Corn Belt states, Iowa led at $9,790/acre and Ohio at $9,350/acre. Verification verdict: **corrected** — dollar figures confirmed accurate, but the URL originally cited (`www.nass.usda.gov/Publications/Todays_Reports/reports/land0825.pdf`) could not be verified to resolve; NASS's report distribution has moved to the ESMIS/Cornell mirror above. Cite `esmis.nal.usda.gov` (or the Cornell mirror), not the `nass.usda.gov` path.*

This $8,930/acre figure is a blended, all-farm-real-estate NASS state average — do not conflate it with per-acre values for top-quality tillable cropland specifically, or with ISPFMRA's expert-opinion class values below (see [`02-land-values-and-price-history.md`](02-land-values-and-price-history.md) rule on not mixing measurement systems).

**[Not confirmed against a primary source at build time]** — the same source is reported to give an "excellent"-class central Illinois cash rent range that fell from $350–$425/acre (2024) to $315–$404/acre (2025); the verification pass could not independently confirm this specific range and found other search results describing different (higher) figures likely conflating "newly negotiated" vs. "existing" rent categories. Use ISPFMRA's class-level cash rents (7.2) or NASS county cash rents ([`03-cash-rents.md`](03-cash-rents.md)) as the primary reference instead.

### 7.2 ISPFMRA 2026 report highlights (cross-reference)

| Land class | Existing cash rent ($/acre) |
|---|---|
| Excellent | $375 |
| Good | $325 |
| Average | $273 |
| Fair | $200 |

| Class | 2025 calendar-year value change |
|---|---|
| Class A | −3% |
| Class B | unchanged |
| Class C | up |
| Class D | up |
| Recreational | up |

Newly negotiated lease-type mix: 35% traditional cash rent, 27% flexible/variable cash rent, 27% crop share, 6% custom, 6% other.

*Source: Illinois Society of Professional Farm Managers and Rural Appraisers, 2026 *Illinois Land Values and Lease Trends* report — [ispfmra.org/download/2026-land-values-report/](https://ispfmra.org/download/2026-land-values-report/); companion farmdoc daily post, [Farmland Prices at Plateau?](https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/) (~April 1, 2026). Per SOURCING.md, ISPFMRA's full report is a member-organization survey publication not archived in full (see [`../sources/MANIFEST.md`](../sources/MANIFEST.md) item 10a); figures here are cited for grounding only. Verification verdict: **confirmed** (triangulated across three independent search queries converging on identical class-level figures and lease-mix percentages). Full 10-region breakdown not retrieved this session — see [`07-ispfmra-benchmarks.md`](07-ispfmra-benchmarks.md).*

## 8. farmdoc Tools, Budgets, and Leasing Publications — URL Directory

These are the primary farmdoc destinations for grounding claims about Illinois farmland returns, budgets, and leasing. **[Not confirmed against a primary source at build time]** — URLs were surfaced via search-engine indexing this session (WebFetch was blocked to farmdoc.illinois.edu and farmdocdaily.illinois.edu), so confirm each resolves before relying on it in a downstream tool call; fact-sheet filenames dated "2017" suggest those specific PDFs may be superseded editions even if still linked from current pages.

| Resource | URL | Purpose |
|---|---|---|
| Illinois Crop Budgets and Historic Returns (handbook section) | [farmdoc.illinois.edu/handbook-sections/illinois-crop-budgets-and-historic-returns](https://farmdoc.illinois.edu/handbook-sections/illinois-crop-budgets-and-historic-returns) | Primary landing page for the recurring crop-budget/return series (Sections 1–3 above) |
| 2026 Budgets for All Regions | [farmdoc.illinois.edu/handbook/2026-budgets-for-all-regions](https://farmdoc.illinois.edu/handbook/2026-budgets-for-all-regions) | Region-by-region 2026 budget detail |
| 2026 crop budgets PDF | [farmdoc.illinois.edu/assets/management/crop-budgets/crop_budgets_2026.pdf](https://farmdoc.illinois.edu/assets/management/crop-budgets/crop_budgets_2026.pdf) | Full downloadable 2026 budget tables |
| Actual/Projected Costs 2026 PDF | [farmdoc.illinois.edu/assets/management/crop-budgets/actual_projected_costs_2026_Aug.pdf](https://farmdoc.illinois.edu/assets/management/crop-budgets/actual_projected_costs_2026_Aug.pdf) | Non-land cost detail underlying the budgets |
| Management homepage | [farmdoc.illinois.edu/management](https://farmdoc.illinois.edu/management) | Entry point to all management content |
| Management handbook | [farmdoc.illinois.edu/management/handbook](https://farmdoc.illinois.edu/management/handbook) | Full FAST/handbook reference |
| Decision Tools index | [farmdoc.illinois.edu/decision-tools](https://farmdoc.illinois.edu/decision-tools) | Index of interactive Excel/web decision tools |
| Farmland and Cropland Index and Return Utility | [farmdoc.illinois.edu/decision-tools/farmland-and-cropland-index-and-return-utility](https://farmdoc.illinois.edu/decision-tools/farmland-and-cropland-index-and-return-utility) | Interactive tool for indexing historical returns to current productivity/price assumptions |
| Farmland Values Resources page | [farmdoc.illinois.edu/farmland-center/farmland-values-resources](https://farmdoc.illinois.edu/farmland-center/farmland-values-resources) | Curated links on Illinois farmland value data |
| Illinois Farm Economics Summit (IFES) | [farmdoc.illinois.edu/ifes](https://farmdoc.illinois.edu/ifes) | Annual outlook conference; slide decks often include the latest return/rent figures |
| Cash Rent Lease Fact Sheet | [farmdoc.illinois.edu/assets/management/leasing-facts-prices/Cash_Rent_Lease_Fact_Sheet_2017.pdf](https://farmdoc.illinois.edu/assets/management/leasing-facts-prices/Cash_Rent_Lease_Fact_Sheet_2017.pdf) | Fixed cash-rent lease primer (filename suggests 2017 edition — check for a newer version) |
| Variable Cash Rent Lease Fact Sheet | [farmdoc.illinois.edu/assets/management/leasing-facts-prices/Variable_Cash_Rent_Lease_Fact_Sheet_2017.pdf](https://farmdoc.illinois.edu/assets/management/leasing-facts-prices/Variable_Cash_Rent_Lease_Fact_Sheet_2017.pdf) | Flexible/variable cash-rent lease primer |
| Illinois Crop-Share Cash Farm Lease (Form CL01) | [farmdoc.illinois.edu/assets/legal/form/Farmdoc_Form_CL01_0912.pdf](https://farmdoc.illinois.edu/assets/legal/form/Farmdoc_Form_CL01_0912.pdf) | Standard crop-share lease legal form |
| Fixed Cash Lease — Short Form | [farmdoc.illinois.edu/assets/legal/form/cashRentShortForm.pdf](https://farmdoc.illinois.edu/assets/legal/form/cashRentShortForm.pdf) | Standard short-form cash lease |
| Farmland Values and Rental Agreements in Illinois for 2026 (handout) | [farmdoc.illinois.edu/wp-content/uploads/2025/09/2025-09-18-Farmland-and-Leases-in-2026-Handout.pdf](https://farmdoc.illinois.edu/wp-content/uploads/2025/09/2025-09-18-Farmland-and-Leases-in-2026-Handout.pdf) | Nick Paulson's Sept. 18, 2025 leasing-outlook handout for the 2026 crop year (see `../sources/MANIFEST.md` item 8) |
| farmdoc homepage | [farmdoc.illinois.edu](https://farmdoc.illinois.edu/) | Top-level site |
| farmdoc daily homepage | [farmdocdaily.illinois.edu](https://farmdocdaily.illinois.edu/) | Daily article archive — best entry point for the latest outlook piece |

Open item: it is unconfirmed whether farmdoc currently publishes an actively updated "Illinois Farmland Leasing Facts" series under that exact title — searches surfaced individual lease fact sheets and legal forms (filenames dated 2017) but not a confirmed current annual "Leasing Facts" compendium. Re-check `farmdoc.illinois.edu/management` and the handbook leasing section directly.

## 9. Known Gaps for a Follow-Up Verification Pass

- The primary year-by-year operator/land-return chart (Section 2) needs to be pulled directly from `crop_budgets_2026.pdf` or the historic-returns handbook section to resolve the internal inconsistency noted above.
- The 2026 ISPFMRA report's full 10-region breakdown (county/region-level values and rents) was referenced in search results but not retrieved in detail.
- Federal Reserve Bank of Chicago *AgLetter* — relevant to Illinois farmland credit conditions and District-level values — was completely inaccessible this session; see [`11-macro-drivers-and-outlook.md`](11-macro-drivers-and-outlook.md) and `../sources/MANIFEST.md` items 7a/7b for what is known second-hand.
- Every URL in Section 8 should be re-verified (HTTP 200 + content match) once direct network access to `farmdoc.illinois.edu` and `farmdocdaily.illinois.edu` is available.

## Cross-references

- [`02-land-values-and-price-history.md`](02-land-values-and-price-history.md) — NASS vs. ISPFMRA measurement systems, full price history
- [`03-cash-rents.md`](03-cash-rents.md) — county-level NASS cash-rent series
- [`04-lease-structures-and-law.md`](04-lease-structures-and-law.md) — lease-termination timing and its role in rent stickiness
- [`05-valuation-math.md`](05-valuation-math.md) — capitalization-rate approaches that complement the operator/land-return framework here
- [`07-ispfmra-benchmarks.md`](07-ispfmra-benchmarks.md) — full ISPFMRA regional detail
- [`11-macro-drivers-and-outlook.md`](11-macro-drivers-and-outlook.md) — AgLetter and broader macro context
- [`12-data-source-directory.md`](12-data-source-directory.md) — consolidated index of every source URL in this knowledge base

## Sources

- University of Illinois farmdoc daily, *2026 Illinois Crop Budgets*, Aug. 19, 2025 — https://farmdocdaily.illinois.edu/2025/08/2026-illinois-crop-budgets.html
- University of Illinois farmdoc daily, *Revised Illinois Crop Budgets for 2026*, Jan. 13, 2026 — https://farmdocdaily.illinois.edu/2026/01/revised-illinois-crop-budgets-for-2026.html
- University of Illinois farmdoc daily, *Considerations for Setting 2026 Cash Rents* (Paulson, Schnitkey, Zulauf, Baltz), Sept. 9, 2025 — https://farmdocdaily.illinois.edu/2025/09/considerations-for-setting-2026-cash-rents.html
- University of Illinois farmdoc daily, *Historical Corn versus Soybean Returns in Illinois* (Paulson, Schnitkey, Zulauf), June 2, 2026 — https://farmdocdaily.illinois.edu/2026/06/historical-corn-versus-soybean-returns-in-illinois.html
- University of Illinois farmdoc daily, *Illinois Farm Real Estate Values Hold Strong in 2025, Even with Lower Farm Incomes* (Zwilling), Aug. 8, 2025 — https://farmdocdaily.illinois.edu/2025/08/illinois-farm-real-estate-values-hold-strong-in-2025-even-with-lower-farm-incomes.html
- University of Illinois farmdoc daily, *2026 Illinois Farmland Price Expectations: Navigating a Stable Yet Softening Market* (Tsay & Schnitkey), Apr. 7, 2026 — https://farmdocdaily.illinois.edu/2026/04/2026-illinois-farmland-price-expectations-navigating-a-stable-yet-softening-market.html
- University of Illinois farmdoc daily, *Farmland Prices and Government Programs*, July 7, 2026 — https://farmdocdaily.illinois.edu/2026/07/farmland-prices-and-government-programs.html
- University of Illinois farmdoc daily, *Outlook for Farmland Values in 2025* (Paulson & Schnitkey), Nov. 2024 — https://farmdocdaily.illinois.edu/2024/11/outlook-for-farmland-values-in-2025.html
- Illinois Society of Professional Farm Managers and Rural Appraisers, *2026 Illinois Land Values and Lease Trends* (report, not archived in full per copyright rule) — https://ispfmra.org/download/2026-land-values-report/ ; companion post https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/
- USDA NASS, *Land Values 2025 Summary*, released Aug. 1, 2025 (describing 2025 values) — https://esmis.nal.usda.gov/sites/default/release-files/pn89d6567/2n49w148w/m039n441h/land0825.pdf
- University of Illinois farmdoc, tool and handbook pages listed in Section 8
- `../SOURCING.md` and `../sources/MANIFEST.md` — sourcing rules and full manifest of attempted retrievals
