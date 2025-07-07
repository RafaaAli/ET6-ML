# 🧠 Create Multiclass Classification Models

---

## 🔢 What is Multiclass Classification?

Multiclass classification is an extension of binary classification where the model can predict **more than two possible classes**.

> Example: A health clinic might extend a binary diabetes model to classify patients into:
> - Non-diabetic  
> - Type-1 diabetic  
> - Type-2 diabetic

The model still produces probability values for each class, and the **probabilities sum to 1**. The class with the **highest probability** is selected as the prediction.

---

## 🧠 How Multiclass Classification Works

Multiclass classification is typically built by **combining multiple binary classifiers**. Two common strategies are:

---

### 🔸 One-vs-Rest (OVR)

- A separate classifier is trained for each class.
- Each classifier learns to distinguish **one class vs. all others**.

**Example (4 shape classes):**
- Classifier 1: square vs not-square  
- Classifier 2: circle vs not-circle  
- Classifier 3: triangle vs not-triangle  
- Classifier 4: hexagon vs not-hexagon

---

### 🔸 One-vs-One (OVO)

- A separate classifier is trained for **each pair** of classes.

**Example (4 shape classes):**
- square vs circle  
- square vs triangle  
- square vs hexagon  
- circle vs triangle  
- circle vs hexagon  
- triangle vs hexagon

The final prediction is based on **combining all binary results** to determine the most likely class.

---

## 🧰 Implementation in Scikit-Learn

Fortunately, **Scikit-Learn supports multiclass classification out of the box**.  
Most classifiers automatically apply OVR or support both strategies.

This means you can often use the **same code as binary classification**, and Scikit-Learn handles the rest internally.

---

## 🚀 Next Step: Train and Evaluate Multiclass Classification Models

Click the button below to open the hands-on exercise in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-org/your-repo/blob/main/week3_classification/multiclass_classification.ipynb)

---
