# Online Retail Sales Dashboard — Power BI

An interactive Power BI dashboard analyzing online retail transaction data, covering revenue trends, customer behavior, and product performance, with month-to-date (MTD) and same-period-last-year (SPLY) comparisons.

## Project Overview

This project takes raw, unprocessed e-commerce transaction data and turns it into a two-page interactive business dashboard. It covers the full analytics workflow — data cleaning, data modeling, DAX measure creation, and dashboard design.

## Dataset

The dataset contains order-level online retail transactions with the following fields:

| Column | Description |
|---|---|
| InvoiceNo | Unique order/invoice identifier |
| StockCode | Product code |
| Description | Product name |
| Quantity | Units sold per transaction line |
| InvoiceDate | Date of transaction |
| UnitPrice | Price per unit |
| CustomerID | Unique customer identifier |
| Country | Customer's country |

## Data Cleaning & Preparation (Power Query)

- Corrected date parsing using UK locale (DD-MM-YYYY) to prevent day/month misreads
- Set correct data types across all columns (Whole Number, Fixed Decimal, Text, Date)
- Removed cancelled/returned orders from the transaction set
- Resolved type-conversion errors in mixed alphanumeric fields (e.g., product codes containing both letters and numbers)
- Built a dedicated Calendar table and linked it to the transactions table to support time-intelligence calculations

## Key Metrics (DAX Measures)

| Measure | Purpose |
|---|---|
| Total Revenue | Total sales value (Quantity × Unit Price) |
| Total Orders | Count of unique orders |
| Total Customers | Count of unique customers |
| Total Quantity | Total units sold |
| Average Order Value | Average revenue per order |
| MTD Revenue | Month-to-date running revenue |
| Revenue vs Same Period Last Year | Year-over-year comparison |

## Dashboard Pages

**1. Sales Overview**
KPI summary cards, revenue trend by month, customer activity by day, quantity by year, revenue by country, orders by month, and revenue by product category.

![Dashboard Overview](screenshots/dashboard-overview.png)

**2. Trend Analysis (MTD & YoY)**
Month-to-date revenue tracking and year-over-year performance comparison to spot growth patterns and seasonality.

![Trend Analysis](screenshots/dashboard-trend-analysis.png)

## Tools Used

- **Power BI Desktop** — data modeling, DAX, dashboard design
- **Power Query** — data cleaning and transformation
- **DAX (Data Analysis Expressions)** — measures and time-intelligence calculations

## Key Insights

- Revenue shows a clear upward trend toward the final quarter of the year, indicating strong seasonal demand.
- Sales are heavily concentrated in the United Kingdom, with a long tail of smaller international markets.
- A small set of product categories account for a large share of total revenue.

## Author

**Lovepreet**
[LinkedIn](https://www.linkedin.com/in/lovepreet-072824395)

