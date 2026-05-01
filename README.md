# vanguora-vintelligence-datathon-2026
This repository contains a pre-provided dataset simulating a Vietnamese fashion e-commerce business from July 2012 to December 2022. It supports tasks such as EDA, forecasting, customer analysis, and building machine learning models.

# 🧠 DATATHON 2026 – The Gridbreakers

## 📊 Sales Forecasting & Business Analytics Project

---

## 📌 Overview

This project is developed for **DATATHON 2026 – The Gridbreakers**, organized by VinTelligence (VinUniversity DS & AI Club).

The goal is to transform raw e-commerce data into **actionable business insights** and build a **revenue forecasting model** to support decision-making in a Vietnamese fashion retail company.

---

## 🎯 Objectives

This project addresses three main tasks:

**1. Exploratory Data Analysis (EDA) & Visualization**

   * Discover patterns, trends, and anomalies in the dataset.
   * Generate business insights through data storytelling.

**2. Business Analytics**

   * Understand customer behavior, product performance, and operational efficiency.
   * Provide actionable recommendations.

**3. Sales Forecasting**

   * Predict future **Revenue** based on historical data.
   * Optimize forecasting accuracy using machine learning models.

---

## 📂 Dataset Description

The dataset simulates operations of an **e-commerce fashion business in Vietnam (2012–2024)** and includes **15 CSV files**, categorized into 4 layers:

### 1. Master Data

* `products.csv` – Product catalog.
* `customers.csv` – Customer information.
* `promotions.csv` – Promotion campaigns.
* `geography.csv` – Location data.

### 2. Transaction Data

* `orders.csv` – Orders
* `order_items.csv` – Order details.
* `payments.csv` – Payment info.
* `shipments.csv` – Shipping data.
* `returns.csv` – Returns.
* `reviews.csv` – Customer reviews.

### 3. Analytical Data

* `sales.csv` – Revenue (training data).
* `sales_test.csv` – Forecasting target.

### 4. Operational Data

* `inventory.csv` – Inventory snapshots.
* `web_traffic.csv` – Website traffic.

---

## 🔗 Data Relationships

* `orders` ↔ `payments`: 1–1.
* `orders` ↔ `shipments`: 1–0/1.
* `orders` ↔ `returns`: 1–many.
* `orders` ↔ `reviews`: 1–many.
* `products` ↔ `inventory`: 1–many.

---

## 🛠️ Project Structure

```
📦 vanguora-vintelligence-datathon-2026
├── 📁 src/
│   ├── vanguora-vintelligence-datathon-2026-mcq.ipynb
│   ├── vanguora-vintelligence-datathon-2026-eda.ipynb
|   ├── vanguora-vintelligence-datathon-2026-visualization.ipynb
│   └── vanguora-vintelligence-datathon-2026-features&model.ipynb
├── 📁 report/
|   └── vanguora-vintelligence-datathon-2026-report.pdf
├── 📁 result/
├── └── submission.csv
└── README.md
```

---

## 📊 Exploratory Data Analysis (EDA)

Key analysis includes:

* Customer segmentation & behavior.
* Product performance & profit margins.
* Promotion effectiveness.
* Return patterns & reasons.
* Website traffic vs sales correlation.
* Inventory optimization insights.

---

## 📈 Modeling Approach

### 🔹 Problem

Build a forecasting model to predict daily Revenue for the period:

```
01/01/2023 → 01/07/2024
```
The objective is to capture sales patterns, seasonality, promotions, and operational factors affecting revenue performance.

### 🔹 Feature Engineering
The following features were created to improve model performance:
* Time-based features: day, week, month, quarter, seasonality.
* Lag features: previous revenue values (e.g., 1-day, 7-day, 30-day lag).
* Rolling statistics: moving average, rolling standard deviation.
* Promotion signals: discount campaigns, marketing activities.
* Inventory signals: stock availability, replenishment indicators.
* Traffic indicators: sessions, visits, customer activity.
### 🔹 Models Used
The main model used for forecasting:
* XGBoost.
Reasons for choosing XGBoost:
* Strong performance on structured/tabular data.
* Handles non-linear relationships effectively.
* Robust to missing values and feature interactions.
* High predictive accuracy for time-series regression with engineered features.

