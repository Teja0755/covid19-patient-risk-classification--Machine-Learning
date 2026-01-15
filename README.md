# 🦠 Classifying At-Risk COVID-19 Patients Using Machine Learning

## 📌 Project Overview
During the COVID-19 pandemic, early identification of high-risk patients was critical for improving clinical outcomes and optimizing healthcare resources. This project applies **supervised machine learning techniques** to classify COVID-19 patients based on their mortality risk using demographic, clinical, and comorbidity-related data.

Using a large-scale public health dataset released by the **Mexican government**, the project focuses on building interpretable and accurate classification models to determine whether a patient is at high risk of death. The workflow emphasizes **data cleaning, feature engineering, model training, evaluation, and feature importance analysis** to derive actionable medical insights.

---

## 🎯 Project Goals
- Predict COVID-19 patient mortality risk using clinical and demographic features  
- Clean and preprocess real-world healthcare data with missing and inconsistent values  
- Engineer meaningful features that improve predictive performance  
- Train and evaluate multiple classification models  
- Identify the most influential risk factors contributing to patient outcomes  

---

## 🧠 Problem Formulation
- **Task (T):** Binary classification of patient mortality risk  
- **Experience (E):** Historical COVID-19 patient records  
- **Performance Measure (P):** Classification accuracy on unseen test data  

---

## 📂 Dataset Description
- **Source:** Mexican Government COVID-19 Open Dataset  
- **Size:** Large-scale patient-level dataset  
- **Target Variable:** Patient mortality status  
- **Features Include:**
  - Demographics (age, gender, patient type)
  - Medical conditions (pneumonia, diabetes, hypertension, obesity, COPD, etc.)
  - Treatment-related attributes (hospitalization status)

Special care was taken to handle dataset-specific encodings where:
- `1` = Yes, `2` = No  
- `97` and `99` represent missing or not-applicable values  

---

## 🧹 Data Cleaning & Preprocessing
The raw dataset required extensive preprocessing to ensure model reliability:

- Converted categorical encodings to consistent boolean representations  
- Addressed missing and invalid values across multiple medical fields  
- Transformed `DATE_DIED` into a binary mortality indicator  
- Filtered confirmed COVID-19 cases using classification flags  
- Dropped features with excessive missing data (e.g., ICU, intubation)  

These steps ensured clean, interpretable inputs for downstream modeling.

---

## 🛠 Feature Engineering
- Converted raw medical indicators into machine-learning-friendly formats  
- Analyzed correlations between features and patient outcomes  
- Reduced redundancy by removing highly correlated or low-impact features  

---

## 🤖 Machine Learning Models
The following supervised classification models were implemented and evaluated:

### 🔹 Decision Tree – ROC Curve
<p align="center">
  <img src="images/decision tree.png" width="600">
</p>

### 🌳 Decision Tree Classifier
- Provided a transparent baseline model
- Enabled straightforward interpretation of decision rules
- Evaluated using training and testing accuracy

### 🔹 Random Forest – ROC Curve
<p align="center">
  <img src="images/randon forest.png" width="600">
</p>

### 🌲 Random Forest Classifier
- Improved predictive performance through ensemble learning
- Reduced overfitting compared to single-tree models
- Allowed extraction of feature importance rankings

---

## 📈 Model Evaluation
- Split data into training and testing sets
- Evaluated models using accuracy metrics
- Compared model generalization to assess robustness
- Analyzed overfitting by comparing train vs test performance  

---

## 🔍 Feature Importance Analysis
Using Random Forest feature importance, the project identified **key predictors of mortality risk**, including:
- Patient type (hospitalized vs outpatient)
- Age
- Presence of pneumonia
- Pre-existing medical conditions

This analysis provides medically meaningful insights rather than treating the model as a black box.

---

## 📜 Key Findings & Insights
- Age and pneumonia status are strong indicators of mortality risk  
- Hospitalized patients show significantly higher risk profiles  
- Ensemble models outperform simpler classifiers in predictive stability  
- Proper data cleaning has a substantial impact on model accuracy  

---

## 🚀 Tools & Technologies
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- **Models:** Decision Tree, Random Forest  
- **Techniques:** Data Cleaning, Feature Engineering, Supervised Learning  
- **Environment:** Jupyter Notebook  

---

## 📌 Future Improvements
- Address class imbalance using resampling techniques  
- Explore advanced models (XGBoost, Logistic Regression)  
- Include recall and precision metrics for healthcare relevance  
- Deploy model as a clinical decision-support prototype  

---
