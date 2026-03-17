# Predictive-Analytics-Lab-Exam-2
# Binary Classification using Polynomial Pipeline Model

## 🔹 Overview

This project performs **Exploratory Data Analysis (EDA)** and builds a **binary classification model** using a **Polynomial Pipeline (Logistic Regression)**. The goal is to classify data into two categories based on two input features.

---

## 🔹 Dataset Description

* **Total Records:** 1020
* **Features:**

  * `Feature1` (float)
  * `Feature2` (integer)
* **Target Variable:**

  * `Target` (categorical: Yes / No)

---

## 🔹 Exploratory Data Analysis (EDA)

The dataset was analyzed to understand its structure and identify issues.

### ✔ Observations:

* Missing values: **20** in Target column
* Duplicate rows: **102**
* Presence of extreme outlier:

  * `Feature1 max = 10000` (significantly higher than normal range ~1–2)

---

## 🔹 Data Preprocessing

To improve data quality and model performance:

* Removed missing values using `dropna()`
* Removed duplicate rows using `drop_duplicates()`
* Removed outliers:

  * Filtered dataset with `Feature1 < 5`
* Converted categorical target into numeric values using encoding

---

🔹 Model Building (Pipeline)

A **Pipeline model** was used to ensure clean and efficient preprocessing and training.

 ✔ Pipeline Components:

1. PolynomialFeatures (degree = 2)

   * Captures non-linear relationships
2. **StandardScaler**

   * Normalizes feature values
3. **LogisticRegression**

   * Used for binary classification
   * `class_weight='balanced'` to handle class imbalance



 Decision Boundary

* A **non-linear decision boundary** was plotted using the polynomial model
* The boundary clearly separates the two classes
* Visualization improved after:

  * Removing outliers
  * Applying scaling
  * Using polynomial transformation

---

Model Evaluation

 Accuracy:

77.22%

 Confusion Matrix:

[[ 37   0]
 [ 41 102]]


Classification Report:

Class 0

  * Precision: 0.47
  * Recall: 1.00

* **Class 1**

  * Precision: 1.00
  * Recall: 0.71


🔹 Key Insights

* The dataset initially contained **noise (outliers)** and **class imbalance**
* A simple linear model was insufficient
* Polynomial transformation improved model capability
* Class imbalance handling improved recall for minority class

Conclusion

The **Polynomial Pipeline model** successfully captured the non-linear nature of the dataset and produced a meaningful decision boundary. Proper preprocessing significantly improved model performance and reliability.


Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn


