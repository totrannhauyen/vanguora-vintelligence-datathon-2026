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

1. **📍 Exploratory Data Analysis (EDA) & Visualization**

   * Discover patterns, trends, and anomalies in the dataset
   * Generate business insights through data storytelling

2. **📍 Business Analytics**

   * Understand customer behavior, product performance, and operational efficiency
   * Provide actionable recommendations

3. **📍 Sales Forecasting**

   * Predict future **Revenue** based on historical data
   * Optimize forecasting accuracy using machine learning models

---

## 📂 Dataset Description

The dataset simulates operations of an **e-commerce fashion business in Vietnam (2012–2024)** and includes **15 CSV files**, categorized into 4 layers:

### 🔹 1. Master Data

* `products.csv` – Product catalog
* `customers.csv` – Customer information
* `promotions.csv` – Promotion campaigns
* `geography.csv` – Location data

### 🔹 2. Transaction Data

* `orders.csv` – Orders
* `order_items.csv` – Order details
* `payments.csv` – Payment info
* `shipments.csv` – Shipping data
* `returns.csv` – Returns
* `reviews.csv` – Customer reviews

### 🔹 3. Analytical Data

* `sales.csv` – Revenue (training data)
* `sales_test.csv` – Forecasting target

### 🔹 4. Operational Data

* `inventory.csv` – Inventory snapshots
* `web_traffic.csv` – Website traffic

---

## 🔗 Data Relationships

* `orders` ↔ `payments`: 1–1
* `orders` ↔ `shipments`: 1–0/1
* `orders` ↔ `returns`: 1–many
* `orders` ↔ `reviews`: 1–many
* `products` ↔ `inventory`: 1–many

---

## 🛠️ Project Structure

```
📦 vanguora-vintelligence-datathon-2026
├── 📁 src/
│   ├── preprocessing.py
│   ├── features.py
│   └── model.py
├── 📁 report/
│   ├── report.tex
|   └── report.pdf
├── submission.csv
├── requirements.txt
└── README.md
```

---

## 📊 Exploratory Data Analysis (EDA)

Key analysis includes:

* Customer segmentation & behavior
* Product performance & profit margins
* Promotion effectiveness
* Return patterns & reasons
* Website traffic vs sales correlation
* Inventory optimization insights

---

## 📈 Modeling Approach

### 🔹 Problem

Forecast daily **Revenue** for the period:

```
01/01/2023 → 01/07/2024
```

### 🔹 Feature Engineering

* Time-based features (day, month, seasonality)
* Lag features & rolling statistics
* Promotion & inventory signals
* Traffic-based indicators

### 🔹 Models Used

* Linear Regression
* Random Forest
* XGBoost / LightGBM
* Time Series Models (ARIMA / Prophet)

---

## 📏 Evaluation Metrics

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score**

Goal:

* Minimize MAE & RMSE
* Maximize R² (closer to 1 is better)

---

## 🚀 How to Run

### 1. Clone repository

```bash
git clone https://github.com/your-repo/datathon-2026.git
cd datathon-2026
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run pipeline

```bash
python src/preprocessing.py
python src/features.py
python src/model.py
```

---

## 📤 Submission Format

File: `submission.csv`

```
Date,Revenue,COGS
2023-01-01,xxx,xxx
...
```

⚠️ Requirements:

* Keep original row order
* No external data usage
* Ensure reproducibility

---

## 💡 Key Insights (Example)

* Certain product segments yield higher profit margins
* Promotions significantly impact short-term revenue spikes
* High return rates correlate with specific sizes/categories
* Web traffic is a strong leading indicator of sales

---

## 🧠 Business Recommendations

* Optimize inventory for high-demand segments
* Personalize promotions by customer segment
* Reduce return rates via sizing improvements
* Invest in high-performing marketing channels

---

## 📎 Reproducibility

* Random seeds are fixed
* Full pipeline is provided
* No external data is used

---

## 👥 Team Members & Responsibilities

### 1/ Tô Trần Nhã Uyên – Data Processing & Exploration

* Data preprocessing & cleaning
* Exploratory Data Analysis (EDA)
* Feature engineering
* Data visualization

---

### 2/ Trần Phú Nghĩa – Modeling & MCQ

* Model selection & training
* Hyperparameter tuning
* Time series forecasting
* Model evaluation (MAE, RMSE, R²)
* Generate final `submission.csv`
* Answering multiple-choice questions (Part 1)

---

### 3/ Nguyễn Đình Sinh Quảng – Business Analysis & MCQ

* Business insight extraction
* Data storytelling
* Answering multiple-choice questions (Part 1)
* Supporting interpretation of results

---

### 4/ Nguyễn Đức Nhật – Advanced Analysis

* Deep-dive analysis across multiple datasets
* Cross-table insights (customer, product, inventory, traffic)
* Supporting EDA & validation of findings
* Contributing to final report

---

## 🤝 Collaboration Workflow

* Member 1 prepares clean dataset and features
* Member 2 builds and optimizes models
* Member 3 & 4 analyze results and generate insights
* All members contribute to final report and submission

---


---

## 📌 Competition Links

* Kaggle: https://www.kaggle.com/competitions/datathon-2026-round-1
* Report: (attach link here)

---

## 📜 License

This project is for academic and competition purposes only.
