# 🏡 California Housing Price Prediction

This repository contains a machine learning project that predicts median house values in California using the California Housing dataset. The project includes data cleaning, feature engineering, exploratory data analysis (EDA), model building, and hyperparameter tuning with various algorithms including Linear Regression, Random Forest, XGBoost, and LightGBM.

---

## 📁 Dataset

- **Source**: California Housing dataset (available via `sklearn.datasets.fetch_california_housing` or Kaggle/CSV)
- **Features include**:
  - Geographical: `longitude`, `latitude`
  - Housing: `housing_median_age`, `total_rooms`, `total_bedrooms`, `population`, `households`
  - Economic: `median_income`
  - Target: `median_house_value`
  - Engineered features: `rooms_per_household`, `bedrooms_per_room`, `population_per_household`
  - One-hot encoded: `ocean_proximity`

---

## 📊 Project Workflow

### 1. Data Preprocessing
- Loaded and inspected the dataset
- Removed outliers
- Handled missing values
- Performed one-hot encoding on categorical features (`ocean_proximity`)

### 2. Feature Engineering
- Created ratio features to better capture relationships:
  - `rooms_per_household`
  - `bedrooms_per_room`
  - `population_per_household`

### 3. Exploratory Data Analysis (EDA)
- Visualized correlations
- Mapped geographical distributions
- Investigated income vs house value relationships

### 4. Modeling
Trained and evaluated the following models:
- **Linear Regression**
- **Random Forest Regressor**
  - With and without `RandomizedSearchCV`
- **XGBoost Regressor**
  - With and without `GridSearchCV`

### 5. Model Evaluation
Used:
- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **R² Score**

Best model performance (XGBoost with Grid Search):
- **MAE: 23,946.59**
- **R² Score: 0.8379**

  
---

## 🛠️ Requirements

- Python 3.8+
- scikit-learn
- xgboost
- pandas
- matplotlib / seaborn
- jupyter notebook / vscode

Install all dependencies with:

``bash
pip install -r requirements.txt

##🧠 Author
Made with 💻 by Prajwal Longia
