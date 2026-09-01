# 🚗 Used Car Price Prediction

This project focuses on predicting the **selling price of used cars** using machine learning models.
It uses features like mileage, brand, fuel type, transmission, and engine size to estimate the price.

---

## 📌 Project Objective

The main goal is to build a model that can accurately predict the price of a used car based on its features.
This helps in:

* Understanding which factors affect car prices
* Building practical machine learning skills
* Comparing different regression models

---

## ⚙️ Project Workflow

The project follows a complete data science pipeline:

**Data Cleaning → EDA → Feature Engineering → Modeling → Evaluation**

---

## 📂 Dataset

The dataset contains information such as:

* Car brand
* Mileage (km)
* Fuel type
* Transmission type
* Engine size
* Selling price (target variable)

---

## 🧹 Data Cleaning

Key steps performed:

* Handled missing values
* Removed duplicate records
* Standardized column names
* Fixed inconsistent brand names (e.g., "toyota", "TOYOTA")

---

## 📊 Exploratory Data Analysis (EDA)

Important insights:

* **Mileage and car age** are highly correlated (≈ 0.90)
* Both negatively affect price (higher mileage → lower price)
* To avoid multicollinearity:

  * ❌ Dropped `car_age_years`
  * ✅ Kept `mileage_km`

Other findings:

* Automatic cars are more expensive than manual
* Hybrid cars have the highest average price

---

## 🛠 Feature Engineering

* Converted categorical variables using **One-Hot Encoding**
* Split data into:

  * Features (X)
  * Target (y = selling_price)

---

## 🔀 Train-Test Split

* 80% training data
* 20% testing data
* Used `random_state=42` for reproducibility

---

## 📏 Feature Scaling

Used **StandardScaler** to normalize features:

* Fit on training data only
* Applied to test data to avoid data leakage

---

## 🤖 Models Used

### 1. Linear Regression

* Simple and interpretable model

### 2. Decision Tree Regressor

* Captures non-linear relationships

### 3. Random Forest Regressor

* Ensemble model for better accuracy

---

## 📈 Model Evaluation

Models were evaluated using:

* **MAE (Mean Absolute Error)** → Average error
* **RMSE (Root Mean Squared Error)** → Penalizes large errors
* **R² Score** → How well model explains data (closer to 1 is better)

---

## 🧪 Results

All models were compared based on performance metrics.
Typically:

* Random Forest performs best
* Linear Regression gives baseline performance
* Decision Tree may overfit

---

## 📌 Key Learnings

* Feature selection is very important (removed multicollinearity)
* Scaling improves model performance
* Ensemble models (Random Forest) are powerful
* Proper evaluation is necessary for regression problems

---

## 🚀 Future Improvements

* Hyperparameter tuning
* Use more advanced models (XGBoost, LightGBM)
* Add more features (location, condition, etc.)
* Deploy as a web app

---

## 🧠 Conclusion

This project demonstrates a complete machine learning workflow from raw data to model evaluation.
It shows how data preprocessing and model selection directly impact prediction performance.

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

---
