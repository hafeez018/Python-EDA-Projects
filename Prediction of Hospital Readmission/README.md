# 🏥 Prediction of Hospital Readmission

A data-analysis project focused on predicting hospital patient readmissions and identifying key factors contributing to readmission risk.

---

## 📌 Project Overview

This project covers the workflow of analysing patient hospital data, deriving features (demographics, length of stay, diagnosis codes, prior admissions), building models or statistical analyses to predict readmission (within 30 days etc.), and extracting actionable insights for clinical decision support.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn
* **Environment:** Jupyter Notebook / Google Colab

---

## 🔄 Workflow Summary

### 1. Data Collection

Hospital dataset with features such as: patient ID, age, gender, diagnosis codes, admission type, length of stay, number of prior admissions, discharge disposition, readmission flag (yes/no).

### 2. Exploratory Data Analysis (EDA)

* Visualise distributions of readmitted vs non-readmitted patients by age, length of stay, prior admissions
* Correlation matrix of numerical features and readmission
* Boxplots/histograms of key features by readmission class
* Analyse missing data, outliers, and class imbalance

### 3. Feature Engineering

* Encode categorical variables (gender, admission type, discharge disposition) using one-hot/label encoding
* Create derived features: e.g., prior_admissions_per_year, length_of_stay_bucket, diagnosis_count
* Scale numeric features if required
* Split data into training and test sets (stratified)

### 4. Modelling / Statistical Analysis

* Build models: Logistic Regression, Random Forest or other classification algorithms to predict readmission risk
* Or perform statistical testing to identify significant predictors of readmission
* Tune hyperparameters if using machine-learning models

### 5. Evaluation

* Metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC
* Focus on recall/precision of readmission class (often minority)
* Use confusion matrix and feature-importance analysis

### 6. Insights & Application

* Identified significant risk factors: e.g., high number of prior admissions, longer length of stay, certain discharge dispositions
* Provided recommendations: improved discharge planning, follow-up appointments for high-risk patients, tailored care-management interventions
* Potential to integrate into hospital operations for patient risk stratification

---

## 📁 Project Structure

```
Hospital-Readmission-Prediction/
│── data/
│   ├── raw/
│   └── processed/
│── notebooks/
│   └── readmission_analysis.ipynb
│── src/
│   ├── preprocess.py
│   ├── features.py
│   ├── model.py
│   └── evaluate.py
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Patients with longer length of stay and multiple prior admissions had higher readmission risk.
* Statistical features such as discharge disposition and diagnosis‐count added incremental predictive value.
* Machine-learning models improved risk stratification over baseline heuristics.
* Class imbalance (fewer readmissions) required specialised handling (e.g., class-weights, oversampling) to achieve adequate recall of readmitted patients.

---

## 🚀 Future Improvements

* Incorporate time-series features (e.g., admission patterns over past year) or temporal embeddings of patient history.
* Use survival analysis or competing-risks models for time-to-readmission rather than binary predicted within x days.
* Build a dashboard for clinicians: input recent patient data → risk score → intervention recommendation.
* Add explainability (e.g., SHAP) so care teams understand why a patient is flagged as high risk.
* Validate models in different clinical settings/hospitals and track performance drift over time.
