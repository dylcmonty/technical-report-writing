# USDA SBIR Topic 8.6 Market Evidence Pack for Perishable Produce

## Scope and definitions

This evidence pack is tailored to a USDA SBIR Phase I proposal (Topic 8.6) and is restricted to **perishable, time-sensitive produce** (fresh vegetables, berries, fruit). It intentionally **excludes storable commodity grains and oilseeds** because the market dynamics (yields, logistics, shrink, and pricing) differ materially.

**Primary national sources used:** USDA National Agricultural Statistics Service Census of Agriculture typology tables, USDA Agricultural Marketing Service refrigerated-truck analysis (AgRTQ), USDA Economic Research Service food-loss documentation, Congressional Research Service produce-market sizing, U.S. Census Bureau population estimates, and Rockefeller Foundation true-cost accounting.

**Farm size ("small" vs "large") definition used in this pack (explicit and reproducible).** This follows the 2022 Census of Agriculture *Farm Typology* table structure:
- **Small family farms:** Gross Cash Farm Income (GCFI) **< $150,000** and **$150,000-$349,999**
- **Midsize family farms:** **$350,000-$999,999**
- **Large family farms:** **$1,000,000-$4,999,999** and **$5,000,000+**
- **Non-family farms:** separate category in the Census typology table

**"Local" definition (policy maximum vs practical service radius).**
- **USDA program "maximum" local definition (commonly used in federal procurement contexts):** a product marketed **<400 miles** from origin **or within the same State**.
- **Consumer perception benchmark (useful for website language):** In a national consumer survey (late 2008), **over 70%** of respondents considered a **50-mile radius "local."**
- For logistics calculations below, "local" is treated as **50-100 miles** as a *scenario*, and "conventional" as **1,000-1,500 miles** as a *scenario* (not asserted as a national average of "food miles").

**Key limitation.**
- The Census "vegetables" sales category used nationally is **"Vegetables, melons, potatoes, and sweet potatoes."** Potatoes/sweet potatoes are included by Census taxonomy and are not always "time-sensitive" in the same way as leafy greens/berries. This pack uses that category as a **best-available national proxy** for perishable produce at scale, and flags the limitation everywhere it matters.

## Common Claim Corrections

The section below lists common claims in local perishable-produce ventures and provides grounded replacements that fit the evidence gathered in this report.

- **Claim:** "Small/local farms produce most of our vegetables (or fresh produce)."
  **Status:** **Unsupported (nationally false for produce sales).** In Census typology, the two "small family farm" categories (<$350k GCFI) account for only **~4.1%** of U.S. *vegetable-group* sales dollars (vegetables+melons+potatoes+sweet potatoes).
  **Corrected claim (defensible):** "U.S. produce sales are highly concentrated: very large family farms and nonfamily farms account for the majority of national produce sales."

- **Claim:** "Small farms are more productive per acre than large farms (for fresh produce)."
  **Status:** **Not supported by this national Census proxy; direction is generally opposite in gross sales/acre for vegetables and berries.** Using Census typology, gross **sales per acre** for the vegetable group are higher for **very large family** and **nonfamily** farms than for small-family categories.
  **Corrected claim (defensible and precise):** "Using USDA Census farm-typology data, produce sales-per-acre are higher on very large and nonfamily operations for vegetables and berries; small farms are more numerous but sell a smaller share of total volume/value."

- **Claim:** "Local food means within 50 miles."
  **Status:** **Partially supported (consumer perception), but not a universal USDA definition.**
  **Corrected claim:** "USDA programs often use a maximum local definition of <400 miles or within-State, while many consumers perceive 'local' closer to ~50 miles."

- **Claim:** "Reefer trucking costs are about $X per mile."
  **Status:** **Supportable with a cited source and a specific freight context (spot produce lanes vs carrier operating cost).**
  **Corrected claim:** "USDA AMS AgRTQ reported Q2 2024 produce truck rates of **$6.45/mile (0-500 miles)** and **$2.81/mile (501-1,500 miles)** (selected routes), while ATRI reports an all-truck average operating cost of **$2.26/mile in 2024**."

- **Claim:** "Local sourcing cuts shipping cost by ~90%."
  **Status:** **Conditionally supportable** (depends on distance, rate band, and payload).
  **Corrected claim (parameterized):** "Using USDA AMS produce truck rates and a full-truck payload assumption, a 50-100 mile move can be ~0.8-1.6¢/lb, while 1,000-1,500 miles can be ~7.0-10.5¢/lb."

