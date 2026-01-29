# 📊 Vendor Performance Analysis & Pricing Strategy

## 📝 Project Context
This is a **Data Analysis project** focused on evaluating vendor performance to optimize procurement decisions. Instead of building a software tool, I performed an end-to-end analysis—from raw data ingestion to statistical hypothesis testing—to answer key business questions regarding **vendor selection** and **profitability**.

The goal was to identify which vendors provide the best value and determine if higher sales volume correlates with better profit margins.

---

## 🔍 Key Analysis Phases

### 1. 📥 Data Pipeline (ETL)
* **Notebook:** `Vendor DB+Data Ingestion -1.ipynb`
* **Task:** Automating the extraction of raw vendor files and loading them into **SQL Server** for structured querying.
* **Technique:** Used Python (`pandas`, `SQLAlchemy`) to handle data quality checks before storage.

### 2. 🧹 Exploratory Data Analysis (EDA)
* **Notebook:** `EDA_2.ipynb`
* **Task:** Cleaning and exploring the dataset to understand sales distribution and pricing trends.
* **Key Insight:** Created aggregated summaries to compare vendor pricing models vs. market averages.

### 3. 📉 Statistical Hypothesis Testing
* **Notebook:** `Vendor_Performance_Analysis_3.ipynb`
* **Task:** Validating assumptions using the **Two-Sample T-Test**.
* **Business Question:** *"Is there a statistically significant difference in profit margins between top-performing and low-performing vendors?"*
* **Outcome:** Provided data-backed recommendations on which vendors to retain or renegotiate with.

---

## 🛠️ Tools & Technologies Used
* **Python:** Main language for analysis.
* **SQL Server:** For data warehousing and querying.
* **Libraries:**
    * `Pandas` & `NumPy`: Data cleaning and manipulation.
    * `Seaborn` & `Matplotlib`: Visualizing trends and distributions.
    * `SciPy`: Conducting statistical tests (T-Test).
* **Power BI / Tableau (Optional):** Used for final dashboarding.

---

## 💡 Business Insights & Conclusion
Through this analysis, we derived the following insights:
* **Vendor Segmentation:** Classified vendors into 'Strategic Partners' (High Volume, High Margin) vs. 'At-Risk' vendors.
* **Pricing Optimization:** Identified products where vendor costs were significantly higher than the average, suggesting room for negotiation.
* **Statistical Validation:** Proved that sales volume does not always guarantee high profit margins, emphasizing the need for margin-focused KPIs.

---

## 🚀 How to Replicate This Analysis
1.  Clone the repo.
2.  Install requirements: `pip install -r requirements.txt`.
3.  Update the SQL connection string in the notebooks.
4.  Run the notebooks in order (1 -> 2 -> 3) to see the full analytical process.

---
![Dashboard Preview](<img width="1283" height="724" alt="Screenshot 2026-01-29 155018" src="https://github.com/user-attachments/assets/1c11abb0-df8d-4cfa-8588-c14c2b6a8973" />
)

