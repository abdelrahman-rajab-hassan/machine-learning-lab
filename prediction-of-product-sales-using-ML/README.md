# Sales Prediction Using Machine Learning

**Author**: Abdelrahman R. J. Hassan

---

## Business Problem
Build a machine learning model to predict `Item Outlet Sales` based on product and outlet attributes.

---

## Data
- **Source**: `sales_predictions_2023.csv`
- **Size**: 8,523 observations × 12 columns
- **Features**: Product identifiers, weight, fat content, visibility, type, MRP, outlet identifier, establishment year, size, location type, and outlet type
- **Target**: `Item Outlet Sales`

---

## Data Preparation

| Step | Details |
|---|---|
| **Inconsistent Categories** | Standardized `Item Fat Content` values (e.g., 'LF' → 'Low Fat', 'reg' → 'Regular') |
| **Data Splitting** | Split into `X_train`, `X_test`, `y_train`, `y_test` |
| **Numerical Features** | Imputed missing `Item Weight` with mean; scaled with `StandardScaler` |
| **Nominal Features** | Imputed with most frequent value; encoded with `OneHotEncoder` |
| **Ordinal Features** | Imputed with most frequent value; encoded with `OrdinalEncoder` (preserving order); scaled with `StandardScaler` |
| **Pipeline** | Combined all steps using `ColumnTransformer` |

---

## Model

**Final Model**: Tuned Random Forest Regressor  
- Tuned via `GridSearchCV` over `n_estimators` and `max_depth`  
- **Best Parameters**: `{'max_depth': 10, 'n_estimators': 200}`

### Performance (Test Set)

| Metric | Value |
|---|---|
| R² | 0.590 |
| MAE | $739.60 |
| RMSE | $1,064.11 |
| MSE | 1,132,330.46 |

### Interpretation
The model explains **59% of the variance** in outlet sales. On average, predictions deviate by **~$739**, giving stakeholders a clear sense of prediction reliability in dollar terms.

---

## Model Comparison

| Model | Test R² |
|---|---|
| Linear Regression | 0.567 |
| Random Forest (Untuned) | 0.552 |
| **Random Forest (Tuned)** ✅ | **0.590** |

The tuned Random Forest outperformed both alternatives and showed reduced overfitting (Train R²: 0.722 vs. Test R²: 0.590).

---

## Recommendations
Use the **Tuned Random Forest Regressor** — it achieves the best generalization and lowest overfitting among all tested models.

---

## Limitations & Next Steps
The model still shows a moderate train/test R² gap (0.722 vs. 0.590). Suggested improvements:

- **Hyperparameter Tuning**: Try `RandomizedSearchCV` with a wider search space  
- **Feature Engineering**: Create new features to better capture sales patterns  
- **Alternative Models**: Explore Gradient Boosting methods (XGBoost, LightGBM)

---

## Contact
For questions, you can email me via: abdelrahman.r.hassan@gmail.com
