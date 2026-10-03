# Myntra Sales & Customer Analysis — Excel Dashboard

## Table of Contents

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

This project is an **Excel-based sales and customer analysis** of a Myntra e-commerce dataset.

The main goal of the project is to understand sales performance, customer behavior, product performance, discount patterns, and geographical performance using Excel.

The analysis converts raw order-level data into useful business insights through:

- Data cleaning and preparation
- Data integration
- Calculated columns
- PivotTables
- KPI analysis
- Product and category analysis
- Customer analysis
- Geographic analysis
- Discount analysis
- Customer concentration analysis
- Charts and dashboard-style reporting

### Key Metrics

| KPI | Value |
|---|---:|
| Total Orders | 3,500 |
| Total Sales After Discount | ₹18.89 Lakh |
| Average Order Value | ₹539.67 |
| Total Discount Given | ₹10.61 Lakh |
| Average Discount | 35.51% |
| Unique Customers | 100 |
| Unique Products Ordered | 3,071 |
| Brands | 72 |
| States | 10 |
| Cities | 24 |
| Analysis Period | Jan 2021 – Mar 2023 |

> **Note:** Sales in this project means the calculated selling value after discount. The dataset does not contain product cost, profit, returns, cancellations, or operating expenses, so profit cannot be calculated from this data.

---

## Business Problem

An e-commerce business needs to understand what is driving its sales and where there are opportunities to improve performance.

This analysis focuses on the following business questions:

1. How much sales value and how many orders were generated?
2. How does sales performance change over time?
3. Which categories and sub-categories generate the most sales?
4. Which brands and products perform best?
5. Which customer age groups contribute the most orders and sales?
6. Which states and cities generate the most sales?
7. How much discount is being given to customers?
8. Which discount ranges generate the most orders and sales?
9. What price ranges are most popular?
10. How concentrated is sales among customers?
11. What patterns can be identified from product ratings?
12. Which areas should be monitored for future business decisions?

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

Excel was used for the complete analysis.

Main features used:

- Excel Tables
- Formulas
- Calculated Columns
- PivotTables
- Pivot-based analysis
- Charts
- Conditional Formatting
- Slicers / interactive filtering
- Customer concentration analysis

### Key Excel Concepts

The analysis uses common Business Analyst and Data Analyst concepts such as:

- KPI analysis
- Aggregation
- Trend analysis
- Segmentation
- Top-N analysis
- Customer concentration
- Category analysis
- Discount analysis
- Geographic analysis
- Exploratory Data Analysis

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

### Q1. What is the overall sales performance?

The dataset contains **3,500 orders** with approximately **₹18.89 lakh in sales after discount**.

The average order value is approximately **₹539.67**.

### Q2. Which category performs best?

The **Men** category generated the highest sales value at approximately **₹5.86 lakh**, followed by Women at approximately **₹5.47 lakh**.

### Q3. Which sub-category performs best?

**Footwear** was the highest-selling sub-category with approximately **₹3.89 lakh** in sales.

### Q4. Which brand generates the highest sales?

**Puma** generated the highest sales among the brands in the dataset, with approximately **₹2.49 lakh**.

### Q5. Which products generate the most sales?

**Jeans** was the highest-selling product with approximately **₹1.73 lakh** in sales.

Other strong products included Shorts, T-Shirts, Sandals, and Jackets.

### Q6. Which customer age group contributes the most?

The **18–25 age group** generated approximately **₹10.83 lakh** in sales and accounted for **1,989 orders**.

### Q7. Which state generates the most sales?

**Gujrat** recorded the highest sales value in the dataset at approximately **₹3.02 lakh**.

### Q8. What is the discount pattern?

The average discount is approximately **35.51%**.

The **30–39% discount band** generated the highest sales value at approximately **₹9.10 lakh**.

However, this analysis shows association only. It does not prove that higher discounts caused higher sales.

### Q9. Which price range is most popular?

