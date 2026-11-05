# upi-autopay-failure-analysis
Analyzing 50k transaction logs using MySQL and DuckDB to reduce involuntary subscription churn.
# 🚀 Optimizing UPI AutoPay: Reducing Peak-Hour Failures

### 📌 Project Overview
**Goal:** Reduce involuntary churn in recurring subscriptions by optimizing payment scheduling.
**Context:** Recent RBI & NPCI regulations on peak-hour transaction loads have caused a spike in auto-debit failures. This project analyzes **50,000 simulated transaction logs** to identify the root cause and proposes a **"Smart-Retry" algorithm** to recover lost revenue.

### 📊 Key Findings

| Metric | Peak Hours (10 AM - 1 PM) | Off-Peak Hours |
| :--- | :--- | :--- |
| **Failure Rate** | **32.74%** 🔴 | **12.15%** 🟢 |
| **Primary Cause** | **System Timeout (67.4%)** | Random Network Drops |

**Insight:** Failures during peak hours are largely due to bank server timeouts, not user balance issues. Shifting retries to 3 AM - 5 AM can potentially recover **18% of lost transactions**.

### 🛠️ Technical Stack
*   **Language:** Python (Pandas for data handling)
*   **Database Engine:** DuckDB (Running MySQL-compatible SQL queries)
*   **Visualization:** Matplotlib & Seaborn
*   **Presentation:** Canva (Strategy Deck)

### 📂 Repository Structure
*   `Razorpay_AutoPay_Optimization_Deck.pdf` ➡️ **The Strategy Deck (Start Here)**
*   `mandate_failure_analysis.ipynb` ➡️ The Python/SQL code used for analysis
*   `subscription_logs.csv` ➡️ The raw dataset generated for this case study
