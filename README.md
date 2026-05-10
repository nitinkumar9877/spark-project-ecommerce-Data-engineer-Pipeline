# 🛒 ShopVista E-Commerce Analytics Pipeline (Azure Data Engineering Project)

## 📌 Project Overview

This project is a complete **end-to-end Azure Data Engineering Pipeline** built for processing and analyzing e-commerce sales data using modern ETL practices.

The system was designed to process both:

- Historical batch datasets
- Incremental daily incoming data

Initially, historical CSV datasets were uploaded into the system. Since the raw data contained missing values, duplicates, inconsistent formats, and unstructured records, a complete ETL workflow was developed using **PySpark on Azure Databricks**.

After validating the transformations using streaming-style processing, the pipeline was automated to run daily at **1:00 AM** to minimize production impact during peak client activity hours.

The final transformed data was used to build an interactive **Power BI Analytics Dashboard** for business insights and reporting.

---

# 🚀 Architecture

```text
Source System → ADLS → Databricks (Bronze → Silver → Gold) → Power BI
```

---

# 🏗️ Medallion Architecture

## 🥉 Bronze Layer
- Stores raw ingested CSV data
- Maintains original source records
- Supports traceability and auditing

## 🥈 Silver Layer
- Data cleaning and transformation
- Duplicate removal
- Null handling
- Data standardization
- Validation checks

## 🥇 Gold Layer
- Business-ready analytical tables
- Aggregated KPIs
- Fact and dimension modeling
- Reporting optimized datasets

---

# ⚙️ Technologies Used

| Technology | Purpose |
|---|---|
| Azure Data Lake Storage (ADLS) | Data Storage |
| Azure Databricks | Data Processing |
| PySpark | ETL Transformations |
| Delta Lake | Optimized Storage |
| Unity Catalog | Data Governance |
| SQL | Data Querying |
| Power BI | Dashboard & Reporting |

---

# 🔄 ETL Pipeline Workflow

## 1️⃣ Data Ingestion
- Uploaded historical CSV files into Azure Data Lake
- Configured incremental daily data ingestion
- Managed raw source data storage

## 2️⃣ Data Cleaning & Transformation
Implemented using **PySpark**:
- Removed duplicates
- Handled missing/null values
- Standardized data formats
- Applied business logic transformations
- Created derived columns and aggregations

## 3️⃣ Batch + Streaming Validation
- Initially validated the pipeline using streaming-style processing
- Ensured transformation reliability and stable outputs
- Later converted the workflow into scheduled batch execution

## 4️⃣ Gold Layer Aggregation
Created analytical datasets for:
- Revenue analysis
- Customer insights
- Product performance
- Regional analysis
- Channel-wise sales

---

# 🤖 Workflow Automation

Created automated Databricks Jobs for:
- Bronze Processing
- Silver Transformation
- Gold Aggregation
- Daily Summary Generation

Later, all jobs were merged into a single orchestrated workflow for complete ETL automation.

## ⏰ Scheduled Execution
- Daily at **1:00 AM**
- Selected to reduce production workload during active business hours

---

# 🔐 Data Governance & Security

Implemented governance using:
- Unity Catalog
- Role-based access control (RBAC)
- Group-level permissions

Sensitive datasets were secured according to user roles and access requirements.

---

# 📊 Power BI Dashboard Features

The dashboard provides interactive analytics including:

- Total Sales
- Units Sold
- Repeat Customer Rate
- Region-wise Customer Analysis
- Revenue Trends
- Brand Performance
- Category Performance
- Sales Channel Analysis

---

# 📈 Key Highlights

✅ End-to-End Azure Data Engineering Project  
✅ Automated ETL Workflow  
✅ Batch + Streaming Processing  
✅ Medallion Architecture  
✅ PySpark Transformations  
✅ Data Governance & RBAC  
✅ Interactive Power BI Dashboard  
✅ Incremental Daily Data Processing  
✅ Production-Style Pipeline Automation  

---

# 📂 Project Structure

```text
project/
│
├── bronze/
├── silver/
├── gold/
├── notebooks/
├── jobs/
├── dashboards/
├── datasets/
└── README.md
```

---

# 🎯 Project Outcome

Successfully built a scalable and production-style Azure Data Engineering pipeline capable of:

- Processing raw CSV datasets
- Handling incremental daily data ingestion
- Performing automated ETL transformations
- Managing secure governed datasets
- Delivering business insights through Power BI dashboards

This project demonstrates practical implementation of modern Data Engineering concepts including automation, governance, ETL processing, and analytics reporting.

---

# 👨‍💻 Author

**Nitin Kumar**  
B.Tech CSE (Data Science)  
Aspiring Data Engineer
