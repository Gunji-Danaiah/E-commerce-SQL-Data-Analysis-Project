# E-commerce SQL Data Analysis Project

## Project Overview
This project demonstrates SQL data analysis skills using an e-commerce database with SQLite.

## Files in this Repository
- `schema.sql` - Database schema with tables: customers, products, orders, order_items
- `insert_data.sql` - Sample data for testing
- `analysis_queries.sql` - All analysis queries used in this project
- `screenshots/` - Output screenshots for each query


## SQL Concepts Demonstrated
- SELECT statements with WHERE clause
- ORDER BY for sorting results
- GROUP BY with aggregate functions (COUNT, SUM, AVG)
- INNER JOIN and LEFT JOIN operations
- Subqueries for complex filtering
- Aggregate functions for business metrics
- Views for reusable queries
- NULL value handling with IFNULL and CASE
- Index creation for optimization

## Key Business Insights
- Identified top customers by spending
- Calculated average revenue per user (ARPU)
- Found customers with no orders
- Analyzed order patterns and customer behavior

## Author
Danaiah Gunji
Date: February 2026

## Sample Query - Average Revenue Per User
```sql
SELECT 
    COUNT(DISTINCT customer_id) as total_customers,
    SUM(total_amount) as total_revenue,
    ROUND(SUM(total_amount) / COUNT(DISTINCT customer_id), 2) as avg_revenue_per_user
FROM orders;
