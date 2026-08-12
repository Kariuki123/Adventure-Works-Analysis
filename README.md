# Adventure Works Power BI Dashboard

## Project Overview

This project delivers a comprehensive business intelligence solution for Adventure Works using Power BI. The dashboard provides executives and business users with actionable insights into revenue, profitability, product performance, customer trends, and sales growth.

The report is divided into two interactive pages that support both high-level strategic analysis and detailed operational insights.

---

# Dashboard Pages

## 1. Executive Summary

The Executive Summary page provides a high-level overview of business performance, allowing decision-makers to quickly assess financial health and category-level profitability.

### Key Metrics

- **Total Revenue:** $24.91M
- **Total Profit:** $10.46M
- **Profit Margin %:** 41.97%
- **Revenue YoY Growth %:** 58.40%

### Key Insights

- Revenue growth trend across multiple years.
- Category-level revenue comparison.
- Profit margin analysis by product category.
- Cost analysis by category.
- Interactive filtering by Year and Product Category.

### Dashboard Screenshot

images/Executive-Summary.png

*Executive Summary page showing revenue, profit, profit margin, year-over-year growth, category revenue analysis, and cost distribution.*

---

## 2. Detailed Insights

The Detailed Insights page focuses on operational performance, sales volume analysis, customer segmentation, and year-over-year revenue comparisons.

### Key Metrics

- **Total Quantity Sold:** 84K
- **Total Orders:** 56K
- **Total Cost:** $14.46M
- **Revenue YTD:** $9.19M

### Key Insights

- Sales quantity and order volume trends.
- Monthly Year-over-Year revenue comparison.
- Product quantity distribution by category.
- Customer performance analysis by education level.
- Revenue and profitability contribution across customer groups.

### Dashboard Screenshot

images/Detailed-Insights.png

*Detailed Insights page displaying sales trends, revenue comparisons, product quantity analysis, and customer performance metrics.*

---

# Data Model

The dashboard follows a Star Schema design to ensure efficient reporting and optimized performance.

### Fact Table

- Fact Sales

### Dimension Tables

- Dim Date
- Dim Product
- Dim Customer
- Dim Territory

### Model Features

- One-to-many relationships.
- Dedicated Date table for Time Intelligence calculations.
- Optimized filtering and aggregations.
- Centralized measure table for DAX calculations.

---

# Key DAX Measures

### Financial Metrics

```DAX
Total Revenue = SUM(Sales[Revenue])

Total Cost = SUM(Sales[Cost])

Total Profit = [Total Revenue] - [Total Cost]

Profit Margin % =
DIVIDE([Total Profit],[Total Revenue],0)
```

### Time Intelligence

```DAX
Revenue YTD =
TOTALYTD([Total Revenue],'Date'[Date])

Revenue Previous Year =
CALCULATE(
    [Total Revenue],
    SAMEPERIODLASTYEAR('Date'[Date])
)

Revenue YoY Growth % =
DIVIDE(
    [Total Revenue]-[Revenue Previous Year],
    [Revenue Previous Year]
)
```

---

# Dashboard Features

✅ Interactive Year Slicers

✅ Product Category Filtering

✅ Dynamic KPI Cards

✅ Revenue Trend Analysis

✅ Profitability Analysis

✅ Customer Performance Insights

✅ Year-over-Year Revenue Tracking

✅ Product Category Performance Evaluation

---

# How to Use

1. Download the `.pbix` file.
2. Open the report using **Power BI Desktop**.
3. Navigate between:
   - Executive Summary
   - Detailed Insights
4. Use the Year and Product Category slicers to filter the report.
5. Hover over visuals for additional insights.
6. Drill into customer and category performance metrics.

---

# Business Value

This dashboard enables stakeholders to:

- Monitor organizational performance.
- Track profitability and revenue growth.
- Identify top-performing products.
- Evaluate customer purchasing behavior.
- Support strategic business decisions through data-driven insights.
- Improve operational and financial performance.

---

## Repository Structure

```text
Adventure-Works-PowerBI/
│
├── AdventureWorks.pbix
├── README.md
│
├── images/
│   ├── Executive-Summary.png
│   └── Detailed-Insights.png
│
└── dataset/
    └── AdventureWorks.xlsx
```

## Preview

### Executive Summary

images/Executive-Summary.png

### Detailed Insights

.png" width="900">
