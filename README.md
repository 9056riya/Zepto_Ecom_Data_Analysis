# Zepto E-Commerce Inventory Data Analysis | PostgreSQL

## Project Overview

This project focuses on analyzing Zepto's e-commerce inventory data using PostgreSQL. The objective is to explore product information, perform data cleaning, and extract meaningful business insights using SQL queries.

The analysis covers product pricing, discounts, stock availability, inventory value, product categories, and weight-based analysis.

## Objectives

- Explore and understand the e-commerce inventory dataset.
- Identify missing values and duplicate product entries.
- Clean and prepare data for analysis.
- Analyze product discounts and pricing patterns.
- Evaluate stock availability across product categories.
- Calculate estimated inventory value and total inventory weight.
- Generate business insights using SQL queries.

## Tools & Technologies

- **Database:** PostgreSQL
- **Language:** SQL
- **Dataset:** Zepto E-commerce Inventory Dataset
- **Platform:** GitHub

## Dataset Description

The dataset contains product-level inventory information, including:

| Column | Description |
|---|---|
| sku_id | Unique product SKU identifier |
| category | Product category |
| name | Product name |
| mrp | Maximum Retail Price |
| discountPercent | Discount percentage |
| availableQuantity | Available inventory quantity |
| discountedSellingPrice | Discounted selling price |
| weightInGms | Product weight in grams |
| outOfStock | Product stock availability |
| quantity | Product quantity |

## Project Workflow

### 1. Database and Table Creation
- Created a PostgreSQL table named `zepto`.
- Defined appropriate data types for product attributes.
- Used SKU ID as the primary key.

### 2. Data Exploration
- Checked the total number of records.
- Retrieved sample product records.
- Identified NULL values.
- Explored distinct product categories.
- Compared in-stock and out-of-stock products.
- Identified product names appearing under multiple SKUs.

### 3. Data Cleaning
- Identified products with zero MRP or discounted selling price.
- Removed records with zero MRP.
- Converted product prices from paise to Indian rupees.

### 4. SQL Data Analysis

The project addresses the following eight business questions:

**Q1. Top 10 Best-Value Products**

Identified the top 10 products with the highest discount percentages.

**Q2. High-MRP Products That Are Out of Stock**

Identified out-of-stock products with an MRP greater than ₹300.

**Q3. Estimated Revenue by Category**

Calculated estimated inventory value for each category using discounted selling price and available quantity.

**Q4. High-Priced Products with Low Discounts**

Identified products with an MRP greater than ₹500 and a discount percentage below 10%.

**Q5. Top 5 Categories by Average Discount**

Calculated and ranked product categories based on their average discount percentage.

**Q6. Price Per Gram Analysis**

Calculated price per gram for products weighing at least 100 grams to compare product value.

**Q7. Product Weight Categorization**

Classified products into three weight categories:
- Low: Below 1,000 grams
- Medium: 1,000–4,999 grams
- Bulk: 5,000 grams and above

**Q8. Total Inventory Weight by Category**

Calculated the total inventory weight for each product category using product weight and available quantity.

## SQL Concepts Used

- CREATE TABLE
- DROP TABLE
- SELECT and DISTINCT
- WHERE conditions
- ORDER BY
- GROUP BY and HAVING
- Aggregate functions (COUNT, SUM, AVG)
- UPDATE and DELETE
- CASE statements
- ROUND()
- LIMIT
- NULL value handling
- Primary keys

## How to Run the Project

1. Install PostgreSQL.
2. Open pgAdmin 4 or another PostgreSQL client.
3. Create a database for the project.
4. Open the provided SQL script.
5. Execute the table creation statement.
6. Import the CSV dataset into the `zepto` table, matching the column structure.
7. Execute the remaining SQL queries to perform data exploration, cleaning, and analysis.

**Note:** The SQL script starts with `DROP TABLE IF EXISTS zepto`, which removes an existing table with that name. Run it carefully.

## Conclusion

This project demonstrates the use of PostgreSQL for exploring and analyzing e-commerce inventory data. It applies SQL techniques to examine pricing, discount patterns, product availability, inventory valuation, and product weight distribution.

The analysis provides a practical understanding of how SQL can be used to answer business-related questions and support data-driven decision-making.

## Project Files

- `ZeptoSQLDataAnalysis.sql` – SQL queries for data exploration, cleaning, and analysis.
- `zepto_v2.csv` – E-commerce inventory dataset.

