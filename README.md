# 📊 Bitcoin Price Prediction and Analysis (2014–2024)

### Authors:  
- Saad Ibrar (SP22-BAI-041)  

## 🧾 Project Overview

This project analyzes and predicts Bitcoin's price trends using historical data from 2014 to 2024. We explore how Bitcoin's price has evolved over the last decade and apply several Machine Learning models to forecast price and classify market movements. The goal is to uncover trends, compare model performances, and gain predictive insights.

---

## 📂 Dataset Description

The dataset used in this project contains:
- Daily Bitcoin data from 2014 to 2024
- Columns:
  - Date
  - Open, High, Low, Close prices (USD)
  - Volume
  - Market Cap (optional)
  
Source file: `BTC-USD.csv`

---

## 🔧 Project Workflow

### 1. **Data Cleaning**
- Removed missing values
- Parsed and sorted dates
- Saved cleaned version as `Cleaned BTC-USD.csv`

### 2. **Data Visualization**
- BTC Price over Time (Line Plot)
- Daily Percentage Change (Volatility)
- Histogram of Daily Returns

---

## 📈 Regression Models

### ✔️ Linear Regression
- **Features:** Open, High, Low, Volume  
- **Target:** Close
- **Performance:**
  - Train RMSE: ~451.37
  - Test RMSE: ~404.94
  - R² Score: 0.9995
- Visualizations: Prediction accuracy, residual plot, feature importance

---

### ✔️ Gradient Descent (Manually Implemented)
- Normalized features
- Cost function optimization over 1000 iterations
- Output: Learned parameters (theta)

---

### ✔️ Decision Tree Regressor
- **Depth:** 5
- **Performance:**
  - Train RMSE: ~764.93
  - Test RMSE: ~944.56
  - R² Score: 0.9971
- Visualizations: Prediction accuracy, residual plot, tree structure, feature importance

---

## 📉 Classification Models (Price Movement: Up/Down)

### ✔️ Naive Bayes
- **Features:** Open, High, Low, Volume
- **Target:** Price_Movement (Up/Down)
- **Accuracy:** ~47.83%
- Visualizations: Confusion Matrix, Class Distributions, PCA plot

---

### ✔️ K-Nearest Neighbors (KNN)
- **k = 5**
- **Accuracy:** ~54.22%
- Performed better than Naive Bayes
- Visualizations: Confusion Matrix, Classification Report

---

### ✔️ Neural Network (Using TensorFlow)
- **Architecture:**
  - Dense (64 units, ReLU) × 2
  - Output: Sigmoid
- **Loss:** Binary Crossentropy
- **Accuracy:** Reported via training history
- Visualizations: Loss and accuracy curves

---

## 📌 Requirements

Install the following libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
```
## 📊 Summary of Model Performances

| Model             | Type           | Accuracy / R² | Test RMSE  | Notes                   |
|------------------|----------------|---------------|------------|-------------------------|
| Linear Regression| Regression     | 0.9995        | ~404.94    | Best for prediction     |
| Gradient Descent | Regression     | N/A           | Visual only| Manually coded          |
| Decision Tree    | Regression     | 0.9971        | ~944.56    | Slight overfitting      |
| Naive Bayes      | Classification | ~47.8%        | N/A        | Weak classifier         |
| KNN              | Classification | ~54.2%        | N/A        | Better than NB          |
| Neural Network   | Classification | via training logs | N/A    | Non-linear patterns     |

---

## 📁 Project Files

- `BitCoin_Price_Project.ipynb` – Main notebook  
- `BTC-USD.csv` – Raw dataset  
- `Cleaned BTC-USD.csv` – Cleaned version  

---

## 📚 Future Work

- Add time-series forecasting using LSTM or ARIMA  
- Improve classification performance using ensemble models (Random Forest, XGBoost)  
- Explore macroeconomic and sentiment data  

---

## 📜 License

This project is for academic and educational use.

