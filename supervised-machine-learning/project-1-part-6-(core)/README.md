# 🛒 Project Overview: Item Outlet Sales Prediction

This project aims to build a machine learning model to predict `Item Outlet Sales` based on various product and store attributes. The goal is to help businesses understand the factors influencing sales and make data-driven decisions.

---

## 📋 Project Steps

1. 📥 **Data Loading and Initial Inspection**: Loading the dataset and performing initial checks for duplicates, null values, and data types.

2. 🧹 **Data Cleaning and Preprocessing**: Handling inconsistencies in categorical features (`Item Fat Content`) and preparing the data for modeling, including imputation of missing values and scaling numerical features.

3. ⚙️ **Feature Engineering**: Creating new features or transforming existing ones to improve model performance.

4. 🤖 **Model Building**: Developing and training machine learning models (`Linear Regression` and `Random Forest Regressor`) to predict sales.

5. 🔧 **Hyperparameter Tuning**: Optimizing model performance using `GridSearchCV` to find the best set of hyperparameters.

6. 📊 **Model Evaluation and Interpretation**: Assessing model performance using R², MAE, MSE, and RMSE, and interpreting the results for stakeholders.

---

## 🔍 Key Findings (Summary)

* 📉 **Linear Regression** showed a weak fit, explaining about 56% of sales variation, indicating high bias.

* 🌲 The **Untuned Random Forest** initially suffered from significant overfitting — high training R² but poor test R².

* ✅ **Hyperparameter Tuning** via `GridSearchCV` successfully reduced overfitting, improving test R² to 59% and lowering MAE — making the **Tuned Random Forest the recommended model**. It explains ~59% of sales price variation with an average prediction error (MAE) of approximately $739.

---

> 💡 This notebook demonstrates a complete workflow from data understanding to model deployment-ready evaluation.
