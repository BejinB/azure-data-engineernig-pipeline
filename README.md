# azure-data-engineernig-pipeline
## End-to-End Azure Data Engineering Pipeline using ADF, Databricks, ADLS Gen2, Synapse & Power BI


### 📌 Project Overview

The objective is to ingest raw data into a data lake using ADF, transform data using
Databricks (PySpark) to create curated Silver datasets, expose Gold-layer data using
Synapse Serverless SQL, and build analytical dashboards in Power BI.The pipeline follows the Medallion Architecture (Bronze–Silver–Gold) to ingest, transform, curate, and analyze data using modern Azure services.

---

### 🏗️ Architecture
![Architecture](architecture/lakehouse_architecture.png)

---
### 🛠️ Technologies Used
- Azure Data Factory (ADF)
- Azure Databricks (Apache Spark)
- Azure Data Lake Storage Gen2 (ADLS Gen2)
- Azure Synapse Analytics (Serverless SQL)
- Parquet
- SQL
- Power BI Desktop

### 🔄 Data Flow
1. **Bronze Layer – Raw Data**

   -Ingested using Azure Data Factory
   -Dynamic pipelines with Lookup + ForEach + Copy activity
      ![WhatsApp Image 2026-01-21 at 4 33 26 PM](https://github.com/user-attachments/assets/4dfabd6f-f36b-4a6e-b6d5-362548b888ac)

   -Stored as raw CSV files in ADLS Gen2


<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/aa4de290-ef8c-4276-9b8c-57ee393953cd" />

3. **Silver Layer – Cleaned & Transformed**

   -Processed using Azure Databricks (PySpark)
   -Schema inference, cleansing, and transformations applied
   -Stored in Parquet format for optimized analytics

<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/cce2c495-375d-44c7-9ff4-4d339d6b5036" />
<img width="1600" height="761" alt="image" src="https://github.com/user-attachments/assets/034f1333-bd12-4b52-a134-f09ff5253489" />
<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/8547fbf7-32b3-41b0-9add-0a1149755cd4" />

4. **Gold Layer – Curated & Analytics Ready**

   -Implemented using Azure Synapse Serverless SQL

   -Created:

      -Views on Silver data using OPENROWSET
<img width="1919" height="914" alt="image" src="https://github.com/user-attachments/assets/350ed720-4e41-48df-9f87-7886a0a2d2b4" />

      -External tables materialized into Gold
   <img width="1600" height="764" alt="image" src="https://github.com/user-attachments/assets/b8f4c520-a92c-47eb-98d7-c320d1876dde" />


   -Optimized for BI consumption

6. **Analytics & Visualization**

   -Power BI Desktop connected using Synapse SQL Endpoint

   -Built dashboards on Gold external tables

   -Enables serverless, pay-per-query analytics

📈 Example Insights:

   -Total Orders by Date
   -Customer Growth Trends
   -Sales Performance over Years
<img width="1600" height="849" alt="image" src="https://github.com/user-attachments/assets/87e350c0-a4d9-4d53-8c7e-9f3f44f19600" />




