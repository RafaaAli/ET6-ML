# 🧠 Introduction to Classification

Classification models are used to make decisions or assign items into categories. Unlike regression modules, which output continuous numbers such as heights or weights, 
classification models output Boolean values—either true or false—or categorical decisions, such as apple, banana, or cherry.

There are many types of classification models. Some work similarly to classical regression models, while others are fundamentally different.
---

## 📘 Introduction

**Classification** is a type of machine learning in which a model is trained to predict which **category** or **class** an item belongs to.

> Example: A health clinic might use diagnostic features such as height, weight, blood pressure, and blood glucose level to predict whether a patient is diabetic.

---

## 🔠 Categorical Data

- **Categorical data** has predefined classes rather than numeric values.
- Some variables can be **both categorical or numeric**, depending on context.  
  Example:
  - **Time** as a numeric value (e.g., seconds)
  - **Speed category** (e.g., fast, medium, slow)
- Others are purely categorical (e.g., shape: circle, triangle, square)

---

## ✅ Prerequisites

- Basic understanding of **mathematics**
- Some experience with **Python programming**
- Familiarity with **Jupyter Notebooks**

---

## 🎯 Learning Objectives

In this module, you will learn:

- When to use **classification**
- How to **train and evaluate a classification model** using the **Scikit-Learn** framework

---

## ❓ What is Classification?

- **Binary classification** involves two categories (e.g., diabetic or non-diabetic).
- The model predicts the **probability** for each class:
  - Example: if the probability of being diabetic is `0.3`, the probability of being non-diabetic is `0.7`.
- A **threshold value** (commonly `0.5`) is used to determine the final prediction:
  - If probability > 0.5 → predict diabetic
  - Otherwise → predict non-diabetic

---

## 🔬 Training and Evaluating a Classification Model

Classification is a **supervised learning** technique.  
It uses:

- **Feature values**: patient measurements
- **Label values**: known classifications (diabetic or not)

We:

1. Train a model using a **subset** of the data
2. Use the remaining data to **evaluate** the model’s predictions

---

## 🧪 A Simple Example

Let’s explore classification using a **single feature**: blood glucose level.

| Blood Glucose | Diabetic |
|---------------|----------|
| 82            | 0        |
| 92            | 0        |
| 112           | 1        |
| 102           | 0        |
| 115           | 1        |
| 107           | 1        |
| 87            | 0        |
| 120           | 1        |
| 83            | 0        |
| 119           | 1        |
| 104           | 1        |
| 105           | 0        |
| 86            | 0        |
| 109           | 1        |

We use the first **eight observations** to train the model.  
We then plot `blood_glucose (x)` against `diabetic (y)`.

<p align="center">
  <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session3/Images/1.png" alt="Description" width="600"/>
</p>

A function `f(x)` needs to output a **probability between 0 and 1** for `y`.

- Low glucose → likely non-diabetic
- High glucose → likely diabetic

This suggests a **sigmoid function** (logistic curve) fits well.


---

### 🧮 Logistic Function (Sigmoid)

- The sigmoid function gives us a smooth transition from class `0` to `1`.
- Threshold (e.g., `0.5`) divides predictions:
  - Below 0.5 → class 0 (non-diabetic)
  - Above 0.5 → class 1 (diabetic)
 
  <p align="center">
    <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session3/Images/2.png" alt="Description" width="600"/>
  </p>

Now we can use the function to calculate a probability value that y is positive, meaning the patient is diabetic, from any value of x by finding the point on the function line for x. We can set a threshold value of 0.5 as the cut-off point for the class label prediction.

Let's test it with the two data values we held back.

 <p align="center">
    <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session3/Images/3.png" alt="Description" width="600"/>
  </p>

---

## 📊 Predictions vs. Actual Labels

Now let’s compare predictions (`ŷ`, or "y-hat") from the logistic model with actual labels:

| x (Glucose) | y (Actual) | ŷ (Predicted) |
|-------------|------------|---------------|
| 83          | 0          | 0             |
| 119         | 1          | 1             |
| 104         | 1          | 0             |
| 105         | 0          | 1             |
| 86          | 0          | 0             |
| 109         | 1          | 1             |

- **Correct** predictions: 83 → 0, 119 → 1, 86 → 0, 109 → 1  
- **Incorrect** predictions: 104 → 0 (should be 1), 105 → 1 (should be 0)

These results illustrate how **thresholding** affects prediction accuracy.

---


## 🚀 Train and Evaluate a Classification Model

Click the button below to open the notebook in Google Colab and follow along with the training and evaluation steps:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-org/your-repo/blob/main/week3_classification/classification_model.ipynb)

---
