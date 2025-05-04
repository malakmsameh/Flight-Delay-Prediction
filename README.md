# ✈️ Flight Delay Prediction

This project analyzes flight delay data to predict arrival delays using machine learning models. It includes data cleaning, feature engineering, model training, and performance evaluation.

---

## 📚 Libraries Used

- `pandas`  
- `numpy`  
- `matplotlib.pyplot`  
- `seaborn`  
- `sklearn.model_selection`: `train_test_split`  
- `sklearn.tree`: `DecisionTreeClassifier`  
- `sklearn.ensemble`: `RandomForestClassifier`  
- `sklearn.linear_model`: `LogisticRegression`  
- `sklearn.metrics`: `accuracy_score`, `classification_report`, `confusion_matrix`, `mean_squared_error`

---

## 📂 Dataset

The dataset used is `flights.csv`, loaded into a DataFrame called `flights_df`.

---

## 🔍 Exploratory Data Analysis (EDA)

- Displayed the first and last 5 rows of the dataset.
- Checked the shape of the dataset using `.shape`.
- Examined dataset info with `.info()` and summary statistics using `.describe()`.

---

## 🛠️ Data Preprocessing

### 🔧 Handling Missing Values
- Removed columns with more than 60% missing values:
  - `CANCELLATION_REASON`, `AIR_SYSTEM_DELAY`, `SECURITY_DELAY`, `AIRLINE_DELAY`, `LATE_AIRCRAFT_DELAY`, `WEATHER_DELAY`
- Replaced missing values in numerical columns with `0`:
  - `DEPARTURE_TIME`, `DEPARTURE_DELAY`, `TAXI_OUT`, `WHEELS_OFF`, `ELAPSED_TIME`, `AIR_TIME`, `WHEELS_ON`, `TAXI_IN`, `ARRIVAL_TIME`, `ARRIVAL_DELAY`

### 🔁 Categorical Variables
- One-hot encoded the following columns:
  - `AIRLINE`, `ORIGIN_AIRPORT`, `DESTINATION_AIRPORT`

### 🎯 Feature Selection
- Target variable: `ARRIVAL_DELAY`
- Removed unnecessary columns for model training.

---

## 🧠 Model Training

Data was split into training and testing sets using `train_test_split`.

### 🌳 Decision Tree
- Trained on training data
- Predicted on test data
- Evaluated using **Mean Squared Error (MSE)**

### 🌲 Random Forest
- Trained on training data
- Predicted on test data
- Evaluated using **MSE**

### 🔄 Logistic Regression
- Trained on training data
- Predicted on test data
- Evaluated using **MSE**

> 🔎 **Note**: Logistic Regression is typically used for classification. If `ARRIVAL_DELAY` is treated as a binary variable (e.g., delayed or on-time), please clarify.

---

## 📈 Model Evaluation

All models were evaluated based on **Mean Squared Error (MSE)** to compare performance.

---

## 📊 Visualizations

- 🔥 **Correlation Heatmap**: Visualizes correlation between numerical features.
- ✈️ **Bar Plot**: Top 20 airlines by flight count.
- ⏱️ **Histogram**: Distribution of arrival delays.
- 📉 **Scatter Plot**: Scheduled departure time vs. arrival delay.

---

## 🧪 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/flight-delay-prediction.git
   cd flight-delay-prediction
