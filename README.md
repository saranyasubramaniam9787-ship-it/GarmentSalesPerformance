# Garment Sales Performance Analysis

## Brief Description of the Project
This project analyzes garment sales data to evaluate overall business performance. It focuses on category-wise and segment-wise sales, identification of top-performing and low-performing products, regional performance, discount impact on profitability, and sales trends over time.  
The project also includes revenue forecasting for the next six months and presents insights using interactive dashboards created in Microsoft Excel.

---

## Installation Instructions
- Install Microsoft Excel (2016 or later recommended)
- Download or clone this repository
- Open the Excel file containing the cleaned dataset and dashboard
- Enable editing and formulas if prompted
- Refresh pivot tables and charts to view updated results

---

## Data Sources
The dataset contains transactional sales records with the following fields:
- Order_ID  
- Customer_Name  
- Product_Category  
- Product_Name  
- Product_ID  
- Units_Sold  
- Unit_Price  
- Discount_%  
- Revenue  
- Product_Cost  
- Profit/Loss  
- Profit Margin %  
- Order_Date  
- City_ID  
- Segment (B2B / B2C)

---

## Code Structure
### Data Cleaning & Transformation
- Removed extra spaces using `CLEAN()` and `TRIM()`
- Standardized customer names and product categories
- Handled missing values:
  - Units sold: negative corrected, null replaced with average
  - Unit price: null replaced with product-wise average
  - Discount: null replaced with average
- Revenue calculation:  
  `Revenue = (Unit_Price × Units_Sold) × (1 – Discount%)`
- Profit calculation:  
  `Profit = Revenue – Product_Cost`
- Profit Margin:  
  `Profit Margin % = (Profit / Revenue) × 100`

Pivot tables and charts used for:
- Category-wise analysis  
- Region-wise analysis  
- Segment-wise analysis  
- Trend and forecast visualization  

---

## Results and Evaluation
### Key Insights
- Dresses generate the highest revenue, while Jeans and Shoes underperform
- Revenue is mainly driven by B2C transactions
- High sales do not always result in high profit due to heavy discounting
- Profit margins vary widely, showing inconsistent pricing strategies
- Sales are concentrated in major cities like Hyderabad and Mumbai
- Revenue distribution is positively skewed with high variability

### Forecast Findings
- Revenue is projected to grow gradually over the next six months
- December is expected to have the highest revenue
- Long-term forecasts show higher uncertainty but an overall upward trend

---

## Future Work
- Extend analysis using Power BI or Python
- Add customer behavior and churn analysis
- Introduce machine learning models for forecasting
- Perform deeper regional and product-level profitability analysis
- Expand B2B segment analysis

---

## Acknowledgments / References
- Dataset: Internal sales transaction dataset (Snitch Fashion Sales Data)
- Tool used: Microsoft Excel
- Concepts: Business analytics, descriptive statistics, forecasting

---

