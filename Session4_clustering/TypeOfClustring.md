# Training a Clustering Model

There are several clustering algorithms, but one of the most commonly used is **K-Means Clustering**. Here's how it works:

### K-Means Clustering Steps:
1. **Vectorization**: Feature values are converted into coordinates.  
   For example, in our flower dataset, two features (petals and leaves) form 2D vectors.
2. **Choose k Clusters**: Decide how many clusters you want (k).  
   Example: If `k = 3`, we aim to group data into 3 clusters.
3. **Initialize Centroids**: Randomly place `k` centroids in the data space.
4. **Assign Points to Nearest Centroid**: Each data point is assigned to its nearest centroid.
5. **Update Centroids**: Move each centroid to the average position of the points assigned to it.
6. **Repeat**: Recalculate assignments and update centroids until:
   - Clusters stabilize (no major changes)
   - A maximum number of iterations is reached

### K-Means in Action
*The following animation shows this process visually:*

<p align="center">
  <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session4/Images/k-means.gif" alt="Description" width="600"/>
</p>

![K-Means Clustering Animation](https://your-public-url.com/kmeans-clustering.gif)

---

## Hierarchical Clustering

Another important technique is **Hierarchical Clustering**, where clusters are nested within larger clusters. This creates a tree-like structure where data can be grouped at different levels of granularity.

### Example:
- Words like _“angry”_ and _“happy”_ may form a small cluster of emotion-related adjectives.
- This group could belong to a broader cluster of human-related adjectives like _“young”_, _“handsome”_, etc.
- That cluster can be part of an even broader one for all adjectives.

### Key Points:
- Does **not** require specifying the number of clusters in advance.
- Helps explore relationships between groups.
- Tends to be more **interpretable** than K-Means in some scenarios.
- Can be **computationally expensive** — not always ideal for large datasets.

### Visualizing Hierarchical Clustering

 <p align="center">
    <img src="https://github.com/MIT-Emerging-Talent/ML/blob/main/Session4/Images/6.jpg" alt="Description" width="600"/>
  </p>

---

### Exercise - Train and evaluate advanced clustering models
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ylyam6zsGUPw-9wC7nRxlVUsrnvbAQw6?usp=sharing)
