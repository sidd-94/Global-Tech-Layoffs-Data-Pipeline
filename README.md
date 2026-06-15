# Global-Tech-Layoffs-Data-Pipeline
Multi-stage SQL data pipeline built to ingest, clean, and standardise a volatile global dataset. Leverages Window Functions, CTEs, and self-joins to eliminate redundancy and fix data fragmentation.

# Global Tech Layoffs Data Pipeline & Analytics

## 📌 Project Overview
This project involved building a robust, multi-stage SQL staging environment to ingest, clean, and standardise a highly volatile global dataset tracking tech industry layoffs. The pipeline ensures data integrity, eliminates redundancy, and transforms raw strings into analysis-ready metrics without losing the primary data source.

## 🛠️ Tools & Technologies Used
* **SQL Flavour:** [e.g., PostgreSQL / MySQL / SQL Server]
* **Window Functions:** `ROW_NUMBER()` used for deduplication.
* **Common Table Expressions (CTEs):** For modular, readable, and high-performance querying.
* **Database Schema Modifications:** `ALTER`, `MODIFY` commands for structural fixes.
* **Advanced Joins:** Self-joins utilised for dynamic data recovery.

## ⚙️ Pipeline & Cleaning Steps
1. **Staging Environment:** Created a secure ingestion layer to isolate raw data from transformations.
2. **Deduplication:** Deployed Window Functions combined with CTEs to isolate and purge duplicate records, optimising storage.
3. **Data Standardisation:** Merged fractured categorical variables (e.g., consolidating fragmented industry names like 'Crypto%') and repaired geographic formatting.
4. **Data Recovery:** Implemented advanced self-joins to dynamically populate missing operational null fields based on historical company profiles.
5. **Type Casting:** Restructured text strings into formal `DATE` data types to enable accurate time-series analysis and forecasting.

## 📂 Repository Structure
* `/scripts`: SQL scripts organised by execution order (1_staging.sql, 2_cleaning.sql, 3_analytics.sql).
* `/schema`: Database architecture and data dictionary layout.
