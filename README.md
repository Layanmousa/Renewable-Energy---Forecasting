# 🌱 Renewable Energy Forecasting

> Machine Learning project for forecasting renewable energy production using historical energy data and weather-related features.

---

## 📖 About

This project demonstrates a complete Machine Learning workflow for predicting renewable energy production. It covers every stage of the forecasting pipeline, from data exploration to model evaluation.

---

## 🎯 Objective

Build a regression model capable of forecasting renewable energy production while understanding the complete forecasting process rather than focusing only on prediction accuracy.

---

## 📊 Dataset Overview

| Feature | Description |
|---------|-------------|
| Date | Date of observation |
| Start_Hour | Production start hour |
| End_Hour | Production end hour |
| Source | Energy source (Wind / Solar) |
| Day_of_Year | Day number within the year |
| Day_Name | Name of the day |
| Month_Name | Month name |
| Season | Season of the year |
| Production | Target variable |

---

## 🔄 Machine Learning Pipeline

```text
Load Dataset
      │
      ▼
Data Understanding
      │
      ▼
Exploratory Data Analysis (EDA)
      │
      ▼
Data Preprocessing
      │
      ▼
Feature Engineering
      │
      ▼
Encoding
      │
      ▼
Train-Test Split
      │
      ▼
Random Forest Regressor
      │
      ▼
Prediction
      │
      ▼
Model Evaluation
```

---

## 🤖 Model

**Random Forest Regressor**

Why Random Forest?

- Handles nonlinear relationships
- Robust to noisy data
- Reduces overfitting by combining multiple decision trees
- Performs well on structured datasets

---

## 📈 Model Performance

| Metric | Score |
|--------|------:|
| MAE | **840.49** |
| RMSE | **1430.42** |
| R² Score | **0.8709** |

The model successfully explained approximately **87%** of the variance in renewable energy production.

---

## 📚 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Git
- GitHub

---

## 💡 Future Improvements

- Apply One-Hot Encoding
- Perform Hyperparameter Tuning
- Add Feature Importance analysis
- Use Cross Validation
- Compare with Gradient Boosting and XGBoost

---

## 📂 Repository Structure

```text
Renewable-Energy-Forecasting/
│
├── Renewable_Energy_Forecasting.ipynb
├── README.md
├── Dataset.csv
└── images/
```

---

## 👩‍💻 Author

**Layan Mousa**

Physics Graduate | AI & Machine Learning Trainee
