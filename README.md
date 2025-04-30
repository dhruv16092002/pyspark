# PySpark Data Engineering Practice

This project showcases my hands-on experience using **PySpark** for building data pipelines and performing data transformations. The focus is on reading data from various **source systems**, applying **data cleaning and transformation logic**, and writing it to multiple **sink systems**.

## 📁 Project Structure

- `/mongo` – There is multiple Jupyter notebooks for mongodb connection and data cleaning
- `/Delta` – Folder containing the delta table in databricks and stored into azure blob storage
- `/mysql` – There is multiple Jupyter notebooks for Mysql connection and data cleaning
- `/S3` – There is multiple Jupyter notebooks for Aws-S3 connection and data cleaning
- `/BigQuery` – There is multiple Jupyter notebooks for Big Query (GCP) connection and data cleaning

## ✅ Key Features

### Data Sources (Read)

- MySQL
- MongoDB
- PostgreSQL
- Azure Blob Storage
- s3
- BigQuery

### Data Cleaning & Transformation

- Performed using PySpark DataFrame API
- SQL and NoSQL data cleaning handled with custom logic
- Schema validation and null handling
- String manipulation and date formatting
- Deduplication and standardization

### Data Sinks (Write)

- MySQL
- MongoDB
- PostgreSQL
- Azure Blob Storage (CSV/Parquet)
- s3
- BigQuery

### Tools & Platforms

- Apache Spark (PySpark)
- Databricks (Notebook experimentation and PySpark SQL usage)
- Jupyter Notebook for interactive development
- Docker and local database setup

## 🧪 Practice Use Cases

- Explored usage of PySpark with NoSQL data models (MongoDB)
- Wrote utility functions to convert raw JSON, CSV, and nested structures
- Migrated data across SQL and NoSQL systems with proper formatting

## 🚀 How to Run

1. Clone the repository
2. Ensure you have the required environments and drivers for databases
3. Update database connection strings in the notebook or config files
4. Run the Jupyter notebook: `pyspark_data_pipeline.ipynb`

## 📌 Requirements

- Python 3.10+
- PySpark
- MongoDB Connector for Spark
- Maven drivers for MySQL and PostgreSQL
- Azure Storage SDK (for blob access)
- Jupyter Notebook

## 🔧 Future Enhancements

- Modularize the notebook into Python scripts and functions
- Add unit tests for transformation logic
- Schedule jobs using Apache Airflow or Azure Data Factory

## 📚 Learnings

- Deepened understanding of PySpark DataFrames and transformations
- Worked with both SQL and NoSQL sources in a unified PySpark pipeline
- Improved data cleaning strategies across diverse data formats
- Gained experience with Databricks for Spark-based analytics

---

Feel free to raise any issues or suggestions to improve this pipeline.

