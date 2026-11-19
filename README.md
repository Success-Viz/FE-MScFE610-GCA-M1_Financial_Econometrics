# Financial Econometrics & Quantitative Return Modeling

An applied portfolio overview of core statistical and quantitative finance methods for analyzing equity return relationships, multicollinearity, dimensionality reduction, and stochastic wealth outcomes.

## Overview
This repository highlights practical econometric and simulation techniques used to study asset return behavior and portfolio uncertainty:

* **Ordinary Least Squares (OLS) Regression:** Models linear relationships between a target return series and a set of explanatory return or factor series with an intercept term, summarizing goodness of fit ($R^2$, adjusted $R^2$) and estimated slope coefficients.
* **Correlation & Variance Inflation Factor (VIF) Diagnostics:** Evaluates pairwise linear correlations and checks explanatory features for multicollinearity using $\text{VIF}_j = \frac{1}{1 - R_j^2}$ to understand how shared movement inflates coefficient variance.
* **Principal Component Analysis (PCA):** Standardizes return features and extracts orthogonal principal components to examine explained variance ratios, cumulative variance, and the number of components needed to capture a target variance threshold (such as 90%).
* **Monte Carlo Investment Simulation:** Simulates periodic contributions under stochastic return paths over a defined investment horizon, summarizing terminal balance distributions via mean, standard deviation, and tail percentiles (such as the 5th and 95th percentiles).

## Tech Stack
* **Language & Data:** Python, NumPy, pandas
* **Econometrics & Machine Learning:** statsmodels, scikit-learn
* **Workflow:** Reproducible numerical scripting and notebook experimentation
