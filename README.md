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

The Power BI model follows a star schema with one fact table and three dimension tables:

- `Fact_Sales` – Stores transaction-level sales data, including date, city, store format, product, quantity, unit price, and sales amount.
- `Dim_Date` – Contains date information used for time-based analysis and date drill-down.
- `Dim_City` – Contains city information used to analyze and compare sales performance across cities.
- `Dim_Product` – Contains product and category information used for product-level sales analysis.

The dimension tables are related to the `Fact_Sales` table to support filtering, aggregation, and analysis in the Power BI dashboard.

## 4. DAX Measures

The model includes these measures:

- **Total Sales**: total sales amount.
- **MoM Sales Growth %**: sales growth compared with the previous month.
- **Running Total Sales**: cumulative sales over the date context.
- **City Sales Rank**: ranks cities by sales.
- **Average Sales per Transaction**: total sales divided by the distinct transaction count.

## 5. Dashboard

The dashboard analyzes Cold Brew seasonal sales and city-level performance.

It includes:
- Cold Brew sales trend
- Sales by city
- Sales by store format
- City slicer for interactive filtering
- Date drill-down hierarchy for Year, Quarter, Month, and Day
- Total Sales
- Average Sales per Transaction
- City Sales Rank

## 6. Key Insights

1. Cold Brew sales rose from approximately $348K in April to a peak of $393K in May, before declining to $303K in June.

2. Bengaluru recorded the highest city-level sales among the four cities shown in the dashboard, followed by Chennai, Hyderabad, and Coimbatore.

3. Flagship stores generated the highest sales among the three store formats. The drill-down also shows that Bengaluru Flagship sales were $523,524.79.

