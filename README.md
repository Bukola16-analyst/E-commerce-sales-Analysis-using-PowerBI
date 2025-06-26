INTRODUCTION

This report provides a clear overview of E-commerce sales based on transaction data collected from an online retail platform. The analysis covers key sales trends and customer behavior to help understand what drives revenue and how business performance varies across products, locations, and time periods.

The dataset includes information such as invoice dates, product descriptions, countries of purchase, sales quantities, and invoice numbers. Using Power BI, we created interactive visuals to track sales over time, identify top-performing products, and find the best-selling days and regions.

AIM

To analyze e-commerce sales data using Power BI in order to identify key sales trends, customer behavior, and business performance insights that support better decisions

OBJECTIVES

 To analyze sales performance over time based on invoice dates, identifying high and low-performing periods.

 To identify the best-selling products and categories by quantity and revenue.

 To determine the most profitable countries by total sales.

 To examine customer purchase patterns, including best-selling days of the week and order frequency.

 To evaluate trends in product demand using product descriptions and sales quantities.

 To create interactive dashboards in Power BI that visualize key performance indicators (KPIs) such as total sales, Total quantity sold, and top-selling items.

 To provide data-driven insights that can inform decisions related to inventory management, marketing strategies, and customer targeting

PROBLEM BEING ADDRESSED

Many e-commerce businesses collect large amounts of sales data but struggle to turn that data into useful insights. Without proper analysis, it is hard to know which products are selling best, when customers are most active, or which countries generate the most revenue. This can lead to poor inventory decisions, missed sales opportunities, and inefficient marketing.

This report aims to solve that problem by analyzing e-commerce sales data using Power BI. By organizing and visualizing the data, we can better understand sales trends, customer behavior, and business performance, helping decision-makers make smarter, data-based choices.

KEY DATASET AND METHODOLOGIES

 Invoice Number — Unique identifier for each transaction

 Invoice Date — Date and time of purchase

 Stock Code — Product code for each item

 Description — Product name or details

 Quantity — Number of units sold

 Unit Price — Price per unit of each item

 Customer ID — Unique ID for each customer

 Country — Country where the order was placed

Methodologies

I used Power Query Editor for the Data Cleaning

Checked for missing or inconsistent values

Ensured consistent letters (e.g., uppercase or lower case)

Ensured correct data types (e.g., numerical, text, date)

 DATA ANALYSIS EXPRESSION(DAX)

The new measures in the data

Total Sales

Total sales = SUMX (data, data [Unit Price] *data [Quantity])

Average unit price

Average unit price = AVERAGE (data [Unit Price])

Total Orders Invoices

Total order invoice=DISTINCTCOUNT (data [Invoice No])

Total Quantity sold

Total Quantity Sold = SUM (data [Quantity])

Average Order Value

Average order value = DIVIDE (data [Total sales], [Total Orders invoice])

Numbers of Customers

Numbers of Customers = DISTINCTCOUNT (data [Customer ID])

Calculated column

I Created a new column weekday but the column invoice date consists of date and time, so I extract only the date adding a new column INVOICE DATE ONLY

INVOICE DATE ONLY = DATE (YEAR (data [Invoice Date]), MONTH (data []), DAY (data [Invoice Date]))

Then Weekdays, the new column is weekdays = FORMAT (‘data’[INVOICE DATE ONLY], “dddd”)

sorting weekdays = WEEKDAY (‘data’[INVOICE DATE ONLY], 2)

where Monday =2, Tuesday= 3

 Analyzed sales trends by month

 Ranked top-selling products and countries by total sales

Analyzed sales by day of the week
 Dashboard Creation in Power BI:

Designed interactive dashboards to display KPIs like:
Total Revenue
Number of Orders
Best-Selling Products
Top Countries by Sales
Sales Trends Over Time
STORY OF DATA

The Data is an Ecommerce sales Datasets downloaded from Kaggle.com

IMPORTANT FEATURES AND THEIR SIGNIFICANCE

STORY OF DATA

The Data is an Ecommerce sales Datasets downloaded from Kaggle.com

Data Structure: The e-commerce dataset used in this analysis is structured in a flat table format, where each row represents a single transaction and each column represents a specific attribute such as description, invoice date, country, quantity, unit price, customer id

IMPORTANT FEATURES AND THEIR SIGNIFICANCE

Invoice Date

Significance: Helps identify sales trends over time, such as daily, monthly, or seasonal patterns. This is Useful for planning promotions, stocking inventory, and tracking performance.
Country

Significance: Shows which regions generate the most sales, this helps businesses target high-performing markets and discover growth opportunities in underperforming regions.
Description(product)

Significance: Reveals which products are frequently purchased. This is important for product planning, marketing focus, and inventory management.
Quantity

Significance: This Indicates the volume of items sold, allowing comparison between high-demand and low-demand products.
Unit Price

Significance: This is Useful for calculating revenue and understanding pricing strategies. This Can help to evaluate which products offer better profit margins.
Customer ID

Significance: This Helps to identify unique customers, track repeat purchases and offer discount for loyalty customer
Invoice Number

Significance: Each invoice represents a unique transaction, which is important for order tracking, fraud detection, and analyzing order patterns.
Total Sales (Calculated column: Quantity × Unit Price)

Significance: A core metric for evaluating overall business performance, profitability, and product contribution to total revenue.
Data Cleaning

I used Power Query Editor for the Data Cleaning

