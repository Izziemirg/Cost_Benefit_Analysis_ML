

# Breast Cancer Relapse Prediction

This repository contains a survival analysis study focused on predicting the time until cancer recurrence in breast cancer patients. The project utilizes demographic and clinical data from 1,091 patients to compare surgical outcomes and build predictive models for long-term health monitoring.

## Overview

The primary objective is to assess how clinical features like surgery type, tumor size, and hormonal status influence the "Relapse-Free Status" of patients over a 25-year period.

## Key Features

Data Source: Clinical dataset of breast cancer patients (ages 21–96).

Target Variables: * Relapse Free Status (Months): Duration until recurrence.

Relapse: Binary event indicator (1 = recurred, 0 = censored).

Tech Stack: Python, Pandas, Scikit-survival, Lifelines, Category Encoders, Seaborn/Matplotlib.

## Analysis & Methodology

1. Non-Parametric Analysis

Kaplan-Meier Estimator: Calculated the overall survival probability.

Finding: The aggregate survival rate 100 months post-surgery is ~64.9%.

Comparative Curves: Stratified survival by surgery type.

Finding: Breast Conserving surgery showed a significantly higher survival rate (72.4%) at 100 months compared to Mastectomy (59.3%).

2. Semi-Parametric Modeling

Cox Proportional Hazard Model: Evaluated the impact of multiple covariates simultaneously.

Significant Predictors Identified:

3-Gene classifier subtype

Hormone Therapy

Tumor Stage & Size

Nottingham Prognostic Index

Lymph node positivity

Model Performance: Achieved a Concordance Index of 0.67 using only statistically significant predictors, ensuring a robust and generalizable model.

## Repository Structure

main.ipynb: Full Jupyter Notebook containing data preprocessing, visualization, and model training.

BreastCancerData.csv: Patient clinical and demographic data.

## How to Use

Install dependencies: pip install lifelines scikit-survival category_encoders

Open main.ipynb to view the step-by-step analysis.

The model outputs provide hazard ratios (exp(coef)) to interpret the risk associated with each clinical feature.
