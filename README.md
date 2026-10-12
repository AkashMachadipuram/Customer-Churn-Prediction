# Customer Churn Prediction

## Project Overview
This machine learning project predicts whether a telecommunications customer is likely to churn (leave the service). The goal is to explore customer behavior, compare classification models, and identify customers who may need retention support.

## Business Problem
Customer churn can lead to lost revenue. Predicting potential churners can help businesses prioritize customer-retention efforts.

## Dataset
- **Dataset:** Telco Customer Churn
- **Target variable:** `Churn`
- **Target encoding:** Yes = 1, No = 0

## Project Workflow
1. Loaded and explored the dataset using Pandas.
2. Investigated churn patterns across customer and service characteristics.
3. Cleaned missing values and encoded categorical features.
4. Split the data into training and test sets using stratification.
5. Trained and evaluated five model configurations.
6. Tuned Decision Tree hyperparameters using GridSearchCV with five-fold cross-validation.
7. Compared models using accuracy, precision, recall, and F1-score.

## Models Evaluated

| Model | Accuracy | Churn Precision | Churn Recall | Churn F1 |
|---|---:|---:|---:|---:|
| Logistic Regression | 82.1% | 68.5% | 60.1% | 0.640 |
| Decision Tree | 80.6% | 70.5% | 46.1% | 0.558 |
| KNN | 76.7% | 57.1% | 48.5% | 0.525 |
| Random Forest | 79.8% | 67.2% | 46.6% | 0.551 |
| Tuned Decision Tree | 74.5% | 51.2% | 79.1% | 0.622 |

## Results and Key Findings
Logistic Regression achieved the highest accuracy (82.1%) and churn F1-score (0.640) among the evaluated models, making it a reasonable initial choice when balancing overall performance and churn detection.

The tuned Decision Tree achieved the highest churn recall (79.1%). This means it identified a larger share of actual churners, but its lower precision (51.2%) means more customers it flagged did not churn.

The preferred model depends on the business trade-off between missing potential churners and contacting customers who would have stayed.

## Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Joblib

## How to Run
1. Download or clone this repository.
2. Install the required Python packages.
3. Place the dataset in the expected location.
4. Open the notebook in Jupyter.
5. Run the notebook cells in order.

## Limitations and Future Improvements
- Use a preprocessing pipeline to prevent data leakage and keep transformations consistent.
- Evaluate performance with cross-validation and further model tuning.
- Assess the business costs of false positives and false negatives.
- Consider threshold tuning and model calibration.
- Test the complete prediction workflow on new customer records.

## Disclaimer
This is an educational machine learning project. Predictions should be validated before being used for real customer-retention decisions.
