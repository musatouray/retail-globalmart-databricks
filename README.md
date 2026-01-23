## Global Mart Retail Analytics Platform
This is an end-to-end Data Lakehouse project built on Databricks, following the Medallion Architecture (Bronze, Silver, Gold). It covers real-world data engineering and analytics workflows using Spark, PySpark, SQL, Delta Lake, Unity Catalog, and CI/CD with Github. Designed for learning and portfolio building.

### Architecture
- Databricks Unity Catalog
- Medallion Architecture (Bronze / Silver / Gold)
- Star Schema (fact and dimensions)
- Power BI report

### Data Flow
Raw CSV → Bronze → Silver → Gold → Star Schema

### Gold Layer
- orders_gold (business-ready)
- dim_customers
- dim_products
- dim_geography
- dim_date
- fact_sales

### Orchestration
- Databricks Workflow
- Idempotent Delta MERGE pipelines
