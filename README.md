# Predicting Used Car Prices

## Overview
This project compares multiple machine learning models to predict used car prices based on historical sales data. The goal is to determine which model provides the most accurate price predictions, helping buyers and sellers make informed decisions. The models evaluated include traditional regression methods, ensemble learning, and gradient boosting algorithms.

## Data
The dataset includes various features related to used car sales, such as:
- **Vehicle Specifications:** Brand, model, year of registration, mileage, power, etc.
- **Transaction Details:** Sale price, date of sale, etc.
- **Categorical Features:** Encoded using suitable methods for each model.

## Models Compared
We evaluated both traditional regression models and advanced machine learning techniques:

### Traditional Regression Models (from `scikit-learn`)
- **Linear Regression** (`sklearn.linear_model.LinearRegression`)
- **Ridge Regression** (`sklearn.linear_model.Ridge`)

### Ensemble Model (from `scikit-learn`)
- **Random Forest Regressor** (`sklearn.ensemble.RandomForestRegressor`)

### Gradient Boosting Models (from respective libraries)
- **XGBoost** (`xgboost.XGBRegressor`)
- **LightGBM** (`lightgbm.LGBMRegressor`)
- **CatBoost** (`catboost.CatBoostRegressor`)

## Methodology
1. **Data Preprocessing:**
   - Handled missing values and outliers.
   - Encoded categorical variables.
   - Scaled numerical features where necessary.
2. **Feature Engineering:**
   - Created additional features such as car age.
3. **Model Training:**
   - Split data into training, validation, and test sets.
   - Trained each model with default hyperparameters.
   - Evaluated performance using RMSE (Root Mean Squared Error).
4. **Hyperparameter Tuning:**
   - Performed grid search for optimal parameter selection.

## Results
The model performance comparison is summarized below:

| Model         | RMSE (Euros) |
|--------------|--------------|
| Linear Regression | 3031.69 |
| Random Forest    | 2189.88|
| XGBoost         | 2135.70 |
| LightGBM        | 2125.25 |
| CatBoost        | 2206.57 |


### Model Performance Comparison
![rmse_compare](https://github.com/user-attachments/assets/5967a14a-eb25-42c9-bf35-d86c238e4045)


### Actual vs. Predicted Prices
![image](https://github.com/user-attachments/assets/f9155a6b-3361-4f54-864e-9a33632f508f)


## How to Use
### Clone the Repository:
```sh
git clone https://github.com/littleteapot3/predicting-used-car-prices.git
```

### Install Dependencies:
```sh
pip install scikit-learn xgboost lightgbm catboost pandas numpy matplotlib seaborn jupyter
```
*(Or use `pip install -r requirements.txt` if available.)*

### Run the Notebook:
```sh
jupyter notebook notebooks/predicting-used-car-prices.ipynb
```

## Conclusion
Among the models compared, **XGBoost demonstrated the lowest RMSE**, suggesting it provides the most accurate predictions. However, all models contribute useful insights, and different choices may be preferred based on interpretability or computational efficiency.

## Acknowledgments
- Developed using Python and machine learning libraries.


