## Sales and Profitability Insights Across Customer Segments
📖 Table of Contents
Project Overview
Data Source
Tools & Technologies
Data Cleaning & Preparation
Exploratory Data Analysis (EDA)
Key Insights
Recommendations
How to Use
📊 Project Overview
This project analyzes sales performance and profitability across different customer segments, product categories, and regions. The primary business objective is to identify high-performing and underperforming products, understand sales trends, evaluate the impact of discounts on profitability, and forecast future revenue to support strategic planning.
Key Objectives:
Analyze category-wise and segment-wise sales performance
Identify top-selling and low-performing products
Evaluate profitability across categories and segments
Examine sales trends over time to identify growth patterns
Analyze the impact of discounts on profit margins
Assess regional sales performance across major cities
Calculate average profit margins for financial evaluation
Forecast sales for the next six months
Present insights through interactive visual dashboards
🗂️ Data Source
Dataset: Snitch Fashion Sales Dataset
Description: The dataset contains detailed transactional records of sales across multiple products, categories, cities, and customer segments. Each row represents an individual order capturing customer information, product details, pricing, discounts, revenue, and profitability.
Size: 2,391 transactions
Key Variables:
Order_ID: Unique identifier for each sales order
Customer_Name: Name of the customer
Product_Category: Category of the product (Accessories, Dresses, Jackets, Jeans, Shoes, T-Shirts)
Product_Name: Name of the product sold
Product_ID: Unique product identifier
Units_Sold: Number of units sold per order
Unit_Price: Price per unit
Discount_%: Discount percentage applied
Revenue: Total revenue after discount
Product_Cost: Cost to produce/procure the product
Profit/Loss: Profit or loss from transaction
Profit Margin%: Profit as percentage of revenue
Order_Date: Date of order placement
City_ID: City where sale occurred (Ahmedabad, Bangalore, Delhi, Hyderabad, Mumbai, Pune)
Segment: Customer segment (B2B or B2C)
🛠️ Tools & Technologies
Language: Excel (Data Cleaning & Analysis), Python (Pandas, NumPy, Matplotlib, Seaborn)
Database: Excel Workbook
Visualization: Power BI, Excel Charts
Documentation: Jupyter Notebook, Excel
Statistical Analysis: Excel Data Analysis ToolPak
🧹 Data Cleaning & Preparation
Data Import Process:
Imported dataset using Excel's Get Data feature from CSV file
Loaded all required worksheets for processing
Data Cleaning Steps:
Order_ID Standardization:
Applied CLEAN and TRIM functions to remove hidden characters and extra spaces
Formula: =CLEAN(TRIM([@[Order_ID]]))
Customer_Name Standardization:
Removed prefixes/suffixes (Mr., Mrs., Ms., Dr., PhD, DVM)
Standardized names to uniform format
Formula: =CLEAN(TRIM(PROPER(CONCAT([@Column1],"",[@Column2]," ",[@Column3]))))
Product_Category & Product_Name Standardization:
Applied CLEAN and TRIM functions for uniformity
Formula: =CLEAN(TRIM([@[Product_Category]]))
Units_Sold Column:
Converted negative values to positive
Imputed zero and null values with average unit quantity by product
Formula: =IF(OR([@[Units_Sold]]="",[@[Units_Sold]]=0),AVERAGEIF([Product_Name],[@[Product_Name]],$E$4:$E$2392),IFS([@[Units_Sold]]=-1,"1",[@[Units_Sold]]=-2,"2",TRUE,[@[Units_Sold]]))
Unit_Price:
Imputed null values with average unit price by product
Formula: =IF(ISBLANK([@[Unit_Price]]),AVERAGEIF([Product_Name],[@[Product_Name]],$F$2:$F$2392),[@[Unit_Price]])
Discount_%:
Replaced null values with average discount by product
Capped values >1 to 1
Formula: =IF(OR([@[Discount_%]]=0,G1=""),AVERAGEIF([Product_Name],[@[Product_Name]],$G$2:$G$2392),IF([@[Discount_%]]>1,1,[@[Discount_%]]))
Revenue Calculation:
Formula: =([@[Unit_Price]]*[@[Units_Sold]])*(1-[@[Discount_%]])
Product_Cost:
Imputed missing values for accurate profit analysis
Profit/Loss Calculation:
Formula: =[@Revenue]-[@[Product_cost]]
Profit Margin Calculation:
Formula: =[@[Profit/Loss]]/[@Revenue]*100
Order_Date:
Populated null values with valid dates using appropriate date logic
City_ID & Segment:
Applied CLEAN and TRIM functions for standardization
Data Type Formatting:
Formatted all columns appropriately (text, numeric, currency)
🔍 Exploratory Data Analysis (EDA)
Statistical Summary:
Revenue Statistics:
Mean: ₹2,336.45
Median: ₹1,857.60
Mode: ₹1,533.60
Standard Deviation: ₹2,125.87
Minimum: ₹16.52
Maximum: ₹29,182.44
Total Revenue: ₹55,86,457.86
Total Records: 2,391
Skewness: 3.47 (positively skewed distribution)
Overall Performance Metrics:
Total Sales: ₹55,86,457
Total Profit: ₹25,73,741
Total Profit Margin: 46%
Total Quantity Sold: 5,671 units
Total Transactions: 2,391
Total Product Categories: 25
Main Analysis Questions Explored:
What are the top-performing product categories?
Dresses lead overall sales
Accessories, Jackets, and T-Shirts show moderate performance
Jeans and Shoes show weak contribution
Which products are top-sellers?
Casual Midi, Crop Top, Graphic Tee, and Maxi Dress are high performers
Bomber Jacket, Loafers, and Watches show strong sales
How does sales performance vary by region?
Hyderabad and Mumbai are top-performing cities
Regional performance varies significantly
Sales concentrated in major metropolitan areas
What is the segment-wise performance?
B2C transactions dominate revenue across all product types
B2B segment is underutilized
What is the impact of discounts on profitability?
High sales don't always translate to high profit due to aggressive discounting
Discount levels vary widely across products
Profit margin differences indicate inconsistent pricing strategies
What are the sales trends over time?
Analyzed trends from 2023-2025
Identified seasonal patterns and growth behavior
What does the revenue forecast show?
Upward trend projected from July to December
Highest revenue expected in December
Moderate growth with seasonal fluctuations
💡 Key Insights
Product Performance Concentration: Sales are concentrated in a few high-performing categories (Dresses lead), while several products (Jeans, Shoes) contribute only marginally to total revenue, indicating an unbalanced product mix.
B2C Dominance: Revenue is primarily driven by B2C transactions across all product types, while the B2B segment remains underutilized, representing a significant growth opportunity.
Discount Impact on Profitability: High sales volumes in some products do not translate into high profits due to aggressive discounting strategies. Profit margin differences across products indicate inconsistent pricing strategies that need optimization.
Regional Dependency: Sales are heavily concentrated in major cities, especially Hyderabad and Mumbai, showing strong regional dependency. Regional demand patterns strongly influence product performance.
Revenue Forecast: The forecast shows an overall upward trend with moderate growth expected over the next six months, with December likely to record the highest revenue. However, there's higher uncertainty in long-term forecasts.
Profit Margin Health: Overall profit margin of 46% indicates stable operational efficiency, but margin variability across products suggests the need for pricing strategy review.
Top Performers: Dresses are the main revenue contributor, followed by Accessories and T-Shirts. Products like Casual Midi, Crop Top, and Graphic Tee are top-sellers.
🚀 Recommendations
Optimize Pricing Strategy: Focus on improving profit from top-selling products rather than only increasing sales volume. Revise pricing and discount strategies for low-profit products to protect margins.
Product Portfolio Management: Support weak-performing products (Jeans, Shoes) using bundling strategies or region-specific promotions. Consider discontinuing consistently low-performing SKUs.
Channel Development: Strengthen the B2C channel while actively developing B2B as a stability channel to reduce dependency on consumer buying behavior and diversify revenue streams.
Regional Expansion: Leverage strong performance in Hyderabad and Mumbai to develop strategies for underperforming regions. Implement region-specific marketing campaigns.
Discount Management: Implement stricter discount controls and monitor product-wise profit regularly to prevent margin erosion. Use data-driven discount strategies based on product profitability.
Inventory Planning: Use the six-month forecast to optimize inventory levels, especially for high-performing products. Prepare for increased demand in November-December.
Performance Monitoring: Establish regular monitoring dashboards to track product-wise profit margins, regional performance, and segment-wise sales to enable quick strategic adjustments.
⚙️ How to Use
Prerequisites:
Microsoft Excel (2016 or later)
Python 3.8+ (optional, for advanced analysis)
Power BI Desktop (optional, for interactive dashboards)
Dependencies (Python):
