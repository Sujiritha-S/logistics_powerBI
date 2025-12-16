# Logistics & Sales Performance — Power BI Report

## Project Overview
This Power BI project analyzes logistics operations and sales performance across products, categories, segments, and countries. The report leverages Power Query and DAX to transform raw order and delivery data into actionable insights for optimizing revenue, profit, and operational efficiency.

## Dashboard Preview 
<img width="1290" height="736" alt="dashboard_preview" src="https://github.com/user-attachments/assets/06416b4f-0a41-4896-b3c7-ab9618e7d1ec" />

## Files Included
- Logistics_Sales_Performance.pbix
- Excel File - Data Source
  - Orders table
  - Products.table
  - Customers table
  - Country table
- Dashboard Screenshots
  - dashboard-preview.png

## Features / Highlights
- **KPI Summary**: Total Sales ($3.12M), Total Orders (16K), Profit ($346K), YoY Growth (47.8%), Late Delivery Rate
- **Sales Trend Analysis**: Monthly sales and profit trends highlighting dips from Aug–Dec
- **Segment Analysis**: Consumer segment performance in sales, orders, and profit
- **Category & Product Insights**: Top 5 high-margin categories and Top 10 revenue-generating products
- **Country-wise Performance**: Sales vs Profit by country to identify high-sales, low-profit regions
- **Operational Risk Analysis**: Late-delivery trends impacting revenue and customer satisfaction
- **Interactive Filters**: Segment, category, product, and country-level filters to customize views

## Tools & Techniques
- Power BI Desktop
  - Power Query Editor
  - DAX (for KPIs, growth, and operational metrics)
  - Conditional formatting, KPI indicators, filters, scliers
  - Dashboard design with consistent color, font, and layout

## Data Preparation
### Steps performed in Power Query:
- Removed irrelevant columns
- Renamed columns for clarity and consistency
- Reordered and cleaned data types
- Created custom conditional column for delivery status (on-time vs late)
- Replaced null/wrong values for clean visuals

## Data Modeling 
- Implemented a **Star Schema** for the dataset  
  - **Fact Table**: Orders (contains sales, profit, quantity, and delivery metrics)  
  - **Dimension Tables**: Product, Customer, and Country
- Established relationships between the fact and dimension tables to enable efficient slicing, dicing, and aggregation of KPIs across different hierarchies  
- Optimized model for DAX calculations and interactive dashboard performance


## DAX Measures & Functions
Custom calculations were made using key DAX functions:
| Function        | Purpose                                                                                  |
|-----------------|------------------------------------------------------------------------------------------|
| `DIVIDE()`      | Calculates ratios like profit margin or on-time delivery percentage                      |
| `AVERAGE()`     | Computes average order values or delivery times                                          |
| `CALCULATE()`   | Applies filters dynamically to compute KPIs like sales, profit, and late deliveries      |
| `COUNTROWS()`   | Counts number of orders, products, or deliveries                                         |
| `DATEADD()`     | Calculates date-shifted measures for trend analysis                                      |
| `TOTALYTD()`    | Computes year-to-date sales and profit growth                                            |
| `TOTALMTD()`    | Computes month-to-date sales and profit                                                  |
| `DISTINCTCOUNT()` | Counts unique orders, customers, or products                                           |
| `SUM()`         | Aggregates sales, profit, or quantity                                                    |
| `SUMX()`        | Performs row-wise aggregation for calculated totals                                      |
| `RELATED()`     | Brings in related table values for enriched calculations                                 |
| `SWITCH()`      | Handles conditional logic for metrics or KPIs                                            |
| `YEAR()`        | Extracts year from date fields for trend analysis                                        |

## Key Insights
- Generated $3.12M in sales from 16K orders with $346K profit and 47.8% YoY growth, but high late-delivery rate poses a risk to customer satisfaction.  
- Consumer segment leads in sales, orders, and profit; top 5 categories and Top 10 products contribute the bulk of revenue.  
- Country-wise analysis revealed regions with high sales but low profit, highlighting opportunities to optimize delivery routes and reduce costs.  
- Monthly sales trends show consistent drops from August to December, indicating operational delays impact year-end revenue.

## Future Enhancements
- Introduce trend visuals to track late deliveries over time  
- Implement predictive analytics for delivery delays and revenue forecasting  
- Add bookmarks and drill-throughs for deeper operational and financial insights
