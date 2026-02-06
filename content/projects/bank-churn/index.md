---
title: "Bank Customer Data Analysis & Churn Prediction"
date: 2026-02-01
draft: false
tags: ["Python", "pandas", "EDA", "Machine Learning"]
summary: "An exploratory analysis of banking customer data and a predictive model for customer churn."
featuredImage: "/images/projects/Banco.png"
---


## 🧠 Project Summary

This project combines **exploratory data analysis (EDA)** with a **basic predictive modeling extension** applied to a real-world banking customer dataset.  
The original EDA was developed as a group academic assignment and later extended individually to frame and solve a **binary classification problem** focused on predicting customer churn (whether a customer will leave the bank)
<img src="/images/projects/mapacalor.png"
     alt="Mapa de calor"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">


---

## 📊 Dataset & Problem

- **Dataset:** Public banking customer dataset from Kaggle, containing 10,127 customers × 23 variables.  
- **Goal:** Understand customer behaviour through data exploration and build a simple, interpretable model to predict customer churn.  
- **Challenge:** Balance rigorous preprocessing and interpretable modeling over complexity.

---

## 🔧 Tools & Technologies

This project was built using:

- **Python**
- **pandas** / **numpy**
- **matplotlib**
- **scikit-learn**

All analysis and modeling is contained in a Jupyter Notebook provided in the repository.

---

## 📋 Approach

1. **Data Cleaning & Preprocessing**
   - Inspect data shape, types and missing values
   - Handle outliers and convert categorical income ranges to numeric
   - Feature renaming and removal of redundant variables
2. **Exploratory Data Analysis (EDA)**
   - Descriptive statistics
   - Visual exploration of distributions and correlations
3. **Predictive Modeling**
   - Framed churn as a binary classification problem
   - Trained a **logistic regression model** for interpretability
   - Evaluated and improved the model using balancing and threshold adjustment
4. **Interpretation**
   - Interpreted model coefficients to understand drivers of churn.

---

## 📈 Key Insights

- **Multicollinearity** observed between credit limit and average open to buy
- **Transaction activity** differentiates customer profiles
- **Churn Indicators:** Lower activity and prolonged inactivity increase churn probability.

---

## 🧪 What I Learned

- How to formulate a business problem into a machine learning task
- Applying statistical reasoning and preprocessing strategies
- Transitioning from descriptive analytics to predictive modeling
- Interpreting regression coefficients in a business context.

---

## 🔗 Links

- **Repository :** https://github.com/javiergonzalvez07-star/estudio-de-csv-banco  
- **Linkedin:** https://www.linkedin.com/in/javier-gonzalvez-sempere-b526552b0/ 
