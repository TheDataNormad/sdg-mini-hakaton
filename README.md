# Nigeria Youth Unemployment & SDG 8: A Data-Driven Look at "Decent Work"

**Author:** Benedict Chidiebere
[GitHub](https://github.com/TheDataNormad) · [LinkedIn](https://linkedin.com/in/benedict-chidiebere)

## Overview

This project investigates whether Nigeria's falling youth unemployment rate represents real progress toward **UN Sustainable Development Goal 8 (Decent Work and Economic Growth)** — or whether it masks a deeper problem of poor job quality, informality, and a mismatch between education and formal employment.

Using Python, SQL, Power BI, and Google Sheets, this project moves from raw government survey data to a defensible, business-relevant set of findings and recommendations.

## Business Question

> Is Nigeria's falling youth unemployment rate real progress toward SDG 8, or a measurement artifact masking poor job quality? Who is most affected, and where is the problem heading?

## Data Sources

| Source | What it provides | Link |
|---|---|---|
| World Bank Open Data | Nigeria youth unemployment (modeled ILO estimate), 1991-2025 | data.worldbank.org, indicator `SL.UEM.1524.ZS` |
| Nigeria National Bureau of Statistics (NBS) | Quarterly Labour Force Survey reports — unemployment, underemployment, informality, NEET, by sex/education/age/region | nigerianstat.gov.ng/elibrary |

## Key Findings

1. **The 2022 drop in unemployment is a measurement artifact, not an economic improvement.** NBS adopted the ILO's 19th ICLS survey standard in Q4 2022, redefining "employed" as 1+ hour of paid work per week. Pre- and post-2022 figures are not directly comparable.
2. **The headline unemployment rate hides poor job quality.** ~93% of employed Nigerians work informally, and youth underemployment remains high — a low unemployment rate does not mean people have stable, decent jobs.
3. **More education is associated with *higher* youth unemployment, not lower** (5.0% for no education vs. 18.3% for post-secondary). Informal work absorbs the uneducated; educated youth queue for scarce formal-sector jobs.
4. *(Forecast finding — to be finalized based on model fit quality.)*

## Methodology

1. **Data acquisition:** Downloaded World Bank CSV and NBS quarterly PDF reports; manually transcribed key aggregate tables from NBS Annex sections.
2. **Cleaning & reshaping (Python/pandas):** Converted wide-format World Bank data to long format; built a clean quarterly series from NBS reports.
3. **Structural break analysis:** Identified and visually separated the pre-/post-2022 methodology change rather than treating the series as continuous.
4. **Segmentation:** Analyzed youth unemployment, NEET, and informality by education level to identify who is most affected.
5. **Forecasting:** Fit a linear regression on the post-2022 quarterly series; evaluated fit quality (R²) before drawing conclusions, to avoid overstating forecast confidence.
6. **Storage (SQL):** [To be added — quarterly indicators stored in a relational database for querying.]
7. **Dashboard (Power BI):** [To be added — interactive dashboard for exploring findings by education, region, and time period.]

## Tools Used

`Python` (pandas, matplotlib, scikit-learn) · `SQL` · `Power BI` · `Google Sheets`

## Repository Structure

```
├── data/                   # Raw and cleaned data files
├── notebooks/               # Jupyter notebooks (exploration, cleaning, analysis, forecasting)
├── sql/                     # Database schema and queries
├── dashboard/                # Power BI file and exported visuals
├── README.md
```

## Related Writing

- [SDG 8 and the Nigerian Economy](#) — introductory article on Medium *(add your Medium link)*

## Status

🚧 In progress — data cleaning and initial analysis complete; forecasting, SQL storage, and Power BI dashboard in development.

## Next Steps

- [ ] Finalize forecast interpretation based on model fit
- [ ] Build SQL database of quarterly indicators
- [ ] Build Power BI dashboard
- [ ] Publish full findings write-up (Part 2 of the article series)
