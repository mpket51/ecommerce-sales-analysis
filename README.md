## E-Commerce Sales Analysis

### Tools: Python · SQL · PostgreSQL · Google Colab

## Project Overview

End-to-end data analysis project covering data cleaning, SQL business analysis, and star schema data modelling on a simulated e-commerce dataset of 500 orders.

## Dataset

- 500 orders · 13 columns

- Raw data included messy real-world issues: duplicates, missing values, inconsistent formats, outliers

- Products: Laptop, Phone, Monitor, Headphones, Webcam, Keyboard, Mouse, USB Hub

## What I Did

**1. Data Cleaning (Python / Pandas)**

- Removed 20 duplicate rows

- Standardized inconsistent text (gender, status, payment, region)

- Fixed 4 mixed date formats → YYYY-MM-DD

- Removed negative prices and outliers (>$5,000)

- Inferred gender from Myanmar customer name prefixes (Ko/U = Male, Ma/Daw = Female)

- Filled missing values using product-level median for prices

**2. SQL Business Analysis (PostgreSQL)**

- Total revenue: $212,878

- Top product: Laptop (38.5% of revenue)

- Top region: West ($88,740)

- Peak month: July ($25,251)

- 27% of orders still pending — identified as key business risk

**3. Data Modelling (Star Schema)**

- Designed and built Star Schema from flat table

- 1 Fact table + 5 Dimension tables (Customer, Product, Date, Location, Payment)

## Key Findings

- Laptop + Phone account for 66% of total revenue

- East region significantly underperforms vs West — potential growth opportunity

- Q1 (Jan–Mar) is the weakest sales period — promotions recommended

- PayPal is the dominant payment method (43.7%)

## Files

- `ecommerce_raw.csv` — original messy dataset

- `ecommerce_cleaned.csv` — cleaned dataset

- `ecommerce_analysis.ipynb` — full cleaning + modelling notebook

- `ecommerce_sql.sql` — SQL queries for business analysis

- `fact_orders.csv` · `dim_customer.csv` · `dim_product.csv` · `dim_date.csv` · `dim_location.csv` · `dim_payment.csv`
