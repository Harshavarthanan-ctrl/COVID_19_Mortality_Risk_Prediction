# 🦠 COVID-19 Mortality Prediction using Machine Learning

This repository contains a data science project focused on predicting the mortality risk of COVID-19 patients based on demographic, clinical, and comorbidity features using logistic regression.

---

## 📌 Project Objective

To develop a predictive classification model that can identify whether a COVID-19 patient is likely to die based on early-stage medical data and risk factors.

---

## 🧾 Dataset Description

The dataset includes information on over 500,000 patients and features such as:

- **Demographics**: AGE, SEX, PREGNANT  
- **Comorbidities**: DIABETES, OBESITY, COPD, ASTHMA, etc.  
- **Clinical Features**: ICU admission, INTUBED, PNEUMONIA  
- **Administrative**: USMER, MEDICAL_UNIT, PATIENT_TYPE  
- **Target Variable**: `DIED` (binary) derived from `DATE_DIED`

> **Note**: The original `DATE_DIED` column was transformed into a binary target:
> - `1` → Patient died
> - `0` → Patient survived (`DATE_DIED == '9999-99-99'`)

---

## 📊 Exploratory Data Analysis

- **Age Distribution**: Normal curve centered around 55–60 years
- **ICU/INTUBATION**: Highly correlated with fatality
- **Comorbidities**: Strong influence on mortality rates
- **Feature Binning**: Optional age-group transformation for clearer visual insights

---

## 🛠️ Feature Engineering

- Null values filled using forward-fill and median strategies
- Categorical encoding using LabelEncoder
- Scaling numerical features using StandardScaler

---

## 🤖 Modeling Approach

- **Model Used**: Logistic Regression (baseline)
- **Train-Test Split**: 80/20
- **Evaluation Metrics**:
  - Accuracy
  - Precision, Recall
  - F1-score
  - Confusion Matrix

---

## ✅ Results

- Logistic Regression provided interpretable results with decent accuracy.
- The model captured the effect of age and comorbidities on patient survival.
- Suitable for baseline comparison with tree-based or ensemble models.

---

## 🚀 How to Run

1. Clone this repository
2. Open in Google Colab or Jupyter
3. Upload the dataset `Covid Data.csv`
4. Run the notebook `covid_mortality_model.ipynb`

---

