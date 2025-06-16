# Uber Fare Prediction 🚕📊

This project applies machine learning regression models to predict Uber fare amounts based on pickup/dropoff geolocation, passenger count, and derived spatial features. It explores both statistical and machine learning methods, including stepwise regression, log transformation, polynomial regression, and random forest.

---

## 📌 Problem Statement

Uber fare pricing is influenced by a combination of geographic and trip-related factors. Accurate fare prediction models can help ride-sharing platforms optimize pricing, reduce fraud, and improve user experience.

---

## 📂 Dataset

- **Source**: Simulated Uber NYC trip dataset (10,000+ observations)
- **Key Features**:
  - Pickup & dropoff latitude and longitude
  - Passenger count
  - Derived pickup region categories (latitude & longitude bins)
  - Fare amount (target variable)

---

## ⚙️ Tools & Libraries

- **Language**: R
- **Libraries**: dplyr, ggplot2, MASS, caret, randomForest
- **Models Used**:
  - Stepwise Regression (via AIC)
  - Log-Transformed Linear Regression
  - Polynomial Regression
  - Random Forest

---

## 🧪 Methodology

1. **Data Cleaning**:
   - Removed outliers in fare and geolocation
   - Validated passenger count and fare ranges

2. **Feature Engineering**:
   - Bucketed geolocation into categories (East/West/North/South)
   - Calculated derived features from coordinates

3. **Modeling**:
   - Stepwise regression with AIC for variable selection
   - Log transformation to address skew and non-linearity
   - Polynomial regression for curvilinear trends
   - Random forest for non-linear interaction learning

4. **Model Evaluation**:
   RMSE was calculated on test data across all models.

---

## 📊 Results

| Model                      | RMSE      |
|---------------------------|-----------|
| Stepwise Regression       | 7.98      |
| Log-Transformed Regression| 8.82      |
| Polynomial Regression     | 7.36      |
| Random Forest             | **5.90**  |

- ✅ **Best Model**: Random Forest
- 🌍 Most influential variables: dropoff coordinates, pickup region

---

## 📈 Visualization

A bar chart was plotted to compare RMSE values across models:

![Model Comparison](images/model_comparison_rmse.png)

---

## 📁 Folder Structure
