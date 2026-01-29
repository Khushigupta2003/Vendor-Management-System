# 📊 Vendor Performance Analysis System

## 📌 Project Overview
This project is an end-to-end data analysis solution designed to optimize **Supply Chain Management** by evaluating vendor performance. 

Instead of just analyzing data in Excel, I built an automated **ETL pipeline** using Python and SQL Server to ingest raw data, performed **Exploratory Data Analysis (EDA)** to understand sales trends, and conducted **Statistical Hypothesis Testing** to determine if high-sales vendors actually provide better profit margins.

The insights from this project help stakeholders make data-driven decisions on **Vendor Selection** and **Product Pricing**.

---

## 📂 Repository Structure & File Descriptions

Here is the breakdown of the coding modules used in this project:

### 1️⃣ `Vendor DB+Data Ingestion -1.ipynb` (ETL Pipeline)
* **Objective:** Automate the process of reading raw data files and storing them into a centralized database.
* **Key Logic:**
    * Connects to **Microsoft SQL Server** using `SQLAlchemy` and `PyODBC`.
    * Implements **Logging** to track ingestion time and status (`logs/ingestion_db.log`).
    * Cleans raw data and loads it into the `Vendor_Management_System` database.
    * Uses `fast_executemany=True` for optimized high-speed data insertion.

### 2️⃣ `EDA_2.ipynb` (Exploratory Data Analysis)
* **Objective:** Analyze the ingested data to find patterns in pricing and sales.
* **Key Logic:**
    * Aggregates data to create a `vendor_sales_summary` table.
    * Visualizes sales distribution using **Seaborn** & **Matplotlib**.
    * Prepares specific datasets for the Dashboard to highlight **Vendor Selection** criteria.
    * Exports processed summaries to CSV and SQL for further reporting.

### 3️⃣ `Vendor_Performance_Analysis_3.ipynb` (Statistical Testing)
* **Objective:** Validate business assumptions using statistics.
* **Key Logic:**
    * **Segmentation:** Classifies vendors into **"Top Performing"** (Top 25% by Sales) and **"Low Performing"** (Bottom 25% by Sales) using Quantiles (0.75 vs 0.25).
    * **Hypothesis Testing:** Performs a **Two-Sample T-Test** (Independent) to compare the **Profit Margins** of these two groups.
    * **Goal:** To check if high sales volume correlates with higher profitability or if "Top" vendors are actually hurting margins.

---

## 🚀 Business Impact & Key Findings

This analysis challenged the traditional belief that "Higher Sales Volume = Better Vendor." Through rigorous statistical testing, we derived the following strategic insights:

### 📉 1. The Volume-Profit Disconnect
Using an **Independent Two-Sample T-Test**, we rejected the null hypothesis ($p < 0.05$), proving that **Top-Tier Vendors operate on significantly thinner margins** compared to niche suppliers. This exposed a critical inefficiency in the current procurement strategy.

### 🧩 2. Vendor Segmentation Model
Instead of a "one-size-fits-all" approach, I developed a segmentation logic using **0.75/0.25 Quantiles**:
* **High-Value Partners:** Vendors delivering consistent profits (Target for long-term contracts).
* **Margin Diluters:** High-volume vendors eroding overall profitability (Target for immediate renegotiation).

### 💡 3. Operational Efficiency
By automating the **ETL pipeline with Python & SQL**, manual data entry errors were eliminated, reducing the data reporting turnaround time by **~40%** (estimated).
---

## 🛠️ Tech Stack & Tools Used
* **Languages:** Python (v3.x), SQL
* **Libraries:**
    * `Pandas`, `NumPy` (Data Manipulation)
    * `Seaborn`, `Matplotlib` (Visualization)
    * `SciPy` (Statistical Hypothesis Testing)
    * `SQLAlchemy`, `PyODBC` (Database Connection)
* **Database:** Microsoft SQL Server (MSSQL Express)
* **Visualization:** Power BI / Tableau (Dashboard linked below)

---

## 📸 Dashboard Preview

*(Here is a snippet of the interactive dashboard visualizing the insights)*

![Dashboard Preview](<img width="1283" height="724" alt="Screenshot 2026-01-29 155018" src="https://github.com/user-attachments/assets/7c833917-1f8b-4c1f-8207-800053664ea4"/>
)

---
