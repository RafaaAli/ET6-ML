# 🔧 Improve Models with Hyperparameters

 If your CDSP project involves a large dataset and you're applying linear regression, this section is recommended. It may also be helpful if you’ve selected a similar project for your ELO.

---

## 🌀 Iterative Training and Tuning

Simple models with small datasets can often be trained in a single step.  
However, **larger datasets** and **more complex models** typically require iterative training — repeatedly feeding training data into the model, evaluating predictions, and adjusting the model accordingly.

If the model's prediction is **accurate enough**, we consider it trained.  
If not, we **tweak** the model and loop again.

---

## 🎚️ What Are Hyperparameters?

**Hyperparameters** are values that control how the model is trained during these loops.  
For example:

- **Learning Rate**: Determines how much the model updates each cycle  
  - Higher = faster learning, but can overshoot optimal values  
  - Lower = slower but more precise convergence

Tuning hyperparameters helps models learn **efficiently and effectively**.

---

## 🧼 Preprocessing Data

**Preprocessing** refers to preparing data before feeding it to the model.  
This includes:

- **Cleaning**: Handling missing values, fixing types
- **Encoding**: Converting categorical data to numerical formats
- **Scaling**: Adjusting feature ranges

> A well-preprocessed dataset can significantly improve model accuracy and stability.

---

## 📏 Scaling Features

A common preprocessing step is to **scale features to a standard range**, usually **between 0 and 1**.

Why? Because models struggle when features vary wildly in magnitude.  
For example:

- Weight of a bike: ~15 kg  
- Distance traveled: ~2000 meters  

By scaling both to a common range, the model can **learn uniformly from all features**.

---

## 🔢 Using Categories as Features

Models can also work with **categorical features** like:

- `"bicycle"`, `"skateboard"`, `"car"`

To use them effectively, we **encode** them using **one-hot vectors**:

| Category    | One-Hot Encoding |
|-------------|------------------|
| Bicycle     | (1, 0, 0)        |
| Skateboard  | (0, 1, 0)        |
| Car         | (0, 0, 1)        |

This lets the model understand category membership **numerically**.

---

## 🚀 Open in Google Colab

Click below to explore how hyperparameters and preprocessing impact model performance:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-org/your-repo/blob/main/week2_regression/hyperparameter_tuning.ipynb)

---
