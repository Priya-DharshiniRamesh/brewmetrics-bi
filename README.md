# BrewMetrics BI

## 1. Project Overview

This project is a Business Intelligence dashboard for BrewMetrics Coffee Co. It uses Power BI for analysis and GitHub and GitHub Copilot as part of the project workflow.

## 2. Dataset

The dataset contains the following fields:

- `date`
- `city`
- `store_format`
- `category`
- `item`
- `quantity`
- `unit_price`
- `sales_amount`

## 3. Data Model

The Power BI model contains four tables:

- `Fact_Sales`
- `Dim_Date`
- `Dim_City`
- `Dim_Product`

## 4. DAX Measures

The model includes these measures:

- **Total Sales**: total sales amount.
- **MoM Sales Growth %**: sales growth compared with the previous month.
- **Running Total Sales**: cumulative sales over the date context.
- **City Sales Rank**: ranks cities by sales.
- **Average Sales per Transaction**: total sales divided by the distinct transaction count.

## 5. Dashboard

The dashboard analyzes Cold Brew seasonal sales and city-level performance.

## 6. Key Insights

1. Cold Brew sales increased from approximately $130K in April to $142.7K in May, before decreasing to approximately $118.2K in June.

2. Bengaluru recorded the highest city-level sales among the four cities shown in the dashboard, followed by Chennai, Hyderabad, and Coimbatore.

3. Flagship stores generated the highest sales among the three store formats. The drill-down also shows that Bengaluru Flagship sales were $523,524.79.
