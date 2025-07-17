
# 🛒 Customer Purchase Behavior Analysis – ETL & Reporting Project

This project delivers an end-to-end data pipeline and analytics solution for understanding and reporting customer purchase behavior in a retail business.  
It combines data engineering, analytics, and dashboarding to provide actionable insights into customer segments, loyalty behavior, and sales patterns.

---

## 🚀 Project Overview

The goal of this project was to:

- Build a robust ETL pipeline to ingest, clean, transform, and persist customer purchase data  
- Perform data quality checks and reconciliation to ensure trust in insights  
- Generate a denormalized reporting table with relevant dimensions and measures  
- Build an interactive dashboard to visualize customer behavior and sales trends  

---

## 🧰 Tech Stack & Tools Used

- ✅ **Python** – For data preparation, ETL scripts, and data quality automation  
- ✅ **Google BigQuery** – Data warehouse for storing staging, persistent, and reporting layers  
- ✅ **Google Looker Studio** – Dashboard and data exploration  
- ✅ **Jupyter Notebooks (.ipynb)** – Development and documentation of ETL workflows  
- ✅ **Visual Studio Code** – IDE for code authoring and debugging  

---

## 📈 Dashboard

<a href="https://lookerstudio.google.com/reporting/f308f1ef-97bf-4173-8854-cf38d6772227/page/ZwWRF" target="_blank">🔗 Click here to access the Looker Studio Dashboard</a>


This dashboard provides:

- Customer segmentation by loyalty, gender, and age group  
- Sales trends by region, category, and channel  
- Key KPIs: total sales, average spend per segment, top products  

---

## 📂 Workflow Steps

1. **Identify sample datasets for assignment**  
   Datasets covering *Customers, Products, Stores, Dates, Transactions* were identified and enriched for realism.

2. **Load data to stage tables**  
   Raw CSV files were loaded into BigQuery staging tables using Python and SQL.

3. **Data analysis & quality checks**  
   Initial data profiling was performed to confirm distributions and identify unrealistic uniformity.  
   Skewed datasets were generated to better reflect real-world behavior (e.g., 65% spend by males, 70% revenue from loyalty customers).

4. **Address data issues**  
   Issues like uniform distributions, nulls, and outliers were corrected before proceeding.

5. **Data monitoring & DQ checks**  
   Data quality checks (row counts, duplicates, null checks) were implemented in ETL and logged.

6. **Build persistent & reporting layers**  
   Data was loaded to the persistent layer after transformation.  
   A denormalized fact table was created for reporting by combining all relevant dimensions and measures.

7. **Reporting & dashboarding**  
   Reporting layer was connected to Looker Studio to build an interactive dashboard for business users.

---

## 📒 Notebooks

Jupyter notebooks documenting the ETL and analytics workflow:

- `1_File_to_Stage_Layer.ipynb` – Load raw CSVs to staging tables  
- `2_Stage_to_Persistent_Layer.ipynb` – Transform and load to persistent layer  
- `3_Reporting_Layer.ipynb` – Create denormalized reporting table  
- `4_SF_Customer_Analytics.ipynb` – Exploratory analytics and insights  

---

## ✅ Highlights

✨ Realistic, skewed customer behavior patterns to enable meaningful analysis  
✨ Data quality and reconciliation strategies baked into the pipeline  
✨ Denormalized fact table designed for fast reporting  
✨ Fully functional interactive dashboard showcasing actionable insights  

---

> This project demonstrates a complete data-to-dashboard solution for retail analytics use cases.  
> Focused on building trust through clean, insightful, and efficient data pipelines.
