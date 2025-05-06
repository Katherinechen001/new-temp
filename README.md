# 1 Introduction

US house prices are affected by a range of factors. This project explores the key drivers of housing values across the United States. We will fit and compare five regression‐based models—  
- Linear Regression  
- Ridge Regression  
- Lasso Regression  
- Elastic Net Regression  
- k-Nearest Neighbors Regression  

Performance will be assessed via multiple error metrics. After selecting the best model, we will identify its most important features and use them for deeper visualization and refined prediction.

# 2 Objective

The goal of this study is twofold:

1. **Interpretation:** Uncover which property attributes most strongly influence US house prices.  
2. **Prediction:** Build a predictive tool that quantifies each factor’s effect on future prices.

# 3 Methodology

## 3.1 Data Preparation and Preprocessing

- **Data source:** `Housing.csv` from Kaggle (545 rows, 13 columns)  
- **Columns:**  
  1. `price`  
  2. `area`  
  3. `bedrooms`  
  4. `bathrooms`  
  5. `stories`  
  6. `mainroad` (Yes/No)  
  7. `guestroom` (Yes/No)  
  8. `basement` (Yes/No)  
  9. `hotwaterheating` (Yes/No)  
  10. `airconditioning` (Yes/No)  
  11. `parking`  
  12. `prefarea` (Yes/No)  
  13. `furnishingstatus` (unfurnished/semi-furnished/furnished)  
- **Steps:**  
  - Load data  
  - Drop NAs  
  - Convert Yes/No to factors  
  - One-hot encode categorical variables  
  - Standardize all predictors  

## 3.2 Model Fitting

We will train and tune the following algorithms on an 80/20 train/test split:

- Ordinary least squares (Linear Regression)  
- Ridge Regression (α = 0)  
- Lasso Regression (α = 1)  
- Elastic Net (α = 0.5)  
- k-Nearest Neighbors Regression (optimal k by cross-validation)  

## 3.3 Model Evaluation

We will compute the following metrics on the test set:

- **MAE:** Mean Absolute Error  
- **MSE:** Mean Squared Error  
- **RMSE:** Root Mean Squared Error  
- **R²:** Coefficient of Determination  

## 3.4 Feature Importance and Selection

- Random Forest impurity-based and permutation-based importance  
- Compare single decision tree vs. ensemble rankings  
- Partial dependence plots for top features  
- (Optional) Local explanations via SHAP

## 3.5 Refined Prediction and Conclusion

- Choose the best model by RMSE (and R²)  
- Provide coefficient or SHAP-based insights on key drivers  
- Discuss limitations and propose improvements

# 4 Visualization

We will include:

1. **Feature Importance Plot:** Global ranking of predictors.  
2. **PDP Grid:** Marginal effects of top variables.  
3. **Tree vs. Forest Comparison:** Stability of importance.  
4. **Coefficient + SE Plot:** Linear model drivers.  
5. **Actual vs. Predicted & Residuals:** Diagnostic checks.  

# 5 Conclusion and Recommendation

Summarize:

- Best performing model and its accuracy.  
- Top factors driving US house prices.  
- Practical recommendations (e.g. focus on amenities, nonlinear size effects).  
- Data/model limitations and future directions (spatial features, segmented models).