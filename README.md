# Olist Data Engineering Project — Databricks + PostgreSQL (Render Cloud)

This project demonstrates a complete end-to-end **Data Engineering Pipeline** using the Olist e-commerce dataset.  
Data is stored in **PostgreSQL (Render Cloud)** and processed in **Databricks** using **PySpark** and the **Medallion Architecture** (Bronze → Silver → Gold).

---

## 🏗️ Architecture Overview

```
PostgreSQL (Render Cloud)
        ↓
  Bronze Layer (Raw Ingestion)
        ↓
  Silver Layer (Cleaned + Standardized + Joined)
        ↓
  Gold Layer (Business Metrics & Analytics Models)
```
  
**Insert architecture image here:**
  
![architecture](docs/architecture.png)

---

## 🧱 Tech Stack

| Layer | Technology |
|------|------------|
| Cloud Database | PostgreSQL (Render) |
| Processing Engine | Databricks (Apache Spark / PySpark) |
| Storage Format | Delta Lake Tables |
| Modeling Approach | Medallion Architecture |
| Languages | Python + SQL |
| Version Control | Git + GitHub |

---

## 📦 Dataset

| Table | Description |
|------|-------------|
| olist_customers_dataset | Customer identity and region data |
| olist_orders_dataset | Order timestamps and status records |
| olist_order_items_dataset | Transaction-level product sales |
| olist_products_dataset | Product catalog and metadata |

---

## 📁 Databricks Workspace Structure

```
project-olist/
│
├── 00_config/
│   ├── 00_env_variables
│   └── 01_test_connection
│
├── 01_ingestion_bronze/
│   ├── 01_load_customers
│   ├── 02_load_orders
│   ├── 03_load_order_items
│   └── 04_load_products
│
├── 02_transform_silver/
│   ├── 01_standardize_datasets
│   └── 02_join_core_tables
│
├── 03_analytics_gold/
│   ├── 01_sales_summary
│   ├── 02_product_ranking
│   └── 03_customer_lifetime_value
│
└── 04_exploratory/
    └── dashboard_analysis
```

---

## 🥇 Gold Layer Analytics Models

| Table | Purpose |
|------|---------|
| gold.sales_summary | Revenue & sales metrics |
| gold.product_ranking | Best-selling and most-profitable products |
| gold.customer_lifetime_value | Customer LTV segmentation for CRM strategy |

---

## 📊 Dashboard Visualizations

Insert your dashboard images here:

**1) Daily Sales Revenue Trend**
```
![daily_sales_trend](docs/daily_sales_trend.png)
```

**2) Top Product Categories by Revenue**
```
![product_ranking](docs/product_ranking_chart.png)
```

**3) Customer Lifetime Value (LTV) Distribution**
```
![ltv_distribution](docs/ltv_distribution.png)
```

**4) Customer Value Segmentation (RFM-style)**
```
![customer_segments](docs/customer_segments.png)
```

---

## 🚀 Next Enhancements (Roadmap)

- Add Airflow orchestration
- Add DBT for modular transformations
- Deploy dashboard to BI tools (Power BI / Looker Studio)

---

## 📄 License

MIT — Free to use for learning and portfolio purposes.

---

## ✨ Author

Made with ❤️ by Hugo.