- **Claim:** "Food waste is 40% of food."
  **Status:** **Partially supported only with careful framing.** USDA ERS's loss-adjusted series estimates **31%** loss at retail+consumer levels (2010) and notes exclusion of farm-level losses.
  **Corrected claim:** "USDA ERS estimated that **31%** of the retail-level food supply went uneaten at the retail and consumer levels in 2010, excluding farm- and pre-retail losses."

- **Claim:** "Fresh produce has the highest waste rates."
  **Status:** **Supported for consumer-level loss shares and high retail shrink; quantify precisely.** In ERS's 2010 table, **fresh fruit total loss = 37%** and **fresh vegetables total loss = 34%**.
  **Corrected claim:** "In USDA ERS's 2010 estimates, total losses were **37% for fresh fruit** and **34% for fresh vegetables**, with most losses at the consumer level."

- **Claim:** "America's food is cheap only because we ignore hidden costs."
  **Status:** **Supportable with a credible true-cost framework and a clear statement of what is included and excluded.**
  **Corrected claim:** "A Rockefeller Foundation true-cost accounting analysis estimated the U.S. food system's 'true cost' at **>=$3.2T/year** versus **~$1.1T/year** in food expenditures, with **~$2.1T** in additional quantified external costs."

## Evidence tables

### Table of farm scale vs outcomes for produce proxies

**Interpretation guidance (important for reviewers):** This table shows **gross sales per acre** (a *value-per-acre* proxy), not physical yields. It is derived from national 2022 Census typology tables and is among the **best-available national size-segmented measures** for produce-like categories.

**Table 1: Farm scale vs outcomes (vegetable-group and berries)**
Sources: USDA NASS 2022 Census "Farm Typology" (sales + farm counts) and typology continuation pages (land in vegetables / land in berries). Calculated columns are shown again with step-by-step arithmetic in the next section.

**Vegetables proxy = "Vegetables, melons, potatoes, and sweet potatoes" sales; denominator = "Land in vegetables" acres.**

| Farm typology (GCFI) | Farms with veg sales (count) | Veg-group sales ($B) | Veg acres (M) | Veg sales per acre ($/acre) | Share of veg-group sales (%) |
|---|---:|---:|---:|---:|---:|
| Small family (GCFI < $150k) | 51,518 | 0.728 | 0.131 | 5,543 | 2.584 |
| Small family (GCFI $150k-$349.9k) | 4,412 | 0.422 | 0.088 | 4,828 | 1.498 |
| Midsize family (GCFI $350k-$999.9k) | 3,934 | 0.950 | 0.223 | 4,266 | 3.369 |
| Large family (GCFI $1M-$4.999M) | 4,016 | 4.445 | 0.850 | 5,231 | 15.765 |
| Very large family (GCFI >= $5M) | 1,407 | 14.705 | 1.772 | 8,301 | 52.159 |
| Nonfamily farms | 5,104 | 6.943 | 0.865 | 8,029 | 24.625 |
| Total | 70,391 | 28.194 | 3.928 | 7,178 | 100.000 |

**Berries proxy = "Berries" sales; denominator = "Land in berries" acres.**

| Farm typology (GCFI) | Farms with berry sales (count) | Berry sales ($B) | Berry acres (M) | Berry sales per acre ($/acre) | Share of berry sales (%) |
|---|---:|---:|---:|---:|---:|
| Small family (GCFI < $150k) | 24,704 | 0.310 | 0.058 | 5,317 | 4.693 |
| Small family (GCFI $150k-$349.9k) | 1,890 | 0.176 | 0.023 | 7,540 | 2.671 |
| Midsize family (GCFI $350k-$999.9k) | 1,586 | 0.416 | 0.045 | 9,346 | 6.304 |
| Large family (GCFI $1M-$4.999M) | 849 | 0.835 | 0.062 | 13,391 | 12.650 |
| Very large family (GCFI >= $5M) | 294 | 2.765 | 0.073 | 37,707 | 41.876 |
| Nonfamily farms | 1,885 | 2.100 | 0.095 | 22,111 | 31.807 |
| Total | 31,208 | 6.603 | 0.357 | 18,501 | 100.000 |

### Reefer transport cost evidence and conversions

**Important framing for reviewers:**  AgRTQ "truck rates" are **observed produce lane pricing (market rates)**, while  reports **fleet operating cost per mile** (carrier costs). These are related but not interchangeable (rates can be above or below costs depending on market conditions).

**Table 2: Reefer transport costs (rate -> $/lb-mile -> $/lb)**
Sources: AMS AgRTQ Q2 2024 national summary truck-rate table; ATRI operating-cost metric via TRID record abstract.
Assumption for conversion: **40,000 lb net payload** (user-adjustable; see sensitivity table and formulas). Rates are per mile; conversion is purely arithmetic.

