
# 🧾 Myntra Sales & Customer Analysis — Excel Dashboard

_Analyzing Myntra sales and customer behavior to support strategic marketing and retail operations decisions using MS Excel._

## 📌 Table of Contents

- [Overview](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#overview)
- [Business Problem](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#business-problem)
- [Dataset](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#dataset)
- [Tools & Technologies](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#tools--technologies)
- [Data Cleaning & Preparation](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#exploratory-data-analysis-eda)
- [Research Questions & Key Findings](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#research-questions--key-findings)
- [Dashboard](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#dashboard)
- [How to Run This Project](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#how-to-run-this-project)
- [Final Recommendations](https://github.com/ayushimishra28/vendor-performance-analysis-sql-python-powerbi-test#final-recommendations)

---

## Overview

This project is an **Excel-based sales and customer analysis** of a Myntra e-commerce dataset. The main goal of the project is to understand sales performance, customer behavior, product performance, discount patterns, and geographical performance using Excel.

---

## Business Problem

An e-commerce business needs to understand what is driving its sales and where there are opportunities to improve performance. This project aims to:
- Quantifying total revenue and order volume to establish an overall performance baseline.
- Identifying top-performing product segments to optimize inventory and merchandising strategy.
- Isolating the highest-grossing brands and individual products driving the most revenue.
- Evaluating which discount ranges yield the highest volume of orders and overall sales.
- Analyzing purchase distributions to identify reliance on high-value repeat buyers versus casual shoppers.

The purpose is not only to create charts, but to use the data to support **data-driven business decisions**.

---

## Dataset

The project uses an Excel workbook containing customer and order-level information.

### Main Data

The main analysis table contains **3,500 order records**.

Important fields include:

- Order ID
- Customer ID
- Product ID
- Date
- Original Price
- Discount %
- Category
- Sub-category
- Product Name
- Brand Name
- Size
- Color
- Ratings
- Customer Age
- City
- State

### Customer Data

The customer table contains:

- Customer ID
- Customer Age
- City
- State

There are **100 unique customers** in the dataset.

### Product Information

Product information is used to analyze:

- Category
- Sub-category
- Product
- Brand
- Size
- Color
- Rating

The order data contains **3,071 unique products** that were ordered.

### Time Period

The data covers:

**January 2021 to March 2023**

An important limitation is that **2023 contains only January to March data**, so full-year 2023 should not be directly compared with complete years such as 2021 and 2022.

---

## Tools & Technologies

### Excel

Excel was used for the complete analysis. Main features used:
- Excel Tables
- Formulas
- Calculated Columns
- PivotTables
- Pivot-based analysis
- Charts
- Conditional Formatting
- Slicers / interactive filtering
- Customer concentration analysis

### GitHub


---

## Data Cleaning & Preparation

The raw order data was prepared before performing the analysis.

### 1. Combined Customer and Product Information

Customer and product attributes were brought into the order-level analysis table using the relevant IDs.

The main relationships were:

- `Customer ID` → Customer information
- `Product ID` → Product information

This created a single analysis-ready table containing order, product, and customer information.

### 2. Checked Data Quality

The dataset was checked for:

- Missing values
- Duplicate records
- Matching Customer IDs
- Matching Product IDs
- Date consistency
- Discount values
- Price values

The analysis data did not contain missing values or duplicate order rows.

### 3. Created Calculated Columns

The following calculated fields were created:

| Column | Purpose |
|---|---|
| `SalesPrice` | Selling price after discount |
| `Dist_Amt` | Discount amount |
| `Year` | Year-level analysis |
| `Month` | Monthly analysis |
| `Month-Year` | Monthly trend analysis |
| `Quarter` | Quarterly analysis |
| `Age_Group` | Customer segmentation |
| `Price_Band` | Product price segmentation |
| `Dist_Band` | Discount segmentation |

### Sales Price

Sales price was calculated as:

```text
Sales Price = Original Price × (1 - Discount %)
```

### Discount Amount

```text
Discount Amount = Original Price × Discount %
```

These calculations helped separate **listed price, discount value, and actual selling value**.

---

## Exploratory Data Analysis (EDA)

The analysis was performed across multiple business dimensions.

### 1. Sales Performance

The project analyzed:

- Total sales
- Total orders
- Average Order Value
- Monthly sales
- Monthly orders
- Quarterly sales
- Year-wise sales

The dataset records **3,500 orders** and approximately **₹18.89 lakh in sales after discount**.

The average order value is approximately **₹539.67**.

### 2. Category Analysis

Sales and orders were analyzed by category.

| Category | Sales | Orders |
|---|---:|---:|
| Men | ₹5.86 Lakh | 1,149 |
| Women | ₹5.47 Lakh | 1,114 |
| Kids | ₹4.43 Lakh | 551 |
| Beauty | ₹3.12 Lakh | 686 |

Men generated the highest sales value and order count in this dataset.

### 3. Sub-category Analysis

Sub-categories were compared using:

- Sales
- Order count
- Average discount

The leading sub-categories by sales include:

- Footwear
- Topwear
- Bottomwear
- Western Wear
- Makeup

**Footwear** generated approximately **₹3.89 lakh** in sales and was the highest-selling sub-category.

### 4. Brand Analysis

Brand-level performance was analyzed using sales and order count.

The top brands by sales include:

1. Puma
2. H&M
3. Roadster
4. Here&Now
5. Adidas

Puma generated approximately **₹2.49 lakh** in sales in the dataset.

### 5. Product Analysis

Top products were identified using total sales and order count.

The highest-selling products by sales included:

- Jeans
- Shorts
- T-Shirts
- Sandals
- Jackets

Jeans generated approximately **₹1.73 lakh** in sales and had **354 orders**.

### 6. Customer Analysis

Customer behavior was analyzed using:

- Age group
- Order count
- Sales
- Average Order Value
- Customer-level sales contribution

The **18–25 age group** generated the highest sales and order volume:

- Sales: approximately **₹10.83 lakh**
- Orders: **1,989**

This shows that younger customers form a major part of the recorded sales activity.

### 7. Geographic Analysis

Sales were analyzed by state and city.

The highest-sales states in the dataset were:

- Gujrat
- Uttar Pradesh
- Punjab
- Bihar
- Rajasthan

Gujrat generated approximately **₹3.02 lakh** in sales.

### 8. Price Band Analysis

Products were grouped into price bands to understand customer purchasing patterns.

The major price bands were:

- Under ₹250
- ₹250–₹499
- ₹500–₹999
- ₹1,000–₹1,999
- ₹2,000+

The **₹500–₹999** band had the highest order count with **1,223 orders**, while the **₹1,000–₹1,999** band generated the highest sales value at approximately **₹6.54 lakh**.

### 9. Discount Analysis

Discount behavior was analyzed using discount bands.

The dataset has an average discount of approximately **35.51%**.

The total calculated discount amount is approximately **₹10.61 lakh**.

The 30–39% discount band generated the highest sales value and order count.

### 10. Rating Analysis

Product ratings were analyzed to understand the distribution of product quality ratings in the dataset.

Ratings were used as a product-level attribute rather than as individual customer review scores.

### 11. Customer Concentration

Customer-level sales were ranked to understand whether sales are highly dependent on a small number of customers.

The top 10 customers contributed approximately **12.42% of total sales**.

This suggests that sales are not entirely dependent on only a very small group of customers in this dataset.

---

## Research Questions & Key Findings

1. **Overall Sales Baseline:** Generated ₹18.89 lakh in net sales across 3,500 orders, averaging ₹539.67 per order
2. **Top Category:** Led by Men’s apparel at ₹5.86 lakh, closely followed by Women’s at ₹5.47 lakh
3. **Top Sub-category:** Driven by Footwear, which captured the highest share at ₹3.89 lakh in sales
4. **Dominant Brand:** Led by Puma, securing the highest brand revenue at ₹2.49 lakh
5. **Highest-Grossing Product:** Anchored by Jeans at ₹1.73 lakh, alongside strong demand for shorts and t-shirts
6. **Primary Demographic:** Dominated by the 18–25 age group, contributing 1,989 orders and ₹10.83 lakh in revenue
7. **Top Geographic Market:** Anchored by Gujarat, which recorded the highest regional sales at ₹3.02 lakh
8. **Discount Efficiency:** Averaged a 35.51% discount, with the 30–39% band yielding a peak revenue of ₹9.10 lakh
9. **Price Point Popularity:** Maximum volume in the ₹500–₹999 range (1,223 orders), but peak revenue in the ₹1,000–₹1,999 range (₹6.54 lakh)
10. **Customer Concentration:** Maintained a healthy distribution, with the top 10 customers accounting for 12.42% of total sales
11. **Temporal Sales Trends:** Peak quarterly revenue achieved in Q1 (₹6.26 lakh), with June 2022 marking the highest individual month (₹84,345)

---

## Dashboard

- The dashboard includes analysis areas such as:
   - Monthly Sales Trend
   - Monthly Orders Trend
   - Sales by Category
   - Top 10 Brands by Sales
   - Top 10 Products by Sales
   - Sales by State
   - Sales by Age Group
   - Sales by Discount Band
   - Orders by Price Band
   - Product Rating Distribution
   - Discount % vs Sales Price
   - Month vs Category Sales

The purpose of the dashboard is to allow a business user to quickly move from **overall performance to detailed product, customer, geography, and discount analysis**.

![Myntra Sales & Customer Analysis Dashboard](https://github.com/csainichakraborty-netizen/Myntra-Sales-and-Customer-Analysis-Excel/blob/c1469a0c6f39ef6f5712b752914ba09a31bdc72f/Dashboard(1).png)
![Myntra Sales & Customer Analysis Dashboard](https://github.com/csainichakraborty-netizen/Myntra-Sales-and-Customer-Analysis-Excel/blob/104fb06eec53dfb3b33ee9bf55cc0ec650dee661/Dashboard(2).png)
---

## How to Run This Project

### Step 1: Download the Excel Workbook

Download the project workbook from this repository.

### Step 2: Open the Workbook

Open the Excel file using Microsoft Excel.

### Step 3: Review the Data

Start with the analysis-ready `Analyzed_data` sheet.

This sheet contains the combined order, product, and customer information.

### Step 4: Review the Calculated Columns

Check:

- SalesPrice
- Dist_Amt
- Year
- Month
- Month-Year
- Quarter
- Age_Group
- Price_Band
- Dist_Band

### Step 5: Review the PivotTables

The `pivot_tables` sheet contains the main aggregated analysis.

Use the PivotTables to review:

- Sales
- Orders
- Average Order Value
- Discounts
- Categories
- Sub-categories
- Products
- Customers
- Year-wise performance

### Step 6: Review Customer Concentration

The `customer_concentration` sheet ranks customers based on sales and calculates cumulative sales contribution.

### Step 7: Use the Dashboard

Use the charts and filters to explore the data from different business perspectives.

---

## Final Recommendations

Based on the analysis, the following areas should be considered for business monitoring and future analysis:

* **Category & Sub-Category Monitoring:** Track demand shifts in high-performing core areas like Men, Women, and Footwear to identify new growth pockets.
* **Brand & Product Tracking:** Audit top revenue drivers like Puma, H&M, and Roadster across sales volume, discounts, and ratings to optimize inventory assortment.
* **Demographic Segmentation:** Analyze purchasing patterns within the dominant 18–25 age group to refine targeted engagement strategies.
* **Discount Efficiency Audits:** Evaluate the 35.51% average discount against order volume, repeat behavior, and margins to ensure promotional profitability.
* **Geographic Expansion:** Monitor state and city performance to scale operations in high-performing regions and troubleshoot underperforming markets.
* **Concentration Risk Management:** Track the 12.42% revenue reliance on the top 10 customers to safely manage repeat-buyer dependencies.
* **Advanced Data Integration:** Incorporate costs, returns, and inventory metrics to pivot from basic sales tracking to advanced profitability and lifetime value analysis.

### Add more business data in future

The current dataset does not contain:

- Quantity sold
- Product cost
- Profit
- Returns
- Cancellations
- Shipping cost
- Marketing spend
- Inventory

Adding these fields would allow deeper analysis such as:

- Profitability analysis
- Product margin analysis
- Return-rate analysis
- Customer Lifetime Value
- Marketing ROI
- Inventory analysis

---

## Project Limitations

This project has some important data limitations.

1. No Profit Data: The dataset does not contain product cost or operating expenses, so profit and profit margin cannot be calculated.
2. No Quantity Data: There is no separate quantity field. Therefore, the analysis treats each order record as one order.
3. No Returns or Cancellations: Sales values cannot be adjusted for returns or cancellations because those fields are not available.
4. Partial 2023 Data: 2023 contains only January to March data. Therefore, full-year 2023 performance should not be compared directly with complete years.
5. Product-Level Ratings: Ratings are available as a product attribute and should not be interpreted as a complete customer review dataset.
