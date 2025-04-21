# AdventureWorks-Dashboard

### Dashboard Link : https://app.powerbi.com/links/hyS65h87kB?ctid=1eba9f97-0b4f-4b17-b77f-b2d4487ad3c4&pbi_source=linkShare

## Problem Statement

This dashboard helps AdventureWorks, a global retail and manufacturing company, understand its sales, products, and customer performance across regions. It enables leadership to monitor revenue trends, identify high-performing product lines, and track customer behavior. By doing so, the company can make data-driven decisions to increase profits, improve product strategies, and target the right customer segments.

The dashboard provides both high-level KPIs and detailed drilldowns into product, geography, and customer metrics. With rising orders and a 41.97% profit margin, the company is growing steadily. However, insights around returns, repeat customer behavior, and underperforming segments guide where to improve.

### Steps followed

- Step 1 : Loaded multiple CSV datasets into Power BI Desktop including Sales Data (2020-2022), Product Lookup, Customer Lookup, and Territory Lookup.

- Step 2 : Opened Power Query Editor and checked "column distribution", "column quality" & "column profile" under the View tab.

- Step 3 : Selected "Column profiling based on entire dataset" for accurate data checks. Removed empty rows and ensured consistent formatting.

- Step 4 : Merged sales data with product prices to calculate revenue and profit. Created calculated columns for "Year" and "Month".

- Step 5 : Created DAX measures like:

  ```
  Total Revenue = SUM(Sales[OrderQuantity] * Product[ProductPrice])
  Total Profit = SUM(Sales[OrderQuantity] * (Product[ProductPrice] - Product[ProductCost]))
  Avg Revenue per Customer = AVERAGEX(VALUES(Customer[CustomerKey]), [Total Revenue])
  ```

- Step 6 : Designed KPIs using card visuals for Revenue, Profit, Orders, and Return Rate.

#Snapshot https://github.com/user-attachments/assets/df71ff52-55aa-458d-a4b2-5ddfe045bc72


- Step 7 : Added a revenue trend line chart with a forecast line based on monthly total revenue.

- Step 8 : Created bar charts showing orders by category and a heatmap table of Top 10 Products with revenue and return %.

- Step 9 : Used slicers to allow filtering by region, year, and category.

- Step 10 : Built a map visual highlighting sales distribution by country using Territory data.

- Step 11 : Developed product-level dashboards showing performance vs. targets for orders, profit, and revenue.

- Step 12 : Created a Customer Detail tab showing top customers, revenue per customer, and purchase behavior by occupation and income group.

- Step 13 : Created a Category Tooltip view for embedding summary metrics inside bar charts.

- Step 14 : Published the report to Power BI Service.

# Snapshot of Dashboard (Power BI Service)
Executive Dashboard - https://github.com/user-attachments/assets/86c7539e-b353-4825-a81c-638a1cd5cd12


# Report(Tabs) Snapshot (Power BI DESKTOP)
Executive Dashboard - https://github.com/user-attachments/assets/1b9b0525-1e95-4bdf-b127-6b158a9d7a7a




# Insights

A multi-page report was created on Power BI Desktop & then published to Power BI Service.

Following inferences can be drawn from the dashboard:

### [1] Total Sales Performance

- Total Revenue = **\$24.9M**
- Total Profit = **\$10.5M**
- Total Orders = **25.2K**
- Return Rate = **2.2%**

### [2] Revenue Trends

- Monthly revenue increased steadily across 2020-2022.
- Peaks visible in **Q2** and **Q4** of each year.
- Average monthly revenue = **\$1.83M**

### [3] Product Performance

- Top categories by order volume: **Accessories (17K orders)**, **Bikes (13.9K orders)**, **Clothing (7K orders)**
- Most returned products are in **Clothing** (e.g. Shorts, Helmets)
- Product insights include target tracking, profit and revenue visualizations

### [4] Regional Performance

- **United States** leads globally in sales volume
- Other high-performing countries include **Canada**, **UK**, **Germany**, and **Australia**
- Regional filters enable easy geographic comparisons

### [5] Customer Behavior

- Total Unique Customers = **12.1K**
- Average Revenue per Customer = **\$1,472**
- Majority of top customers are in **Professional** and **Skilled Manual** roles
- Repeat customers dominate order share

### [6] Additional KPIs

- Sales Growth (2022 vs 2021): **+12.5%**
- Profit Margin: **41.97%**
- Most Ordered Product: **Tires and Tubes**
- Most Returned Product Type: **Shorts**
-
