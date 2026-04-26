# Ensemble Tree Methods for ``Stroke Prediction``
---

## 📌 Project Overview
This notebook focuses on predicting the likelihood of stroke using a dataset containing various health and lifestyle factors.

### 🛠 Model Specifications
*   **Target Variable:** `stroke` (binary: 0 or 1)
*   **Dataset:** `stroke.csv`
*   **Data Status:** Mixed data types (numerical and categorical), with missing values in `bmi` handled by imputation. Class imbalance is a significant challenge.
*   **Preprocessing:**
    *   Numerical features (`age`, `avg_glucose_level`, `bmi`): Imputed with mean, scaled with `StandardScaler`.
    *   Categorical features (`gender`, `hypertension`, `heart_disease`, `ever_married`, `work_type`, `Residence_type`, `smoking_status`): Imputed with most frequent, encoded with `OneHotEncoder`.
*   **Model Used:** `DecisionTreeClassifier`
*   **Mandatory Step:** Performed a **Train/Test Split** with `stratify=y` due to class imbalance.

---

## 🎯 Primary Objective
> **Task:** Develop a model to predict stroke, specifically focusing on improving recall for the stroke class due to the critical nature of false negatives.

---
