# 🚕 Uber Fare Price Prediction

This project focuses on predicting Uber ride fare prices based on key trip features such as distance, time, passenger count, and datetime attributes. The dataset is derived from historical Uber ride records in New York City.

---

## 📁 Dataset

The dataset contains the following key columns:
- `fare_amount`: The fare (target variable)
- `pickup_datetime`: Date and time of the ride
- `pickup_longitude` / `pickup_latitude`: Pickup location
- `dropoff_longitude` / `dropoff_latitude`: Dropoff location
- `passenger_count`: Number of passengers

---

## 📊 Objective

To build an Exploratory Data Analysis (EDA) and feature engineering pipeline that helps understand:
- Relationship between fare and distance
- Impact of passenger count
- Temporal trends (hour, day, month)
- Categorical effects like weekends, holidays, and rush hours

---

## 🧪 Steps Performed

### 1. **Data Cleaning**
- Removed missing/null values
- Filtered outliers in fare and location coordinates

### 2. **Feature Engineering**
- Calculated `distance_km` using Haversine formula
- Extracted:
  - `hour`, `day`, `month` from `pickup_datetime`
  - `day_of_week`, `time_of_day`, `weekend`, `rush_hour`, `holiday`

### 3. **Categorical Encoding**
- One-hot encoding for: `day_of_week`, `time_of_day`
- Cyclical encoding for: `hour` and `month` using sine and cosine transformations
- Binary encoding for: `holiday`, `rush_hour`, `weekend`

### 4. **EDA (Exploratory Data Analysis)**
- Visualized:
  - Fare vs. distance
  - Fare vs. passenger count
  - Temporal patterns across hour, day, and month
- Bar plots and scatter plots to observe data distributions

### 5. **Feature Scaling**
- Standardized `distance_km` and `passenger_count` for use in ML models
- Cyclical encoded features already in [-1, 1] range (no scaling needed)

---

## 📦 Technologies Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## 🔍 Example Visualizations

- **Fare vs Distance Scatter Plot**
- **Fare by Hour, Day of Week, and Month**
- **Fare Impact by Rush Hour, Weekend, Holiday**

---

## 📂 Folder Structure

