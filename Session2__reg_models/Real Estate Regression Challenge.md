# 🧠 Regression Challenge: Predicting Property Prices

Predicting the **selling price** of a residential property depends on several factors, including property age, nearby amenities, and location.

In this challenge, you'll use a dataset of **real estate sales transactions** to predict the **price-per-unit** of a property based on its features. The price-per-unit in this dataset corresponds to a unit measurement of **3.3 square meters**.

---

## 📚 Dataset Source

Citation:
> Yeh, I. C., & Hsu, T. K. (2018). *Building real estate valuation models with comparative approach through case-based reasoning.* Applied Soft Computing, 65, 260-271.

Retrieved from the UCI ML Repository:
> Dua, D. and Graff, C. (2019). *UCI Machine Learning Repository.* Irvine, CA: University of California, School of Information and Computer Science.

---

## 📊 Review the Data

Run the following Python code to load and inspect the dataset:

```python
import pandas as pd

# Load the dataset
data = pd.read_csv('data/real_estate.csv')
data.head()
```

---

## 💡 Feature Descriptions

| Feature                    | Description                                                        |
|---------------------------|--------------------------------------------------------------------|
| `transaction_date`        | Date of transaction (e.g., 2013.250 = March 2013)                  |
| `house_age`               | Age of the house (in years)                                        |
| `transit_distance`        | Distance to the nearest light rail station (in meters)            |
| `local_convenience_stores`| Number of nearby convenience stores                                |
| `latitude`                | Geographic coordinate - latitude                                   |
| `longitude`               | Geographic coordinate - longitude                                  |
| `price_per_unit`          | House price per unit area (target label, in 3.3 m² units)          |

---

## 🎯 Task

Your challenge is to:

- 🔍 Explore and prepare the data  
- 🧠 Select predictive features that help predict the `price_per_unit`  
- 🛠️ Train a regression model to predict housing prices  
- 🎯 Achieve a **Root Mean Squared Error (RMSE) < 7** on your test set  

There is **no single correct solution** — be creative! Use markdown and code cells in your notebook to document your process and decisions.

📎 *A sample solution is available in* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1owppMYGhRs9sgOqen9ODF1nKINIsS40n)

---

## 🧪 Use the Trained Model

Once you have a trained model, use it to predict `price_per_unit` for the following transactions:

| transaction_date | house_age | transit_distance | local_convenience_stores | latitude  | longitude |
|------------------|-----------|------------------|---------------------------|-----------|-----------|
| 2013.167         | 16.2      | 289.3248         | 5                         | 24.98203  | 121.54348 |
| 2013.000         | 13.6      | 4082.015         | 0                         | 24.94155  | 121.50381 |



