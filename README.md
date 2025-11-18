# Churn Prediction
This project builds a machine learning model to predict customer churn using a Logistic Regression classifier. The workflow includes data loading, preprocessing, feature scaling, model training, and performance evaluation.

 Dataset

The model uses a dataset named customer_dataset.csv, which contains customer records, features, and a binary churn label.

The column CustomerID is removed because it does not contribute to predictive power.

🔧 Steps Performed
1. Data Preparation

Loaded dataset using pandas.

Removed non-informative column (CustomerID).

Split data into:

Features (X)

Target (y = Churn)

Created an 80/20 train-test split.

2. Feature Scaling

Scaled numerical features using StandardScaler to improve model performance and ensure consistent feature ranges.

3. Model Training

Trained a Logistic Regression model using scikit-learn.

Fit the model on the scaled training data.

Generated predictions for the test set.

4. Model Evaluation

Evaluated the model using:

Accuracy

Precision
 Precision was 0.00, likely because the model did not predict any positive (churn) cases, triggering an UndefinedMetricWarning.
This often occurs with:

Imbalanced datasets

Weak model signal

Need for tuning or rebalancing (e.g., SMOTE, class weights)

 Results
Metric	Score
Accuracy	0.65
Precision	0.00
