# 🌙 Moons Classification with PyTorch

This project demonstrates how to build, train, and evaluate a neural network classifier using PyTorch on a **non-circular, non-linear dataset** known as the `make_moons` dataset.

---

## 🚀 Scenario

Imagine you're working on a **space radar system** that classifies objects based on their radar signature patterns.

You receive a 2D signal from each object. Based on past data, you've learned that:
- **Type A objects** form one moon-shaped cluster
- **Type B objects** form a second, interleaved moon-shaped cluster

Your task is to develop a binary classifier that can **accurately distinguish** between these two types of objects, even when the signal data includes some noise.

This project guides you through the full deep learning workflow:

---

## 🧠 What You'll Learn

- How to **generate non-linear data** using `make_moons()`
- How to **build a binary classification model** in PyTorch
- The importance of **non-linear activation functions** like ReLU
- How to train both:
  - A **linear model** (with no activations)
  - A **non-linear model** (using ReLU)
- How to **visualize decision boundaries** and interpret underfitting vs. good fit
- How to evaluate model performance using **logits**, **sigmoid**, and **accuracy**

---

## 🧪 Dataset

We use the `make_moons()` function from `sklearn.datasets` to generate:
- 1000 samples
- 2 interleaved moon-shaped clusters
- With Gaussian noise added for realism

This dataset is a common benchmark for testing non-linear classifiers.

---

## 🧰 Tools & Libraries

- Python 3.11+
- PyTorch
- Scikit-learn
- Matplotlib
- Helper function: `plot_decision_boundary()` from [Daniel Bourke’s PyTorch course](https://github.com/mrdbourke/pytorch-deep-learning)

---

## 📊 Model Comparison

| Model         | Activation | Decision Boundary | Accuracy | Notes             |
|---------------|------------|-------------------|----------|--------------------|
| `model_linear` | None       | Straight line     | Moderate | Underfits data     |
| `model_relu`   | ReLU       | Non-linear curve  | Higher   | Captures patterns  |

---

## 📁 Project Structure

