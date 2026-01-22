# azure-data-engineernig-pipeline
## End-to-End Azure Data Engineering Pipeline using ADF, Databricks, ADLS Gen2, Synapse & Power BI


## 📌 Project Overview

The objective is to ingest raw data into a data lake using ADF, transform data using
Databricks (PySpark) to create curated Silver datasets, expose Gold-layer data using
Synapse Serverless SQL, and build analytical dashboards in Power BI.The pipeline follows the **Medallion Architecture (Bronze–Silver–Gold)** to ingest, transform, curate, and analyze data using modern Azure services.

---

## 🏗️ Architecture
<img width="1024" height="585" alt="image" src="https://github.com/user-attachments/assets/1ad49f5c-5a0a-4dd0-a8c5-2c2b91779547" />

---
## 🛠️ Technologies Used
- **Azure Data Factory** – Data ingestion & orchestration
- **Azure Data Lake Storage Gen2** – Central data lake
- **Azure Databricks** – Spark-based transformations
- **Azure Synapse Analytics (Serverless SQL)** – Views & external tables
- **Parquet** – Optimized storage format
- **Power BI Desktop** – Reporting & visualization

SQL & PySpark

## 🔄 Data Flow
### 🟤 Bronze Layer – Raw Data
- Ingested using Azure Data Factory
- Dynamic pipelines with Lookup + ForEach + Copy activity
   
<img width="1600" height="763" alt="image" src="https://github.com/user-attachments/assets/d8232798-5d23-421d-9a92-eb16e4a302b3" />

<img width="1600" height="760" alt="image" src="https://github.com/user-attachments/assets/240dd1b1-f2f3-49f2-91e5-df582f6e7437" />


- Stored as raw CSV files in ADLS Gen2



<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/aa4de290-ef8c-4276-9b8c-57ee393953cd" />


### ⚪ Silver Layer – Cleaned & Transformed

- Processed using Azure Databricks (PySpark)
- Schema inference, cleansing, and transformations applied
- Stored in Parquet format for optimized analytics


<img width="1600" height="761" alt="image" src="https://github.com/user-attachments/assets/034f1333-bd12-4b52-a134-f09ff5253489" />
<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/8547fbf7-32b3-41b0-9add-0a1149755cd4" />


### 🟡 Gold Layer – Curated & Analytics Ready

- Implemented using Azure Synapse Serverless SQL
- Created:
   - Views on Silver data using OPENROWSET
   
<img width="1600" height="760" alt="image" src="https://github.com/user-attachments/assets/bcef3eb5-e775-479d-9035-e2a317f6d13a" />


   - External tables materialized into Gold

      
<img width="1600" height="764" alt="image" src="https://github.com/user-attachments/assets/b8f4c520-a92c-47eb-98d7-c320d1876dde" />
<img width="1919" height="914" alt="image" src="https://github.com/user-attachments/assets/350ed720-4e41-48df-9f87-7886a0a2d2b4" />


-Optimized for BI consumption

### 📊 Analytics & Visualization

- Power BI Desktop connected using Synapse SQL Endpoint
- Built dashboards on Gold external tables
- Enables serverless, pay-per-query analytics

📈 **Example Insights:**

   - Total Orders by Date
   - Customer Growth Trends
   - Sales Performance over Years
   
<img width="1600" height="849" alt="image" src="https://github.com/user-attachments/assets/87e350c0-a4d9-4d53-8c7e-9f3f44f19600" />




