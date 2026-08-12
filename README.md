# Adventure Works Power BI Dashboard

## Project Overview

This project delivers an interactive business intelligence solution for **Adventure Works** using Power BI. The dashboard provides stakeholders with a comprehensive view of revenue performance, profitability, product category trends, customer behavior, and year-over-year business growth.

The report is designed to support executive decision-making through intuitive visualizations, KPI tracking, and interactive filtering capabilities.

---

## Dashboard Pages

### 1. Executive Summary

The Executive Summary page provides a high-level overview of organizational performance and profitability.

#### Key Metrics
- **Total Revenue:** $24.91M
- **Total Profit:** $10.46M
- **Profit Margin:** 41.97%
- **Revenue YoY Growth:** 58.40%

#### Key Insights
- Revenue trend analysis across 2015–2017.
- Revenue contribution by product category.
- Profit margin comparison across categories.
- Product cost distribution analysis.
- Interactive Year and Product Category filtering.

#### Visuals Included
- KPI Cards
- Revenue Trend by Year
- Revenue by Product Category
- Profit Margin by Category
- Total Cost by Category

---

### 2. Detailed Insights

The Detailed Insights page focuses on operational sales performance and customer analytics.

#### Key Metrics
- **Total Quantity Sold:** 84K
- **Total Orders:** 56K
- **Total Cost:** $14.46M
- **Revenue YTD:** $9.19M

#### Key Insights
- Quantity sold and order trends by year.
- Monthly Year-over-Year revenue comparison.
- Product quantity distribution by category.
- Customer performance analysis by education level.
- Revenue and profitability contribution across customer segments.

#### Visuals Included
- KPI Cards
- Quantity Sold & Orders Trend
- Year-over-Year Revenue Comparison
- Product Quantity Analysis
- Customer Performance Matrix

---

## Dashboard Preview

Instead of static screenshots, an exported PDF containing all report pages has been included within the repository.

📄 **Dashboard Preview:**  
Adventure%20Works%20Pdf.pdf

The PDF contains:
- Executive Summary Page
- Detailed Insights Page
- Interactive dashboard layout preview
- KPI and performance visualizations

---

## Data Model

The dashboard follows a Star Schema design to ensure efficient performance and scalability.

### Fact Table
- Sales Fact Table

### Dimension Tables
- Date Dimension
- Product Dimension
- Customer Dimension
- Category Dimension

### Model Features
- One-to-Many Relationships
- Time Intelligence Support
- Optimized Filtering Performance
- Centralized DAX Measures

---

## Key DAX Measures

### Financial Metrics

```DAX
Total Revenue =
SUM(Sales[Revenue])

Total Cost =
SUM(Sales[Cost])

Profit =
[Total Revenue] - [Total Cost]

Profit Margin % =
DIVIDE([Profit],[Total Revenue],0)
```

### Time Intelligence

```DAX
Revenue YTD =
TOTALYTD(
    [Total Revenue],
    'Date'[Date]
)

Revenue Previous Year =
CALCULATE(
    [Total Revenue],
    SAMEPERIODLASTYEAR('Date'[Date])
)

Revenue YoY Growth % =
DIVIDE(
    [Total Revenue] - [Revenue Previous Year],
    [Revenue Previous Year]
)
```

---

## Dashboard Features

- Interactive Year Slicers
- Product Category Filters
- Dynamic KPI Cards
- Revenue Trend Analysis
- Profitability Tracking
- Customer Segmentation
- Year-over-Year Revenue Analysis
- 
