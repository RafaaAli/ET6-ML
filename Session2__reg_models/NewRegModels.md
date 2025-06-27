# Discover New Regression Models
---

## Beyond Simple Linear Models

We looked at fitting a **straight line** to data points. However, regression can model **many kinds of relationships**, including those:

- With **multiple factors**
- Where one factor's influence depends on another

---

## Experimenting with Models

Regression models are widely used because they are:

- Effective with **small datasets**
- **Robust** and resistant to noise
- **Interpretable**
- Available in a variety of forms

---

### 🔹 Linear Regression

- The **simplest form** of regression  
- Can handle **any number of features**  
- Comes in variants based on:
  - The **number of features**
  - The **shape** of the curve that fits the data

### ➕ Linear Algorithms: Beyond Basic Linear Regression

So far, we've used **Linear Regression**, specifically the **Ordinary Least Squares (OLS)** method.  
However, linear models come in several **variants** designed to improve performance and handle more complex scenarios — especially when dealing with **high-dimensional data**.

One such variant is **Lasso Regression**.


### What is Lasso?

**Lasso** stands for **Least Absolute Shrinkage and Selection Operator**. It's a linear regression algorithm that includes a **regularization** term — specifically an **L1 penalty** — in its cost function.

This regularization helps:

- Prevent **overfitting**
- Automatically **select important features** by shrinking some coefficients to **exactly zero**



### How Lasso Works

The Lasso cost function is:

```math
Loss = MSE + λ * Σ|wᵢ|
```
Where:

- MSE is the Mean Squared Error

- λ (lambda) is a regularization hyperparameter

- Σ|wᵢ| is the sum of the absolute values of the model weights

This L1 penalty forces the model to reduce less useful weights to zero, effectively performing feature selection during training.

---

### Decision Trees

- Use a **step-by-step** rule-based approach to predict a variable  
- Example: In our **bicycle rental** scenario:
  - The tree might first split data based on season (Spring/Summer vs. Autumn/Winter)
  - Then, make predictions based on the day of the week
  - E.g., Spring/Summer-Monday → 100 rentals/day  
    Autumn/Winter-Monday → 20 rentals/day

---

### Ensemble Algorithms

- Combine **multiple decision trees** for stronger predictions  
- Can handle **complex and noisy datasets**  
- Popular example: **Random Forest**

> Ensemble models are widely used in real-world machine learning tasks for their **robustness** and **accuracy**.

---

## Try It Yourself

Data scientists often **experiment with multiple models** to see which performs best on a given problem.

In the following exercise, you’ll try out a few different models and compare their performance on the **same dataset**.

---

### Open in Google Colab

Click below to launch the notebook and experiment with model training and comparison:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1owppMYGhRs9sgOqen9ODF1nKINIsS40n)

---
