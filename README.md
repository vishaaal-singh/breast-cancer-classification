# Breast Cancer Classification using Logistic Regression


## Project Overview

This project focuses on classifying breast cancer tumors as **benign** or **malignant** using **Logistic Regression**, a powerful machine learning algorithm. Breast cancer is one of the most common types of cancer among women, and early detection through accurate classification can significantly improve treatment outcomes.

The goal is to build a predictive model that analyzes tumor features and classifies tumors accordingly.

## Dataset

The dataset used for this project is the **Breast Cancer Wisconsin Dataset**, which contains medical measurements related to breast cancer tumors. The target variable is binary, where:
- **2** represents benign tumors
- **4** represents malignant tumors

### Features

The dataset consists of the following 11 attributes:

1. **Clump Thickness**: Thickness of the lump.
2. **Uniformity of Cell Size**: Consistency in the size of the cell nuclei.
3. **Uniformity of Cell Shape**: Consistency in the shape of the cell nuclei.
4. **Marginal Adhesion**: Measures how closely the cells stick together.
5. **Single Epithelial Cell Size**: Size of a single epithelial cell.
6. **Bare Nuclei**: The absence of a nucleus in some cells.
7. **Bland Chromatin**: Texture of the cell’s chromatin.
8. **Normal Nucleoli**: Appearance of the nucleolus.
9. **Mitoses**: Cell division measurement.
10. **Class**: Target variable (2 = benign, 4 = malignant).

## Results

### Confusion Matrix

A **Confusion Matrix** is a table used to evaluate the performance of a classification model. In this case, it compares the predicted breast cancer classifications (benign or malignant) with the actual classifications in the test dataset.

Here's the code used to generate the confusion matrix:

```python
from sklearn.metrics import confusion_matrix

# Generating the confusion matrix
cm = confusion_matrix(y_test, y_pred)
print("Confusion Matrix:")
print(cm)

# Output
Confusion Matrix:
[[84  3]
 [ 3 47]]
```

### Explanation
True Negatives (TN): 84 cases where benign tumors were correctly predicted as benign.
False Positives (FP): 3 cases where malignant tumors were incorrectly predicted as benign (Type I error).
False Negatives (FN): 3 cases where benign tumors were incorrectly predicted as malignant (Type II error).
True Positives (TP): 47 cases where malignant tumors were correctly predicted as malignant.

## Conclusion
The high accuracy and low standard deviation demonstrate that the logistic regression model performs well in classifying breast cancer tumors as benign or malignant. However, it's crucial to focus on the confusion matrix, particularly minimizing false negatives (i.e., predicting malignant tumors as benign), as this has significant medical implications.



