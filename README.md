***Sales and Profitability Insights Across Customer Segments***

📖 **Table of Contents**

- Project Overview
- Data Source
- Tools & Technologies
- Data Cleaning & Preparation
- Exploratory Data Analysis (EDA)
- Key Insights
- Recommendations
- How to Use


**Project Overview**

This project analyzes sales performance and profitability across different customer segments, product categories, and regions. The objective is to identify high-performing and underperforming products, analyze sales trends, evaluate the impact of discounts on profitability, and forecast future revenue for better business decision-making.

**Key Objectives**

- Analyze category-wise and segment-wise sales performance
- Identify top-selling and low-performing products
- Evaluate profitability across categories
- Examine sales trends over time
- Analyze the impact of discounts on profit margins
- Assess regional sales performance
- Calculate average profit margins
- Forecast sales for the next six months
- Present insights using interactive dashboards


**Data Source**

Dataset: Garment Sales Dataset  

- **Records:** 1,500+ sales transactions  
- **Variables:** Product Category, Product Name, Sales Amount, Profit, Discount, City, Customer Type, Date  
- **File Format:** Excel (.xlsx)
- **Dataset Size:** ~1–2 MB
- **Total Transactions:** 2,391

Dataset: Snitch Fashion Sales Dataset
From Entri Elevate

**Description**:  
The dataset contains transactional records of sales across multiple products, categories, cities, and customer segments. Each row represents a single order including customer information, product details, pricing, discounts, revenue, and profit.

**Key Variables**

- Order_ID – Unique identifier for each order
- Customer_Name – Name of the customer
- Product_Category – Product category (Accessories, Dresses, Jackets, Jeans, Shoes, T-Shirts)
- Product_Name – Name of the product
- Product_ID – Unique product identifier
- Units_Sold – Number of units sold
- Unit_Price – Price per unit
- Discount_% – Discount percentage
- Revenue – Total revenue after discount
- Product_Cost – Cost of the product
- Profit/Loss – Profit or loss per transaction
- Profit Margin % – Profit percentage
- Order_Date – Date of order
- City_ID – Sales location
- Segment – Customer segment (B2B or B2C)


**Tools & Technologies**

- Excel – Data cleaning and statistical analysis

Visualization Tools

- Excel Charts

Database

- Excel Workbook

Documentation

- Microsoft Word
- Excel

Statistical Analysis

- Excel Data Analysis ToolPak


**Data Cleaning & Preparation**

Data Import Process

- Imported dataset using Excel Get Data from CSV
- Loaded worksheets for processing

Data Cleaning Steps

Order_ID Standardization

Used the following formula to remove hidden characters and spaces.

=CLEAN(TRIM([@[Order_ID]]))

Customer Name Standardization

- Removed prefixes such as Mr., Mrs., Dr., PhD
- Converted names into a consistent format

=CLEAN(TRIM(PROPER(CONCAT([@Column1],"",[@Column2]," ",[@Column3]))))

Product Category Standardization

=CLEAN(TRIM([@[Product_Category]]))

Units Sold

- Converted negative values to positive
- Replaced missing values with average units sold by product

Revenue Calculation

=([@[Unit_Price]]*[@[Units_Sold]])*(1-[@[Discount_%]])

Profit Calculation

=[@Revenue]-[@[Product_cost]]

Profit Margin Calculation

=[@[Profit/Loss]]/[@Revenue]*100

Additional Cleaning

- Filled missing Unit Price and Discount values
- Standardized City and Segment fields
- Corrected date formats
- Assigned proper data types for each column


**Exploratory Data Analysis (EDA)**

Revenue Statistics

- Mean: ₹2,336.45
- Median: ₹1,857.60
- Mode: ₹1,533.60
- Standard Deviation: ₹2,125.87
- Minimum: ₹16.52
- Maximum: ₹29,182.44
- Total Revenue: ₹55,86,457.86
- Total Records: 2,391
- Skewness: 3.47 (positively skewed distribution)

Overall Performance Metrics

- Total Sales: ₹55,86,457
- Total Profit: ₹25,73,741
- Profit Margin: 46%
- Total Quantity Sold: 5,671 units
- Total Transactions: 2,391


**Key Insights**

Product Performance

- Dresses generate the highest revenue
- Accessories and T-Shirts show moderate performance
- Jeans and Shoes contribute less to total revenue

Customer Segment

- B2C transactions dominate total sales
- B2B segment remains underutilized

Discount Impact

- High discounts increase sales but reduce profit margins
- Pricing strategies vary across products

Regional Performance

- Hyderabad and Mumbai are the top-performing cities
- Sales are concentrated in major metropolitan regions

Revenue Forecast

- Sales expected to grow gradually
- December projected to generate the highest revenue

Profit Margin

- Overall profit margin is 46%
- Profitability varies across product categories


**Recommendations**

Pricing Strategy

- Optimize discount strategies to protect profit margins
- Focus on improving profitability of top-selling products

Product Portfolio Management

- Improve performance of weak categories like Jeans and Shoes
- Use bundling strategies or targeted promotions

Channel Development

- Strengthen B2C channels
- Expand B2B partnerships to diversify revenue streams

Regional Expansion

- Replicate successful strategies from Hyderabad and Mumbai
- Implement region-specific marketing campaigns

Discount Management

- Monitor discounts carefully
- Implement data-driven pricing strategies

Inventory Planning

- Use forecast insights to optimize inventory levels
- Prepare for increased demand during November–December

**How to Use**

**Prerequisites**

- Microsoft Excel (2016 or later)
- Power BI Desktop (optional, for dashboard visualization)

**Steps to Run**

**Clone the Repository**

```bash
git clone https://github.com/saranyasubramaniam9787-ship-it/GarmentSalesPerformance.git
cd GarmentSalesPerformance
```

**Data Files Setup**

- Place the **E-Commerce_Sales_Dataset.xlsx** file in the `/data` folder.
- Ensure all worksheets (Customer, Product, Store, Sales) are available.

**Excel Analysis**

- Open **Ecommerce_Analysis_Workbook.xlsx**
- Enable macros if prompted
- Navigate through the following sheets:
  - Raw Data
  - Cleaned Data
  - Analysis
  - Visualizations

**Output**

- Cleaned dataset in `/output`
- Statistical summary reports
- Excel charts and visual analysis
- Dashboard insights

**Dashboard Screenshots**

**Category-wise Sales Performance**

- Dresses lead with the highest revenue and units sold
- Accessories, Jackets, and T-Shirts show moderate performance


**Top-Selling Products**

- Casual Midi  
- Crop Top  
- Graphic Tee  
- Maxi Dress  


**Regional Sales Analysis**

- Hyderabad and Mumbai dominate sales
- Ahmedabad, Bangalore, Delhi, and Pune show varying performance


**Sales Trends Over Time (2023–2025)**

- Clear growth trajectory observed
- Seasonal patterns identified


**Revenue Forecast Analysis**

- Upward trend from July to December
- Upper and lower confidence bounds displayed