---
### 🔹 Hyperparameter Optimization
To improve performance, Optuna was used for automated hyperparameter tuning.
Optimized parameters include:
* n_estimators.
* max_depth.
* learning_rate.
* subsample.
* colsample_bytree.
* min_child_weight.
* gamma.
* reg_alpha.
* reg_lambda.

---
## 🔹 Evaluation Metrics

* **MAE (Mean Absolute Error).**
* **RMSE (Root Mean Squared Error).**
* **R² Score.**

Goal:

* Minimize MAE & RMSE.
* Maximize R² (closer to 1 is better).

---
## 🔹 Final Outcome
The tuned XGBoost + Optuna pipeline delivered strong forecasting performance and was selected as the final model for daily revenue prediction.

---
## 🚀 How to Run

### 1. Clone repository

```bash
git clone [(attach link here)]([https://drive.google.com/drive/folders/1Jg3fHJugJVlRgAq5aoQGmYV28adSFBoh?usp=drive_link](https://github.com/totrannhauyen/vanguora-vintelligence-datathon-2026.git))
cd vanguora-vintelligence-datathon-2026
```

### 2. Run notebook

```bash
src/
├── vanguora-vintelligence-datathon-2026-eda.ipynb
├── vanguora-vintelligence-datathon-2026-features.ipynb
├── vanguora-vintelligence-datathon-2026-visualization.ipynb
├── vanguora-vintelligence-datathon-2026-model.ipynb
└── vanguora-vintelligence-datathon-2026-mcq.ipynb
```

---

## 3. Output

File: `submission.csv`

```
Date,Revenue,COGS
2023-01-01,xxx,xxx
...
```

⚠️ Requirements:

* Keep original row order.
* No external data usage.
* Ensure reproducibility.

---

## 💡 Key Insights (Example)

* Certain product segments yield higher profit margins.
* Promotions significantly impact short-term revenue spikes.
* High return rates correlate with specific sizes/categories.
* Web traffic is a strong leading indicator of sales.

---

## 🧠 Business Recommendations

* Optimize inventory for high-demand segments.
* Personalize promotions by customer segment.
* Reduce return rates via sizing improvements.
* Invest in high-performing marketing channels.

---

## 📎 Reproducibility

* Random seeds are fixed.
* Full pipeline is provided.
* No external data is used.

---

## 👥 Team Members & Responsibilities

### 1/ Tô Trần Nhã Uyên – Data Processing & Exploration (Team Leader)

* Answering multiple-choice questions (Part 1).
* Data cleaning.
* Exploratory Data Analysis (EDA).
* Feature engineering.
* Data visualization.

---

### 2/ Trần Phú Nghĩa – Modeling

* Feature engineering.
* Model training & tuning (XGBoost).
* Forecasting **Revenue** & evaluation (MAE, RMSE, R²).

---

### 3/ Nguyễn Đình Sinh Quảng – Business Analysis & MCQ

* Answering multiple-choice questions (Part 1).
* Data visualization.
* Business insight extraction.
* Data storytelling.
* Contributing to final report.
* Supporting interpretation of results.

---

### 4/ Nguyễn Đức Nhật – Advanced Analysis

* Business insight extraction.
* Data storytelling.
* Contributing to final report.

---

## 🤝 Collaboration Workflow

* Member 1 leads coordination, preprocessing, feature engineering, and core model development.
* Member 2 develops and optimizes additional predictive models.
* Member 3 analyzes business insights and interprets results.
* Member 4 visualization, and reporting.
* All members collaborate on final submission and presentation.

---


---

## 📌 Competition Links

* Kaggle: https://www.kaggle.com/competitions/datathon-2026-round-1
* Report: [(attach link here)](https://drive.google.com/drive/folders/1Jg3fHJugJVlRgAq5aoQGmYV28adSFBoh?usp=drive_link)
* Github: [(attach link here)](https://github.com/totrannhauyen/vanguora-vintelligence-datathon-2026.git)

---

## 📜 License

This project is for academic and competition purposes only.
