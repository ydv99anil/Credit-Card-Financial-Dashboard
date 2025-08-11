# Credit Card Financial Dashboard
This repository contains an end-to-end analytics solution for credit card business analysis using **MySQL and Power BI**. It includes **data modelling, SQL setup, data loading**, and an **interactive dashboard** for advanced financial and customer insights.

## 🚀 Project Overview
The dashboard enables real-time monitoring of key credit card metrics, helping analysts and business users:
- Track transaction trends, revenue, and interest earnings.
- Analyze customer demographics, segment performance, and satisfaction.
- Evaluate product uptake and utilization patterns.

## 📁 Repository Contents

| File/Folder | Description |
|-------------|-------------|
| `credit_card.csv` | Main transaction dataset |
| `customer.csv` | Customer demographic and profile data |
| `cc_add.csv` | Additional credit card transactional data |
| `cust_add.csv` | Additional customer data |
| `cc_sql.sql` | SQL script for creating MySQL database and tables |
| `Credit card dashboard.pbix` | Power BI dashboard file |
| `CREDIT_CARD_CUSTOMER_REPORT.pdf` | PDF report: customer insights |
| `CREDIT_CARD_TRANSACTION_REPORT.pdf` | PDF report: transaction analysis |


## 🛠️ How to Use
### 1. Database Setup
- Run cc_sql.sql in MySQL to create the database and tables.
- Import CSVs into MySQL using MySQL Workbench or:

## 2. Loading Data

**Importing with MySQL Workbench**

- Ensure `OPT_LOCAL_INFILE=1` is enabled in your connection settings.
- Use:
```sql
LOAD DATA LOCAL INFILE 'path/to/credit_card.csv'
INTO TABLE cc_detail
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
```

- Repeat the process for other CSVs and tables.

#### Troubleshooting
- Make sure local_infile is enabled on both server and client.
- Use the correct path, with proper folder separators (Windows: \, or /).

### 3. Power BI Dashboard

- Open Credit card dashboard.pbix in Power BI Desktop.
- Update database connection credentials.
- Refresh datasets and explore the reports:
- Explore the interactive dashboards:
  - Credit Card Transaction Report: Overall transactions, revenue, interest and product insights.
  - Credit Card Customer Report: Customer segments, age, income, gender, activation and behavior.

 ### 4. Reports
- View PDF reports for printable summaries of customer and transaction insights.


## 💡 Features
- Week-by-week revenue & interest tracking.
- Customer segmentation by demographics & geography.
- Card product performance analysis (Blue, Silver, Gold, Platinum).
- KPIs on utilization and spending patterns.

## 📊 Technologies
- MySQL – database & ETL
- Power BI – dashboard & visualization
- SQL – data transformation
- CSV – data storage

### Note:
Be sure to configure your database and local environment to enable CSV import as described above. For large datasets, the LOAD DATA LOCAL INFILE method is especially fast.
