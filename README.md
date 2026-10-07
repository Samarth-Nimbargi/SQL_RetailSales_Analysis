# 🛒 Retail Sales Analysis — SQL Project

## 📌 Project Overview

This project analyzes a retail sales dataset using **MySQL** to understand sales performance, customer behavior, product categories, purchasing patterns, and sales trends.

The project focuses on using SQL to transform raw retail transaction data into meaningful business insights through **data cleaning, exploratory analysis, aggregation, filtering, CTEs, and window functions**.

---

## 🎯 Business Problem Statement

A retail business wants to better understand its sales transactions and customer purchasing behavior.
The objective is to use SQL to analyze this data and answer key business questions related to **sales performance, customer behavior, category performance, high-value transactions, monthly trends, and purchasing patterns**.

---

## 🗂️ Dataset / Database Structure

The project uses a single MySQL table:

### `retail_sales`

| Column            | Data Type | Description                   |
| ----------------- | --------- | ----------------------------- |
| `transactions_id` | INT       | Unique transaction identifier |
| `sale_date`       | DATE      | Date of the transaction       |
| `sale_time`       | TIME      | Time of the transaction       |
| `customer_id`     | INT       | Customer identifier           |
| `gender`          | VARCHAR   | Customer gender               |
| `age`             | INT       | Customer age                  |
| `category`        | VARCHAR   | Product category              |
| `quantity`        | INT       | Quantity purchased            |
| `price_per_unit`  | FLOAT     | Price per unit                |
| `cogs`            | FLOAT     | Cost of goods sold            |
| `total_sale`      | FLOAT     | Total sales value             |

---

# 🔄 Project Process

The analysis was performed through the following steps:

```text
Raw Retail Dataset
       ↓
Database & Table Creation
       ↓
Data Loading
       ↓
Data Cleaning
       ↓
Data Exploration
       ↓
Business Question Analysis
       ↓
SQL Aggregation & Filtering
       ↓
CTEs & Window Functions
       ↓
Business Insights
       ↓
Recommendations
```

---

# 🧹 1. Database & Data Cleaning

### Database Creation

```sql
CREATE DATABASE p1_retail_db;
USE p1_retail_db;
```

A `retail_sales` table was created with appropriate data types for transaction, customer, product, and sales information.

### Data Quality Checks

The dataset was checked for missing values in important columns such as:

* Transaction ID
* Sale date
* Sale time
* Gender
* Category
* Quantity
* COGS
* Total Sale

Records containing missing critical values were removed before analysis.

---

# 🔎 2. Data Exploration

Initial exploration was performed to understand the dataset.

### Key exploratory questions

* How many total sales transactions are present?
* How many unique customers are present?
* What product categories are available?

SQL functions used include:

* `COUNT()`
* `COUNT(DISTINCT)`
* `DISTINCT`

---

# 📊 3. Business Questions

The project answers the following **10 business questions**:

1. Retrieve all sales made on 2022-11-05.
2. Retrieve all Clothing transactions in Nov-2022 where the quantity sold is 4 or more.
3. Calculate the total sales for each category.
4. Find the average age of customers who purchased from the Beauty category.
5. Find all transactions where the total sale is greater than 1000.
6. Find the total number of transactions made by each gender in each category.
7. Calculate the average sale for each month and find the best-selling month in each year.
8. Find the top 5 customers based on the highest total sales.
9. Find the number of unique customers who purchased from each category.
10. Create sales shifts (Morning, Afternoon, Evening) and find the number of orders in each shift.

---

# 💡 Key Insights

The analysis can be used to identify the following business insights:

- **Revenue is evenly spread:** Total sales are 908,230 across 1,987 transactions. Electronics leads (311,445), closely followed by Clothing (309,995) and Beauty (286,790). Each category reaches a similar number of unique customers (141 to 149).
- **Clothing sells most often, Beauty sells for the most per order:** Clothing has the most transactions (698) but the lowest average order value (about 444). Beauty has the fewest transactions (611) but the highest average order value (about 469). Beauty customers average 40.42 years old.
- **Gender split is balanced:** Female customers made 1,012 transactions and male customers made 975. Only Beauty leans female (330 vs 281).
- **A few customers drive a big share of revenue:** The top 5 customers contributed 148,470, about 16.3% of total sales. Customer 3 alone spent 38,440.
- **Evening is the busiest shift:** 1,062 orders (53.4%) came in the evening, versus 548 in the morning and 377 in the afternoon.
- **Peak months and bulk orders:** Average sale per transaction peaked in July 2022 (541.34) and February 2023 (535.53). In Nov 2022, there were 17 Clothing orders of 4 units each (none above 4), and 11 transactions on 2022-11-05.

---

# 📌 Business Recommendations

Based on the analysis, a retail business could consider:

1. **Grow Beauty's reach.** It has the highest order value but the fewest transactions and customers. Targeted campaigns for female customers and the around-40 age group could lift volume.
2. **Raise Clothing basket value.** Bundles, multi-buy offers and upselling can increase revenue per order for the category with the most transactions.
3. **Retain top customers.** Introduce a loyalty or VIP program, since about 16% of revenue depends on just 5 customers.
4. **Plan around the evening peak.** Schedule staff and stock for after 18:00, and run time-limited offers to lift the quiet afternoon shift.
5. **Prepare for peak months.** Stock up and run campaigns ahead of July and February, but check total monthly revenue first, since this analysis used average sale.

---

# 🛠️ Tools & Technologies

* **Database:** MySQL
* **Language:** SQL
* **Development Environment:** MySQL Workbench
* **Version Control:** Git & GitHub

---

# 📁 Project Structure

```text
SQL-Retail-Sales-Analysis/
│
├── README.md
│
├── SQL - Retail Sales Analysis.sql
│
└── dataset/
    └── SQL - Retail Sales Analysis.csv
```

---

# 🚀 Skills Demonstrated

This project demonstrates practical experience with:

* SQL querying
* Data cleaning
* Data validation
* Exploratory data analysis
* Sales analysis
* Customer analysis
* Aggregation
* Date and time analysis
* CTEs
* Window functions
* Business problem solving
* Translating business questions into SQL queries
