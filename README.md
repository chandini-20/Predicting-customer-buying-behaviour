# Predicting-customer-buying-behaviour
# ✈️ Customer Booking Prediction

This project analyzes airline customer booking behavior using a dataset of 50,000 records. The objective is to predict whether a booking will be completed, based on various customer and flight features.

---

## 🔍 Dataset

- **Source**: `customer_booking.csv`
- **Rows**: 50,000
- **Columns**: 14
- **Target Variable**: `booking_complete` (1 = booking completed, 0 = not completed)

---

## 🛠️ Libraries Used

- Python 3
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- xgboost
- chardet (for encoding detection)

---

## 🧪 Project Workflow

1. **Data Import & Cleaning**
   - Detected file encoding using `chardet`
   - No missing values

2. **Exploratory Data Analysis**
   - Visualized feature importance using Mutual Information

3. **Feature Engineering**
   - Converted categorical variables using `.factorize()` and `get_dummies()`
   - Feature scaling with `MinMaxScaler`

4. **Feature Selection**
   - Top features:
     - `route`
     - `booking_origin`
     - `flight_duration`
     - `wants_extra_baggage`
     - `length_of_stay`
     - `num_passengers`

5. **Modeling**
   - Algorithms Used:
     - Random Forest Classifier
     - XGBoost Classifier
   - Models trained with:
     - Top 6 features
     - All features (923 after one-hot encoding)

---

## 📈 Model Performance

| Model              | Features       | Accuracy | AUC Score |
|-------------------|----------------|----------|-----------|
| Random Forest      | Top 6          | 83.36%   | 0.566     |
| Random Forest      | All Features   | 84.76%   | 0.548     |
| XGBoost Classifier | Top 6          | 84.79%   | 0.523     |
| XGBoost Classifier | All Features   | 84.96%   | 0.543     |

---

## 📂 Folder Structure

