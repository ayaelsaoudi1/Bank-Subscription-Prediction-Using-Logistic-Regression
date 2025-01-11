# Bank-Subscription-Prediction-Using-Logistic-Regression
Bank Subscription Prediction Using Logistic Regression: A Comparative Analysis of Train and Test Accuracy

---

## Project Overview

This project aims to predict whether a customer will subscribe to a bank service based on various features using logistic regression. The analysis evaluates the model's performance on both training and testing datasets, comparing their accuracies to assess generalization capabilities.

## Dataset Description

### Training Data:
- **Size**: 518 rows
- **Columns**:
  - `interest_rate`: Interest rate for the customer.
  - `credit`: Credit score.
  - `march`: Binary indicator (1 if March, else 0).
  - `may`: Binary indicator (1 if May, else 0).
  - `previous`: Previous interactions with the customer.
  - `duration`: Duration of the last interaction.
  - `y`: Subscription outcome (yes/no).

### Testing Data:
- **Size**: 222 rows
- **Columns**: Same as the training data.

## Steps and Methodology

### 1. Data Preprocessing
- Checked for and confirmed no missing values in both datasets.
- Mapped the target variable `y` from `yes/no` to `1/0` for binary classification.
- Removed unnecessary columns, such as `Unnamed: 0`.
- Added a constant term for the intercept in the logistic regression model.

### 2. Model Training
- Used the `statsmodels` library to train a logistic regression model on the training dataset.
- Included all features (`interest_rate`, `credit`, `march`, `may`, `previous`, `duration`) as independent variables.
- Reviewed the model summary for statistical significance and model coefficients.

### 3. Train-Test Split Ratio
- Calculated the split ratio:
  - **Training Set**: 70.00%
  - **Testing Set**: 30.00%

### 4. Model Evaluation
- Predicted outcomes for both training and testing datasets.
- Evaluated performance using:
  - **Confusion Matrix**: To analyze true positives, false positives, true negatives, and false negatives.
  - **Accuracy Score**: To measure the percentage of correct predictions.

## Results

### Confusion Matrices and Accuracy:

#### Testing Set:
- **Confusion Matrix**: [[93, 18], [13, 98]]
- **Accuracy**: 86.04%

#### Training Set:
- **Confusion Matrix**:[[218, 41], [30, 229]]
- **Accuracy**: 86.29%

## Insights:
- The test accuracy (86.04%) is slightly lower than the train accuracy (86.29%), which is expected and indicates the model generalizes well to unseen data.
- The small accuracy difference (0.25%) suggests minimal overfitting.
