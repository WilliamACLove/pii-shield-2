# Illinois Farm Lease Structures and Lease Law

Reference material on how Illinois farmland is leased — arrangement types and prevalence, the exact math behind flexible/variable cash rents, and the statutory rules governing termination, oral leases, and landlord liens. **This is not legal advice**; for an actual lease, notice-to-quit, or lien enforcement, consult an Illinois attorney and read the current statutory text at ilga.gov directly.

**Data current as of:** ISPFMRA 2025 Land Values Report (released ~Mar 27, 2025); ISPFMRA mid-year survey (cited Apr 2026); farmdoc daily 2026-leasing-year survey (Apr 13, 2026); farmdoc daily variable-rent parameter revision (Sept 30, 2025); farmdoc daily net-share-rent series (Jan 17, 2025); USDA NASS Land Values & Cash Rents (Aug 1, 2025, describing 2025); Chicago Fed AgLetter (Feb 2026, describing Q4 2025); Illinois Compiled Statutes, consolidated text current as of build date.
**Built/verified:** 2026-07-12

---

## 1. Lease type prevalence

Illinois farmland is leased under four broad structures: **fixed (traditional) cash rent**, **flexible/variable cash rent**, **crop share** (traditional or modified), and **custom farming**. The Illinois Society of Professional Farm Managers and Rural Appraisers (ISPFMRA) and University of Illinois farmdoc both survey the mix annually, but three separate survey administrations produced three different breakdowns for 2025-2026. Per [SOURCING.md](../SOURCING.md) rule 6, all three are reported below rather than reconciled, since they appear to reflect different survey waves and category granularity, not a correction of one another.

**ISPFMRA 2025 Land Values Report (annual flagship survey, released ~March 27, 2025):**

| Lease type | % of ISPFMRA members reporting use, 2025 |
|---|---|
| Traditional (fixed) cash rent | 41% |
| Variable/flexible cash rent | 26% |
| Traditional crop share | 21% |
| Other/unspecified | ~12% |

