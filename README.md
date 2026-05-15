# 📊 Sales Performance Dashboard — Power BI

An interactive Power BI dashboard built to track and analyze sales performance across regions and product categories, covering data from **2020 to 2026**.

---

## 🖼️ Dashboard Preview

> Open `Sales_Performance_Dashboard.pbix` in Power BI Desktop to explore the full interactive report.

---

## 📌 Features

- **KPI Cards** — Revenue, Profit, Orders, and Profit Margin at a glance
- **Monthly Trends** — Line/bar charts showing performance over time (Jan 2025 and beyond)
- **Regional Breakdown** — Compare sales and profit across regions
- **Product Category Analysis** — Identify top-performing and underperforming categories
- **Year-over-Year (YoY) Growth** — DAX-powered measures for period comparison
- **Running Totals** — Cumulative revenue and profit tracking
- **Interactive Slicers** — Filter by year, region, and product category

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard design and publishing |
| **Power Query (M)** | Data cleaning and transformation |
| **DAX** | KPI measures (YoY growth, profit margin %, running totals) |

---

## 📁 Repository Structure

```
sales-performance-dashboard/
│
├── Sales_Performance_Dashboard.pbix   # Main Power BI report file
└── README.md                          # Project documentation
```

---

## 📈 Key DAX Measures Used

```dax
-- Year-over-Year Revenue Growth
YoY Growth % = 
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Date'[Date])),
    CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Date'[Date]))
)

-- Running Total Revenue
Running Total Revenue = 
CALCULATE(
    [Total Revenue],
    FILTER(ALLSELECTED('Date'), 'Date'[Date] <= MAX('Date'[Date]))
)

-- Profit Margin %
Profit Margin % = DIVIDE([Total Profit], [Total Revenue])
```

---

## 🚀 How to Use

1. **Clone or download** this repository
2. Open `Sales_Performance_Dashboard.pbix` in **Power BI Desktop** (free download at [powerbi.microsoft.com](https://powerbi.microsoft.com))
3. If prompted, update the **data source path** to point to your local data files
4. Interact with slicers and visuals to explore insights

---

## 💡 Key Insights

- Identified **top-performing products** driving the majority of revenue
- Flagged **underperforming regions and categories** to support strategic decisions
- Tracked **monthly revenue trends** to detect seasonality and growth patterns

---

## 📅 Data Coverage

| Attribute | Details |
|---|---|
| **Time Range** | 2020 – 2026 |
| **Granularity** | Monthly |
| **Metrics** | Revenue, Profit, Orders, Profit Margin % |

---

## 👤 Author
Viraj Patil

## 📄 License

This project is for portfolio and educational purposes.
