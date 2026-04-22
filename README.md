# Student Financial Behavior & Spending Pattern Analysis

## Project Overview
An end-to-end data analytics project analyzing spending patterns 
of 1,000 university students across 9 spending categories.

## Tools Used
- **Excel** — Initial data exploration and cleaning
- **PostgreSQL** — Database design, storage, and SQL analysis
- **Power BI** — Interactive dashboard and visualization

## Dataset
- 1,000 students, 9 spending categories
- 9,000 rows in long format after transformation
- Period: January 2026

## Key Findings
- Total monthly student spending: $1,795,083
- Housing is the largest expense at 38.8% of total spending
- 98.6% of students spend beyond their monthly income
- Average student spends 195% of their monthly income
- Card and UPI payment methods show identical spending behavior

## Repository Structure
- `data/` — Cleaned dataset in CSV format
- `sql/` — SQL scripts for table creation, data loading, and analysis
- `docs/` — Project documentation and query reference
- `powerbi/` — Power BI dashboard file

## Database Schema
Star schema with 3 tables:
- `dim_students` — Student demographic information
- `dim_categories` — Spending categories with necessity flags  
- `fact_spending` — Individual spending transactions

## How to Run
1. Install PostgreSQL
2. Run `sql/01_create_tables.sql` to create the schema
3. Import `data/student_spending_long.csv` into staging table
4. Run `sql/02_load_data.sql` to populate dimension and fact tables
5. Run `sql/03_analysis_queries.sql` for all analysis queries
6. Open `powerbi/student_spending.pbix` in Power BI Desktop
