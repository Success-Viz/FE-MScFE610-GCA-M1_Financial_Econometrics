# Financial Econometrics — Module 1 Graded Coding Assignment (`FE610`)

An applied financial econometrics workflow in Python evaluating excess stock returns across four analytical modules[cite: 10, 13]: **OLS Regression**, **Correlation & Multicollinearity (VIF)**, **Principal Component Analysis (PCA)**, and **Monte Carlo Investment Simulation**[cite: 16, 17, 18].

## Dataset & Scope
* **Sample Period:** Quarterly excess return data spanning 2000–2024 (~96–99 quarters), defined as raw quarterly returns minus the quarterly risk-free rate derived from the 3-month US Treasury Bill (`^IRX`)[cite: 13, 23].
* **Universe & Assignment:** 18 US equities across 6 GICS sectors (*Consumer Staples*, *Technology*, *Financials*, *Healthcare*, *Industrials*, *Retail*) with the **Dow Jones Industrial Average (`DJI`)** included as a market factor[cite: 14, 15].
* **Assigned Sample (`studentID = 627545`):** Target stock **`AAPL`** (*Technology*) modeled alongside peer stocks **`JNJ`**, **`MRK`**, **`PFE`** (*Healthcare*), **`WMT`** (*Retail*), and **`DJI`**[cite: 23].

## Project Structure & Methods
1. **Part 1 — OLS Linear Regression (`fit_ols_model`)**: Fits an ordinary least squares model with an intercept term (`sm.add_constant(..., prepend=True)`) to estimate how peer excess returns and `DJI` explain target excess returns, reporting $R^2$, Adjusted $R^2$, and parameter coefficients[cite: 25, 27, 29, 30].
2. **Part 2 — Correlation Matrix & Multicollinearity (`compute_correlation_and_vif`)**: Computes the pairwise Pearson correlation matrix and Variance Inflation Factors ($\text{VIF}_j = \frac{1}{1 - R_j^2}$) across exogenous variables to evaluate collinearity and variance inflation[cite: 42, 44, 46].
3. **Part 3 — Principal Component Analysis (`apply_pca`)**: Applies `sklearn.decomposition.PCA` to standardized returns across all 5 assigned stocks to examine variance explained by each component, cumulative variance, and the number of components required to reach at least 90% variance (`n_components_90`)[cite: 17, 56, 57, 59].
4. **Part 4 — Monte Carlo Investment Simulation (`simulate_investment`)**: Simulates monthly contribution compounding over a specified horizon across multiple stochastic return paths, summarizing the distribution of final balances via mean, standard deviation, 5th percentile, and 95th percentile[cite: 17, 70, 71, 73, 74].

## Tools & Libraries
* **Python**, **NumPy**, **pandas**[cite: 19]
* **statsmodels** (`OLS`, `variance_inflation_factor`)[cite: 19, 27, 44]
* **scikit-learn** (`PCA`)[cite: 19, 57]
* **Jupyter Notebook**[cite: 10, 19]