| Source / series | Metric | Distance band | Rate ($/mile) | Implied ($/lb-mile) @40,000 lb | Implied cents/lb-mile |
|---|---|---|---:|---:|---:|
| USDA AMS AgRTQ (Q2 2024) | Produce truck **rate** | 0-500 miles | 6.45 | 0.000161 | 0.0161 |
| USDA AMS AgRTQ (Q2 2024) | Produce truck **rate** | 501-1,500 miles | 2.81 | 0.000070 | 0.0070 |
| USDA AMS AgRTQ (Q2 2024) | Produce truck **rate** | 1,501-2,500 miles | 2.48 | 0.000062 | 0.0062 |
| USDA AMS AgRTQ (Q2 2024) | Produce truck **rate** | 2,501+ miles | 1.63 | 0.000041 | 0.0041 |
| ATRI (2024 data) | Truck **operating cost** | All miles (avg) | 2.26 | 0.000057 | 0.0057 |

**Representative distance conversion (example "local" vs "conventional")** using AMS AgRTQ Q2 2024 rates and 40,000 lb payload.

| Scenario | Distance (mi) | Rate used | Cost per truckload ($) | Cost per lb ($/lb) | Cost per lb (cents) |
|---|---:|---|---:|---:|---:|
| Local (example) | 50 | 0-500 rate ($6.45/mi) | 322.50 | 0.00806 | 0.806 |
| Local (example) | 100 | 0-500 rate ($6.45/mi) | 645.00 | 0.01613 | 1.613 |
| Conventional (example) | 1,000 | 501-1,500 rate ($2.81/mi) | 2,810.00 | 0.07025 | 7.025 |
| Conventional (example) | 1,500 | 501-1,500 rate ($2.81/mi) | 4,215.00 | 0.10538 | 10.538 |

**Sensitivity to payload (illustrative; based on alternate net-payload assumptions).** Using the same AMS rates above.

| Distance (mi) | Rate ($/mile) | Cost (cents/lb) @30,000 lb | @40,000 lb | @45,000 lb |
|---:|---:|---:|---:|---:|
| 50 | 6.45 | 1.075 | 0.806 | 0.717 |
| 100 | 6.45 | 2.150 | 1.613 | 1.433 |
| 1,000 | 2.81 | 9.367 | 7.025 | 6.244 |
| 1,500 | 2.81 | 14.050 | 10.538 | 9.367 |

### Produce waste and shrink evidence

**Table 3: Waste/shrink (supply chain + on-farm field loss evidence)**
Core USDA food-loss benchmark (2010): ERS Loss-Adjusted Food Availability (LAFA) table for retail and consumer losses by commodity group.
Retail shrink detail: ERS Food Availability System "Food Loss" page (2016 retail shrink volumes and ranges for fresh produce).
On-farm: field measurement study of NC vegetable farms (unharvested/unused produce volumes).

| Stage / metric | Fresh fruit | Fresh vegetables | Notes |
|---|---:|---:|---|
| **2010 total loss (% of retail-level supply)** | 37% | 34% | ERS table: combines retail + consumer loss.  |
| **2010 retail loss (%)** | 12% | 10% | ERS table.  |
| **2010 consumer loss (%)** | 25% | 24% | ERS table; consumer dominates.  |
| **2010 supply (billion lb at retail level)** | 37.6 | 53.5 | ERS table.  |
| **2010 total loss (billion lb)** | 13.9 | 18.0 | ERS table.  |
| **Retail shrink range (fresh fruit items, 2011-12 store data applied to 2016 quantities)** | 4.1%-43.1% | - | Range across 24 fresh fruits (bananas low, papayas high).  |
| **Retail shrink average (fresh vegetables; 2011-12 store data applied to 2016 quantities)** | - | 11.6% average | Average across 31 fresh vegetables.  |
| **Retail shrink volume in 2016 (supermarket loss)** | 6.7B lb (24 fruits) | 6.2B lb (31 vegetables) | ERS store-loss totals.  |
| **On-farm unharvested/unused produce (field measurement, NC vegetables, 2017)** | - | 5,114.59 kg/ha | Grand mean of produce left unharvested.  |
| **On-farm unutilized share (NC vegetables, 2017)** | - | 42% of marketed yield | "Available, unutilized produce averaged 42% of North Carolina marketed yields."  |

