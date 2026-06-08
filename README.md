# Understanding Health Insurance Cost Predictions Using Deep Neural Networks, Monte Carlo Simulation and Shapley Values

MSc dissertation submitted in partial fulfilment of the requirements for the degree **Master of Science (Mathematical Statistics & Actuarial Sciences)** at the University of the Free State, Bloemfontein Campus.

**Author:** Thabang Bongani Junior Baloyi
**Supervisor:** Dr J.M. Blomerus
**Date:** May 2026

## Overview

This dissertation develops a three-stage statistical framework for health insurance cost prediction using a publicly available benchmark dataset of one million policyholder records. The three stages are:

1. **Prediction** -- A deep neural network is trained to predict insurance charges, with a five-phase hyperparameter comparison selecting the final architecture. The DNN is benchmarked against a Gamma generalised linear model (GLM), a random forest and an XGBoost ensemble.

2. **Simulation** -- Parametric Monte Carlo simulation generates synthetic policyholder profiles from fitted marginal distributions. The trained network is evaluated at each profile, producing a model-implied predicted-cost distribution validated through joint-distribution diagnostics and residual-augmented sensitivity analysis.

3. **Explanation** -- Shapley values decompose each predicted cost into additive feature contributions at both the global level and conditionally within high-cost regions defined by upper-tail thresholds.

## Key Results

- The DNN achieves a test-set R-squared of **0.9957**, outperforming the GLM (0.9571), random forest (0.9899) and XGBoost (0.9955).
- Shapley attribution identifies **smoking status, coverage level and medical history** as the dominant cost drivers globally.
- In the upper tail, the importance ranking shifts: coverage level, medical history and family medical history overtake smoking status, showing that the factors driving extreme predicted costs differ from those most important on average.

## Methods and Tools

- **Models:** Feed-forward deep neural network (funnel architecture), Gamma GLM with log link, random forest, XGBoost
- **Simulation:** Parametric Monte Carlo with fitted marginal distributions, bootstrap Monte Carlo resampling, residual-augmented sensitivity analysis
- **Explainability:** SHAP (SHapley Additive exPlanations), conditional Shapley analysis at upper-tail thresholds
- **Diagnostics:** PCA projections, correlation heatmaps, energy distance permutation tests, t-SNE, convergence monitoring (MCSE)
- **Language:** Python (TensorFlow, scikit-learn, XGBoost, SHAP, pandas, NumPy, matplotlib)

## Repository Structure

```
.
├── README.md
├── Msc_Mathematical_Statistics_Dissertation.pdf
├── src/                    # Model training and evaluation scripts
│   ├── dnn_model.py
│   ├── glm_benchmark.py
│   ├── rf_benchmark.py
│   ├── xgboost_benchmark.py
│   ├── monte_carlo.py
│   └── shapley_analysis.py
├── data/                   # Data loading and preprocessing
├── notebooks/              # Exploratory analysis and figures
├── results/                # Saved model outputs and figures
└── requirements.txt
```

## Dissertation Structure

| Chapter | Title |
|---------|-------|
| 1 | Introduction |
| 2 | Literature Review |
| 3 | Methods and Data |
| 4 | Results |
| 5 | Conclusion |

## How to Cite

```
Baloyi, T.B.J. (2026). Understanding Health Insurance Cost Predictions Using Deep Neural
Networks, Monte Carlo Simulation and Shapley Values. MSc dissertation, University of the
Free State, Bloemfontein.
```

## Keywords

deep neural network, health insurance cost prediction, Monte Carlo simulation, Shapley values, explainable machine learning, generalised linear model, random forest, XGBoost, statistical learning

## Licence

This work is submitted under the intellectual property policies of the University of the Free State. All rights reserved.