Source: ISPFMRA, *2025 Illinois Land Values Report* (released ~March 27, 2025), [ispfmra.org/download/2025-land-values-report](https://ispfmra.org/download/2025-land-values-report/); corroborated by Farm Progress and FarmWeekNow coverage, April 2025.

**ISPFMRA mid-year survey (finer categories, cited in an ISPFMRA post dated April 1, 2026):**

| Lease type | % of arrangements |
|---|---|
| Variable cash rent | 34% |
| Cash rent (fixed) | 25% |
| Traditional share rent | 21% |
| Modified share rent | 14% |
| Custom farming | 6% |

Source: ISPFMRA, "Farmland Prices at Plateau?" (April 1, 2026), [ispfmra.org/2026/04/01/farmland-prices-at-plateau](https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/).

**farmdoc daily survey for the 2026 leasing year:**

| Lease type | % of arrangements, 2026 |
|---|---|
| Traditional (fixed) cash rent | 35% |
| Traditional crop share | 27% |
| Variable cash rent | 27% |
| Other | ~11% |

The article states there are more fixed-cash-rent than variable-cash-rent contracts statewide, and that 67% of surveyed farm managers expect 2027 cash rents to be unchanged from 2026. Source: J. Tsay and G. Schnitkey, "Illinois Cash Rents and Leasing Expectations Through 2027," *farmdoc daily* (16):63, April 13, 2026, based on ISPFMRA survey data, [farmdocdaily.illinois.edu/2026/04/illinois-cash-rents-and-leasing-expectations-through-2027.html](https://farmdocdaily.illinois.edu/2026/04/illinois-cash-rents-and-leasing-expectations-through-2027.html).

Across all three surveys, fixed cash rent is the single largest category (25%-41% depending on wave), variable/flexible cash rent runs 26%-34%, and crop share (traditional + modified combined) runs 21%-41%; custom farming is a small niche (6% where separately tracked). See also [03-cash-rents.md](03-cash-rents.md) for cash-rent level data and [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md) for the full ISPFMRA survey program.

### Landowner return by lease structure

| Lease structure | Landowner income, $/acre (Excellent-quality land, 2025) |
|---|---|
| Traditional crop share | $250 |
| Cash rent | $300 |
| Custom farming | $375 |

Source: ISPFMRA, *2025 Illinois Land Values Report*, [ispfmra.org/download/2025-land-values-report](https://ispfmra.org/download/2025-land-values-report/) (2025 leasing-year data). Custom farming's smaller survey share (6% above) coexists with the highest per-acre landowner return, because the arrangement gives the landowner 100% of the crop and 100% of the price/yield risk (see §4).

---

## 2. Fixed cash rent

The tenant pays a flat, pre-negotiated $/acre amount regardless of yield or price outcomes; the tenant bears all production and price risk, the landowner bears none (beyond counterparty/credit risk). This is the plurality arrangement in every survey above. Cash-rent price levels, county detail, and multi-year trend are covered in [03-cash-rents.md](03-cash-rents.md); this document covers only the payment-timing and legal mechanics (§6-§7).

---

## 3. Flexible (variable) cash rent — exact formulas

Two mechanically distinct flexible-cash-rent models circulate in Illinois/Midwest extension and practitioner literature under the same "flexible" or "variable" cash rent label. Both set a base rent at signing and true it up after harvest; they differ in *how* the true-up is computed. Report both distinctly — do not conflate them.

### 3a. Farmdoc "cash rent with bonus" model (rent-factor-on-total-revenue)

Developed at University of Illinois farmdoc (G. Schnitkey, 2011) and still the reference model behind farmdoc's FAST "Cash Rent with Bonus Worksheet."

**Formula:**

```
Base Rent(crop) = Anticipated Price ($/bu) × Trend-Adjusted Yield (bu/acre) × Rent Factor
Calculated Rent(crop, at harvest) = Actual Yield (bu/acre) × Actual Price ($/bu) × Rent Factor
Bonus(crop) = MAX(0, Calculated Rent(crop) − Base Rent(crop))
Total Rent Paid = Base Rent + Σ Bonus(crop)   [summed/averaged across the rotation]
```

**Variable definitions:**
- **Rent Factor** — a fixed percentage applied to gross crop revenue to convert it to rent per acre. Historically **33% for corn and 40% for soybeans** in the original 2011 Illinois model.
- **Trend-Adjusted Yield** — a multi-year (e.g., 5-year Olympic average or trend-line) yield, ideally sourced from crop-insurance Actual Production History (APH) records.
- **Anticipated Price** — the new-crop futures price (e.g., December corn, November soybean contract) near lease signing.
- **Actual Price** — the price realized at harvest (fall cash/elevator price or a contract-specified average).

**Worked example** (base case, from the original 2011 article): base rent = $200/acre; at harvest, actual corn yield = 190 bu/acre and actual soybean yield = 55 bu/acre. Applying the 33%/40% rent factors to actual yield × actual price produces a bonus of **$111/acre (corn)** and **$33/acre (soybean)**, for a combined average bonus of **$144/acre**. Total rent paid = $200 base + $144 bonus = **$344/acre**. Source: G. Schnitkey, "Cash Rent with Bonus Leasing Arrangement: Description and Example," *farmdoc daily*, September 2011, [farmdocdaily.illinois.edu/2011/09/cash-rent-with-bonus-leasing-a-1.html](https://farmdocdaily.illinois.edu/2011/09/cash-rent-with-bonus-leasing-a-1.html); worksheet tool at [farmdoc.illinois.edu/fast-tools/cash-rent-with-bonus-worksheet](https://farmdoc.illinois.edu/fast-tools/cash-rent-with-bonus-worksheet).

**2025 recalibration.** In September 2025, farmdoc authors revised the rent factors slightly below the historical 33%/40% figures, recalibrated against 2007-2024 corn/soybean prices (the "new era" following the 2005/2007 RFS mandate). For a 50-50 corn-soybean rotation, the **2024** variable rent under the revised parameters would have averaged **$302/acre**, $35 below that year's average fixed cash rent of **$337/acre**. Projected farmer return under a variable lease was near break-even (~$4/acre) for 2025 and negative for 2026. The exact new rent-factor percentages replacing 33%/40% were not obtained in the underlying research pass — **[not confirmed against a primary source at build time]**; pull the precise figures directly from the article or its FAST tool before quoting a specific new percentage. Source: N. Paulson, G. Schnitkey, C. Zulauf, "Revised Variable Cash Lease Parameters," *farmdoc daily* (15):179, September 30, 2025, [farmdocdaily.illinois.edu/2025/09/revised-variable-cash-lease-parameters.html](https://farmdocdaily.illinois.edu/2025/09/revised-variable-cash-lease-parameters.html).

### 3b. "Trigger revenue" model (base-rent-plus-share-of-revenue-above-trigger)

A second formulation circulated via Extension/Farm Progress channels and farmdoc cost budgets, mechanically different from 3a: instead of applying a rent factor to *total* actual revenue, it pays the landowner a share only of the revenue *above* a cost-covering trigger.

**Formula:**

```
Base Cash Rent = 90% × Current/Reference Fixed Cash Rent   (negotiable starting discount)
Revenue Trigger(crop) = Base Cash Rent + Nonland Production Costs (per crop cost budget)
Actual Crop Revenue(crop) = Actual Yield × Actual Price
Bonus(crop) = MAX(0, [Actual Crop Revenue(crop) − Revenue Trigger(crop)] × Landowner Share)
Total Cash Rent(crop) = Base Cash Rent + Bonus(crop)
```

**Variable definitions:**
- **Landowner Share** — the negotiated percentage (commonly **50%**) of revenue above the trigger paid to the landowner as a bonus.
- **Nonland Production Costs** — per-acre input/operating costs (seed, fertilizer, chemicals, crop insurance) excluding land, typically drawn from University of Illinois or extension crop budgets.

**Worked example:** current fixed cash rent = $250/acre → base rent = $225/acre (90%). Corn revenue trigger = $1,050/acre; soybean revenue trigger = $700/acre; landowner share above trigger = 50%. In a scenario where yields/prices run 10% above base assumptions: corn yield 202.4 bu/acre at $5.89/bu = $1,191/acre revenue → bonus = ($1,191 − $1,050) × 50% = $70.50 → **cash rent = $295.50/acre** for corn. Soybean yield 61.6 bu/acre at $13.48/bu = $830/acre revenue → bonus = ($830 − $700) × 50% = $65 → **cash rent = $289.50/acre** for soybean. Source: Farm Progress, "How to build a flexible cash-rent lease" (secondary source summarizing farmdoc/extension methodology), [farmprogress.com/management/how-to-build-a-flexible-cash-rent-lease](https://www.farmprogress.com/management/how-to-build-a-flexible-cash-rent-lease); corroborated by farmdoc, *Variable Cash Rent Lease Fact Sheet* (2017), [farmdoc.illinois.edu/assets/management/leasing-facts-prices/Variable_Cash_Rent_Lease_Fact_Sheet_2017.pdf](https://farmdoc.illinois.edu/assets/management/leasing-facts-prices/Variable_Cash_Rent_Lease_Fact_Sheet_2017.pdf). Note: a related cited scenario uses a $943/acre corn trigger and $677/acre soybean trigger with the same 50% share-above-trigger mechanic — trigger levels are cost-budget-dependent and will differ by year and cost assumptions; confidence on the exact vintage of the $1,050/$700 example is **low** per the underlying research (undated Farm Progress secondary source).

---

## 4. Crop share and custom farming

### 4a. Traditional crop share

Landlord and tenant split both crop proceeds and specified input costs by an agreed ratio — most commonly **50/50**.

```
Landowner receives: 50% of crop proceeds + 50% of government/commodity payments
Landowner pays: 50% of shared input costs (seed, fertilizer, chemicals, drying, storage, crop insurance) + 100% of real estate property tax
Tenant receives: 50% of crop proceeds
Tenant pays: 50% of shared input costs + 100% of labor, machinery, and machinery operating costs (fuel, repairs)
```

Common variants: a **2/3-1/3** split (tenant takes 2/3 of the crop, pays all seed cost but only 2/3 of fertilizer/chemical cost) and a **60/40** split (tenant takes 60% of the crop; input-cost sharing is negotiated separately and is sometimes still 50/50 even when the crop split is 60/40). Source: University of Illinois farmdoc, *Crop Share Lease Fact Sheet* (2017 edition), [farmdoc.illinois.edu/assets/management/leasing-facts-prices/Crop_Share_Lease_Fact_Sheet_2017.pdf](https://farmdoc.illinois.edu/assets/management/leasing-facts-prices/Crop_Share_Lease_Fact_Sheet_2017.pdf). No single numeric worked example for the 50/50 split was located in the underlying research pass — the ratio logic is a long-standing farmdoc convention, not an annually revised figure.

### 4b. Landowner's adjusted net-share rent as % of crop returns (benchmarking metric)

farmdoc's long-running method for testing whether a crop-share rent level is proportionate to the landowner's land contribution:

```
Net-Share Rent % = (Landowner's Share of Gross Crop Revenue − Landowner's Share of Input Costs) / Total Crop Returns × 100
```

Historical range: **15%-20%** of crop returns on lower-productivity soils, up to **35%-37%** on the highest-productivity soils. The series rose from a 2014 low to a 2021 peak, then declined through a 2023 low (except in higher-rated central-Illinois soils, where 2015 was the low point), with 2024-2025 projected to rise again on lower per-acre production costs. Source: B. Zwilling, "Landowner's Adjusted Net-Share Rent as a Percent of Crop Returns," *farmdoc daily*, January 17, 2025, [farmdocdaily.illinois.edu/2025/01/landowners-adjusted-net-share-rent-as-a-percent-of-crop-returns.html](https://farmdocdaily.illinois.edu/2025/01/landowners-adjusted-net-share-rent-as-a-percent-of-crop-returns.html).

### 4c. Custom farming

The landowner keeps the entire crop and any government payments, pays for all cropping inputs, and pays a local farmer/custom operator a fixed per-acre or per-operation fee to till, plant, spray, and harvest. This reverses the risk allocation of a cash-rent lease: the owner bears 100% of production and price risk and, correspondingly, captures the largest per-acre return among the structures reported in the ISPFMRA 2025 data (§1) — $375/acre on Excellent land versus $300/acre for cash rent and $250/acre for traditional crop share. Custom farming was the smallest category by survey share (6%, ISPFMRA mid-year survey). Source: ISPFMRA 2025 Land Values Report (as above); custom-farming mechanics corroborated by Illinois Agriculture Authority overview, [illinoisagricultureauthority.com/illinois-farmland-leasing-and-rental](https://illinoisagricultureauthority.com/illinois-farmland-leasing-and-rental/) (undated secondary source — used only to corroborate structure, per [SOURCING.md](../SOURCING.md) rule 2).

Custom rates are conventionally set at a machinery cost basis plus a 5%-15% margin (cost basis excludes profit). Illustrative 2025 harvest cost basis: combining corn **$54.40/acre** (up from $38.50/acre in 2021), combining soybeans **$47.60/acre** (up 3%-4% since 2023). Source: University of Illinois farmdoc, *Machinery Cost Estimates: Field Operations*, 2025 edition, [farmdoc.illinois.edu/assets/management/machinery-costs/field_operations_2025.pdf](https://farmdoc.illinois.edu/assets/management/machinery-costs/field_operations_2025.pdf); corroborated by Farm Progress, "Illinois custom-harvest rates up nearly 4% since 2023."

---

## 5. Statutory termination notice — 735 ILCS 5/9-206

Illinois's general farm-tenancy termination rule is codified at **735 ILCS 5/9-206** (Illinois Code of Civil Procedure, Article IX). The operative requirement, as corroborated across the Illinois General Assembly's own codification and independent legal databases (FindLaw, LawServer, onecle.com — see verification note below):

> "In order to terminate tenancies from year to year of farm lands, occupied on a crop share, livestock share, cash rent or other rental basis, the notice to quit shall be given in writing not less than 4 months prior to the end of the year of letting. Such notice may not be waived in a verbal lease."

The statute also supplies a suggested notice-to-quit form identifying the tenant, describing the leased premises, and specifying the last day of the lease year.

**Verification note:** this session's environment blocked direct fetching of ilga.gov (see [SOURCING.md](../SOURCING.md), "Build-environment disclosure"); the quoted text above was independently cross-checked in two separate research passes against secondary legal-database mirrors (FindLaw, LawServer, onecle) that returned matching language, and is treated as **confirmed** per those sources rather than a byte-verified fetch of the primary ilga.gov page. Read the current codification directly at [ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-206](https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-206) before relying on this as a verbatim legal citation.

**Applies to every rental basis** — cash rent, crop share, livestock share, or other — for a year-to-year tenancy. It does not apply to leases with a fixed term stated in a written contract (which terminate per their own terms), only to the year-to-year tenancy that arises from continued occupancy without a new written term.

### 5a. The March 1 lease-year convention and the practical notice deadline

Illinois courts presume, absent convincing evidence of a different actual term, that a year-to-year farm tenancy runs **March 1 to the last day of February** — a convention with roots in historical livestock-farm operating cycles. Under that presumption, the 4-month notice window in 735 ILCS 5/9-206 falls **on or before roughly November 1** (4 calendar months before March 1). farmdoc's own extension bulletin is titled "October 31 is 'Notice' Deadline for Many Farm Leases," and that October 31 framing is the common practitioner shorthand — but note the precise arithmetic: November of the preceding year is exactly 4 months before the following March 1, so "on or before November 1" is the more defensible reading of the statute's "not less than 4 months" language; report both framings rather than picking one as exact, since practitioner sources use them inconsistently. Sources: farmdoc, *October 31 is "Notice" Deadline for Many Farm Leases* (Ag Law & Tax Brief ALTB_04-11), [farmdoc.illinois.edu/assets/legal/altb/ALTB_04-11.pdf](https://farmdoc.illinois.edu/assets/legal/altb/ALTB_04-11.pdf); Illinois Extension, "Terminating a Farm Lease in Illinois," Farm Coach blog, September 29, 2025, [extension.illinois.edu/blogs/farm-coach/2025-09-29-terminating-farm-lease-illinois](https://extension.illinois.edu/blogs/farm-coach/2025-09-29-terminating-farm-lease-illinois).

Cash-grain (row-crop) operations have increasingly shifted away from the March 1 convention to a **calendar-year (January 1-December 31)** lease term, to give an incoming tenant more lead time to prepare for spring planting after a tenant transition. For those leases, the 4-month notice deadline shifts to on/before roughly **September 1** (4 months before January 1). Source: same farmdoc/Extension termination guidance as above; secondary corroboration via Farmonaut, "Illinois Farm Lease Termination: October 31 Deadline Alert" (undated) — **[secondary source; not independently confirmed against a primary University of Illinois document beyond the ALTB_04-11 bulletin cited above]**.

### 5b. Life-tenant landlords — 735 ILCS 5/9-206.1

A companion, more specialized provision governs termination timing when the landlord (lessor) is a life tenant: the farm tenancy continues through the end of the current lease year in which the life tenant's interest terminates (unless the parties agree otherwise in writing); if the life tenancy ends less than 6 months before the end of the lessee's tenancy but before the next crop year begins, the tenant is entitled to reimbursement of reasonable field-preparation costs from the succeeding life tenant or remainderman. See [ilga.gov](https://codes.findlaw.com/il/chapter-735-civil-procedure/il-st-sect-735-5-9-206-1/) for the consolidated text (direct ilga.gov section link not independently re-verified in this build; FindLaw mirror cited).

---

## 6. Oral leases and the Statute of Frauds

Illinois oral (verbal) farm leases are enforceable for terms **up to one year** under the Illinois Frauds Act, **740 ILCS 80/2**. Only a contract for the sale or lease of land "for a longer term than one year" must be in writing and signed by the party to be charged (or their lawfully authorized agent) to be enforceable:

> No action shall be brought to charge any person upon a contract for the sale of lands... or upon any agreement that is not to be performed within the space of one year from the making thereof... unless the promise or agreement upon which such action shall be brought, or some memorandum or note thereof, shall be in writing.

Illinois courts treat a year-to-year oral farm tenancy — even one that in practice runs many years (e.g., a purported oral "lifetime" arrangement) — as a **series of successive one-year lettings**, each individually under a year and thus outside the Statute of Frauds writing requirement. However, **termination of an oral year-to-year tenancy still requires the written 4-month notice under 735 ILCS 5/9-206** — the notice-to-quit obligation is not excused merely because the underlying lease was oral. Source: 740 ILCS 80/2, [ilga.gov/legislation/ilcs/ilcs3.asp?ActID=2036](https://www.ilga.gov/legislation/ilcs/ilcs3.asp?ActID=2036); corroborated by Rincker Law, "Ask Ruth: How do you Terminate an Oral Farm Lease in Illinois?", [rinckerlaw.com/ask-ruth-how-do-you-terminate-an-oral-farm-lease-in-illinois](https://rinckerlaw.com/ask-ruth-how-do-you-terminate-an-oral-farm-lease-in-illinois/). Same verification caveat as §5 applies: quoted language was cross-checked via secondary legal databases, not a direct ilga.gov fetch, in this build environment.

---

## 7. Landlord's statutory crop lien — 735 ILCS 5/9-316

Illinois law grants every farm landlord a statutory lien on crops grown on the leased premises, codified (notably) within the Code of Civil Procedure rather than a separate agricultural-lien chapter:

> "Every landlord shall have a lien upon the crops grown or growing upon the demised premises for the rent thereof... and also for the faithful performance of the terms of the lease. Such lien shall continue for the period of 6 months after the expiration of the term..."

Key mechanics:
- **Duration:** the lien continues **6 months after lease expiration**.
- **Enforcement:** by distraint (seizure of the crop or its proceeds), under the Article IX distraint procedures of the Code of Civil Procedure.
- **Priority:** the lien has priority over UCC Article 9 security interests and other agricultural liens.
- **Purchaser protection:** a good-faith purchaser of the crop takes free of the lien **unless** the landlord gave written notice (by registered or certified mail) within the preceding 6 months.

Source: 735 ILCS 5/9-316, [ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-316](https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-316); see also National Agricultural Law Center, "Statutory Agricultural Lien Rapid Finder Chart: Illinois," [nationalaglawcenter.org/wp-content/uploads/assets/agliens/illinois.pdf](https://nationalaglawcenter.org/wp-content/uploads/assets/agliens/illinois.pdf). As with §5-§6, this quotation was corroborated via independent secondary legal-database searches rather than a direct ilga.gov fetch in this build environment; verify against the live statute before using as a formal citation.

---

## 8. Payment timing customs

A common Illinois cash-rent payment schedule splits payment **50% due around March 1** (spring, lease-year start) and **50% due around November 1** (fall, post-harvest), though the split is fully negotiable. There has been a market shift toward **100% payment upfront in spring**, especially on professionally managed farms — this eliminates the landowner's risk of tenant nonpayment on the fall installment and can justify a modest rent reduction, since the landowner receives funds well before harvest. Source: Illinois Extension, "Farm Leasing Series: Cash-Rent Farm Lease Contract Tips for Landowners and Farmers," Farm Coach blog, November 11, 2025, [extension.illinois.edu/blogs/farm-coach/2025-11-11-farm-leasing-series-cash-rent-farm-lease-contract-tips-landowners-and](https://extension.illinois.edu/blogs/farm-coach/2025-11-11-farm-leasing-series-cash-rent-farm-lease-contract-tips-landowners-and).

---

## 9. Model lease forms

University of Illinois farmdoc's Agricultural Law section publishes fillable model lease documents that serve as Illinois's de facto standard reference forms:

- Fixed Cash Rent Lease (including a "short form" for one-year terms)
- Crop-Share Cash Farm Lease
- Livestock-Share Lease
- Pasture Lease
- Three conservation-practice addendums (released September 26, 2019) that parties can attach to negotiate specific conservation terms alongside any of the above

Source: farmdoc, *Agricultural Law*, [farmdoc.illinois.edu/agricultural-law](https://farmdoc.illinois.edu/agricultural-law); "Conservation Addendums for Illinois Farm Leases," *farmdoc daily*, September 26, 2019, [farmdocdaily.illinois.edu/2019/10/conservation-addendums-for-illinois-farm-leases.html](https://farmdocdaily.illinois.edu/2019/10/conservation-addendums-for-illinois-farm-leases.html).

Note: a possible reference to "UAA" model lease forms could not be corroborated as a distinct named form series or organization in the underlying research — **[not confirmed against a primary source at build time]**. Treat the farmdoc/University of Illinois Extension forms above as the standard Illinois reference model leases unless a specific "UAA" series is independently identified.

---

## 10. Market context: rent levels are softening across independent measures

Three independently administered surveys agree directionally that Illinois cash rents plateaued or softened in 2025, though they diverge on magnitude — a divergence attributable to different sampling frames (professional farm managers vs. NASS's landowner/operator survey vs. Chicago Fed's ag-lender survey), not a data error:

| Source | Metric | Finding |
|---|---|---|
| ISPFMRA (professional farm managers) | Excellent-land cash rent range | $350-$425/acre (2024) → $315-$404/acre (2025) |
| ISPFMRA | Average-land cash rent range | $283-$355/acre (2024) → $260-$342/acre (2025) |
| USDA NASS (statistical survey) | Illinois state-average non-irrigated cropland cash rent | $265/acre (2025), down $4/acre from 2024 (essentially flat, after a +$47/acre gain 2020-2024) |
| Federal Reserve Bank of Chicago (ag-lender survey) | Illinois average cash rent, y/y change | −2% in 2025 — the 7th District's first Illinois cash-rent decline since 2020 |

Sources: ISPFMRA 2025 Land Values Report, [ispfmra.org/download/2025-land-values-report](https://ispfmra.org/download/2025-land-values-report/); USDA NASS, *2025 Land Values & Cash Rents* (released August 1, 2025), [nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf](https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf); corroborated by DTN, "Illinois Dominates Top 10 List of Highest County Cash Rents in Corn Belt," August 23, 2025; Federal Reserve Bank of Chicago, *AgLetter*, "Midwest Farmland Values Ended 2025 with Solid Growth," February 2026 (covering Q4 2025), [chicagofed.org/publications/agletter/2025-2029/february-2026](https://www.chicagofed.org/publications/agletter/2025-2029/february-2026). NASS county detail: Sangamon County recorded Illinois's highest 2025 county average at $372/acre (+$3 vs. 2024's $369); Piatt County, the 2024 leader at $377/acre, fell $54/acre in 2025. See [03-cash-rents.md](03-cash-rents.md) for full county-level detail and multi-year trend.

---

## Sources

- Illinois General Assembly (ilga.gov), 735 ILCS 5/9-206, *Notice to terminate tenancy of farm land*: [ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-206](https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-206)
- Illinois General Assembly (ilga.gov), 735 ILCS 5/9-206.1 (life-tenant landlord termination timing) — text corroborated via FindLaw mirror: [codes.findlaw.com/il/chapter-735-civil-procedure/il-st-sect-735-5-9-206-1](https://codes.findlaw.com/il/chapter-735-civil-procedure/il-st-sect-735-5-9-206-1/)
- Illinois General Assembly (ilga.gov), 735 ILCS 5/9-316, *Lien upon crops*: [ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-316](https://www.ilga.gov/legislation/ilcs/fulltext.asp?DocName=073500050K9-316)
- Illinois General Assembly (ilga.gov), 740 ILCS 80/2, Illinois Frauds Act: [ilga.gov/legislation/ilcs/ilcs3.asp?ActID=2036](https://www.ilga.gov/legislation/ilcs/ilcs3.asp?ActID=2036)
- National Agricultural Law Center, "Statutory Agricultural Lien Rapid Finder Chart: Illinois": [nationalaglawcenter.org/wp-content/uploads/assets/agliens/illinois.pdf](https://nationalaglawcenter.org/wp-content/uploads/assets/agliens/illinois.pdf)
- University of Illinois farmdoc, Ag Law & Tax Brief ALTB_04-11, "October 31 is 'Notice' Deadline for Many Farm Leases": [farmdoc.illinois.edu/assets/legal/altb/ALTB_04-11.pdf](https://farmdoc.illinois.edu/assets/legal/altb/ALTB_04-11.pdf)
- Illinois Extension, Farm Coach blog, "Terminating a Farm Lease in Illinois," September 29, 2025: [extension.illinois.edu/blogs/farm-coach/2025-09-29-terminating-farm-lease-illinois](https://extension.illinois.edu/blogs/farm-coach/2025-09-29-terminating-farm-lease-illinois)
- Illinois Extension, Farm Coach blog, "Farm Leasing Series: Cash-Rent Farm Lease Contract Tips for Landowners and Farmers," November 11, 2025: [extension.illinois.edu/blogs/farm-coach/2025-11-11-farm-leasing-series-cash-rent-farm-lease-contract-tips-landowners-and](https://extension.illinois.edu/blogs/farm-coach/2025-11-11-farm-leasing-series-cash-rent-farm-lease-contract-tips-landowners-and)
- Rincker Law, "Ask Ruth: How do you Terminate an Oral Farm Lease in Illinois?": [rinckerlaw.com/ask-ruth-how-do-you-terminate-an-oral-farm-lease-in-illinois](https://rinckerlaw.com/ask-ruth-how-do-you-terminate-an-oral-farm-lease-in-illinois/)
- ISPFMRA, *2025 Illinois Land Values Report* (released ~March 27, 2025): [ispfmra.org/download/2025-land-values-report](https://ispfmra.org/download/2025-land-values-report/)
- ISPFMRA, "Farmland Prices at Plateau?" April 1, 2026: [ispfmra.org/2026/04/01/farmland-prices-at-plateau](https://ispfmra.org/2026/04/01/farmland-prices-at-plateau/)
- J. Tsay and G. Schnitkey, "Illinois Cash Rents and Leasing Expectations Through 2027," *farmdoc daily* (16):63, April 13, 2026: [farmdocdaily.illinois.edu/2026/04/illinois-cash-rents-and-leasing-expectations-through-2027.html](https://farmdocdaily.illinois.edu/2026/04/illinois-cash-rents-and-leasing-expectations-through-2027.html)
- G. Schnitkey, "Cash Rent with Bonus Leasing Arrangement: Description and Example," *farmdoc daily*, September 2011: [farmdocdaily.illinois.edu/2011/09/cash-rent-with-bonus-leasing-a-1.html](https://farmdocdaily.illinois.edu/2011/09/cash-rent-with-bonus-leasing-a-1.html)
- farmdoc, "Cash Rent with Bonus Worksheet" (FAST tool): [farmdoc.illinois.edu/fast-tools/cash-rent-with-bonus-worksheet](https://farmdoc.illinois.edu/fast-tools/cash-rent-with-bonus-worksheet)
- N. Paulson, G. Schnitkey, C. Zulauf, "Revised Variable Cash Lease Parameters," *farmdoc daily* (15):179, September 30, 2025: [farmdocdaily.illinois.edu/2025/09/revised-variable-cash-lease-parameters.html](https://farmdocdaily.illinois.edu/2025/09/revised-variable-cash-lease-parameters.html)
- Farm Progress, "How to build a flexible cash-rent lease": [farmprogress.com/management/how-to-build-a-flexible-cash-rent-lease](https://www.farmprogress.com/management/how-to-build-a-flexible-cash-rent-lease)
- farmdoc, *Variable Cash Rent Lease Fact Sheet* (2017): [farmdoc.illinois.edu/assets/management/leasing-facts-prices/Variable_Cash_Rent_Lease_Fact_Sheet_2017.pdf](https://farmdoc.illinois.edu/assets/management/leasing-facts-prices/Variable_Cash_Rent_Lease_Fact_Sheet_2017.pdf)
- farmdoc, *Crop Share Lease Fact Sheet* (2017): [farmdoc.illinois.edu/assets/management/leasing-facts-prices/Crop_Share_Lease_Fact_Sheet_2017.pdf](https://farmdoc.illinois.edu/assets/management/leasing-facts-prices/Crop_Share_Lease_Fact_Sheet_2017.pdf)
- B. Zwilling, "Landowner's Adjusted Net-Share Rent as a Percent of Crop Returns," *farmdoc daily*, January 17, 2025: [farmdocdaily.illinois.edu/2025/01/landowners-adjusted-net-share-rent-as-a-percent-of-crop-returns.html](https://farmdocdaily.illinois.edu/2025/01/landowners-adjusted-net-share-rent-as-a-percent-of-crop-returns.html)
- Illinois Agriculture Authority, "Illinois Farmland Leasing and Rental" (secondary, corroborating source): [illinoisagricultureauthority.com/illinois-farmland-leasing-and-rental](https://illinoisagricultureauthority.com/illinois-farmland-leasing-and-rental/)
- University of Illinois farmdoc, *Machinery Cost Estimates: Field Operations*, 2025: [farmdoc.illinois.edu/assets/management/machinery-costs/field_operations_2025.pdf](https://farmdoc.illinois.edu/assets/management/machinery-costs/field_operations_2025.pdf)
- USDA NASS, *2025 Land Values & Cash Rents* (released August 1, 2025): [nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf](https://www.nass.usda.gov/Publications/Highlights/2025/2025LandValuesCashRents_FINAL.pdf)
- DTN, "Illinois Dominates Top 10 List of Highest County Cash Rents in Corn Belt," August 23, 2025: [dtnpf.com/agriculture/web/ag/news/business-inputs/article/2025/08/23/illinois-dominates-top-10-list-cash](https://www.dtnpf.com/agriculture/web/ag/news/business-inputs/article/2025/08/23/illinois-dominates-top-10-list-cash)
- Federal Reserve Bank of Chicago, *AgLetter*, "Midwest Farmland Values Ended 2025 with Solid Growth," February 2026: [chicagofed.org/publications/agletter/2025-2029/february-2026](https://www.chicagofed.org/publications/agletter/2025-2029/february-2026)
- University of Illinois farmdoc, *Agricultural Law* (model lease forms): [farmdoc.illinois.edu/agricultural-law](https://farmdoc.illinois.edu/agricultural-law)
- farmdoc daily, "Conservation Addendums for Illinois Farm Leases," September 26, 2019: [farmdocdaily.illinois.edu/2019/10/conservation-addendums-for-illinois-farm-leases.html](https://farmdocdaily.illinois.edu/2019/10/conservation-addendums-for-illinois-farm-leases.html)
- [../SOURCING.md](../SOURCING.md) — sourcing standards and build-environment disclosure (network egress was blocked for all primary-source domains at build time; all figures and statutory quotations above were corroborated via independent secondary-source cross-checks rather than direct primary-document fetches, per the verification pass)
- [../sources/MANIFEST.md](../sources/MANIFEST.md) — full source manifest with retrieval status

See also: [03-cash-rents.md](03-cash-rents.md), [07-ispfmra-benchmarks.md](07-ispfmra-benchmarks.md), [08-farmdoc-returns-and-tools.md](08-farmdoc-returns-and-tools.md), [glossary.md](glossary.md).
