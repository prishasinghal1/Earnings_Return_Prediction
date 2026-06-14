# Earnings_Return_Prediction

## Overview

This project was developed as part of the Trexquant Global Alpha Researcher Program, a quantitative finance challenge focused on predicting stock returns on earnings announcement days.

Publicly listed U.S. companies report earnings four times annually. These earnings announcements often trigger significant market reactions, leading to elevated trading activity, increased volatility, and substantial stock price movements. Accurately forecasting returns during these events is a challenging problem due to the noisy, non-stationary, and highly competitive nature of financial markets.

The objective of the challenge was to predict the earnings-day returns of U.S. equities using an anonymized dataset derived from Trexquant's extensive collection of technical, fundamental, news, and options-based features. Model performance was evaluated using the Pearson Correlation Coefficient between predicted and actual returns on a held-out test set.

## Approach

The project focused on building a robust machine learning pipeline for cross-sectional return prediction under realistic market constraints.

Key components of the workflow included:

* Unsupervised feature engineering to identify predictive signals from a large set of anonymized features.
* Spearman Rank Correlation analysis to reduce feature redundancy and eliminate highly correlated variables.
* Cross-sectional normalization to improve feature comparability across securities.
* Time-aware validation strategies to prevent look-ahead bias and better simulate real-world deployment.
* Ensemble modeling using LightGBM and XGBoost to capture nonlinear relationships and improve generalization.

The final solution combined predictions from multiple gradient boosting models to generate stable out-of-sample forecasts.

## Results

The ensemble achieved an out-of-sample Pearson Correlation Coefficient of **0.0583679** on the evaluation dataset.

While seemingly small in magnitude, correlation-based metrics are standard in quantitative finance, where even modest predictive power can be valuable when applied across large universes of securities and repeated over many trading periods.

## Technologies Used

* Python
* Pandas
* NumPy
* SciPy
* XGBoost
* LightGBM
* Scikit-learn

## Key Learnings

* Feature engineering for high-dimensional financial datasets
* Correlation-based feature selection techniques
* Gradient boosting for alpha prediction
* Time-series validation and prevention of look-ahead bias
* Robust model evaluation in quantitative finance applications
