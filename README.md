# AWS Garments Data Engineering Project

## 📌 Project Overview
This project demonstrates building a simple ETL pipeline using AWS cloud services.
The garments dataset was uploaded to Amazon S3, cataloged using AWS Glue, and queried using Amazon Athena.
Data visualization was created using Amazon QuickSight.

---

## 🛠 AWS Services Used
- Amazon S3 – Data storage
- AWS IAM – Role and permission management
- AWS Glue – Data catalog and crawler
- Amazon Athena – SQL query execution
- Amazon QuickSight – Data visualization dashboard

---

## 🔄 Project Workflow
1. Uploaded CSV dataset to S3 bucket.
2. Created IAM role with required permissions.
3. Configured Glue Crawler to scan S3 data.
4. Generated table in AWS Data Catalog.
5. Queried data using Athena.
6. Connected Athena to QuickSight for dashboard creation.

---

## 🧮 Sample SQL Queries

### View Sample Data
```sql
SELECT * 
FROM "AwsDataCatalog"."garments"."data"
LIMIT 5;
```

### Total Sales by Category
```sql
SELECT category, SUM(sales) AS total_sales
FROM "AwsDataCatalog"."garments"."data"
GROUP BY category;
```

### Sales Greater Than 5000
```sql
SELECT category, SUM(sales) AS total_sales
FROM "AwsDataCatalog"."garments"."data"
GROUP BY category
HAVING SUM(sales) > 5000;
```

---

## 🏗 Architecture

CSV File → Amazon S3 → AWS Glue Crawler → Data Catalog → Amazon Athena → QuickSight Dashboard

---

## 📊 Project Outcome
- Built end-to-end AWS ETL pipeline
- Successfully queried cloud data using SQL
- Created interactive dashboard in QuickSight

---

## 🚀 Skills Demonstrated
AWS | ETL | SQL | Data Engineering | Cloud Analytics | Business Intelligence
