# Global Sales Dashboard

## Project Overview

This Power BI project presents a comprehensive **Global Sales Dashboard** designed to empower decision-making for [Your Organization/Client's Name]. The dashboard consolidates sales data from multiple sources, providing insights into key performance indicators (KPIs), sales trends, and regional performance. This tool supports business analysts and executives in:

- Monitoring sales performance across different regions.  
- Analyzing trends and patterns in product categories.  
- Evaluating metrics like revenue, profit, and sales growth.  
- Optimizing strategies and operations through actionable insights.
PowerBI.com - https://app.powerbi.com/groups/me/reports/7799e6bc-2235-4a55-a588-2b99323b66a4/c0c3b7a5392f6091415d?experience=power-bi

<img width="644" alt="image" src="https://github.com/user-attachments/assets/dbec22d6-73f6-4860-815c-70ea78c1ff92" />

---

## Visualizations and Insights  

The dashboard features several interactive visualizations:  

1. **KPI Gauges**:  
   - **Achieved Sales**: Displays total sales achieved (e.g., 13M out of 25M).  
   - **Achieved Profit**: Highlights the total profit achieved (e.g., 1.47M out of 2.93M).  

2. **Card Visuals**:  
   - **Count of Customer Name**: Indicates the total number of unique customers (e.g., 51.29K).  
   - **Sum of Quantity**: Shows the total quantity of products sold (e.g., 178K).  

3. **Line Chart**:  
   - **Sum of Profit and Sum of Sales by Year and Quarter**: Tracks trends in sales and profit over time to identify seasonal growth patterns.  

4. **Pie Chart**:  
   - **Sum of Profit by Category**: Represents profit distribution across product categories like Technology, Furniture, and Office Supplies.  

5. **Map Visualization**:  
   - **Sum of Sales and Sum of Profit by Country and Category**: Displays sales and profit across regions on an interactive map for geographical insights.  

6. **Scatter Chart**:  
   - **Average Sales by Category**: Plots the average sales and profit for each product category to highlight performance trends and outliers.  

7. **Funnel Chart**:  
   - **Sum of Discount by Category**: Visualizes the distribution of discounts across product categories.

---

## Power Query Transformations  

The following transformations were performed in Power Query:  

1. **Data Import**:  
   - Imported datasets from multiple sources such as Excel and SQL Server.  

2. **Data Cleaning**:  
   - Removed duplicates and filtered null or invalid values.  
   - Standardized date formats and renamed ambiguous columns for clarity.  

3. **Transformations**:  
   - Merged datasets (e.g., linking sales data with customer and region information).  
   - Created calculated columns for new metrics, such as "Profit Percentage."  
   - Applied data grouping to calculate aggregates like region-wise sales totals.  

4. **Advanced Transformations**:  
   - Unpivoted columns to create a more analysis-friendly data structure.  
   - Added conditional columns to categorize products or territories.

---

## DAX Calculations  

Dynamic DAX measures and calculations were implemented to enhance dashboard interactivity:  

1. **Key Performance Indicators (KPIs)**:  
   - **Total Revenue**: `SUM(Sales[Revenue])`  
   - **Profit Margin**: `DIVIDE(SUM(Sales[Profit]), SUM(Sales[Revenue]), 0)`  
   - **Year-over-Year Growth**: `([This Year Revenue] - [Last Year Revenue]) / [Last Year Revenue]`  

2. **Time Intelligence Measures**:  
   - **Year-to-Date Sales**: `TOTALYTD(SUM(Sales[Revenue]), Calendar[Date])`  
   - **Rolling 12-Month Sales**: `CALCULATE(SUM(Sales[Revenue]), DATESINPERIOD(Calendar[Date], LASTDATE(Calendar[Date]), -12, MONTH))`  

3. **Dynamic Segmentation**:  
   - Created measures to segment customers based on revenue tiers (e.g., High Value, Mid-Tier, Low Value).  

4. **Custom Metrics**:  
   - **Sales Variance**: Highlights underperforming regions.  
   - **Rankings**: Ranks top-performing products and regions dynamically.  

---

## Features of the Dashboard  

- **Interactive Filters**: Filter data by region, product category, or sales period.  
- **Dynamic Visualizations**: Includes charts, maps, and tables for multi-dimensional data exploration.  
- **Drillthrough Capabilities**: Analyze specific regions or products in detail.  
- **Bookmarks**: Predefined views such as "Top 10 Products" or "Quarterly Overview" for quick insights.  

---

## Conclusion  

This **Global Sales Dashboard** provides an intuitive and data-driven interface for analyzing sales performance across regions and categories. By leveraging Power BI’s capabilities, the project delivers actionable insights, enabling stakeholders to make informed decisions and optimize strategies.  

For further details or questions, please contact: rutujakokate430@gmail.com
