# 🚀 Fraud Detection at Scale

An end-to-end machine learning project to detect fraudulent financial transactions in a highly imbalanced dataset.

---

## 📌 Problem Statement

Fraud detection is challenging due to:
- Extreme class imbalance (~0.13% fraud)
- High cost of missed fraud (false negatives)
- Need to control false alarms (false positives)

The goal is to build a model that maximizes fraud detection while keeping false alerts manageable.

---

## 🧠 Approach

### 1. Data Understanding & EDA
- Explored transaction patterns
- Identified fraud concentration in specific transaction types
- Detected heavy skew in transaction amounts

### 2. Feature Engineering
- Created balance-based features
- Log-transformed skewed variables
- Built domain-informed ratios

### 3. Handling Imbalance
- Used time-based train/validation/test split
- Applied threshold tuning instead of relying on default 0.5

### 4. Modeling
- Baseline: Logistic Regression
- Advanced: XGBoost

### 5. Key Insight: Data Leakage
- Detected leakage via feature importance
- Removed leakage features
- Re-trained model for realistic performance

---

## 📊 Final Model Performance (XGBoost)

- **Precision:** 0.85  
- **Recall:** 0.92  
- **F1 Score:** 0.88  
- **PR AUC:** 0.967  

### Confusion Matrix (Test Set)

- Fraud detected: 3674  
- Fraud missed: 334  
- False alarms: 636  

---

## 📈 Model Comparison

| Model                | Precision | Recall | F1 Score |
|---------------------|----------|--------|----------|
| Logistic Regression | 0.96     | 0.50   | 0.66     |
| XGBoost             | 0.85     | 0.92   | 0.88     |

---

## 📉 Evaluation Metrics

- ROC Curve
- Precision-Recall Curve (primary metric for imbalance)
- Threshold tuning analysis

---

## ⚠️ Key Learnings

- Default thresholds are not suitable for imbalanced data
- High performance can indicate data leakage
- Feature importance is critical for debugging models
- Recall vs precision tradeoff must be aligned with business needs

---

## 🛠 Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib

---

## 📦 Future Improvements

- Real-time fraud detection pipeline
- Model monitoring for concept drift
- Advanced ensemble methods
- Cost-sensitive optimization




Tasmiah  
