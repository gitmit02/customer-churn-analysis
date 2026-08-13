# 📊 AI-Powered SaaS Customer Churn & Sentiment Analytics

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Models-FFD21E?style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)

An end-to-end data analytics and Natural Language Processing (NLP) project that combines large-scale quantitative customer data with AI-classified qualitative feedback to identify root causes of customer churn and deliver actionable retention strategies.

---

## 📌 Project Overview

Customer churn is one of the most critical metrics for SaaS companies. While quantitative metrics (support tickets, subscription tiers) reveal *who* is churning, qualitative exit feedback reveals *why*.

This project processes **95,090 customer records** and utilizes zero-shot NLP models to analyze **~3,500 unstructured exit interview responses**. The aggregated data is transformed into an interactive Power BI dashboard and an executive strategy presentation.

<img width="1378" height="793" alt="dashboard_overview" src="https://github.com/user-attachments/assets/b5b24776-6973-43b8-b901-b1b31e4c2d1f" />


---

## 🛠️ Tech Stack & Skills

* **Data Processing & EDA:** Python, Pandas, NumPy
* **AI & NLP Classification:** Hugging Face Transformers (`zero-shot-classification`), PyTorch, Gemini API
* **Business Intelligence & Dashboard:** Power BI, DAX, Power Query
* **Executive Presentation:** Executive Storytelling, Data Visualization

---

## 🔑 Key Insights & Analytics

### 1. Quantitative Risk Factors
* **Overall Churn Rate:** **20.83%** (19,811 out of 95,090 customers).
* **Tier Vulnerability:** Lower-tier plans exhibit higher churn—**Standard (22.18%)** and **Basic (22.16%)**—compared to **Enterprise (15.08%)**.
* **The 4-Ticket Escalation Cliff:** Churn remains stable around ~20% for accounts logging 0–3 support tickets, but **spikes sharply past 30% once a customer logs 4+ tickets** (30.04% at 4 tickets, 33.90% at 6 tickets).

### 2. Qualitative Exit Drivers (AI Classification)
Out of 3,368 categorized text feedback responses:
1. 💰 **Price Concerns (32.9% / 1,108 users):** Renewal price increases and perceived lack of ROI.
2. 🎧 **Support Delays (26.7% / 898 users):** Unhelpful responses and long ticket resolution turnaround.
3. ⚙️ **Product & Performance (21.9% / 737 users):** Feature gaps, system bugs, and downtime.

### 3. Customer Sentiment Matrix
* **94.5% of departing users (3,184 / 3,368)** expressed **Disappointment** rather than sudden anger or frustration.
* **Top Crosstab Drivers:** `Price × Disappointed` (**1,075**) and `Support × Disappointed` (**867**).

---

## 🚀 Repository Structure

```text
├── data/
│   ├── structured_data.csv            # Raw numerical customer records
│   ├── exit_interviews.csv            # Raw unstructured text responses
│   └── final_merged_data.csv          # Cleaned & AI-classified unified dataset
├── notebooks/
│   └── classification_and_eda.ipynb   # Colab notebook for Hugging Face NLP & EDA
├── dashboard/
│   ├── Churn_Analytics.pbix           # Power BI Dashboard file
│   └── PowerBI_Churn_Dashboard.pdf    # Exported PDF view of the dashboard
├── presentation/
│   └── Executive_Presentation.pdf     # 5-Slide Executive Storytelling Presentation
└── README.md                          # Project Documentation

```
---

## ⚙️ How to Run the NLP Pipeline
1. **Clone the Repository:**
```text
git clone [https://github.com/your-username/saas-customer-churn-analytics.git](https://github.com/your-username/saas-customer-churn-analytics.git)
cd saas-customer-churn-analytics
```
2. **Install Required Packages:**
```text
pip install pandas numpy torch transformers
```
3. **Install Required Packages:**
Open notebooks/classification_and_eda.ipynb in Google Colab (with T4 GPU enabled) or locally to run the batch classification pipeline using Hugging Face's zero-shot-classification pipeline.
 