Checked for missing or inconsistent values

Ensured consistent letters (e.g., uppercase or lower case)

Ensured correct data types (e.g., numerical, text, dates)

Data splitting

The data were split into two categories

Independent and dependent variables or value

PRE- ANALYSIS BOARD

Project split

INDEPENDENCE VARIABLES/VALUES includes:

Description

country

DEPENDENT VARIABLES OR VALUES includes: invoice date

Quantity

Stock Code

Unit Price

Total sales

invoice No

weekdays

Total orders invoice

INDUSTRY TYPE; E. COMMERCE DATASET

STAKEHOLDER: Company Management Team

Potential Analysis

Top selling Description(product) by total sales
Bestselling weekdays by total sales
Best country by total sales
Top countries by average order value
Top Quantity Sold by Description
Monthly Sales Trends
Top 5 stock code by Total order


Potential Insights

1 Top selling description(product) by revenue, this enables us know the best performing product with the highest revenue which can help in stock inventory

2 Understand which of the Days has the highest revenue, this shows which days of the week customers are most active in purchasing, this can help the company to restock around peak days and also do promotional offers or discount sales to continue driving more sales

3 Best country by total sales, help us highlights the market with the highest contribution to overall sales revenue, this can help the company to consider-country specific promotions, customer loyalty programs

United Kingdom is the Top country and this can guide future expansion.

4 Top countries by Average Order Value, this reveals where customers are spending the most per order

5 Top Quantity Sold by Description, this helps to uncovers which products sell the highest number of units, regardless of the price

world war 2 Gliders has the highest quantity sold but not top in revenue, it is a popular product but low-priced product and this is ideal for promotional offer.

IN-ANALYSIS BOARD

In analysis Observation

1 Top Selling Description (Product) by Total Sales, the Top selling product is Dotcom Postage with a total sale of 206K, this help us identify which specific products are generating the highest revenue.

2 Best Selling Weekdays by Total Sales, Thursday tops the charts with the total sales of 2.1M, follow by Tuesday with total sales of 1.9M

3 Best Country by Total Sales, United Kingdom has the highest total sales, follow by Netherlands

4 Top country by Average Order Value, the Netherlands has the highest Average order value.

5 for the Top Quantity Sold by Description, World War 2 Gliders has the highest quantity sold but not top in revenue.

6 for the monthly sales trends Analysis, this is to track growth pattern, the month of December has the highest sales and this might be as a result of holiday shopping behavior and this is great for planning seasonal campaign to boost more sales.

In-analysis Insights

1 Top selling description(product) by revenue, this enables us know the best performing product with the highest revenue which can help in stock inventory

2 understand which of the Days has the highest revenue, this shows which days of the week customers are most active in purchasing, this can help the company to restock around peak days and also do promotional offers or discount sales to continue driving more sales

3 Best country by total sales, help us highlights the market with the highest contribution to overall sales revenue, this can help the company to consider-country specific promotions, customer loyalty programs

United Kingdom is the Top country and this can guide future expansion.

4 Top c countries by Average Order Value, this reveals where customers are spending the most per order

5 Top Quantity Sold by Description, this helps to uncovers which products sell the highest number of units, regardless of the price

world war 2 Gliders has the highest quantity sold but not top in revenue, it is a popular product but low-priced product and this is ideal for promotional offer.



FINAL OBSERVATION AND RECOMMENDATION

1. Observation: “Dotcom Postage” is the top-selling product by revenue (206K).

Recommendation: Maintain strong inventory levels for this product and consider offering similar or related products to maximize sales. Use it as a standard product for developing new bundles.

2. Observation: Thursday and Tuesday have the highest total sales (£2.1M and £1.9M).

· Recommendation: Schedule major promotions, product launches, and marketing campaigns on these high-performing weekdays to maximize impact. Also, ensure that inventory and logistics are optimized to meet increased demand on these days.

3. Observation: The United Kingdom is the top contributor to total sales.
· Recommendation: Invest in localized marketing, customer retention strategies, and possibly expand fulfillment centers or services in the UK to support growing demand.

4. Observation: The Netherlands has the highest Average Order Value (AOV).
· Recommendation: Introduce premium products, bundle offers, or loyalty rewards targeted specifically at customers in the Netherlands to encourage continued high-value purchases.

5. Observation: “World War 2 Gliders” has the highest quantity sold, though not the highest revenue.
· Recommendation: Use this high-volume product in bundle deals, or as a gift item with larger purchases to drive cross-selling and customer satisfaction.

6 Observation: November and December records the highest sales, likely due to holiday shopping behavior.

· Recommendation: Launch early holiday marketing campaigns, prepare inventory in advance, and run seasonal discounts to take full advantage of holiday demand.

Conclusions

This E-commerce sales analysis helped us better understand how the business is performing and where the main opportunities are. By using Power BI, I discovered which products sell the most, when customers are most active, and which countries bring in the most revenue.

I found that “Dotcom Postage” made the most money, while “World War 2 Gliders” sold the most units. Thursday and Tuesday were the busiest sales days, which can help plan future promotions. The United Kingdom had the highest total sales, and the Netherlands had the highest average order value, showing that customers there spend more per purchase. November and December had the most sales, likely due to the holiday season.

These insights can help the business improve decision-making around product stocking, marketing, and planning for peak sales periods. By focusing on what works best, the company can grow sales and better meet customer needs
