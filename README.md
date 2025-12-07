# SuperStore-analytics-project-aws
📊 Sales Analytics Project Using SQL on AWS (S3 • Glue • Athena • QuickSight)

This project showcases an end-to-end data analytics pipeline on AWS, where I used IAM, S3, AWS Glue, Athena, and QuickSight to perform sales analysis on the db_hellosql.orders dataset.
The repository contains SQL scripts, transformation logic, and documentation of the analytics performed.

🚀 Project Overview

This project demonstrates how raw data can be:

Stored in Amazon S3

Cataloged using AWS Glue Data Catalog

Queried and analyzed using AWS Athena

Visualized in Amazon QuickSight

Secured using AWS IAM

The analysis includes:

Top-selling products

Average order value

Product-level sales summary

Query-based insights for dashboards

🛠️ AWS Services Used

**✔ AWS IAM**

Created IAM roles and policies

Managed secure access to S3, Glue, Athena and QuickSight

Followed least-privilege access

**✔ Amazon S3**

Used as the data lake to store raw and processed datasets

Folder structure for organized analytics

**✔ AWS Glue**

Built a Glue Crawler to automatically infer schema

Created Glue Data Catalog tables

Enabled Athena to query the dataset

**✔ AWS Athena**

Used for all SQL-based analytics

Performed transformations & calculations

Ran analytical queries on datasets in S3

**✔ Amazon QuickSight**

Connected Athena as a data source

Built dashboards for:

Top products

Revenue summary

Average order value

Order trends

📂 Repository Structure

superstoreanalysis/
├── queries/
└── README.md/
├──IMAGES

🧠 SQL Queries Included
1️⃣ Top 5 Products by Total Sales
SELECT product, SUM(sales) AS total_sales
FROM db_hellosql.orders
GROUP BY product
ORDER BY total_sales DESC
LIMIT 5;

2️⃣ Average Order Value (AOV)
SELECT 
    SUM(sales) / COUNT(DISTINCT "order id") AS avg_order_value
FROM db_hellosql.orders;

3️⃣ Sales Summary by Product
SELECT 
    product,
    SUM(sales) AS total_sales,
    COUNT(DISTINCT "order id") AS total_orders,
    AVG(sales) AS avg_sales_per_order
FROM db_hellosql.orders
GROUP BY product
ORDER BY total_sales DESC;

🎯 What This Project Demonstrates

This project highlights my ability to work with AWS Cloud analytics stack:

✔ Building and managing S3 data lake
✔ Creating schemas using Glue Crawler
✔ Running SQL analytics using Athena
✔ Implementing secure access via IAM
✔ Designing dashboards in QuickSight
✔ Writing clean, structured SQL for business insights

📈 Visualizations in QuickSight (Summary)

Top 5 Products by Sales

Average Order Value Trend

Revenue by Product Category

Order Volume Overview

Sales Summary Dashboard

🔮 Future Enhancements

Build a Glue ETL job to clean/transform data

Add monthly/quarterly trend analysis

Integrate Athena CTAS queries

Add Power BI / Tableau alternative dashboard

🙌 Connect With Me

GitHub: (https://github.com/MOHDAKRAM43/)
LinkedIn: (https://www.linkedin.com/in/mohd-akram-6a210a259/)
