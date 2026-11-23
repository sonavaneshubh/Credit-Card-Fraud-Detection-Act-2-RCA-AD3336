# Credit Card Fraud Detection using Logistic Regression

## Project Overview
This project implements a **Logistic Regression classification model** to detect fraudulent credit card transactions. It uses transaction-related numerical features to classify transactions as legitimate or fraudulent.

The project focuses on data preprocessing, model training, prediction, evaluation, and threshold comparison.

## Objectives
- Understand and implement Logistic Regression for binary classification.
- Preprocess and clean a real-world transaction dataset.
- Split data into training and testing sets.
- Apply feature scaling using StandardScaler.
- Predict fraudulent transactions.
- Evaluate the model using classification metrics.
- Compare different decision thresholds.

## Dataset Information
- **Dataset:** Credit Card Fraud Detection
- **Total records before cleaning:** 290,738
- **Total features:** 30
- **Target column:** `Class`
- **Problem type:** Binary classification

### Target Classes

| Class | Meaning |
|---|---|
| 0 | Legitimate transaction |
| 1 | Fraudulent transaction |

The dataset contains numerical transaction features such as `Time`, anonymized features (`V1`–`V28` where available), and `Amount`.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab / Jupyter Notebook

## Project Workflow

1. Dataset loading and inspection
2. Data cleaning
3. Missing-value handling
4. Duplicate removal
5. Feature-target separation
6. Train-test splitting (80:20)
7. Feature scaling using StandardScaler
8. Logistic Regression model training
9. Fraud prediction
10. Model evaluation
11. ROC curve and AUC analysis
12. Classification threshold comparison
13. Overfitting and underfitting analysis

## Data Preprocessing

- Removed duplicate records.
- Removed rows containing missing values.
- Separated features (`X`) and target (`y`).
- Used stratified train-test splitting.
- Applied StandardScaler to numerical features.

### Dataset after cleaning

| Description | Value |
|---|---:|
| Records before cleaning | 290,738 |
| Records after cleaning | 283,726 |
| Columns | 31 |
| Training samples | 226,980 |
| Testing samples | 56,746 |
| Missing values remaining | 0 |

## Model

**Logistic Regression** is a supervised machine learning algorithm used for binary classification. It estimates the probability of a transaction belonging to a class using the sigmoid function.

The model predicts:

- `0` – Legitimate transaction
- `1` – Fraudulent transaction

The default classification threshold is 0.5. Thresholds of 0.3, 0.5, and 0.7 were also tested.

## Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall (Sensitivity)
- Specificity
- F1-score
- Confusion Matrix
- ROC Curve
- ROC-AUC

Accuracy measures overall correctness, while Precision, Recall and F1-score are particularly important for imbalanced fraud-detection datasets.

## Threshold Comparison Results

The model was evaluated using three classification thresholds.

| Threshold | Accuracy | Precision | Recall | F1 Score |
|---:|---:|---:|---:|---:|
| 0.3 | 0.9992 | 0.8356 | 0.6421 | 0.7262 |
| 0.5 | 0.9991 | 0.8462 | 0.5789 | 0.6875 |
| 0.7 | 0.9990 | 0.8448 | 0.5158 | 0.6405 |

### Best Threshold

The threshold **0.3** achieved the highest Recall and F1-score among the three tested thresholds.

A lower threshold helps detect more fraudulent transactions, although it may increase false-positive predictions.

## Key Observations

- The dataset is highly imbalanced, with legitimate transactions significantly outnumbering fraudulent transactions.
- Accuracy alone is not sufficient to measure fraud-detection performance.
- Lowering the decision threshold improved Recall.
- Threshold 0.3 achieved the best F1-score in the tested comparison.
- Logistic Regression can provide a useful baseline for fraud detection.

## Conclusion

Logistic Regression was successfully implemented for credit card fraud detection. The dataset was cleaned and preprocessed, and the model was trained using an 80:20 train-test split.

The model was evaluated using several performance metrics and different classification thresholds. The results demonstrate the importance of Recall and F1-score when working with imbalanced datasets. Threshold 0.3 performed best among the tested thresholds when prioritizing fraud detection.

This project helped understand the practical implementation of Logistic Regression, data preprocessing, model evaluation, and classification threshold selection.

## Author

**Shubham Sonwane**

AI & Data Science Engineering Student

---

*Academic Machine Learning Project – CIE 2*
