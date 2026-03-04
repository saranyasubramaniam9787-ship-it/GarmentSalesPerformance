Garment Sales Performance Analysis
Description of the Project
This project analyzes garment sales data to evaluate overall business performance. It focuses on category-wise and segment-wise sales, identification of top-performing and low-performing products, regional performance, discount impact on profitability, and sales trends over time.
The project also includes revenue forecasting for the next six months and presents insights using interactive dashboards created in Microsoft Excel.
________________________________________
 Installation Instructions
1.	Install Microsoft Excel (2016 or later recommended).
2.	Download or clone this repository.
3.	Open the Excel file containing the cleaned dataset and dashboard.
4.	Enable editing and formulas if prompted.
5.	Refresh pivot tables and charts to view updated results.
________________________________________
Data Sources
The dataset contains transactional sales records with the following key fields:
•	Order_ID
•	Customer_Name
•	Product_Category
•	Product_Name
•	Product_ID
•	Units_Sold
•	Unit_Price
•	Discount_%
•	Revenue
•	Product_Cost
•	Profit/Loss
•	Profit Margin %
•	Order_Date
•	City_ID
•	Segment (B2B / B2C)
Each row represents a single sales transaction across different products, cities, and customer segments.
________________________________________
Code Structure (Excel Logic & Formulas)
Data Cleaning & Transformation Includes:
•	Removal of extra spaces and hidden characters using CLEAN() and TRIM().
•	Standardization of customer names and product categories.
•	Handling missing and invalid values:
o	Units sold: negative values corrected, nulls replaced with average.
o	Unit price: null values replaced with product-wise average.
o	Discount: null values replaced with average discount.
•	Revenue calculation:
Revenue = (Unit_Price × Units_Sold) × (1 – Discount%)
•	Profit/Loss calculation:
Profit = Revenue – Product_Cost
•	Profit Margin calculation:
Profit Margin % = (Profit / Revenue) × 100
Pivot tables and charts are used for:
•	Category-wise analysis
•	Region-wise analysis
•	Segment-wise analysis
•	Trend and forecast visualization
________________________________________
Results and Evaluation
Key Insights:
•	Dresses generate the highest revenue, while Jeans and Shoes underperform.
•	Revenue is mainly driven by B2C transactions.
•	High sales do not always result in high profit due to heavy discounting.
•	Profit margins vary widely, showing inconsistent pricing strategies.
•	Sales are concentrated in major cities like Hyderabad and Mumbai.
•	Revenue distribution is positively skewed with high variability.
Forecast Findings:
•	Revenue is projected to grow gradually over the next six months.
•	December is expected to have the highest revenue.
•	Long-term forecasts show higher uncertainty but an overall upward trend.
________________________________________
Future Work
•	Extend analysis using Power BI or Python for automation.
•	Add customer behaviour and churn analysis.
•	Introduce machine learning models for more accurate forecasting.
•	Perform deeper regional and product-level profitability optimization.
•	Expand B2B segment analysis.
________________________________________
Acknowledgments / References
•	Dataset: Internal sales transaction dataset (Snitch Fashion Sales Data).
•	Tool used: Microsoft Excel (Pivot Tables, Charts, Forecasting).
•	Concepts referenced: Descriptive statistics, business analytics, and time series forecasting.

