# Project Scoping Memo
## Rx Share Dynamics in Medicare Diabetes GLP-1s: Novo vs Lilly

**Author:** Aditi Ghosh
**Date:** [27/04/2026]
**Engagement type:** Self-initiated case study (simulated client: Novo Nordisk Commercial Leadership)

---

### Business question
In the Medicare Part D diabetes segment — Novo Nordisk's commercial stronghold — is Eli Lilly's Mounjaro taking prescribing share from Ozempic, and what targeted commercial response should Novo deploy?

### Hypothesis
Between 2022 and 2023, Mounjaro's share gains in Medicare diabetes GLP-1 prescribing came primarily from Ozempic, not from Trulicity — meaning Lilly's Mounjaro launch is genuinely shifting market share away from Novo rather than cannibalizing Lilly's own older diabetes franchise.

### Method
- **Year-over-year share-shift analysis:** Compares 2022 vs 2023 brand-level market shares across all four diabetes-indicated GLP-1 brands (Ozempic, Mounjaro, Trulicity, Rybelsus). Identifies the brand(s) that lost the share Mounjaro gained — this directly tests the hypothesis.
- **Decile and specialty diagnostics:** Applies a ZS-style decile framework (rank 169K prescribers by total GLP-1 volume, segment into deciles) and cross-cut by specialty (top 5 specialties capture 96% of volume) to reveal whether share movements are clinically driven (endocrinology, top decile) or coverage-driven (primary care, mid-deciles) — which determines the right commercial lever.
- **Geographic concentration analysis:** Examines state-level share dynamics, focusing on the top 10 states (which account for ~80% of national volume), to identify where Novo's field-force response should be concentrated and where regional patterns diverge from national averages.

### Scope in
- Medicare Part D Prescribers by Provider and Drug, years 2022 and 2023
- Four commercially active diabetes GLP-1 brands: Ozempic, Mounjaro, Trulicity, Rybelsus
- NPI-level analysis aggregated by brand, specialty, state, and prescribing decile
- Diagnosis of share dynamics + targeted, segment-specific commercial recommendations

### Scope out (with rationale)
- **Obesity-indicated GLP-1 prescribing (Wegovy, Zepbound):** Excluded because Medicare Part D does not reimburse obesity drugs. The obesity segment is strategically critical and is flagged as a Phase 2 study requiring commercial claims data (e.g., IQVIA Xponent).
- **Commercial payer behavior:** Excluded — not available in public datasets. Findings will reflect Medicare dynamics specifically, which represent ~30% of total US GLP-1 volume.
- **Patient-level analysis** (adherence, persistence, switching at patient level): Excluded — Medicare prescriber-drug data does not link to longitudinal patient records.
- **Pricing and rebate strategy:** Cost-per-claim is roughly equivalent across the four brands ($1,290–$1,500), confirming pricing is not the primary competitive lever in this segment. Recommendations will focus on field force, clinical positioning, and prescriber engagement rather than payer contracting.

### Expected output
1. **10-slide strategy deck** (PDF + PPTX): executive summary, market context, methodology, three findings slides, driver analysis, segment-specific recommendations, risk and limitations, proposed Phase 2.
2. **Interactive Power BI dashboard:** specialty × decile × geography views with brand-share filters and 2022→2023 share-shift visualizations.
3. **Technical appendix:** Jupyter notebook published to GitHub with full reproducibility — data preparation, decile computation, share-shift methodology.
4. **3-minute Loom walkthrough** of headline findings for portfolio and recruiter use.

### Key methodological caveats (will appear in the deck)
- Medicare Part D captures ~30% of total US GLP-1 volume; findings are directionally indicative of the diabetes segment but should not be extrapolated to commercial payers without additional data.
- CMS suppresses prescriber-drug records with ≤10 unique patients for privacy; this primarily affects low-volume prescribers and biases low-decile analysis.
- The dataset cannot disaggregate diabetes-indicated prescribing from off-label use; specialty mix (96% concentrated in standard diabetes-managing specialties) supports the diabetes-indication assumption empirically.
- 2022 vs 2023 is a single-year comparison; multi-year trajectory would strengthen confidence in directional findings.