# Diabetes-Prediction-using-Machine-Learning
# 🩺 Diabetes Prediction using Machine Learning  

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-0.24-orange?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)  
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)  
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen)](https://github.com/your-username/diabetes-prediction-ml)  

---

## 📖 Project Overview  

This project focuses on **predicting diabetes** using patient demographic and medical data. It demonstrates a complete Machine Learning workflow, including:  

- Data Cleaning & Preprocessing  
- Outlier Treatment & Encoding  
- Class Imbalance Handling with SMOTE  
- Model Training & Hyperparameter Tuning  
- Evaluation & Comparison of Logistic Regression vs Random Forest  
- Visualization of Results  

The **Random Forest model** achieved the best ROC-AUC performance.

---

## 📂 Dataset  

**Source:** Local CSV (`diabetes_prediction_dataset.csv`)  
**Total Records:** 100,000  
**Target Column:** `diabetes` (0 = No, 1 = Yes)

### Features:  

| Feature               | Type     | Description |
|-----------------------|----------|-------------|
| gender                | Categorical | Patient gender |
| age                   | Numeric  | Age in years |
| hypertension          | Binary   | Hypertension presence |
| heart_disease         | Binary   | Heart disease presence |
| smoking_history       | Categorical | Smoking history |
| bmi                   | Numeric  | Body Mass Index |
| HbA1c_level           | Numeric  | Glycated hemoglobin level |
| blood_glucose_level   | Numeric  | Blood glucose level |
| diabetes              | Binary   | Target variable |

**Dataset Stats:**  
- No missing values  
- 3,854 duplicate rows (removed)  
- Class imbalance: ~8.5% positive class  

---

## 🧹 Data Preprocessing  

**Steps performed:**  

1. **Duplicate removal**  
2. **Outlier treatment** using IQR capping  
3. **Categorical encoding:** One-Hot Encoding for `gender` & `smoking_history`  
4. **Train/Test split:** 80% train / 20% test (stratified)  
5. **SMOTE oversampling** applied in pipeline for class imbalance  

---

## 🤖 Models Implemented  

### 1️⃣ Logistic Regression  
- StandardScaler  
- SMOTE oversampling  
- Class weight = balanced  
- Evaluated with 5-fold cross-validation ROC-AUC  

### 2️⃣ Random Forest  
- Hyperparameter tuning via **RandomizedSearchCV**  
- 3-fold cross-validation  
- Optimized for **ROC-AUC**  

---

## 📊 Model Performance  

| Model                | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|----------------------|----------|-----------|--------|----------|---------|
| Logistic Regression  | 0.8808   | 0.4165    | 0.8762 | 0.5646   | 0.9591  |
| Random Forest        | 0.9258   | 0.5520    | 0.8414 | 0.6667   | 0.9728  |

**✅ Best Model:** Random Forest (highest ROC-AUC)

---

## 🔍 Feature Importance  

**Top 5 Features (Random Forest):**  

1. HbA1c_level  
2. blood_glucose_level  
3. age  
4. bmi  
5. hypertension  

---

## 📈 Visualizations  

- Class distribution  
- Boxplots for outlier analysis  
- Confusion matrices for both models  
- ROC curve comparison  
- Precision-Recall curve comparison  
- Metrics bar chart  

---

## 🛠 Technologies Used  

- Python 3.11  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Imbalanced-learn (SMOTE)  

---

## 🚀 How to Run  

1. Clone repository:  
```bash
git clone https://github.com/your-username/diabetes-prediction-ml.git
pip install -r requirements.txt
Classification final.ipynb

