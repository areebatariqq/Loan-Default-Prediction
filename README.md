# Loan-Default-Prediction

This project develops a classification model to predict the likelihood of a loan applicant defaulting, using real financial data. By identifying high-risk applicants, the model helps financial institutions reduce losses and make more informed lending decisions.

---

## 📁 Dataset

- **Source**: [Lending Club Loan Dataset](https://www.kaggle.com/datasets/wordsforthewise/lending-club) on Kaggle
- The dataset includes financial and personal information of loan applicants such as loan amount, annual income, credit history, employment length, debt-to-income ratio, and loan status (default or paid).

---

## 📌 Project Objective

- To build a predictive model that classifies whether a loan will default.
- To address data quality and imbalance for reliable predictions.
- To generate actionable insights and recommendations for lenders.

---

## 🔧 Tools and Technologies Used

- **Google Colab** (for implementation)
- **Python**
- **Pandas, NumPy, Matplotlib, Seaborn** (EDA & visualization)
- **Scikit-learn** (modeling and preprocessing)
- **LightGBM, SVM (Support Vector Machine)** (classification models)
- **SMOTE (Synthetic Minority Over-sampling Technique)** (for class imbalance)
- **Classification Metrics**: Precision, Recall, F1-Score, ROC-AUC

---

## 📊 Steps Performed

### 1. Data Preprocessing
- Removed irrelevant or high-missing-value columns.
- Encoded categorical features.
- Normalized/standardized numeric variables.
- Handled missing values with imputation techniques.
- Addressed class imbalance using **SMOTE** (to generate synthetic examples of default cases).

### 2. Model Training & Evaluation
- Trained two primary models:
  - **LightGBM Classifier**: Gradient boosting-based model known for handling large datasets.
  - **Support Vector Machine (SVM)**: Useful for finding hyperplanes that separate loan statuses.
- Evaluated models using:
  - **Precision** (minimize false positives)
  - **Recall** (identify all defaulters)
  - **F1-Score**
  - **ROC-AUC Curve**

### 3. Model Comparison
- Compared metrics and confusion matrices.
- Selected the best model based on **F1-Score and ROC-AUC**.

---

## ✅ Results

- **Best Model**: LightGBM (higher F1 and ROC-AUC)
- **Top Risk Indicators**:
  - High debt-to-income ratio
  - Low credit score / credit history
  - Length of employment < 1 year
  - Loan purpose (e.g., small business, medical)
  - Loan amount relative to income

---

## 📋 Business Recommendations

- **Stricter screening** for applicants with high DTI (Debt-to-Income).
- Require **longer employment history** for high loan amounts.
- Consider **loan purpose** in risk analysis.
- Use this model for **pre-approval risk scoring** to filter high-risk profiles early.

---

### 🧾 Input (Sample Applicant):
```json
{
  "Loan_Amount": 15000,
  "Annual_Income": 42000,
  "Credit_Score": 620,
  "Employment_Length": 1,
  "Debt_To_Income": 0.42,
  "Purpose": "small_business"
}

