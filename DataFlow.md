# 🔄 **End-to-End Data Flow Visualization Steps**

This document describes the **complete data pipeline** from raw data ingestion to reporting dashboard and monitoring.

---

## 1️⃣ **Source Data Identification**

Collect **sample CSV datasets**:
- `Customers`
- `Products`
- `Transactions`
- `Stores`
  
Made changes to these files by adding few new columns and metrics.

---

## 2️⃣ **Stage Layer (Raw Zone) – BigQuery**

✅ Load **raw CSVs** to **BigQuery staging tables** using Python scripts.  
✅ Data remains unchanged, retaining original structure.

### Tools Used:
- `pandas` – for reading CSVs
- `google-cloud-bigquery` – for loading data into BigQuery

📒 Notebook:  
- [`1_File_to_Stage_Layer.ipynb`](./1_File_to_Stage_Layer.ipynb)

🛠️ **Example Code:**
```python
 load_job = client.load_table_from_file(source_file, table_id, job_config=job_config)
```
---
## 3️⃣ Data Profiling & Validation
✅ Use Python to analyze staged data:
- Nulls, duplicates
- Distribution checks
- Skew simulation (e.g. loyalty ratio, gender-based spending)

📌 Notebooks:
1_File_to_Stage_Layer.ipynb
4_SF_Customer_Analytics.ipynb

---
## 4️⃣ Persistent Layer (Clean Zone) – BigQuery
✅ Apply cleaning, standardization, business logic
- Load data into normalized persistent tables
- Includes clean dimensions

💡 Key Actions:
- Deduplication
- Date formatting, standardization

Transformation logic (e.g., gender mapping)

📌 Notebook:
2_Stage_to_Persistent_Layer.ipynb
---
## 5️⃣ Reporting Layer (Semantic Layer)

✅ Build denormalized reporting table from persistent layer

- Combines facts and dimensions into a wide table for easy dashboarding

💡 Techniques:

✅ SCD2 implementation to track historical changes

Partitioning by date, clustering by frequently used filters.

---
## 6️⃣ Dashboarding with Looker Studio

✅ Connect BigQuery reporting table to Google Looker 

Build interactive visualizations

📊 Key Insights:
- Customer segmentation (loyalty, gender, age group)
- Regional/category sales breakdown  
- KPIs: sales, average spend, top products

## 7️⃣ Monitoring & Data Quality Automation

✅ Python-based checks implemented across pipeline:

- Row count checks between layers
- Null/duplicate checks
- Logging of issues

---
