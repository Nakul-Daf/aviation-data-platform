# Enterprise Aviation Data Platform: Case Study ✈️

> **Disclaimer:** *This repository is a portfolio case study. The actual codebase, proprietary data, and specific business logic remain confidential and are not shared here in compliance with Non-Disclosure Agreements (NDAs). The architectural patterns and methodologies described below represent my personal contributions to the enterprise solution.*

## 📖 Project Overview
This project involved designing and building a highly scalable, automated data platform for the aviation sector. The primary goal was to process massive volumes of telemetry and operational data, moving it through a Medallion architecture (Bronze-Silver-Gold) to enable advanced analytics, robust reporting, and downstream machine learning models.

## 🛠️ Technology Stack
* **Compute & Processing:** Azure Databricks, PySpark
* **Storage & Format:** Azure Data Lake Storage (ADLS Gen2), Delta Lake
* **Governance & Security:** Unity Catalog, Azure Key Vault
* **Orchestration:** Databricks Workflows, Apache Airflow, Azure Data Factory (ADF)
* **Languages:** Python, SQL

## 🏗️ Architecture & Methodology
### The Medallion Architecture
1.  **Bronze Layer (Raw Data):** * Ingested raw, untransformed data from multiple source systems.
    * Implemented mock data generation and datatype enforcement to guarantee initial schema integrity and prevent downstream pipeline failures.
2.  **Silver Layer (Cleansed & Conformed):** * Engineered PySpark pipelines to clean, filter, and transform the data across 20+ distinct schemas.
    * Designed process-mapping master tables to strictly align and standardize column names between the Bronze and Silver layers.
    * Executed complex data profiling (pattern matching, outlier detection, and null handling) to resolve quality issues prior to final transformation.
3.  **Gold Layer (Curated for Business):** * Developed and validated primary key logic to ensure accurate joins and data revalidation across large, complex datasets.
    * Created optimized Databricks notebooks and views dedicated to core KPI calculations for business intelligence consumption.

### Orchestration & Governance
* **Automated Workflows:** Replaced manual triggers with fully automated job orchestration utilizing Databricks Workflows and Apache Airflow, complete with intelligent retry logic for fault tolerance.
* **Data Governance:** Secured the entire data lifecycle using Databricks Unity Catalog, ensuring strict access controls and data lineage tracking.

## 🚀 Key Achievements & Impact
* Successfully delivered a scalable data layer that processes information across **20+ schemas**, significantly reducing data silos.
* Improved cross-team engineering consistency by introducing standardized process-mapping tables.
* Enhanced pipeline reliability by implementing robust data profiling and automated retry logic in Airflow, drastically reducing manual intervention during ETL failures.

---
*Created by [Nakul Daf](https://www.linkedin.com/in/nakul-daf/) | Data Engineer*
