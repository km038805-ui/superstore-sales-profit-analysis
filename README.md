# Superstore Sales & Profit Analysis — Portfolio Practice Project

**By:** Muhammad K. — Data Analyst in progress, Madinah, Saudi Arabia
**GitHub:** https://github.com/km038805-ui
**Skills used:** Excel, Google Sheets, Python, Pandas, SQL-style grouping, Data Cleaning, Power BI-ready tables

> Portfolio practice project. This is **not client work and not work for any employer**.
> The data is public Kaggle data, analysed as practice.

## Data source
- **Kaggle dataset:** Sample Superstore / Superstore Sales — https://www.kaggle.com/datasets/vivek468/superstore-dataset-final and https://www.kaggle.com/datasets/roopacalistus/superstore
- **File:** `superstore.csv` — raw 10800 rows, 21 columns, US retail orders 2015-01-03 to 2018-12-30.
- **Download mirror used (no Kaggle login needed):** https://github.com/amulyasree26/superstore-sales-analysis (data/raw/superstore.csv)
- **Licence / use:** public Kaggle dataset, for educational and analytical use. Sample Superstore is a well-known teaching dataset, not real transactions.

## What I cleaned
- Standardised column names to snake_case.
- Removed **799 duplicate Row IDs** — cleaned file has **10001 rows** and **5015 orders**.
- 18 missing postal codes were marked "Unknown" instead of deleting those orders, because the sales and profit were still valid.
- Converted Order Date / Ship Date to real dates, added `year` and `profit_margin_pct`.

## Key findings (real numbers from the data)
- Total sales: **$2,297,200.86**; total profit: **$286,397.02**; overall profit margin **12.47%**.
- Sales by category: Technology $836,154.03, Furniture $741,999.80, Office Supplies $719,047.03.
- Profit by category: Technology $145,454.95, Office Supplies $122,490.80, Furniture only $18,451.27 — Furniture sells a lot but earns very little.
- Most profitable region: West $108,418.45, then East $91,522.78.
- Sales grew every year: 2015 $484,247.50 -> 2018 $733,215.26.
- **18.71% of order lines (1871 rows) lost money.**
- Worst sub-category: Tables **-$17,725.48** profit; best: Copiers **$55,617.82**.
- Average discount: **15.62%** — high discounts are part of why Furniture and Tables lose money.

## Files
- `superstore_sales_cleaned.csv` / `.xlsx` — cleaned data + Excel summaries by category, region and year
- `analysis.py` — Python/Pandas cleaning and analysis
- `charts/` — sales by category, profit by region, sales by year
- `findings.json` — all numbers above, computed by the script

> The cleaned Excel workbook (.xlsx) and chart images are in the local portfolio / CV, not in this repo, because this upload contains text files only.

## What a business can learn from this
Stop discounting Tables and Furniture so heavily, protect the profitable Technology lines (Copiers, Phones, Accessories), and focus growth on the West region, which is already the most profitable.
