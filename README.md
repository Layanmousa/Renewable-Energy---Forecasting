# Renewable Energy Production Forecasting

A machine learning time-series forecasting project that predicts renewable energy production using a chronological, leakage-safe workflow.

---

# Project Objective

This project aims to forecast future renewable energy production while preserving the chronological order of the data. The workflow follows best practices for time-series machine learning to avoid data leakage and produce reliable predictions.

---

# Dataset

Expected dataset:

```text
Energy Production Dataset.csv
```

Main features include:

- Date
- Start_Hour
- End_Hour
- Source
- Season
- Production

---

# Project Workflow

1. Load and inspect the dataset
2. Clean duplicate records
3. Convert and sort dates
4. Exploratory Data Analysis (EDA)
5. Feature Engineering
6. Create lag and rolling features
7. Chronological Train/Test Split
8. Data Preprocessing
9. Train multiple regression models
10. Time-Series Cross Validation
11. Model Evaluation
12. Residual Analysis
13. Overfitting Check
14. Hyperparameter Tuning
15. Feature Importance
16. Save the trained pipeline

---

# Feature Engineering

The project generates historical features for each renewable energy source.

Features include:

- Lag_1
- Lag_2
- Rolling_Mean_3

Time features include:

- Month
- Day
- Day of Week
- Weekend
- Cyclical Month Encoding
- Cyclical Weekday Encoding

These features improve forecasting while preventing target leakage.

---

# Data Split

The dataset is divided chronologically:

- **80% Training**
- **20% Testing**

A random split is intentionally avoided because forecasting models should always predict future observations.

---

# Preprocessing

The preprocessing pipeline includes:

### Numerical Features

- Median Imputation
- StandardScaler

### Categorical Features

- Most Frequent Imputation
- OneHotEncoder

The entire preprocessing process is handled inside a Scikit-learn Pipeline.

---

# Models Compared

The following regression models are evaluated:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

---

# Baseline Forecast

A persistence baseline is used:

```text
Prediction(t) = Production(t-1)
```

This baseline provides a simple benchmark to verify that machine learning models add predictive value.

---

# Evaluation Metrics

The project evaluates models using:

- MAE
- RMSE
- R² Score

Additional analyses include:

- Time-Series Cross Validation
- Training vs Testing Error
- Residual Analysis
- Actual vs Predicted Visualization

---

# Time-Series Cross Validation

Instead of standard K-Fold validation, the project uses:

```python
TimeSeriesSplit()
```

This ensures that each validation fold only uses historical observations to predict future ones.

---

# Hyperparameter Tuning

Random Forest is optimized using:

```python
GridSearchCV()
```

Parameters include:

- n_estimators
- max_depth
- min_samples_split
- min_samples_leaf
- max_features

The best model is selected using RMSE from TimeSeriesSplit.

---

# Feature Importance

The final Random Forest model identifies the most influential predictors.

Typical important features include:

- Previous Production
- Rolling Mean
- Energy Source
- Season
- Time Features

---

# Saved Model

The trained forecasting pipeline is saved locally as:

```text
renewable_energy_forecasting_pipeline.joblib
```

The model file is excluded from GitHub because of its size.

---

# Installation

```bash
pip install numpy pandas matplotlib scikit-learn joblib jupyter
```

---

# Running the Project

1. Place the dataset in the project folder.
2. Open the notebook.
3. Run all cells from top to bottom.
4. Wait until GridSearchCV finishes.
5. Review the evaluation results and generated plots.

---

# Project Structure

```text
RenewableProject.ipynb
Energy Production Dataset.csv
README.md
PROJECT_SUMMARY.md
.gitignore
```

---

# Key Findings

- Chronological evaluation provides more realistic forecasting performance.
- Lag and rolling features significantly improve prediction quality.
- Time-Series Cross Validation produces more reliable model evaluation.
- Residual analysis shows that extreme production values remain the most difficult to predict.

---

# Limitations

- Weather data is not included.
- Maintenance information is unavailable.
- Only one future holdout period is evaluated.
- A single model is used for all energy sources.

---

# Future Improvements

- Integrate weather features
- Use longer lag windows
- Train separate models for each energy source
- Apply Walk-Forward Validation
- Compare XGBoost and LightGBM
- Explore deep learning forecasting models
- Deploy the project using Streamlit or FastAPI

---

# Author

**Layan Mousa**
