# Adventure Works Power BI Dashboard

## Project Overview

This project delivers a comprehensive business intelligence solution for Adventure Works using Power BI. The dashboard is designed to provide executives and business stakeholders with a clear view of revenue performance, profitability, sales trends, customer behavior, and product category performance.

The report enables users to monitor key business KPIs, analyze year-over-year growth, evaluate profit margins, and identify revenue-driving product categories through interactive visualizations and filters.

---

## Dashboard Pages

### 1. Executive Summary

This page serves as the strategic overview of the business, presenting high-level performance metrics and category-based profitability insights.

#### Key Metrics
- **Total Revenue:** $24.91M
- **Total Profit:** $10.46M
- **Profit Margin %:** 41.97%
- **Revenue YoY Growth %:** 58.40%

#### Key Insights
- Tracks total revenue performance across years.
- Highlights revenue contribution by product category.
- Compares profit margins across product categories.
- Shows cost distribution by product category.
- Interactive filters for Year and Product Category allow focused analysis.

**Visuals Included**
- KPI Cards
- Revenue Trend by Year
- Total Revenue by Product Category
- Profit Margin % by Product Category
- Total Cost by Product Category

*Caption: Executive Summary dashboard displaying overall financial performance, category profitability, revenue growth, and cost analysis.*

---

### 2. Detailed Insights

This page provides a deeper operational analysis, focusing on sales volume, order patterns, product performance, and customer segmentation.

#### Key Metrics
- **Total Quantity Sold:** 84K
- **Total Orders:** 56K
- **Total Cost:** $14.46M
- **Revenue YTD:** $9.19M

#### Key Insights
- Analyzes trends in total quantity sold and order volumes over time.
- Compares monthly revenue performance against the previous year.
- Breaks down product quantity sold by category.
- Evaluates customer purchasing behavior based on education level.
- Displays total orders, quantity sold, revenue, and profit margin in a customer performance matrix.

**Visuals Included**
- KPI Cards
- Quantity Sold & Orders Trend
- Year-over-Year Revenue Comparison
- Product Quantity Distribution Donut Chart
- Customer Performance Matrix

*Caption: Detailed Insights dashboard showing sales trends, revenue comparisons, product category contributions, and customer performance analytics.*

---

## Data Model

The report is built using a star-schema-based data model designed for efficient analytics and scalable reporting.

### Core Tables
- Fact Sales
- Product Dimension
- Customer Dimension
- Date Dimension
- Territory/Region Dimension

### Model Features
- Centralized fact table for sales transactions.
- Dedicated Date Dimension supporting time intelligence calculations.
- One-to-many relationships between dimensions and fact tables.
- Optimized model for fast filtering and aggregation.

---

## Key DAX Calculations

### Sales & Profitability
- Total Revenue
- Total Cost
- Total Profit
- Profit Margin %

### Time Intelligence
- Revenue YTD
- Previous Year Revenue
- Year-over-Year Revenue Growth %
- Running Totals

### Sales Performance
- Total Orders
- Total Quantity Sold
- Category Contribution %
- Revenue by Product Category

---

## Dashboard Features

- Interactive slicers for Year and Product Category.
- Dynamic KPI calculations.
- Year-over-Year trend analysis.
- Customer segmentation analysis.
- Product category performance evaluation.
- Revenue and profitability monitoring.
- Executive-friendly layout for quick decision-making.

---

## How to Use This Dashboard

1. Download the `.pbix` file from the repository.
2. Open the file using **Power BI Desktop**.
3. Navigate between the **Executive Summary** and **Detailed Insights** tabs.
4. Use the **Year** and **Product Category** slicers to filter report data.
5. Hover over visuals for additional insights and detailed metrics.
6. Analyze trends and performance indicators to support business decision-making.

---

## Business Value

This dashboard helps stakeholders:

- Monitor organizational financial performance.
- Track revenue growth and profitability.
- Identify top-performing product categories.
- Understand customer purchasing patterns.
- Support strategic planning with data-driven insights.
- Improve operational and sales performance through actionable analytics.
