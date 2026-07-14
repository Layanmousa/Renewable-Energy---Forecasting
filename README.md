# Renewable Energy Production Forecasting

<p align="center">
  <img src="actual_vs_predicted.png" width="850">
</p>

A Machine Learning project that predicts renewable energy production using historical, temporal, and engineered features. The project follows a complete forecasting workflow including data exploration, preprocessing, feature engineering, model training, evaluation, and visualization.

---

# Dataset

The dataset contains renewable energy production records collected over time.

### Dataset Information

- Records: **51,864**
- Target Variable: **Production**

### Features

- Date
- Start Hour
- End Hour
- Source
- Day of Year
- Day Name
- Month
- Season

---

# Project Workflow

```
Dataset
   │
   ▼
Data Exploration
   │
   ▼
Data Cleaning
   │
   ▼
Feature Engineering
   │
   ▼
Lag Feature Creation
   │
   ▼
Categorical Encoding
   │
   ▼
Train/Test Split
   │
   ▼
Random Forest Regressor
   │
   ▼
Prediction
   │
   ▼
Performance Evaluation
```

---

# Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

# Feature Engineering

To improve forecasting performance, several features were engineered, including:

- Day of Year
- Month
- Season
- Day Name
- Encoded Energy Source
- **Lag_1 (Previous Production Value)**

The **Lag_1** feature allows the model to learn temporal dependencies, significantly improving prediction accuracy.

---

# Machine Learning Model

**Random Forest Regressor**

The model predicts renewable energy production based on historical production values and temporal features.

---

# Model Performance

| Metric | Score |
|---------|-------:|
| MAE | **377.43** |
| RMSE | **610.80** |
| R² Score | **0.9763** |

---

# Prediction Visualization

The following figure compares the actual historical production values with the model predictions.

<p align="center">
  <img src="actual_vs_predicted.png" width="850">
</p>

The predicted values closely follow the historical production trend, demonstrating the effectiveness of the Random Forest model and the engineered temporal features.

---

# Key Improvement

The largest improvement in this project came from introducing the **Lag_1** feature.

Using the previous production value enabled the model to capture historical patterns, reducing prediction error and increasing forecasting accuracy.

---

# Skills Demonstrated

- Machine Learning
- Time Series Forecasting
- Feature Engineering
- Data Preprocessing
- Random Forest Regression
- Model Evaluation
- Data Visualization
- Python Programming

---

# Future Improvements

- Adaptive Feature Engineering
- Rolling Window Statistics
- Lag_24 Feature
- Hyperparameter Optimization
- XGBoost
- LightGBM
- LSTM Forecasting
- Transformer-based Forecasting
- SHAP Explainability

---

# Repository Structure

```
Renewable-Energy---Forecasting/
│
├── RenewableEnergyProject.ipynb
├── Renewable-Energy.csv
├── actual_vs_predicted.png
└── README.md
```

---

# Author

**Layan Mousa**

GitHub: https://github.com/Layanmousa
---

## 👩‍💻 Author

**Layan Mousa**
