# E-Commerce_Purchase_Prediction
Project Overview

This project builds a machine-learning classification pipeline to
predict whether an e-commerce browsing session will result in revenue
(Revenue). The notebook uses a Decision Tree classifier and evaluates
performance with classification metrics, including the F1-score.

Objectives

Prepare numerical and categorical session data for modelling.

Train a Decision Tree classifier to predict the Revenue target.

Evaluate the model on a held-out test set.

Tune selected hyperparameters using cross-validation.

Technologies Used

Python

Pandas and NumPy

Scikit-learn

Jupyter Notebook / JupyterLab

Workflow

Load shop_smart_ecommerce.csv.

Separate input features from the Revenue target.

Identify numerical and categorical columns.

Split the data into training and testing sets using an 80/20 split,
stratified by target.

Build a preprocessing pipeline:

Standardise numerical features with StandardScaler.

One-hot encode categorical features with OneHotEncoder.

Train a DecisionTreeClassifier with class weighting to help
address class imbalance.

Evaluate predictions using F1-score, a classification report, and a
confusion matrix.

Run GridSearchCV with five-fold cross-validation to tune tree
depth and minimum leaf size.

Results

On the notebook's held-out test set, the initial model reported: -
F1-score: 0.6278 - Accuracy: 0.85 - Precision for Revenue =
1: 0.50 - Recall for Revenue = 1: 0.83

The five-fold grid search reported a best cross-validation F1-score of
0.6344, with: - max_depth = 4 - min_samples_leaf = 50

These figures are from the current notebook outputs and may vary if the
data or code changes.

Files

ShopSmart.ipynb --- notebook containing preprocessing, model
training, evaluation, and hyperparameter tuning.

shop_smart_ecommerce.csv --- input dataset required to run the
notebook.

How to Run

Clone or download this repository.

Place shop_smart_ecommerce.csv in the same directory as
ShopSmart.ipynb.

Install the required libraries:

pip install pandas numpy scikit-learn jupyter

Launch JupyterLab or Jupyter Notebook and run the cells in order.

Notes

The dataset is not included in this README; add it to the repository
only if its licence permits redistribution. Otherwise, provide the
original dataset source.

This project is for learning and demonstration. Model performance
should be assessed in context before using predictions for real
business decisions.
