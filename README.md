# 🧠 Pusula Data Science Case Study
Burak Bora Sayar || 01buraksayar@gmail.com
--
## Case Summary  
This project was developed as part of the Pusula Intern Data Science 2025 case study.
Our goal is to analyze the provided patient data (EDA) and prepare it for model training (preprocessing).  
Note: No model training has been performed.
The project's goal is to clean and transform the data to produce a model-ready dataset.

---

## 🎯 Objectives

1.To understand the dataset and examine missing values ​​and distributions.  

2.To convert the Target column (Treatment Duration) and other duration information to numerical values.  

3.To perform count-based feature engineering from lists such as Chronic Disease, Diagnosis, and Allergies.  

4.To fill in missing values:  
  - Numeric → IterativeImputer  
  - Categorical → SimpleImputer  
    
5.To encode categorical variables:  
  - Cross-Validation based Target Encoding  

6.To normalize numeric variables (StandardScaler).  

7.The result: a fully numeric, complete, scaled, and encoded dataset.  

---

## 🛠 Method Used
- EDA (Exploratory Data Analysis)
  - Visualization with histogram, boxplot, countplot, and heatmap
  - Missing Value Analysis
  - Correlation Matrix
- Preprocessing
  - String to numeric conversion (TedaviSuresi, UygulamaSuresi)
  - Feature Engineering (Count Features)
  - Missing Value Filling (IterativeImputer, SimpleImputer)
  - Scaling (StandardScaler)
  - Encoding (CV-Based Target Encoder)
- Validation
  - Check for Missing Values ​​(0 Missing)
  - Shape Comparison (Original vs. Processed)
  - Sample Row Display
 
---
## 📊 EDA Informations
- Datasets: 2235 rows,13 columns
- Target (TedaviSuresi) → string format, "X Seans" type → converted to numeric.
- UygulamaSuresi was converted to numeric in the same way.
- Count properties were generated from the KronikHastalik, Tanilar, and Alerji columns.
- Numerical distributions were examined using box plots, and outliers were identified.
- Correlation analysis: Yas and UygulamaSuresi_num showed significant relationships with the target variable.
- Frequency distributions of categorical columns (Bolum, TedaviAdi, Cinsiyet, etc.) were generated.

---

## 🧹 Preprocessing Pipeline

Numerical Features  
  ├─ IterativeImputer → filling the missing 
  └─ StandardScaler → scaling  

Categorical Features  
  ├─ SimpleImputer("MISSING") → filling the missing  
  └─ CVTargetEncoder → cross-validation based encoding  

Sonuç: Original X shape (2235, 11) → Transformed X shape (2235, 11)

---
## ✅ Model-Ready Check
  - ✔️ Number of missing values: 0
  - ✔️ All columns are numeric (float64)
  - ✔️ Original 11 columns → converted 11 numeric columns
  - ✔️ The first 5 rows of the sample consist entirely of numeric values

---

## 📂 Project Structure

├── main.ipynb   
├── README.md                 
├── Talent_Academy_Case_DT_2025.xlsx           

---

## 🏆 Result
  - The dataset has been analyzed and made model-ready.
  - All categorical and string fields have been encoded.
  - Missing values ​​have been filled in, and numerical values ​​have been scaled.
  - The dataset can now be fed directly into any regression/classification model.