**USDA's national value-of-loss benchmark (often cited in proposals):** ERS estimated total food loss at retail + consumer levels in 2010 at **~133B lb (31%)** and **$161.6B** (retail value), explicitly excluding farm-level and farm-to-retail losses.

### Health and environmental externality estimates

**Table 4: "True cost" externality estimates (U.S.-specific, with scope statements)**
Primary source:  True Cost of Food framework (2021).

| Estimate | Value | Scope and what is/isn't included |
|---|---:|---|
| Current annual food expenditure | ~$1.1T/year | Report's "current expenditure on food" baseline.  |
| Additional quantified external costs | ~$2.1T/year | Sum of quantified metrics across five impact areas.  |
| True cost of food (lower bound) | **>=$3.2T/year** | Report frames as "at least" $3.2T and notes it is not exhaustive.  |
| Quantified human health costs | $1,145B/year | Subcomponents shown (e.g., other NCDs 604, obesity/overweight 359, food insecurity 146, pollution impacts 36).  |
| Quantified environment costs | $350B/year | Subcomponents shown (GHG 223, water use 60, soil erosion 67).  |
| Quantified biodiversity costs | $455B/year | Subcomponents shown (land use 342, pollution 110).  |
| Quantified livelihoods costs | $134B/year | Subcomponents shown (lack of benefits 76, underpayment 33, occupational health/safety 24, child labor 1).  |
| Quantified economy costs | $21B/year | Subcomponent shown (subsidies 21).  |

**Scope caveat:** The report's U.S. food system cost analysis includes production through consumption stages but states it **does not include food service and hospitality in cost analyses**.

## Reproducible calculations

### Reproducible calculations

All arithmetic below is computed directly from the cited sources.

**Calculation set for productivity proxy: sales per acre by farm typology**

1) **Vegetable-group sales per acre for "very large family farms (GCFI >= $5M)"**
Inputs from Census typology:
- Vegetable-group sales = **14,705,441** ($1,000) = **$14,705,441,000**
- Vegetable acres ("land in vegetables") = **1,771,631 acres**

Formula:
Sales per acre = (Sales dollars) / (Acres)

Arithmetic:
$14,705,441,000 / 1,771,631 = **$8,300.51 per acre**

2) **Vegetable-group sales per acre for "small family farms (GCFI < $150k)"**
Inputs:
- Sales = **728,484** ($1,000) = **$728,484,000**
- Acres = **131,417 acres**

Arithmetic:
$728,484,000 / 131,417 = **$5,543.30 per acre**

3) **Berries sales per acre for "nonfamily farms"**
Inputs:
- Berry sales = **2,100,211** ($1,000) = **$2,100,211,000**
- Berry acres ("land in berries") = **94,984 acres**

Arithmetic:
$2,100,211,000 / 94,984 = **$22,111.21 per acre**

**Calculation set for shipping overhead: $/lb from $/mile**

4) **Cost per lb for a 1,000-mile shipment (conventional scenario)**
Inputs:
- Rate = **$2.81/mile** (AMS AgRTQ, Q2 2024, 501-1,500 miles band)
- Distance = **1,000 miles** (scenario assumption)
- Payload = **40,000 lb** (scenario assumption; adjust)

Formula:
Cost per lb = (Rate $/mile x Distance miles) / Payload lb

Arithmetic:
($2.81 x 1,000) / 40,000 = $2,810 / 40,000 = **$0.07025/lb = 7.025¢/lb**

5) **Cost per lb for a 50-mile shipment (local scenario)**
Inputs:
- Rate = **$6.45/mile** (AMS AgRTQ, Q2 2024, 0-500 miles band)
- Distance = **50 miles** (scenario assumption)
- Payload = **40,000 lb** (scenario assumption)

Arithmetic:
($6.45 x 50) / 40,000 = $322.50 / 40,000 = **$0.00806/lb = 0.806¢/lb**

6) **Implied $/lb-mile** (useful for sensitivity and for proposal clarity)
Formula:
$/lb-mile = ($/mile) / (payload lb)

Example (0-500 band):
$6.45 / 40,000 = **$0.00016125 per lb-mile**

**Calculation set for market sizing: population x per-capita produce spending**

7) **U.S. per-capita produce consumer sales (range)**
Inputs:
- U.S. consumer sales of fruit+vegetable products estimated at **$160B-$190B annually** (CRS estimate).
- U.S. population (July 1, 2024) = **340.1 million** from U.S. Census Bureau population estimates.

Per-capita (low) = $160,000,000,000 / 340,100,000 = **$470.45/person/year**
Per-capita (high) = $190,000,000,000 / 340,100,000 = **$558.66/person/year**

