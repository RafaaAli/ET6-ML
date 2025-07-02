# Regression in Machine Learning

## Introduction

**Regression** is a commonly used machine learning technique for predicting **numeric values**, such as prices, quantities, or sizes.

It is considered one of the most fundamental approaches in applied machine learning because of its:

- Simplicity and interpretability
- Speed of training and evaluation
- Usefulness in low-data scenarios

> Example: A bike rental company can use regression to predict the number of bicycles rented on a future date, using features like day of the week, season, or temperature.

---

## What is Regression?

Regression works by establishing a **relationship** between:

- **Features** (independent variables) — e.g., temperature, season, day
- **Label** (dependent variable) — the value to predict (e.g., number of rentals)

It’s a form of [**supervised learning**](https://github.com/MIT-Emerging-Talent/ET6-Recitations-6002x/blob/main/Session_08/ML.md) — we train the model on labeled historical data and evaluate its predictions on unseen data.

---

## Simple Example

We aim to predict **bike rentals** using **temperature** as the only feature.

### Sample Data

| Temperature (°F) | Rentals |
|------------------|---------|
| 56               | 115     |
| 61               | 126     |
| 67               | 137     |
| 72               | 140     |
| 76               | 152     |
| 82               | 156     |
| 54               | 114     |
| 62               | 129     |

We train the model using five of these points:

| x (Temp) | y (Rentals) |
|----------|-------------|
| 56       | 115         |
| 61       | 126         |
| 67       | 137         |
| 72       | 140         |
| 76       | 152         |

---
## Model Training

We aim to find a **function** `f(x)` that maps temperature to rental count, like this:

f(x)=y

Let's see how the y and ŷ values compare in a plot:

<p align="center">
  <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session2/Images/1.png" alt="Description" width="600"/>
</p>

Now we need to fit these values to a function, allowing for some random variation. You can probably see that the plotted points form an almost straight diagonal line; in other words, there's an apparent linear relationship between x and y, so we need to find a linear function that's the best fit for the data sample. There are various algorithms we can use to determine this function, which will ultimately find a straight line with minimal overall variance from the plotted points; like this:

<p align="center">
  <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session2/Images/2.png" alt="Description" width="600"/>
</p>

Using linear regression, we find the best-fit line. Let's say the model learns:

f(x) = 20 + 1.7x

This means for every 1°F increase in temperature, rentals increase by ~1.7 bikes.

The line represents a linear function that can be used with any value of x to apply the slope of the line and its intercept (where the line crosses the y axis when x is 0) to calculate y. In this case, if we extended the line to the left, we'd find that when x is 0, y is about 20, and the slope of the line is such that for each unit of x you move along to the right, y increases by about 1.7. We can therefore calculate our f function as 20 + 1.7x.

## Validation Example

Now we test the model on data it hasn’t seen before:

| x (Temp) | y (Actual) | ŷ (Predicted) |
|----------|------------|---------------|
| 82       | 156        | 159.4         |
| 54       | 114        | 111.8         |
| 62       | 129        | 125.4         |

Let's see how the y and ŷ values compare in a plot:

<p align="center">
  <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session2/Images/3.png" alt="Description" width="600"/>
</p>

We've defined our predictive function, we can use it to predict labels for the validation data we held back and compare the predicted values (which we typically indicate with the symbol ŷ, or "y-hat") with the actual known y values.

The plotted points that are on the function line are the predicted ŷ values calculated by the function, and the other plotted points are the actual y values.

There are various ways we can measure the variance between the predicted and actual values, and we can use these metrics to evaluate how well the model predicts.

> 📌 **Note**  
>  
> Machine learning is based in statistics and math, and it's important to be aware of specific terms that statisticians and mathematicians (and therefore data scientists) use.  
>  
> You can think of the difference between a predicted label value and the actual label value as a measure of error. However, in practice, the "actual" values are based on sample observations (which themselves might be subject to some random variance).  
>  
> To make it clear that we're comparing a predicted value (ŷ) with an observed value (y), we refer to the difference between them as the **residuals**.  
>  
> We can summarize the residuals for all of the validation data predictions to calculate the overall **loss** in the model as a measure of its predictive performance.

One of the most common ways to measure the loss is to square the individual residuals, sum the squares, and calculate the mean. Squaring the residuals has the effect of basing the calculation on absolute values (ignoring whether the difference is negative or positive) and giving more weight to larger differences. This metric is called the Mean Squared Error.

For our validation data, the calculation looks like this:

## Error & Loss

The **difference between actual and predicted values** is called the **residual**.

| y (Actual) | ŷ (Predicted) | Residual (y - ŷ) | Residual² |
|------------|---------------|------------------|-----------|
| 156        | 159.4         | -3.4             | 11.56     |
| 114        | 111.8         | 2.2              | 4.84      |
| 129        | 125.4         | 3.6              | 12.96     |
| **Sum**    |               |                  | **29.36** |
| **MSE**    |               |                  | **9.79**  |

**Mean Squared Error (MSE)** gives an average of squared errors.

---

## RMSE and Interpretation

To interpret the error in the original units (rentals), take the square root of MSE:

```math
RMSE = √MSE = √9.79 ≈ 3.13
```
So, is that any good? It's difficult to tell, because MSE value isn't expressed in a meaningful unit of measurement. We do know that the lower the value is, the less loss there is in the model, and therefore, the better it's predicting. This makes it a useful metric to compare two models and find the one that performs best.

Sometimes, it's more useful to express the loss in the same unit of measurement as the predicted label value itself; in this case, the number of rentals. It's possible to do this by calculating the square root of the MSE, which produces a metric known, unsurprisingly, as the Root Mean Squared Error (RMSE).

√9.79 = 3.13

So, our model's RMSE indicates that the loss is just over 3, which you can interpret loosely as meaning that on average, incorrect predictions are wrong by around three rentals.

There are many other metrics that can be used to measure loss in a regression. For example, R2 (R-Squared) (sometimes known as coefficient of determination) is the correlation between x and y squared. This produces a value between 0 and 1 that measures the amount of variance that can be explained by the model. Generally, the closer this value is to 1, the better the model predicts.

---

# Regression

**Supervised machine learning** techniques involve training a model to operate on a set of **features** and predict a **label** using a dataset that includes some already-known label values.

The training process fits the features to the known labels to define a **general function** that can be applied to new features for which the labels are unknown, and predict them.

You can think of this function like this, in which `y` represents the label we want to predict and `x` represents the features the model uses to predict it:

```math
y = f(x)
```

In most cases, `x` is actually a **vector** that consists of multiple feature values, so more precisely, the function could be expressed as:

y = f([x₁, x₂, x₃, ...])


The goal of training the model is to find a function that performs some kind of **calculation on the x values** that produces the result `y`.

We do this by applying a machine learning algorithm that tries to **fit the x values** to a calculation that produces `y` **reasonably accurately** for all of the cases in the training dataset.

---

## Types of Supervised Learning Algorithms

There are many machine learning algorithms for supervised learning. We can broadly divide them into two types:

- **Regression algorithms**  
  Predict a `y` value that is a **numeric value**, such as the price of a house or the number of sales transactions.

- **Classification algorithms**  
  Predict to which **category or class** an observation belongs.  
  The `y` value in a classification model is a **vector of probability values** between 0 and 1 — one for each class — indicating the likelihood of the observation belonging to each class.

---

## 🚲 About This Notebook

In this notebook, we'll focus on **regression**, using an example based on a real study in which data for a **bicycle sharing scheme** was collected and used to predict the number of rentals based on **seasonality** and **weather conditions**.

We'll use a **simplified version** of the dataset from that study.

> 🧪 **Try it on Google Colab**  
> Click the link below to open the notebook directly in Colab:  
> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1bcL4XD7iY7VGdFlzvi2YIjukA5RQ6S4Z)
---

>
📌 **Citation**  
The data used in this exercise is derived from **Capital Bikeshare**, and it's used in accordance with the published license agreement.



