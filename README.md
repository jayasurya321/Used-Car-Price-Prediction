# Machine Learning Algorithms for Used Car Price Prediction System

![GitHub](https://img.shields.io/badge/license-MIT-blue)
![Python](https://img.shields.io/badge/Python-3.8%2B-green)

A machine learning-based system to predict used car prices using 10+ regression algorithms. This project compares performance metrics (RMSE, R²) of models like **Random Forest**, **XGBoost**, and **Neural Networks**, achieving up to **92.96% accuracy**.

---

## 📌 Project Overview

### Goal
Predict the fair market value of used cars based on features like mileage, year, manufacturer, and vehicle condition.

### Key Features
- **10+ Algorithms Tested**: Linear Regression, Ridge/Lasso, Decision Trees, Random Forest, XGBoost, LightGBM, MLP, and more.
- **Optimized Preprocessing**: Handles missing values, outliers, and categorical encoding.
- **Performance Comparison**: XGBoost outperformed others with **R² = 0.9297** and **RMSE = 0.2657**.

### Highlighted Results
| Model                | R² Score   | RMSE      |
|----------------------|------------|-----------|
| XGBoost              | 0.9297     | 0.2657    |
| Random Forest        | 0.9271     | 0.2706    |
| Gradient Boosting    | 0.9278     | 0.2692    |
| Decision Tree        | 0.8547     | 0.3821    |

---

## 📂 Dataset

**Source**: [Craigslist Vehicles Dataset](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) (426,880 entries, 26 features).

### Preprocessing Steps
1. **Dropped Irrelevant Columns**: `posting_date`, `VIN`, `image_url`, etc.
2. **Handled Missing Values**: Used `IterativeImputer`.
3. **Label Encoding**: Converted categorical features (e.g., `manufacturer`, `fuel_type`).
4. **Outlier Removal**: Applied IQR method for `price`, `odometer`, and `year`.
5. **Standardization**: Scaled features using `StandardScaler`.

---

## 🛠 Installation

### Dependencies
- Python 3.8+
- Libraries:
  ```bash
  pip install pandas numpy scikit-learn matplotlib seaborn xgboost lightgbm
