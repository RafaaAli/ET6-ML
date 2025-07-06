# ML Model Comparison Challenge

Welcome to this hands-on challenge from the *Empowering Insight* ML workshop. In this task, you'll build and compare machine learning models for regression and classification — with a focus on modeling, not data exploration.

## Objective

This challenge is designed to help you practice training and evaluating different ML models. We intentionally skip detailed data exploration and visualization so you can gain more practical experience with setting up, fitting, and tuning models.

---

## Challenge 1: California House Price Prediction (Regression)

### Scenario

You are given a dataset containing socio-economic and geographic information about California districts. Your goal is to predict the **median house value** based on features such as income, housing age, and population.

### What to Do

1. Load the California Housing dataset.
   ```pyton
   from sklearn.datasets import fetch_california_housing
   housing = fetch_california_housing(as_frame=True)
   data = housing.frame
   ```
   
3. Split the data into training and test sets.
4. Train the following regression models:
   - Linear Regression
   - Lasso Regression
   - Random Forest Regressor
   - Gradient Boosting Regressor
5. Evaluate each model using **Root Mean Squared Error (RMSE) and R ^2**.
6. Plot regression lines for a single feature to compare model fit.

💡 **Focus**: How do ensemble and regularized models compare to simple linear regression?

---

## Challenge 2: Mushroom Classification (Decision Tree)

### Scenario

Using the UCI Mushroom dataset, build a classifier to determine if a mushroom is **edible or poisonous** based on physical attributes.

### What to Do

1. Load and preprocess the dataset using one-hot encoding.
2. Split the dataset into training and test sets.
3. Train a **Decision Tree Regressor**.

---

## Key Skills Practiced

- Regression model training
- Use of RMSE and classification metrics
- Code organization for real-world modeling tasks

---

## Final Note

Please attempt to complete the challenges on your own. We’ll provide a solution notebook for review — compare it with your work and reflect on any differences or improvements.

This exercise is a great preparation step for the **Collaborative Data Science Project (CDSP)**, where you’ll model real data using similar tools and approaches.

Happy modeling! 
