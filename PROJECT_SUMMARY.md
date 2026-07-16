# Renewable Energy Forecasting — One-Page Project Summary

## Objective
Forecast renewable-energy production using a valid, reproducible, and explainable time-series machine-learning workflow.

## Main correction
The original notebook used a random train-test split after creating a lag feature. That evaluation can mix later observations into training and earlier observations into testing. The improved version uses a chronological 80/20 holdout and `TimeSeriesSplit`.

## Data preparation
The dataset is sorted by `Source`, `Date`, and `Start_Hour`. Calendar variables are created once, including cyclical month and weekday encodings. `Lag_1`, `Lag_2`, and `Rolling_Mean_3` are created within each energy source. The rolling mean uses shifted history, preventing the current production value from entering its own predictors.

## Modeling
Categorical variables (`Source` and `Season`) are handled with `OneHotEncoder`, while numerical columns use median imputation and scaling. Three baseline models are compared:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

A naive persistence forecast using `Lag_1` is included as a minimum performance benchmark.

## Evaluation
Models are compared using MAE, RMSE, and R² through five-fold time-series cross-validation and an untouched future test period. The project also includes a chronological actual-versus-predicted plot, residual analysis, a train-versus-test RMSE overfitting check, Random Forest tuning, and transformed feature-importance interpretation.

## Deliverable
The final tuned preprocessing-and-model pipeline is saved as:

`renewable_energy_forecasting_pipeline.joblib`

## Limitations
The project does not include weather, maintenance, equipment availability, or demand constraints. Future improvements could add walk-forward validation, longer lag windows, and separate models for each energy source.
