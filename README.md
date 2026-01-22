# azure-data-engineernig-pipeline
## End-to-End Azure Data Engineering Pipeline using ADF, Databricks, ADLS Gen2, Synapse & Power BI


### 📌 Project Overview

The objective is to ingest raw data into a data lake using ADF, transform data using
Databricks (Spark) to create curated Silver datasets, expose Gold-layer data using
Synapse Serverless SQL, and build analytical dashboards in Power BI.

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
1. **Bronze Layer**  
   - Raw data ingested from GitHub using **Azure Data Factory**
   - Stored in ADLS Gen2 (CSV/JSON)

2. **Silver Layer**  
   - Data cleaned and transformed using **Azure Databricks (Spark)**
   - Stored in **Parquet format**

3. **Gold Layer**  
   - External tables created on Silver data using **Synapse Serverless SQL**
   - Optimized for analytics

4. **Analytics**  
   - Power BI connected to Synapse SQL endpoint
   - Reports built on Gold layer tables



## 📂 Repository Structure