The **₹500–₹999** price band recorded the highest number of orders with **1,223 orders**.

The **₹1,000–₹1,999** band generated the highest sales value at approximately **₹6.54 lakh**.

### Q10. How concentrated are sales among customers?

The top 10 customers contributed approximately **12.42% of total sales**.

This provides a useful view of customer concentration and helps identify whether sales depend heavily on a small customer group.

### Q11. What does the time analysis show?

Sales vary month to month. Q1 generated the highest quarterly sales in the dataset at approximately **₹6.26 lakh**.

The strongest monthly sales period in the dataset was **June 2022**, with approximately **₹84,345** in sales.

Because 2023 only contains January–March data, it should be treated as a partial year.

---

## Dashboard

The dashboard includes analysis areas such as:

1. Monthly Sales Trend
2. Monthly Orders Trend
3. Sales by Category
4. Top 10 Brands by Sales
5. Top 10 Products by Sales
6. Sales by State
7. Sales by Age Group
8. Sales by Discount Band
9. Orders by Price Band
10. Product Rating Distribution
11. Discount % vs Sales Price
12. Month vs Category Sales

The purpose of the dashboard is to allow a business user to quickly move from **overall performance to detailed product, customer, geography, and discount analysis**.

![Myntra Sales & Customer Analysis Dashboard](https://github.com/csainichakraborty-netizen/Myntra-Sales-and-Customer-Analysis-Excel/blob/c1469a0c6f39ef6f5712b752914ba09a31bdc72f/Dashboard(1).png)
![Myntra Sales & Customer Analysis Dashboard](images/dashboard(2).png)
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

### 1. Monitor high-performing categories

Men and Women are the largest sales categories in the dataset. Their performance should be monitored regularly to understand changes in demand.

### 2. Focus on high-performing sub-categories

Footwear is the highest-selling sub-category. Product-level and brand-level performance within Footwear can be studied further to identify growth opportunities.

### 3. Track top brands and products

Puma, H&M, Roadster and other high-performing brands contribute significantly to sales. Monitoring their sales trends, order volume, discounts, and ratings can support assortment decisions.

### 4. Segment customers by age

The 18–25 customer group contributes a large share of orders and sales. Customer segmentation can be used to understand different purchasing patterns across age groups.

### 5. Monitor discount effectiveness

The average discount is relatively high at approximately 35.51%. Discount analysis should therefore track both sales and order response rather than only increasing discounts.

Future analysis should compare:

- Discount %
- Orders
- Sales
- Average Order Value
- Customer repeat behavior

This can help identify whether discounts are being used efficiently.

### 6. Monitor geographic performance

State and city-level sales can help identify high-performing markets and locations with lower sales.

### 7. Monitor customer concentration

The top 10 customers contribute about 12.42% of total sales. Customer concentration should be tracked over time to identify changes in dependency on high-value customers.

### 8. Add more business data in future

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

### No Profit Data

The dataset does not contain product cost or operating expenses, so profit and profit margin cannot be calculated.

### No Quantity Data

There is no separate quantity field. Therefore, the analysis treats each order record as one order.

### No Returns or Cancellations

Sales values cannot be adjusted for returns or cancellations because those fields are not available.

### Partial 2023 Data

2023 contains only January to March data. Therefore, full-year 2023 performance should not be compared directly with complete years.

### Product-Level Ratings

Ratings are available as a product attribute and should not be interpreted as a complete customer review dataset.

---

## Conclusion

This Excel project demonstrates how raw e-commerce data can be transformed into a structured business analysis.

The analysis covers:

**Sales → Products → Categories → Brands → Customers → Geography → Pricing → Discounts → Customer Concentration**

The main objective is to provide a clear view of business performance and identify areas that can be explored further using more detailed business data.

This project also demonstrates practical skills in:

- Excel data preparation
- Data analysis
- PivotTables
- KPI development
- Business problem solving
- Customer segmentation
- Trend analysis
- Dashboard design
- Business insight generation
