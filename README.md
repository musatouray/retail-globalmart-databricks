## Global Mart Retail Analytics Platform

An end-to-end **Data Lakehouse analytics project** built on Databricks, following the **Medallion Architecture (Bronze, Silver, Gold)**.  
The project demonstrates real-world data engineering practices including incremental data loading, dimensional modeling, and analytics-ready data design using **Spark, PySpark, SQL, Delta Lake, and Unity Catalog**.

Designed as both a **learning project and a portfolio-grade implementation** aligned with production data engineering patterns.

---

### 🏗️ Architecture
- Databricks with Unity Catalog for governance
- Medallion Architecture (Bronze / Silver / Gold)
- Kimball-style Star Schema (facts and dimensions)
- Power BI for analytics and reporting

---

### 📈 Data Flow
Raw CSV → Bronze → Silver → Gold → Star Schema → Power BI

---

### 🥉 Bronze Layer
- Raw data ingestion from CSV files
- Minimal transformations
- Schema inference and storage as Delta tables (`orders_bronze`)

---

### 🥈 Silver Layer
- Data cleansing and standardization
- Type casting, validation, and basic data quality rules
- Schema evolution handled using Delta Lake
- Stored as Delta tables (`orders_silver`)

---

### 🥇 Gold Layer
- Enriched, business-ready fact-level order data (`orders_gold`)
- Dimensional modeling for BI and analytics use cases

### 🧠 Data Modeling Notes
- Fact table grain: one row per order line
- Surrogate keys used for all dimensions
- Dimensions implemented as SCD Type 1

**Star Schema (Power BI ready)**
- `dim_customers`
- `dim_products`
- `dim_geography`
- `dim_date`
- `fact_sales`

---

### 🔄 Orchestration
- Databricks Workflows for end-to-end pipeline execution
- Idempotent Delta MERGE operations for incremental and repeatable loads
