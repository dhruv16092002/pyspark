# 🚀 PySpark ETL Architecture in Databricks  

This project demonstrates an **end-to-end ETL (Extract, Transform, Load) architecture** implemented in **Databricks using PySpark**. It is designed to connect with multiple **data sources**, perform **data transformation and business logic**, and load processed data into various **target systems** efficiently.  

The architecture supports **plug-and-play connectivity**, allowing you to read from any source system and write to any target database or cloud storage — all within Databricks notebooks.  

---

## 🏗️ ETL Architecture Overview  

![ETL Architecture in Databricks](./assets/etl_architecture.png)  

**Core Workflow:**  
1. **Extract** – Read data from multiple data sources (SQL, NoSQL, Cloud, APIs, etc.) using connectors and drivers.  
2. **Transform** – Clean, validate, and enrich the data using PySpark DataFrame and SQL APIs.  
3. **Load** – Write the processed data into target systems like Delta tables, MySQL, PostgreSQL, BigQuery, etc.  

---

## 📁 Project Structure  

| Folder | Description |
|--------|--------------|
| `/Mongo` | Contains multiple Databricks notebooks for MongoDB data extraction, transformation, and loading. |
| `/Mysql` | Includes notebooks for MySQL data ingestion, cleaning, and writing to target systems. |
| `/S3` | Contains notebooks for AWS S3 read/write operations using PySpark. |
| `/BigQuery` | Notebooks for reading and writing data to Google BigQuery (GCP). |
| `/Delta` | Notebooks demonstrating creation and management of Delta tables in Databricks (stored in Azure Blob or ADLS). |
| `/DynamicColumnMapping` | Logic to handle schema mapping dynamically between source and target systems. |

---

## ✅ Key Features  

### 🔹 Data Sources (Extract)  
- MySQL  
- MongoDB  
- PostgreSQL  
- Amazon S3  
- Azure Blob Storage  
- Google BigQuery  
- Oracle  
- FTP and APIs  

### 🔹 Data Cleaning & Transformation (Transform)  
- Built using **PySpark DataFrame API** and **SQL transformations**  
- Schema validation, null handling, deduplication, and standardization  
- Date and string formatting for consistent schema design  
- Support for **custom business logic** directly inside Databricks notebooks  
- Dynamic column mapping across data systems  

### 🔹 Data Targets (Load)  
- Delta Tables (Databricks / Azure)  
- MySQL  
- PostgreSQL  
- BigQuery  
- MongoDB  
- Amazon S3 / Azure Blob Storage (CSV/Parquet formats)  

---

## ⚙️ Tools & Technologies  

- **Databricks** – Notebook-based PySpark environment  
- **Apache Spark (PySpark)** – Core for distributed data processing  
- **Maven (MVN)** – For managing external JDBC connectors and JAR dependencies  
- **Python (pip)** – For installing and managing packages  
- **Docker** – Used for local testing of databases  
- **Cloud Platforms** – AWS, Azure, GCP  

---

## 🧪 Practice Use Cases  

- Data migration between SQL and NoSQL systems  
- Transformation of nested JSON and semi-structured data  
- Unified PySpark pipeline for heterogeneous data formats  
- Incremental data load with schema evolution handling  
- Writing ETL logic in Databricks notebooks for automation and testing  
