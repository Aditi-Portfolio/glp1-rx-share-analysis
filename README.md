# Rx Share Dynamics in Medicare Diabetes GLP-1s

Self-initiated case study analyzing prescribing share dynamics between Novo Nordisk and Eli Lilly in the Medicare Part D diabetes GLP-1 segment, 2022–2023.

## Project context

The GLP-1 category has been transformed by the launch of Eli Lilly's Mounjaro in 2022, which has rapidly captured share in the diabetes market historically dominated by Novo Nordisk's Ozempic. This analysis uses public Medicare Part D claims data to diagnose where Novo is losing share, why, and what commercial response is warranted.

## Data source

This project uses the Medicare Part D Prescribers by Provider and Drug dataset, available free from CMS:

https://data.cms.gov/provider-summary-by-type-of-service/medicare-part-d-prescribers/medicare-part-d-prescribers-by-provider-and-drug

Filters applied: Years 2022 and 2023; Brand names Ozempic, Mounjaro, Trulicity, Rybelsus.

Filtered exports yield ~315K rows per year. Save them locally as `data/glp1_medicare_2022.csv` and `data/glp1_medicare_2023.csv` (this folder is gitignored).

## Repo structure

- `scoping_memo.md` — project scoping document
- `notebooks/` — Jupyter notebooks
- `data/` — local only, not committed

## Status

In progress. Week 1 (scoping + EDA) complete. Decile and share-shift analysis underway.

## Author

Aditi Ghosh — [LinkedIn](https://linkedin.com/in/aditi-ghosh03/)