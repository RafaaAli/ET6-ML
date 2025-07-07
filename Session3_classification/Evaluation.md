# 📊 Evaluate Classification Models

---

## 🎯 Why Evaluate on Unseen Data?

The **training accuracy** of a classification model is not enough — what really matters is how well the model performs on **new, unseen data**. After all, the true goal of machine learning is to make accurate predictions in real-world scenarios.

---

## 🧪 Prediction Review

Previously, we trained a model to predict whether a patient is diabetic based on their **blood glucose level**.

Here's how the model performs on test data not used in training:

| x (Glucose) | y (Actual) | ŷ (Predicted) |
|-------------|------------|---------------|
| 83          | 0          | 0             |
| 119         | 1          | 1             |
| 104         | 1          | 0             |
| 105         | 0          | 1             |
| 86          | 0          | 0             |
| 109         | 1          | 1             |

- `x`: Blood glucose level  
- `y`: Actual diabetic status  
- `ŷ`: Predicted diabetic status

---

## 🧮 Why Accuracy Isn’t Enough

Simply calculating the number of correct predictions can be misleading.  
We need **richer metrics** to understand different types of errors.

---

## 🧾 Confusion Matrix

A **confusion matrix** gives a more detailed view:


|                | Predicted 0 | Predicted 1 |
|----------------|-------------|-------------|
| Actual 0       | **2** (TN)  | **1** (FP)  |
| Actual 1       | **1** (FN)  | **2** (TP)  |

Where:

- **TP** = True Positives  
- **TN** = True Negatives  
- **FP** = False Positives  
- **FN** = False Negatives

Shading is often used to emphasize the diagonal cells where predicted = actual.

---

## 📐 Key Evaluation Metrics

Based on the confusion matrix:

- **Accuracy** = (TP + TN) / Total  
  _How many predictions were correct overall?_

- **Recall** = TP / (TP + FN)  
  _Out of all actual positives, how many did the model correctly identify?_

- **Precision** = TP / (TP + FP)  
  _Out of all predicted positives, how many were actually positive?_

These metrics provide a **nuanced view** of model performance — especially important in domains like healthcare where **false negatives or false positives** carry real consequences.

---

## 🚀 Exercise - Perform Classification with Alternative Metrics

Click below to open the interactive exercise in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-org/your-repo/blob/main/week3_classification/classification_metrics.ipynb)

---
