# Patient Readmission Prediction (K-Nearest Neighbors)

## Overview:
This project builds a KNN classification model to predict patient readmission risk using medical and
demographic features. The goal is to help healthcare organizations identify high-risk patients and
support targeted care planning.

## Business Question:
Can K-Nearest Neighbors accurately predict which patients are at higher risk of readmission?

## Dataset:
- 10,000 medical records
- Features: demographic, clinical, and visit-related variables
- Target: ReAdmis (0 = not readmitted, 1 = readmitted)

## Data Preparation:
- Removed duplicates and handled missing values
- Capped outliers using Z-score thresholds
- Encoded categorical variables (binary + LabelEncoder)
- Selected statistically significant predictors using SelectKBest
- Scaled features using StandardScaler to support distance-based modeling

## Modeling Approach:
- Algorithm: K-Nearest Neighbors Classifier
- Train/test split: 80/20 with stratification
- Cross-validation: 10-fold to identify optimal k value
- Optimal k identified: 16

## Results:
- Accuracy: 97%
- AUC: 0.99

## Insights:
- Patients with longer initial hospital stays and more children showed higher readmission
likelihood.
- Standardized features significantly improved model performance.
- The model effectively distinguishes high-risk patients for targeted interventions.

## Conclusion:
The KNN model demonstrates exceptional predictive performance and provides actionable insights
to support healthcare decision-making and reduce readmission rates.
