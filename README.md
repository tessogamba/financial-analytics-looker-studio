# Financial Analytics Dashboard: Data Studio, formerly Looker Studio

An interactive financial analytics dashboard built with **Looker Studio**, visualising financial statement data for 12 public companies from 2009 to 2023. Data sourced from the [financial-analytics-bigquery](https://github.com/tessogamba/financial-analytics-bigquery) project.

## Live Dashboard

[View Dashboard on Looker Studio](https://datastudio.google.com/s/iOk5aX6aaVQ)

## Dashboard Preview

<img width="2242" height="1310" alt="Screenshot 2026-06-06 at 16 45 26" src="https://github.com/user-attachments/assets/6ede1d09-6e15-4eaf-85cd-76a9bed7e671" />

## What the Dashboard Shows

Five interactive visualisations answering key investor questions:

1. **Compound Annual Growth Rate (CAGR) by Company**: which companies grew fastest over the full period, ranked highest to lowest
2. **Average Net Profit Margin by Company**: which companies are most profitable, comparing average margins across all years
3. **Year-on-Year Revenue Growth (%)**: how revenue growth fluctuated year by year for the top 5 companies (AMZN, AAPL, GOOG, MSFT, NVDA)
4. **Absolute Revenue Growth 2009–2023**: total revenue gained or lost per company in raw dollar terms
5. **Financial Risk Indicators**: liquidity and leverage risk categorisation per company per year using current ratio and debt/equity ratio

## Data Source

Raw dataset: [Financial Statements of Major Companies (2009–2023)](https://www.kaggle.com/datasets/rish59/financial-statements-of-major-companies2009-2023), sourced from Kaggle. Transformed using BigQuery SQL and visualised in Looker Studio.

| View | Description | Rows |
|------|-------------|------|
| `cagr_analysis` | Compound annual growth rate per company | 12 |
| `avg_profitability_margins` | Average net profit margin per company | 12 |
| `yoy_growth` | Year-on-year revenue growth per company per year | 161 |
| `company_revenue_growth` | Absolute revenue growth first vs last year | 12 |
| `financial_risk` | Liquidity and leverage risk indicators per company per year | 161 |

## Key Insights

- Amazon recorded the highest CAGR at 26%, growing from $24.5B to $514B in revenue
- Google and Apple followed at 21% and 19% CAGR, respectively
- MSFT led on average net profit margin at 27%, followed by GOOG at 23%
- Sears (SHLDQ) and AIG posted negative CAGRs of -11% and -2%, consistent with Sears' 2018 bankruptcy
- Apple flagged as a liquidity risk in recent years (current ratio below 1)
- Tech sector compounded aggressively while traditional sectors (retail, insurance, banking) stagnated or declined

## Dashboard Features

- **Company filter** - select one or multiple companies to filter all charts simultaneously
- **Year filter** - filter by specific year or range
- **Conditional formatting** - risk table colour coded by severity (green/amber/red)
- **Tooltips** - hover on any data point for exact values
- **Dark theme** - Bloomberg-style dark navy design

## Tools

Looker Studio, Google BigQuery, SQL, GitHub

## Related Projects

- [financial-analytics-bigquery](https://github.com/tessogamba/financial-analytics-bigquery) — The BigQuery SQL pipeline that produced this data
- [retail-analytics-dbt](https://github.com/tessogamba/retail-analytics-dbt) — Analytics engineering pipeline created with dbt and Snowflake
- [retail-analytics-tableau](https://github.com/tessogamba/retail-analytics-tableau) — Tableau dashboard created on top of the dbt pipeline

## Author

**Teresia Ogamba (Tess Ogamba)** — Analytics Engineer & Data Analyst

[LinkedIn](https://linkedin.com/in/tessogamba) | [Website](https://tessogamba.com) | [GitHub](https://github.com/tessogamba)
