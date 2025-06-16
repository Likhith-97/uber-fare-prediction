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
- **Libraries**: `dplyr`, `ggplot2`, `MASS`, `caret`, `randomForest`
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
   - Created spatial feature bins

3. **Modeling**:
   - Stepwise regression for variable selection
   - Log transformation to handle skewed fare data
   - Polynomial regression for non-linearity
   - Random forest for capturing complex interactions

4. **Evaluation**:
   - RMSE used to assess model performance on the test set

---

## 📊 Results

| Model                      | RMSE      |
|---------------------------|-----------|
| Stepwise Regression       | 7.98      |
| Log-Transformed Regression| 8.82      |
| Polynomial Regression     | 7.36      |
| **Random Forest**         | **5.90**  |

- ✅ **Best Model**: Random Forest
- 🌍 Key drivers: Dropoff coordinates & pickup zones

---

## 📈 Model Performance Comparison

The chart below shows RMSE values across all models:

![Model RMSE Comparison](images/model_comparison_rmse.png)

- ✅ **Random Forest** performed the best
- 📉 Polynomial Regression followed closely

---

## 📂 Project Files

- 📘 [Uber Fare Prediction Notebook](notebooks/uber_fare_prediction.Rmd)
- 📊 [Uber Dataset](data/uber.csv)
- 🖼️ [RMSE Chart](images/model_comparison_rmse.png)

---

## 🔧 Future Improvements

- Include Haversine distance as a feature
- Hyperparameter tuning for Random Forest
- Deploy interactive dashboard using Shiny or Streamlit

---

## 🙋‍♂️ Author

**Likhith Kumar Vuchooru**  
MS in Business Analytics, Drexel University  
📧 lv395@drexel.edu  
🔗 [GitHub](https://github.com/Likhith-97)
