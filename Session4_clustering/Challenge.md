# Clustering Challenge: Uncover Hidden Patterns in Data

## Scenario

You’ve just joined a data science team working on a project to analyze behavioral patterns from an anonymized dataset. The dataset contains **three numeric features** (`A`, `B`, and `C`), but no labels. Your task is to use **unsupervised machine learning** to identify natural groupings in the data.

The twist? You don’t know how many clusters exist—your job is to find out!

---

## Dataset Description

The dataset is in `clusters.csv`, with the following columns:

| A          | B          | C          |
|------------|------------|------------|
| -0.087492  | 0.398000   | 0.014275   |
| -1.071705  | -0.546473  | 0.072424   |
| ...        | ...        | ...        |

Each row is a sample. Your task is to identify **how many meaningful clusters** exist and group the data accordingly.

---

## Objectives

Your goal is to:

1. Load and explore the dataset
2. Normalize the features using `MinMaxScaler`
3. Apply **PCA** to reduce the features to 2D for visualization
4. Use the **Elbow Method** to determine the best number of clusters (`k`)
5. Train a **KMeans** model with the chosen `k`
6. Visualize the clusters in 2D space
7. Train an **Agglomerative Clustering** model for comparison
8. Visualize the agglomerative clusters
9. Compare the results and reflect on which model performs better

---
## import Data Set
```python
import pandas as pd

data = pd.read_csv('https://raw.githubusercontent.com/MIT-Emerging-Talent/ET6-ML/refs/heads/main/Session4_clustering/clusters.csv')
data.head()
```

## Suggested Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.preprocessing import MinMaxScaler
from sklearn.decomposition import PCA
from sklearn.cluster import KMeans, AgglomerativeClustering
```

## Solution 

[Open in Google Colab](https://colab.research.google.com/drive/1kxjKYsSLkdTueEZVEiK7TZhpxwNnVG8O#scrollTo=-yts4YblcMAk)
