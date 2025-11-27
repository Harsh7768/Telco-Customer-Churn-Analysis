# Telco-Customer-Churn-Analysis
Predictive churn model using Logistic Regression. Features analyzed to define a High-Risk customer segment for targeted MRR savings.

---

### 1. Project Goal & Business Value

This project moves beyond simple customer prediction to define a **profit-driven retention strategy**. The primary objective was to leverage predictive analytics to isolate the customers most likely to churn and identify the underlying factors driving that decision, ensuring retention efforts yield the maximum **Return on Investment (ROI)**.

---

### 2. Technical Methodology & Performance

The analysis was executed using the following pipeline:

* **Data Preparation:** Handled data inconsistencies (e.g., converting blank strings to numeric values) and applied **One-Hot Encoding** to all categorical features to prepare the dataset for modeling.
* **Model:** Employed a **Logistic Regression Classifier** from `Scikit-learn`, chosen for its high **interpretability** and ability to yield feature coefficients.
* **Performance:** The model achieved an overall **Classification Accuracy of 82.19%** and a balanced **F1-Score of 0.64** on the holdout test set.

---

### 3. Key Technical Findings: Causal Feature Analysis

A rigorous **Feature Importance Analysis** was conducted on the model coefficients to isolate the true causal drivers of attrition: 

* **Contract Term is King:** **Contract\_Two year** was the strongest negative predictor of churn (coefficient $\approx 1.40$), while **Contract\_One year** was also highly influential, demonstrating that long-term commitment is the primary defense against churn.
* **Fiber Optic Risk:** **InternetService\_Fiber optic** was identified as the single strongest positive predictor of churn (coefficient $\approx 1.06$), suggesting that service quality, connection stability, or pricing for the premium service is a critical churn trigger.
* **Top 3 Absolute Drivers:** **Contract\_Two year**, **InternetService\_Fiber optic**, and **Contract\_One year**.

This analysis shows the business exactly where to focus effort for the highest impact.

---

### 4. Strategic Business Impact & Recommendation

The analytical insight was translated directly into an action plan:

* **Targeted Segmentation:** Defined a **High-Risk/High-Value customer segment** (based on churn probability and high monthly charges) that represents the most critical leakage point for the business, given the high overall churn rate of **26.54%**.
* **Monetary Justification:** The analysis identified a potential loss of **$10,000 to $15,000 in Monthly Recurring Revenue (MRR)** contained within this segment.
* **Recommendation:** Recommended shifting retention budget to exclusively target the identified high-risk segment with contract upgrade incentives (e.g., discounted 2-year terms).

---

### 5. Tech Stack

| Category | Tools |
| :--- | :--- |
| **Programming** | Python |
| **Data Manipulation** | Pandas, NumPy |
| **Modeling/Metrics** | Scikit-learn (LogisticRegression) |
| **Visualization** | Seaborn, Matplotlib |
---

**Final Action:** Commit 
