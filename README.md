# DA5401_DAL_Lab_A6
# Assignment 6: Imputation via Regression for Missing Data

- **Name:** Karan Kishore
- **Roll Number:** DA25D400

---

## Assignment Task

This project focuses on handling missing data in the UCI Credit Card Defaults dataset. The main goal was to implement and compare different imputation strategies to see how they affect the performance of a final classification model.

---

## Files

- `DA25D400_Assignment6_DA5401 (1).ipynb`

---

## Tasks Done

1.  **Data Loading and Preparation:** Loaded the dataset and renamed the target column for clarity.
2.  **Missing Data Creation:** Artificially introduced 5% missing values into the `BILL_AMT1` + 'AGE' for dataset A and just 'BILL_AMT1' for dataset B, C to simulate a real-world scenario.
3.  **Imputation Strategies:** Implemented and compared five different strategies to handle the missing data:
    - Median Imputation
    - Linear Regression Imputation
    - Non-Linear (KNN) Imputation
    - Non-Linear (Decision Tree) Imputation - doesn't work too well here
    - Listwise Deletion (Dropping Rows)
4.  **Model Training:** Trained a Logistic Regression classifier on each of the cleaned datasets.
5.  **Comparative Analysis:** Created a summary table to compare the performance (F1-Score, Recall, etc.) of the models resulting from each imputation strategy.

---

## Bonus Part

- **Class Imbalance Handling:** Used `RandomOverSampler` (a CBO technique) on the training data to handle the natural class imbalance. This was done *after* the train-test split to avoid data leakage.
- **Hyperparameter Tuning:** Implemented `GridSearchCV` to fine-tune the Logistic Regression classifier, searching for the optimal regularization parameters to improve its performance.
- **Side-by-Side Comparison:** Provided a final analysis comparing the results of a standard model vs. a fine-tuned model to show the benefits of hyperparameter tuning.
