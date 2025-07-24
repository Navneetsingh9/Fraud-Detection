# Fraud-Detection
## 📌 Project Overview

This project focuses on detecting fraud in mobile financial transactions, where some transactions have been falsely flagged by existing systems. The dataset includes various types of operations such as CASH-IN, CASH-OUT, DEBIT, PAYMENT, and TRANSFER.

I performed thorough Exploratory Data Analysis (EDA) to understand transaction patterns, followed by building machine learning models like Logistic Regression and XGBoost. The aim is to improve fraud detection accuracy and analyze the weaknesses of the current flagging algorithms.

Future steps include:
- Feature engineering (e.g., customer behavior profiling)
- Trying out more models (e.g., Random Forest, LightGBM)
- Comparing ensemble vs baseline methods

## 📦 Dataset Overview

The dataset includes millions of financial transactions across several transaction types:

| Transaction Type | Description |
|------------------|-------------|
| `CASH-IN`        | Depositing cash to increase account balance |
| `CASH-OUT`       | Withdrawing cash from the account |
| `DEBIT`          | Sending money to a bank account |
| `PAYMENT`        | Paying merchants for goods/services |
| `TRANSFER`       | Sending money to other users |

Each record includes:
- Transaction type
- Amount
- Sender/receiver account types and balances
- A flag indicating whether the transaction was fraudulent
- A flag indicating if the transaction was caught by the existing algorithm

Kaggle link-https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download

---
## 🧪 Steps Followed

### 1. 📊 Exploratory Data Analysis (EDA)
- Distribution of transaction types
- Patterns in fraud vs non-fraud
- Imbalance analysis
- Detection mismatches between `isFraud` and `isFlaggedFraud`

### 2. Models Applied
- **Logistic Regression**: As a baseline model due to its simplicity and interpretability.
- **XGBoost Classifier**: For more accurate and robust fraud prediction on imbalanced data.
- **(Planned)**: Random Forest, LightGBM, Neural Networks.

### 3. Preprocessing Techniques
- Dropped unnecessary columns like `nameOrig`, `nameDest`
- Scaled features where required
- Used class balancing
- Train/test split with stratification

---
## 📌 Key Findings

- Most fraudulent transactions are **CASH-OUT** and **TRANSFER**
- Many frauds go **undetected by the current flagging algorithm**
- Simple models like Logistic Regression perform reasonably well, but **tree-based models like XGBoost** yield significantly better recall and F1 scores.

---

## 🚀 Future Work

- Advanced feature engineering (e.g., transaction frequency)
- Model stacking and ensemble learning
- Deploying as an API or stream processor for real-time fraud detection

---

