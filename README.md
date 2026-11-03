# Warta EduLab 2026 — 1st Place

**Motor Insurance Claim Frequency Prediction | Data Science Competition**

This repository documents our winning solution from the **Warta EduLab 2026 Data Science Competition**, organized by Warta TUiR.

Our three-person team developed a machine learning solution to predict claim frequencies for motor third-party liability (TPL) insurance policies using anonymized historical data. The final model achieved **25.22% normalized Gini** on the organizer's hidden evaluation set, securing **1st place**.

## Solution Overview

- **Dataset:** 491,229 insurance policy records, supplemented with historical policy and claims data.
- **Feature Engineering:** 565 features derived from insurance history, claim patterns, and vehicle characteristics.
- **Modeling:** Ensemble of 15 LightGBM models with a Poisson objective, with hyperparameters optimized using Optuna.
- **Validation:** Repeated 5-fold stratified cross-validation across three random seeds, with percentile-rank averaging of model predictions.

## My Contribution

My primary responsibility was **vehicle data preprocessing and feature engineering**, with a focus on extracting predictive information from raw vehicle records.

- **Data Cleaning:** Processed and structured vehicle make and model data to extract characteristics such as fuel type, body style, and engine capacity.
- **Target Encoding:** Developed risk-related features for over 5,800 vehicle-model categories using target encoding.
- **Leakage Prevention:** Implemented out-of-fold encoding to reduce overfitting and prevent target leakage.

Vehicle-related features ranked among the **10 most important predictors** in the final model.

## Technical Report

The full methodology, experiments, validation results, and limitations are documented in the report:

**[Read the Technical Report (PDF)](./report.pdf)**

The original source code and competition datasets are not publicly available. This repository serves as documentation of the competition project.

**Team:** Bartosz Eppel, Mateusz Gonera, Jakub Marczak.
