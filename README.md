# 🚨 End-to-End Fraud Detection & Anomaly Detection System

A **production-style Machine Learning project** that detects fraudulent financial transactions using **supervised and unsupervised learning**, handles **extreme class imbalance**, applies **threshold tuning**, and delivers **business-ready insights via Power BI**.

This project is designed to be **resume-ready, interview-ready, and industry-aligned**.

---

## 📌 Table of Contents

1. Project Overview
2. Business Problem
3. Dataset Description
4. Tech Stack
5. Project Architecture
6. Step-by-Step Workflow
7. Machine Learning Models
8. Threshold Tuning Strategy
9. Evaluation Metrics
10. Key Visualizations (Graphs)
11. Power BI Dashboard
12. Folder Structure
13. How to Run the Project
14. Key Learnings
15. Resume Description

---

## 🔍 1. Project Overview

Financial fraud is rare but extremely costly. This project builds an **end-to-end fraud detection system** that:

* Detects fraudulent transactions from highly imbalanced data
* Minimizes missed frauds using recall-focused optimization
* Supports real-world scenarios with anomaly detection
* Enables decision-making using interactive dashboards

---

## 🧠 2. Business Problem

**Problem:**
Fraudulent transactions represent less than 1% of all transactions, making traditional accuracy-based models ineffective.

**Goal:**

* Maximize **fraud recall** (catch as many frauds as possible)
* Maintain acceptable false positives
* Provide interpretable outputs for business teams

---

## 📊 3. Dataset Description

**Source:** Kaggle – Credit Card Fraud Detection Dataset

**Details:**

* 284,807 transactions
* 492 fraud cases (0.17%)
* Features `V1–V28` are PCA-transformed
* `Amount`, `Time`, `Class` (Target)

**Target Variable:**

* `0` → Legitimate Transaction
* `1` → Fraudulent Transaction

---

## 🧰 4. Tech Stack

**Programming & ML**

* Python (3.9+)
* NumPy, Pandas
* Scikit-learn
* Imbalanced-learn (SMOTE)
* XGBoost

**Visualization**

* Matplotlib
* Seaborn
* Power BI

---

## 🏗 5. Project Architecture

```
Data (Kaggle CSV)
      ↓
EDA & Preprocessing
      ↓
Class Imbalance Handling (SMOTE)
      ↓
Model Training
(Logistic → Random Forest → XGBoost)
      ↓
Threshold Tuning
      ↓
Anomaly Detection (Isolation Forest)
      ↓
Predictions & Risk Scores
      ↓
Power BI Dashboard
```

---

## 🔄 6. Step-by-Step Workflow

### Step 1: Data Loading & Exploration

* Loaded raw transaction data
* Identified severe class imbalance
* Performed statistical analysis

### Step 2: Exploratory Data Analysis (EDA)

* Fraud vs Non-Fraud distribution
* Transaction amount patterns
* Time-based fraud behavior

### Step 3: Data Preprocessing

* Standardized transaction amounts
* Removed non-informative features
* Stratified train-test split

### Step 4: Handling Class Imbalance

* Applied **SMOTE** only on training data
* Ensured no data leakage

---

## 🤖 7. Machine Learning Models

### 1️⃣ Logistic Regression (Baseline)

* Simple, interpretable benchmark

### 2️⃣ Random Forest

* Captures non-linear patterns
* Strong performance on tabular data

### 3️⃣ XGBoost (Final Model)

* Gradient boosting for high accuracy
* Handles imbalance using `scale_pos_weight`
* Best recall–precision tradeoff

### 4️⃣ Isolation Forest (Unsupervised)

* Detects anomalies when labels are unavailable
* Industry-relevant for real fraud systems

---

## 🎯 8. Threshold Tuning Strategy

**Why Threshold Tuning?**

* Default probability threshold (0.5) misses frauds
* Fraud detection prioritizes **recall over precision**

**Approach:**

* Generated Precision–Recall curve
* Analyzed Recall vs Threshold graph
* Selected lower threshold (e.g. 0.2) to maximize recall

**Business Impact:**

* Fewer missed frauds
* Acceptable increase in false alerts

---

## 📐 9. Evaluation Metrics

Accuracy is misleading for imbalanced data.

**Used Metrics:**

* Recall (Primary)
* Precision
* ROC-AUC Score
* Confusion Matrix

---

## 📈 10. Key Visualizations (Graphs)

The following graphs were generated in Jupyter Notebook:

1️⃣ **Class Imbalance Plot**
Shows extreme imbalance between fraud and legitimate transactions

2️⃣ **Transaction Amount Distribution**
Helps identify unusual spending behavior

3️⃣ **Precision–Recall Curve**
Visualizes tradeoff between catching frauds and false alarms

4️⃣ **Recall vs Threshold Curve**
Used to select business-optimal probability threshold

5️⃣ **Feature Importance (XGBoost)**
Explains which transaction patterns influence fraud detection

---

## 📊 11. Power BI Dashboard

**Dashboard Capabilities:**

* Fraud rate & total fraud amount (KPIs)
* Fraud probability distribution
* Detected vs missed fraud analysis
* Transaction-level drill-down
* Risk-based filtering

**Audience:**

* Fraud analysts
* Risk management teams
* Business stakeholders

---

## 📁 12. Folder Structure

```
Fraud_Detection_Project/
│
├── creditcard.csv
├── fraud_detection.ipynb
├── fraud_predictions.csv
├── README.md
└── fraud_env/
```

---

## ▶️ 13. How to Run the Project

1. Clone or download the repository
2. Create and activate virtual environment
3. Install dependencies
4. Place `creditcard.csv` in project folder
5. Launch Jupyter Notebook
6. Run cells sequentially
7. Open Power BI and load `fraud_predictions.csv`

---

## 🧠 14. Key Learnings

* Handling extreme class imbalance is critical
* Recall matters more than accuracy in fraud
* Threshold tuning is a real-world necessity
* Unsupervised models add robustness
* Dashboards convert ML into business value

---

## 🏆 15. Resume Description (Ready to Use)

> Built an end-to-end fraud detection system using XGBoost with threshold tuning on highly imbalanced financial data, achieving high fraud recall, and designed an interactive Power BI dashboard for real-time fraud monitoring.

---

⭐ If you find this project useful, give it a star and feel free to fork or extend it!
