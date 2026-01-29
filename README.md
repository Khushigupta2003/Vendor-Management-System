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

## 🧠 Data Analysis Conclusion & Business Insights

Based on the analysis performed in the notebooks, the following conclusions were drawn:

### 📉 1. Volume vs. Margin Trade-off
The Statistical T-Test analyzed whether "Top Vendors" (High Sales Volume) provide significantly better profit margins than "Low Vendors".
* **Finding:** *(Note: If your p-value was < 0.05)* The analysis suggests a **significant difference**, meaning high-volume vendors likely operate on thinner margins.
* **Recommendation:** High-volume vendors should not be judged solely on revenue. Negotiation strategies should focus on improving their margin percentages.

### 📊 2. Vendor Pricing Strategy
Through EDA, we identified that certain vendors consistently price products above the market average without adding proportional value.
* **Action:** These vendors are flagged for "Pricing Renegotiation".

### 🏆 3. Vendor Classification
Vendors have been segmented into:
* **Strategic Partners:** High Sales + High Margin (Retain & Reward)
* **Volume Drivers:** High Sales + Low Margin (Renegotiate Costs)
* **At-Risk:** Low Sales + Low Margin (Consider Dropping)

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

![Dashboard Preview](<img width="1283" height="724" alt="Screenshot 2026-01-29 155018" src="https://github.com/user-attachments/assets/7c833917-1f8b-4c1f-8207-800053664ea4" />
)

---
