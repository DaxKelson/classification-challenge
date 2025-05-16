# classification-challenge
# Spam Email Classification

## Overview

As part of a supervised machine learning project, we were tasked with building a model to help an Internet Service Provider (ISP) improve its spam detection system. Using a dataset containing email metadata and a binary label indicating whether the message was spam or not, we implemented and evaluated two classification models:

- Logistic Regression
- Random Forest Classifier

The objective was to determine which model more accurately identifies spam messages.

---

## Data Description

The dataset includes various features extracted from email text such as character frequencies, capital letter statistics, and symbol counts. The target variable is:

- `spam`: 
  - `1` = spam  
  - `0` = not spam

Data was loaded from:  
**https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv**

---

## Process

1. **Data Import & Exploration**
   - Loaded the CSV file into a Pandas DataFrame.
   - Reviewed the structure and contents of the dataset.

2. **Preprocessing**
   - Created the label set `y` from the `spam` column.
   - Created the features DataFrame `X` from the remaining columns.
   - Verified class balance using `value_counts()`.

3. **Train-Test Split**
   - Split the dataset into training and testing sets using `train_test_split()` with `random_state=1`.

4. **Feature Scaling**
   - Applied `StandardScaler` to normalize feature values for both models.

5. **Model Development**
   - **Logistic Regression**  
     - Trained using the scaled training data.  
     - Predictions made on test data.  
     - Evaluated with `accuracy_score`.

   - **Random Forest Classifier**  
     - Trained using the same scaled training data.  
     - Predictions made on test data.  
     - Evaluated with `accuracy_score`.

6. **Evaluation**
   - Compared model performance to determine which model classified spam more effectively.

---

## Results

| Model               | Accuracy |
|--------------------|----------|
| Logistic Regression| 93.6% |
| Random Forest      | 95% |

> Based on the accuracy scores, the **Random Forest Classifier** outperformed Logistic Regression in detecting spam emails. though the difference was not great.

---

## Summary

- Both models demonstrated high accuracy in identifying spam emails.
- The Random Forest Classifier performed best overall, aligning with (or differing from) our initial expectations.
- This model would be recommended for deployment in the ISP's email filtering system.

---
---

## Author

Dax Kelson
