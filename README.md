# Medicare GLP-1 Competitive Landscape: Novo Nordisk vs Eli Lilly (2022–2023)

**Self-initiated consulting case study | Data Analytics Portfolio Project**  
**Author:** Aditi Ghosh | Data Analyst, Zifo Technologies  
**Contact:** ghoshaditi58@gmail.com | [LinkedIn](https://linkedin.com/in/aditi-ghosh03/)

---

## Project Summary

This project investigates the competitive dynamics between Novo Nordisk and Eli Lilly in the Medicare GLP-1 diabetes drug market using publicly available CMS Medicare Part D data (2022–2023).

The analysis was designed to simulate a real-world consulting engagement: starting from a business question, building a segmentation framework, pressure-testing hypotheses, and delivering a data-driven strategic recommendation.

> **The surface story:** Novo Nordisk gained 8.1 percentage points of market share in 2023.  
> **The real story:** That gain came from Eli Lilly's Trulicity collapsing — not from Novo winning against Mounjaro. In the high-value prescriber segment, the battle is nearly even.

---

## Business Question

> *"Novo Nordisk appears to be winning the GLP-1 market in 2023. Is this gain real, sustainable, and uniformly distributed — or is something more nuanced happening beneath the headline numbers?"*

---

## Data Source

| Field | Detail |
|---|---|
| **Source** | CMS Medicare Part D Prescribers by Provider and Drug |
| **URL** | [data.cms.gov](https://data.cms.gov/provider-summary-by-type-of-service/medicare-part-d-prescribers/medicare-part-d-prescribers-by-provider-and-drug) |
| **Years** | 2022 (187,475 rows) and 2023 (315,333 rows) |
| **Scope** | Diabetes indication only (Medicare Part D does not reimburse obesity-indication GLP-1) |
| **Brands analyzed** | Ozempic, Rybelsus (Novo Nordisk) and Trulicity, Mounjaro (Eli Lilly) |
| **Unique prescribers** | 169,404 in 2023 |
| **Total prescriptions** | 44.5 million in 2023 |

> **Note:** Raw CMS files are not included in this repository due to file size. Download directly from the CMS link above. All processed/export files used for analysis and visualization are in `data/processed/` and `data/dashboard_exports/`.

---

## Key Findings

### Finding 1 — The Brand Share Shift

| Brand | Company | 2022 Share | 2023 Share | Change |
|---|---|---|---|---|
| Ozempic | Novo Nordisk | 38.9% | 47.4% | **+8.5pp** |
| Rybelsus | Novo Nordisk | 6.0% | 5.6% | -0.4pp |
| Trulicity | Eli Lilly | 54.6% | 35.8% | **-18.8pp** |
| Mounjaro | Eli Lilly | 0.5% | 11.2% | **+10.7pp** |

- **Trulicity collapsed 18.8pp in one year.** Mounjaro absorbed more of that collapse (+10.7pp) than Ozempic did (+8.5pp).
- **Mounjaro grew 21x in prescriber count** — from 2,034 to 44,382 unique prescribers.
- **Novo's company share:** 44.9% → 53.0% (+8.1pp)
- **Lilly's company share:** 55.1% → 47.0% (-8.1pp)

### Finding 2 — Volume-Based Segmentation (Decile Framework)

Prescribers were ranked by annual GLP-1 prescription volume and divided into 10 groups (deciles). The top 10% — **Decile 10** — write **42% of all prescriptions**.

| Segment | Prescribers | % of Volume | Novo 2022 | Novo 2023 | Change |
|---|---|---|---|---|---|
| Low (D1-3) | ~51,000 | 6% | 47% | 55% | +8pp |
| Mid (D4-7) | ~68,000 | 52% | 45% | 53% | +8pp |
| **High (D8-10)** | **~17,000** | **42%** | **42%** | **51%** | **+9pp** |

**Critical finding:** In Decile 10, Novo's lead is only **2 percentage points** (51% vs 49%). In 2022, Lilly led here. This is the most contested and commercially significant segment.

**Hypothesis tested and rejected:** The initial hypothesis was that endocrinologists — being more evidence-driven — would disproportionately choose Mounjaro based on clinical data. This was **rejected by the data**: all five specialties (Internal Medicine, Family Practice, NP, PA, Endocrinology) show nearly identical Novo/Lilly competitive splits at D10 (range: 49.8–52.4%). Volume, not specialty, determines behavior.

### Finding 3 — Geographic Concentration

Mounjaro's high-volume expansion is **not a national pattern** — it is concentrated in the Southern US.

| State | Mounjaro YoY Growth (D10) |
|---|---|
| Alabama | +23.7pp |
| Louisiana | +21.8pp |
| Arkansas | +18.8pp |
| Indiana | +18.3pp |
| Georgia | +18.0pp |
| Kentucky | +17.8pp |
| Oklahoma | +17.2pp |
| South Carolina | +17.1pp |
| Tennessee | +15.4pp |
| Texas | +15.0pp |

8 of the top 10 fastest-growing Mounjaro states are in the Southern US. Massachusetts, by contrast, saw only **+7.9pp** — approximately 3x slower than Alabama.

**Novo's strongest state:** North Carolina (58.9% D10 share)  
**Novo's weakest state:** Massachusetts (33.7% D10 share)

---

## Strategic Recommendation

### Three-Tier Geographic Defense Framework

| Tier | States | Commercial Action | Data Rationale |
|---|---|---|---|
| **1 — Stronghold Defense** | TX, CA, NY, FL | 12-15 rep visits/yr on D10 prescribers. KOL programs. CV outcomes positioning (SELECT trial). | ~25% of national D10 volume. Novo currently leads. Protect margin. |
| **2 — Southern Battleground** | AL, LA, TN, GA, IN, KY, OK, SC, AR | Aggressive rep coverage matching Lilly intensity. Head-to-head clinical positioning. RWE generation. | Mounjaro YoY +17.5pp avg vs +13.4pp national. Active fight zone. |
| **3 — Withdrawn / Lost** | MA, OH, MI | Maintain minimum coverage. Redirect resources to Tiers 1 & 2. | Lilly leads by 14+pp. Recovery cost outweighs expected gain. |

### Illustrative Financial Scenario

> ⚠️ **Disclosure:** The figures below are scenario-based estimates using industry benchmarks layered on CMS data findings. They are not predictions and are not derived directly from CMS data. Market size, growth decay assumptions, and recovery rates are industry estimates.

| Component | Value | Basis |
|---|---|---|
| Market size | ~$18.3B | Industry estimate: 44.5M scripts × ~$411 avg net price |
| D10 revenue exposure | ~$7.7B | **Data-derived:** $18.3B × 42% (D10 volume share) |
| Revenue at risk (3yr) | ~$1.6B | Assumes Mounjaro growth halves from 2023 pace |
| Defensive investment | ~$200M | Industry benchmark: low end of pharma defensive campaign range |
| Expected recovery | ~$960M | $1.6B × 60% (mid-range defensive benchmark) |
| Estimated ROI | ~5x | $960M ÷ $200M |

ROI remains positive across 50–70% recovery scenarios (3.2x–5.6x).

---

## Methodology

### Analytical Framework

1. **Decile Construction:** Ranked all 169,404 prescribers by total annual GLP-1 prescription volume. Segmented into 10 equal groups.
2. **Multi-Cut Analysis:** Analyzed competitive dynamics across 5 dimensions: brand level, company level, specialty × decile, prescriber transitions, and geographic state-level.
3. **Hypothesis Testing:** Generated 3 candidate hypotheses. Tested each against the data. Retained what survived. Discarded what didn't.

### Hypotheses Tested

| Hypothesis | Verdict | Evidence |
|---|---|---|
| Clinical evidence drives endocrinologists to disproportionately choose Mounjaro | **REJECTED** | All 5 specialties show nearly identical Novo/Lilly split at D10 (2.6pp range) |
| Rep coverage intensity explains the volume-driven pattern | **UNRESOLVED** | Sales force allocation data not in CMS — cannot be tested |
| Mounjaro's D10 expansion is geographically concentrated in Southern states | **CONFIRMED** | 8 of top 10 growth states are Southern; 3x faster than coastal academic states |

---

## Repository Structure

```
glp1-rx-share-analysis/
│
├── README.md                          ← This file
│
├── data/
│   ├── processed/                     ← Cleaned data files used for analysis
│   │   ├── brand_year_share.csv
│   │   ├── company_year_share.csv
│   │   ├── share_by_specialty_year.csv
│   │   ├── share_by_decile_year.csv
│   │   ├── specialty_growth.csv
│   │   └── kpi_metrics.csv
│   │
│   └── dashboard_exports/             ← All CSVs feeding Power BI dashboard
│       ├── brand_by_group_both.csv
│       ├── decile10_composition.csv
│       ├── heatmap_grouped.csv
│       ├── high_decile_composition.csv
│       ├── novo_lilly_by_decile.csv
│       ├── share_by_group.csv
│       ├── specialty_yoy_change.csv
│       ├── state_brand_share.csv
│       ├── state_tier_summary.csv
│       ├── tier_distribution.csv
│       ├── top10_mounjaro_growth.csv
│       └── trulicity_flow.csv
│
├── notebooks/
│   └── glp1_analysis.ipynb            ← Full analysis notebook (EDA → findings)
│
├── reports/
│   ├── GLP1_Competitive_Analysis_Novo_vs_Lilly.pptx   ← 10-slide consulting deck
│   ├── GLP1_Competitive_Analysis_Novo_vs_Lilly.pdf    ← PDF export for easy viewing
│   └── candidate_findings.md          ← Strategic findings document
│ 
│ 
├── Pressure_test.md
│ 
│ 
└── .gitignore
```

---

## Tools Used

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data cleaning, EDA, decile construction, geographic analysis |
| Jupyter Notebook | Exploratory analysis and hypothesis testing |
| Power BI Desktop | Interactive dashboard (3 views: Overview, Specialty × Decile, Geographic) |
| PptxGenJS | Programmatic PowerPoint deck generation |

---

## Dashboard

The interactive Power BI dashboard covers three analytical views:

**View 1 — Overview**
Brand share 2022 vs 2023, company-level comparison, Trulicity flow visualization, KPI cards (Novo 53.0%, Lilly 47.0%, Mounjaro +10.7pp)

**View 2 — Specialty × Decile**
Share by decile group for both companies across both years, D10 composition by specialty, specialty prescriber growth rates

**View 3 — Geographic Tier Analysis**
Top 10 Mounjaro growth states, tier distribution by volume, state-level competitive position

> 

---

## Limitations & Data Scope

| Limitation | Impact |
|---|---|
| **Diabetes indication only** | GLP-1 obesity market (Wegovy, Zepbound) is not captured |
| **Medicare Part D only** | Private insurance prescribing patterns not included |
| **2023 is most recent public data** | CMS releases with 18-month lag; 2024 data not yet available |
| **Sales force data unavailable** | Rep coverage hypothesis cannot be directly tested |
| **Financial projections are illustrative** | Market size and recovery rates are industry benchmarks, not measured |

---

## About This Project

This case study was self-initiated to demonstrate consulting-grade analytical thinking applied to a real pharma competitive intelligence problem. It uses the same publicly available data source that IQVIA, ZS Associates, and other pharma analytics firms use for benchmarking.

The analytical approach follows a hypothesis-driven consulting methodology:
- Define the business question
- Build a segmentation framework (decile-based)
- Generate and test hypotheses
- Pressure-test findings before accepting them
- Translate findings into a strategic recommendation
- Be transparent about what is measured vs. estimated

---

## Author

**Aditi Ghosh**  
Data Analyst | Zifo Technologies Private Limited, Chennai  
B.Tech Biotechnology, Heritage Institute of Technology, Kolkata (DGPA: 9.36/10)  

📧 ghoshaditi58@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/aditi-ghosh03/)  
💻 [GitHub](https://github.com/Aditi-Portfolio)

---

*Data: CMS Medicare Part D 2022–2023 (public domain). Analysis conducted as a self-initiated portfolio project.*
