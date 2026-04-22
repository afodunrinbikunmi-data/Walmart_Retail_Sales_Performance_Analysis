# Walmart_Retail_Sales_Performance_Analysis
A Power BI Business Intelligence project analyzing 6,436 records to identify the correlation between macroeconomic factors (Fuel Price, CPI, Unemployment) and retail performance.

## Project Summary
An analysis of weekly sales performance across 45 Walmart store locations covering 6,436 weekly records over three years (2010–2012).
The goal was to identify what drives sales — examining store performance gaps, holiday impact, seasonal trends, and the relationship between sales and external economic factors.

**Key finding: Fuel prices show the strongest external correlation
with weekly sales — more impactful than unemployment, temperature,
or CPI.**

## Dataset Overview
| Field | Detail |
|---|---|
| Records | 6,436 weekly sales entries |
| Stores | 45 locations |
| Period | 2010 — 2012 |
| Source | Walmart Store Sales Dataset (Kaggle) |

## Key Columns in the Dataset
| Column | Description |
|---|---|
| Store | Unique store identifier (1–45) |
| Date | Week ending date for each record |
| Weekly_Sales | Total weekly revenue per store |
| Holiday_Flag | Binary (1 = holiday week, 0 = regular week) |
| Temperature | Average regional temperature (°F) |
| Fuel_Price | Average regional fuel price per gallon ($) |
| CPI | Consumer Price Index — cost of living measure |
| Unemployment | Regional unemployment rate (%) |

## Tools Used
| Tool | Purpose |
|---|---|
| Microsoft Excel | Data cleaning, feature engineering, PivotTable analysis |
| Power Query | Date format standardisation via locale conversion |
| Microsoft Power BI | DAX measures, 2-page interactive dashboard |
| DAX | Custom KPI measures and external factor calculations |

## Data Cleaning & Preparation
- Standardised inconsistent date formats via Power Query locale conversion
- Converted all columns to correct data types
- Verified zero duplicate records across 6,436 rows
- Checked for missing values — none found
- Engineered calculated columns:
  - `Holiday Label` — converts binary flag to Holiday Week / Regular Week
  - `Sales Band` — classifies weekly sales as High, Medium or Low
  - `Year` — extracted from date for YoY analysis
  - `Month` — extracted from date for seasonal trend analysis
  - `Day` — extracted from date for granular temporal analysis

## Key Questions & Analysis
1. Which stores contribute the most to total sales and how large is the gap?
2. Do holiday periods significantly increase weekly sales?
3. Is there consistent year-on-year growth across the period?
4. What seasonal patterns exist in monthly sales performance?
5. Does fuel price correlate with weekly sales performance?
6. Does unemployment rate affect Walmart's weekly sales?
7. Is there any relationship between temperature and sales?

## Key Insights
- **9× store performance gap** — Store 20 ($301M) vs Store 33 ($33M)
- **7.84% holiday uplift** — positive but modest and unevenly distributed
- **2011 strongest year** — $2.45B, up 6.9% from $2.29B in 2010
- **December always peaks** — January always weakest, consistent every year
- **Fuel price = strongest external driver** — inverse relationship confirmed
- **Unemployment = no impact** — Walmart is recession-resilient by design
- **Temperature effect overridden by holidays** — December cold + December high sales
- **Revenue heavily concentrated** — small number of stores carry the network

## Recommendations
1. Audit bottom 10 stores — 9× gap is a business problem, not a market reality
2. Build tiered holiday promotional calendar based on individual event performance
3. Monitor fuel prices weekly — trigger promotions when prices fall

## Dashboard / Visualization
The Power BI dashboard contains 2 report pages:

| Page | Focus |
|---|---|
| Sales Performance | KPIs, sales trend by year, store performance bar, holiday comparison |
| External Factors | Fuel vs sales, unemployment scatter, temperature vs sales, KPI cards |

## Project Structure
'''text
├── data/
│   └── walmart_sales.xlsx
├── dashboard/
│   └── walmart_dashboard.pbix
├── report/
│   └── Walmart_Sales_Analysis.pptx
├── screenshots/
│   ├── sales_performance.png
│   └── external_factors.png
└── README.md
'''
