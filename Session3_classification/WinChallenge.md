# 🍷 Classification Challenge: Wine Cultivar Prediction

Wine experts can identify wines from specific vineyards through smell and taste, but the factors that give different wines their individual characteristics are actually based on their **chemical composition**.

In this challenge, you will train a **classification model** to analyze the chemical and visual features of wine samples and classify them based on their **cultivar (grape variety)**.

---

### Challenge Objective

Your task is to:

- Explore the dataset and train a classification model.
- Evaluate your model using **precision**, **recall**, **F1-score**, and **AUC**.
- Your goal: **achieve a recall greater than 0.95 (95%)**.

> There is no single correct solution — experiment, document your steps.

---

###  Train and Evaluate a Model

Add the necessary code and markdown cells to:

- Preprocess and split the dataset into training and testing sets.
- Train at least **two classification models** (e.g., Logistic Regression, Random Forest).
- Evaluate your models using a **confusion matrix** and classification metrics.
- Optionally, plot **ROC curves** to visualize performance.
- Use `Pipeline` for consistent preprocessing (e.g., scaling with `StandardScaler`).

---

###  Use the Model on New Data

Once you're satisfied with the model's performance, use it to predict the class of the following two **new wine samples**:

```python
sample1 = [13.72, 1.43, 2.5, 16.7, 108, 3.4, 3.67, 0.19, 2.04, 6.8, 0.89, 2.87, 1285]
sample2 = [12.37, 0.94, 1.36, 10.6, 88, 1.98, 0.57, 0.28, 0.42, 1.95, 1.05, 1.82, 520]
```

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16nx9LuP1840OH_IF9YiWPa7ZnPC4o-Ma#scrollTo=7Nx1lI9B_AM7)
