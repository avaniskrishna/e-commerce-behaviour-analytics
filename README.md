# E-Commerce User Behavior Analytics: From Bot Detection to Customer Segmentation

## 📌 Project Overview
This project implements a complete end-to-end data pipeline for a multi-category online store. It addresses critical e-commerce challenges, including **anomaly detection (bot filtering)**, **customer value segmentation (RFM)**, and **retention analysis**, culminating in an interactive **Tableau Business Intelligence dashboard**.

## 🛠️ Tech Stack
* **Data Processing:** Python (Pandas, NumPy)
* **Visualization:** Tableau Desktop
* **Statistical Modeling:** RFM (Recency, Frequency, Monetary) Analysis, Cohort Retention Matrices
* **Engineering:** Velocity-based Bot Filtering

---

## 🚀 Key Features

### 1. Data Engineering & Bot Detection
* **Data Simulation:** Generated 80,000+ rows of raw user clickstream data (View, Add to Cart, Purchase).
* **Bot Injection:** Injected 5,000 "Burst Bot" events to test pipeline resilience against non-human traffic.
* **Velocity Filtering:** Developed a Python script that flags users exceeding 40 actions/hour, successfully isolating 50 bot accounts.
* **Relational Modeling:** Performed complex joins between transactional logs and RFM scoring tables to create a unified model in Tableau.

### 2. RFM Customer Segmentation
* **Scoring Logic:** Engineered a model based on **Recency, Frequency, and Monetary** values to categorize user value.
* **Quantile Ranking:** Used `pd.qcut` to rank users from 1 to 5 across all three metrics.
* **Segment Mapping:** Grouped users into four actionable tiers: **Champions, Loyal, At Risk, and Lost**.
* **Revenue Insight:** Identified that the "Champions" segment drives nearly 100% of the total **$970,734 revenue** in this dataset.

### 3. Cohort Retention Analysis
* **Retention Matrix:** Developed a Monthly Retention Matrix using `Cohort Month` to track user longevity.
* **The "Churn Cliff":** Discovered that retention drops from 100% in Month 1 to 23% by Month 3, highlighting a critical need for long-term engagement.



### 4. Interactive Tableau Dashboard
* **Conversion Funnel:** Visualized the user journey from **View (5,000 users)** to **Purchase (3,956 users)**, showing a 79% total conversion rate.
* **Action Filters:** Integrated segment-level drill-downs where selecting a customer tier (e.g., "At Risk") updates the funnel to show unique drop-off patterns.

---

## 📊 Strategic Business Insights

### 1. High-Value Customer Dependency (Pareto Risk)
* **Insight:** Analysis reveals that the **Champions** segment accounts for nearly **100% of total revenue**.
* **Recommendation:** Launch a tiered **Loyalty Program** to transition "Loyal" customers into the "Champion" bracket to diversify the revenue base.

### 2. The "Month 3" Retention Crisis
* **Insight:** While early retention is stable, there is a massive **77% churn rate** by the third month.
* **Recommendation:** Propose personalized "Win-back" coupons or automated email triggers starting at the 45-day mark to flatten the churn curve.

### 3. Funnel Optimization Opportunity
* **Insight:** Identified a **12.9% abandonment rate** specifically at the "Add to Cart to Purchase" stage.
* **Recommendation:** Implement **Abandoned Cart Push Notifications** or simplify the checkout UI to recover a portion of the $160,000+ currently sitting in "Lost" segment carts.
