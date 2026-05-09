# Retail Pricing & Demand Forecasting

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3D3D3D?style=for-the-badge)

> A full-stack data analysis pipeline covering retail sales forecasting and inflation-adjusted pricing — from raw ETL through EDA, SQLite storage, and an interactive Excel dashboard.

---

## Overview

This project demonstrates the complete data analyst workflow using three real-world datasets: Rossmann retail store sales (1M+ rows), a multi-store demand forecasting dataset, and Italian macroeconomic inflation data from ISTAT and Eurostat.

| Stage | Tools Used |
|-------|-----------|
| Data Ingestion & ETL | Python · Pandas · OS |
| Exploratory Data Analysis | Jupyter · Seaborn · Matplotlib |
| Statistical Analysis | NumPy · SciPy |
| Database Storage | SQLite3 · pandas to_sql() |
| Dashboard & Reporting | Excel (openpyxl) · Dark Professional Theme |

---

## Key Insights

- **Promotional lift**: Promo days drive an **+81.4% uplift** in average daily sales vs. non-promo days
- **Best store type**: Store Type B consistently outperforms A, C, and D in revenue per day
- **Peak inflation**: Italy hit **8.7% HICP inflation in 2022** — highest since the 1980s
- **Italy vs EU-27**: Italian inflation tracked 0.6–1.3 pp above the EU-27 average from 2021–2023
- **Inflation-adjusted pricing**: Real price formula demonstrated using HICP index (base 2025=100)
- **Seasonal pattern**: December sales spike; January shows consistent post-holiday trough

---

## Project Structure

```
retail-pricing-demand-forecasting/
├── Script.ipynb                          <- Main analysis notebook (all 9 sections)
├── requirements.txt                      <- Python dependencies
├── .gitignore
│
├── dashboard/
│   └── Retail_Dashboard.xlsx            <- Dark-theme Excel dashboard (4 sheets, 9 charts)
│
├── reports/
│   ├── Retail_Analysis_Questions.pdf    <- Full analysis brief
│   └── Annual inflation rate italy vs su.png
│
└── data/
    ├── 01_rossmann/
    │   ├── rossmann_store_metadata.csv
    │   ├── rossmann_store_sales_train.csv   <- 1M+ rows (download from Kaggle)
    │   └── rossmann_store_sales_test.csv
    ├── 02_demand/
    │   ├── retail_inventory_sales.csv
    │   ├── store_item_demand_train.csv
    │   └── store_item_demand_test.csv
    ├── 03_istat/
    │   ├── istat_hicp_monthly_4digit.csv
    │   └── istat_nic_weights_6digit.csv
    ├── 04_eurostat/
    │   ├── eurostat_hicp_annual_index.csv
    │   └── eurostat_hicp_inflation_rate.csv
    └── 05_holidays/
        └── italy_public_holidays_2023.csv
```

---

## Datasets

| Dataset | Source | Size | Description |
|---------|--------|------|-------------|
| Rossmann Store Sales | [Kaggle](https://www.kaggle.com/c/rossmann-store-sales) | 1,017,209 rows | Daily sales for 1,115 German drug stores (2013–2015) |
| Store Item Demand | [Kaggle](https://www.kaggle.com/c/demand-forecasting-kernels-only) | 913,000 rows | Daily demand for 50 items across 10 stores |
| Retail Inventory Sales | Kaggle | ~500K rows | Multi-category retail inventory and sales data |
| ISTAT HICP Monthly | [ISTAT](https://www.istat.it) | ~2,400 rows | Italian consumer price indices 2025–2026 (ECOICOP-4) |
| Eurostat HICP Annual | [Eurostat](https://ec.europa.eu/eurostat) | ~3,000 rows | Annual HICP inflation rates 2014–2025 (EU-27 countries) |

> **Note:** The large Rossmann training CSV (37MB) exceeds GitHub's recommended file size. Download it directly from Kaggle and place it in `data/01_rossmann/`.

---

## Analysis Sections (Script.ipynb)

| Cell | Dataset | Questions Answered |
|------|---------|-------------------|
| 1 | Rossmann | Sales by store type, top/bottom performers |
| 2 | Rossmann | Monthly sales trends 2013–2015 |
| 3 | Rossmann | Promotional impact on daily sales |
| 4 | Rossmann | Holiday effects on sales (state + school) |
| 5 | Demand | Category-level unit volume analysis |
| 6 | Demand | Price elasticity across product categories |
| 7 | Demand | Seasonal demand patterns |
| 8 | ISTAT | Overall HICP inflation trend · Inflation-adjusted pricing |
| 9 | Eurostat | Italy annual inflation 2014–2025 · Italy vs. EU-27 |

---

## Dashboard

The Excel dashboard (`dashboard/Retail_Dashboard.xlsx`) features a **dark professional theme** (#0D1B2A background) with:
- 6 KPI summary cards
- 9 embedded Python-generated charts (Rossmann, Demand, Italy Inflation)
- 3 colour-coded section headers
- Interactive slicers for time period and category filtering

---

## Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/ali112-akbar/retail-pricing-demand-forecasting
cd retail-pricing-demand-forecasting

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download large datasets from Kaggle
# Place rossmann_store_sales_train.csv in data/01_rossmann/

# 4. Run the analysis
jupyter notebook Script.ipynb
```

---

## Requirements

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
openpyxl>=3.1
jupyter>=1.0
requests>=2.31
scipy>=1.11
```

---

## Portfolio Readiness: 9/10

**Strengths**
- Complete end-to-end pipeline (ETL → EDA → SQL → Dashboard)
- Three independent real-world datasets with cross-domain analysis
- Professional Excel dashboard with dark theme and embedded charts
- Macroeconomic context (Italy HICP) makes it unique vs. standard retail projects
- SQLite storage demonstrates database skills alongside Python proficiency

**What would make it 10/10**
- Deploy the dashboard as an interactive Streamlit or Dash web app
- Add predictive modelling (time-series forecasting with Prophet or statsmodels)

---

## Author

**Ali Akbar**
GitHub: [@ali112-akbar](https://github.com/ali112-akbar)
Email: ali123akbar12@gmail.com

---
*Last updated: May 2026*
