# E-commerce Order Analysis SQL Project

## Overview

This project utilises SQL to analyse online order data from an e-commerce store. The analysis aims to provide insights into sales trends, customer behaviour, product performance, and account manager effectiveness.

## Table of Contents

1. [Data Sources](#data-sources)
2. [Setup Instructions](#setup-instructions)
3. [SQL Queries](#sql-queries)
4. [Key Insights](#key-insights)
5. [Future Enhancements](#future-enhancements)


## Data Sources

The project uses the following tables:

- `orders`: Contains information about each order (order_no, order_date, ship_date, total, etc.)
- `products`: Product information (product_id, product_name, product_category, retail_price, etc.)
- `account`: Account details (account_id, account_manager, city, etc.)

## Setup Instructions

1. Ensure you have a SQL database system installed (e.g., MySQL).
2. Create a new database named `abc_orders` using the command:
   ```sql
   CREATE DATABASE abc_orders;
   USE abc_orders;

Run the setup.sql script to create the necessary tables and import data.
Update the date format in the orders table:

SET SQL_SAFE_UPDATES = 0;
UPDATE orders
SET order_date = STR_TO_DATE(order_date, '%m/%d/%Y'),
ship_date = STR_TO_DATE(ship_date, '%m/%d/%Y');
ALTER TABLE orders
MODIFY COLUMN order_date date, 
MODIFY COLUMN ship_date date;
SET SQL_SAFE_UPDATES = 1;


SQL Queries
The project includes various SQL queries for in-depth analysis:

• Revenue analysis by product category
• Count of unique products ordered
• Yearly revenue analysis
• Order date range analysis
• Product category with lowest average price
• Top 10 highest performing products
• Revenue and profit analysis by account manager
• Highest selling product analysis for 2017
• Average order amount by customer type
• 5th highest selling product
• Lowest selling product
•Most profitable product

Key Insights
(This section will be populated with key findings after running the analyses. Some potential insights based on the queries:)

• Product category performance in terms of revenue
• Year-over-year revenue trends
• Price range and performance of different product categories
• Top-performing products and their characteristics
• Account manager performance in terms of revenue and profit
• Customer spending patterns by type
• Identification of best-selling and underperforming products

Future Enhancements

• Implement more advanced analytics such as customer lifetime value calculation and churn prediction
• Create visualisations using a BI tool like Power BI or Tableau
• Automate the data import process for real-time analysis
• Develop a dashboard for easy monitoring of key performance indicators
