# Gene-Environment Interaction Analysis

## Overview

This repository contains a statistical modeling project evaluating over 1,000 observations to isolate significant independent environmental effects and gene-gene interactions. The analysis engineers a multiple linear regression (OLS) model using `pandas` and `statsmodels` and applies rigorous statistical diagnostics to ensure predictive accuracy.

## Methodology

1. **Data Exploration & Visualization:** Analyzed the normality of the target outcome variable ($Y$) and plotted scatter distributions against environmental factors ($E1$–$E4$).
2. **Initial OLS Regression:** Modeled the main effects of 4 environmental variables and 20 genetic variables ($G1$–$G20$).
3. **Bonferroni Correction:** Applied multiple testing corrections across all 24 variables to strictly control for Type I false-positive risks, isolating variables that remained statistically significant.
4. **Interaction Term Analysis:** Engineered pairwise interaction terms for the surviving significant variables ($E1, E3, G6, G19$) and re-evaluated the OLS model to capture complex relationships.
5. **Residual Diagnostics:** Plotted the distribution of residuals and residuals vs. fitted values to confirm homoscedasticity and absence of bias.

## Key Results

* **Predictive Accuracy:** The final multiple linear regression model successfully explains **57.5% of the outcome variance** (Adj. $R^2 = 0.573$).
* **Isolated Interactions:** Identified a highly significant gene-gene interaction (**G6 $\times$ G19**) with a heavily corrected $p$-value of $0.000054$, alongside strong independent main environmental effects for $E1$ and $E3$.
* **Diagnostics:** Residual plots confirm a normal distribution (Prob JB = 0.780), validating the model's structural integrity.

## Repository Structure

* `analysis.ipynb` — The core Jupyter Notebook containing all data reshaping, OLS modeling, and statistical testing.
* `P2_698052.csv` — The dataset containing the 1,000+ genetic and environmental observations.
* `scatterplots_Y_vs_E.png` — Visualization of outcome variance across environmental variables.
* `residual_plots.png` — Diagnostic plots verifying model validity.
* `requirements.txt` — Required Python dependencies.