8) **Ohio produce-market proxy (consumer sales)**
Inputs:
- Ohio population (July 1, 2024) = **11,883,304**.
- Per-capita range from step 7.

Low: 11,883,304 x $470.45 = **$5.59B/year**
High: 11,883,304 x $558.66 = **$6.64B/year**

9) **Summit County proxy (consumer sales)**
Inputs:
- Summit County population (July 1, 2024) = **538,370**.

Low: 538,370 x $470.45 = **$253.3M/year**
High: 538,370 x $558.66 = **$300.8M/year**

## Summary Findings

The sentences below condense the main numerical findings into short, reusable statements.

- In 2022, very large family farms (GCFI >=$5M) generated **52.2%** of U.S. vegetable-group sales.
- Small family farms (GCFI <$350k) generated **4.1%** of U.S. vegetable-group sales in 2022.
- In 2022, U.S. vegetable-group sales totaled **$28.2B** (vegetables, melons, potatoes, sweet potatoes).
- USDA ERS estimates fresh fruit losses totaled **37%** in 2010 (12% retail, 25% consumer).
- USDA ERS estimates fresh vegetable losses totaled **34%** in 2010 (10% retail, 24% consumer).
- AMS AgRTQ reported Q2 2024 produce truck rates of **$6.45/mile (0-500 mi)** and **$2.81/mile (501-1,500 mi)**.
- Using AMS Q2 2024 rates and a 40,000-lb payload, 1,000 miles implies **~7.0¢/lb** in linehaul trucking cost.
- ERS estimates **133B lb (31%)** of the 2010 food supply went uneaten at retail and consumer levels, excluding farm-level losses.
- A consumer survey found **82%** of respondents had bought locally grown fresh produce; **over 70%** considered food grown within 50 miles "local."
- A true-cost accounting analysis estimated the U.S. food system's "true cost" at **>=$3.2T/year** versus **~$1.1T/year** in expenditures.

## Limitations

**Why these are "best available" and not perfect.** National data rarely report *physical yields by farm size* for "fresh vegetables/berries/fruit" as a single category. The 2022 Census farm typology is one of the few national sources that **jointly** provides:
- consistent, national farm-size segmentation (by GCFI),
- commodity-group sales values,
- and crop land-use measures (e.g., land in vegetables; land in berries).

**How to present the productivity story credibly (and reviewer-proof).**
- Use "**sales per acre**" (gross value per acre) rather than "yield," unless a commodity-specific yield dataset is added later.
- Explicitly call the vegetable category a **proxy** and note it includes potatoes/sweet potatoes.
- Emphasize that the innovation targets **time-sensitivity and shrink**, where value is lost even when production is high; align this with the ERS finding that consumer-level loss is large for fresh produce.

**How to position logistics cost without overclaiming.**
- It is defensible to say that trucking adds **single-digit cents per pound locally** and **high single- to low double-digit cents per pound for cross-country distances**, *given explicit assumptions*.
- Note that these are **linehaul rate conversions** and exclude additional real-world costs (multi-stop routing, detention, rejected loads, temperature excursions, empty backhaul, and related factors).

**How to position the "waste problem" without mixing incompatible scopes.**
- Use ERS LAFA for a headline national benchmark (31% across all foods; 34-37% for fresh produce groups).
- Use field-measured on-farm evidence (e.g., 42% of marketed yields in NC vegetable fields) as **contextual evidence** that farm-level loss can be substantial and often missing from national accounting.
- Clearly state that the ERS 2010 national totals exclude farm-level and pre-retail losses.

**How to use "true cost" in SBIR without triggering reviewer skepticism.**
- Lead with the **scope statement** ("does not include food service/hospitality in cost analyses") and that it is a **lower bound** ("at least $3.2T").
- Present the quantified domains (health, environment, biodiversity, and livelihoods) as **externalities context** and keep the core grant logic anchored in measurable Phase I outcomes (reduced shrink, reduced miles, reduced handling time, improved cold-chain reliability).

## References
- USDA National Agricultural Statistics Service. *2022 Census of Agriculture: Farm Typology* and continuation tables for land in vegetables and berries.
- USDA Agricultural Marketing Service. *Agricultural Refrigerated Truck Quarterly*, Quarter 2, 2024.
- USDA Economic Research Service. *Loss-Adjusted Food Availability Documentation* and *Food Loss* data pages.
- Congressional Research Service. *Marketing and Pricing in the U.S. Fruit and Vegetable Industry*.
- U.S. Census Bureau. 2024 national and local population estimates.
- Rockefeller Foundation. *True Cost of Food* (2021).
