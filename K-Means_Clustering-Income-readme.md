# 🎯 K-Means Clustering – Income Dataset

## 📌 Introduction
K-Means Clustering is an unsupervised machine learning algorithm used to divide data points into a specified number of clusters based on their similarity.

It groups data points by assigning them to the nearest cluster centroid and repeatedly updating the centroid positions until the clusters become stable.

This project uses an Income dataset to perform K-Means Clustering based on Age and Income. It also explores Feature Scaling and the Elbow Method to identify the optimal number of clusters.

## 📊 What This Project Does
- Loads the Income dataset using Pandas.
- Explores dataset information using `df.info()`.
- Visualizes Age and Income using scatter plots.
- Applies K-Means Clustering with 3 clusters.
- Identifies cluster labels and centroid locations.
- Visualizes clusters using different colors.
- Applies Min-Max Scaling to Age and Income.
- Performs K-Means Clustering again after scaling.
- Uses the Elbow Method to find the optimal number of clusters.
- Calculates Sum of Squared Errors (SSE) using model inertia.

## 🔄 K-Means Clustering Workflow

Load Income Dataset  
        ↓  
Explore and Visualize Data  
        ↓  
Initialize K-Means Model  
        ↓  
Create 3 Clusters  
        ↓  
Assign Cluster Labels  
        ↓     
Identify Cluster Centroids  
        ↓  
Visualize Clusters  
        ↓  
Apply Min-Max Scaling  
        ↓  
Perform K-Means Again  
        ↓  
Apply Elbow Method  
        ↓  
Find Optimal Number of Clusters

## 📊 Dataset Information

**Dataset:** Income Dataset

**File Name:** `income.csv`

The dataset contains information about individuals based on their age and income.

**Features Used:**
- `Age`
- `Income($)`

**Target:** No predefined target variable, because K-Means is an unsupervised learning algorithm.

**Number of Clusters:** 3 (initial clustering)

## 🧠 Key Concepts Covered

### 1. K-Means Clustering
- An unsupervised machine learning algorithm.
- Groups similar data points into clusters.
- Uses centroids to represent the center of each cluster.
- Assigns each data point to its nearest centroid.

### 2. Centroids
- The center point of a cluster.
- Calculated using the mean position of the data points assigned to that cluster.
- Updated during each iteration of the K-Means algorithm.

### 3. Feature Scaling
Feature Scaling brings numerical features into a similar range so that features with larger values do not dominate distance calculations.

This project uses Min-Max Scaling.

### 4. Min-Max Scaling
- Scales values into a range between 0 and 1 by default.
- Helps normalize features with different measurement ranges.
- Important for distance-based algorithms such as K-Means.

### 5. Elbow Method
- Helps determine the optimal number of clusters.
- Runs K-Means with different values of K.
- Calculates the SSE for each value.
- Plots K against SSE.
- The elbow point indicates a suitable number of clusters.

### 6. Inertia (WCSS)
Inertia measures the sum of squared distances between each data point and its assigned cluster centroid.

It is also called Within-Cluster Sum of Squares (WCSS).

**Formula:**

\[
WCSS = \sum_{i=1}^{k}\sum_{x \in C_i} ||x-\mu_i||^2
\]

Where:
- `k` = Number of clusters
- `Cᵢ` = Data points belonging to cluster i
- `x` = Individual data point
- `μᵢ` = Centroid of cluster i

Lower inertia indicates that data points are closer to their respective centroids. However, inertia generally decreases as the number of clusters increases.

## 🛠️ Tech Stack

- Python
- Pandas
- Matplotlib
- Scikit-learn

## 📈 Operations Performed

| Operation                      | Description                                             |
|--------------------------------|---------------------------------------------------------|
| `pd.read_csv()`                | Loads the Income dataset.                               |
| `df.info()`                    | Displays dataset information.                           |
| `plt.scatter()`                | Visualizes Age and Income.                              |
| `KMeans()`                     | Initializes the K-Means clustering model.               |
| `fit_predict()`                | Fits the model and assigns cluster labels.              |
| `cluster_centers_`             | Returns the coordinates of cluster centroids.           |
| `df[df['Cluster']==0]`         | Filters data points belonging to cluster 0.             |
| `MinMaxScaler()`               | Initializes the Min-Max scaling method.                 |
| `fit()`                        | Learns the scaling parameters.                          |
| `transform()`                  | Scales the selected feature values.                     |
| `inertia_`                     | Returns the sum of squared distances within clusters.   |
| `range()`                      | Generates different cluster counts for the Elbow Method.|
| `plt.plot()`                   | Plots the Elbow Method graph.                           |
| `plt.xlabel()` / `plt.ylabel()`| Adds labels to the graph axes.                          |
| `plt.show()`                   | Displays visualizations.                                |

## 💡 Key Learnings

1. Understood the working of K-Means Clustering.
2. Learned how to group data points based on similarity.
3. Understood the role of centroids in cluster formation.
4. Practiced visualizing clusters using scatter plots.
5. Learned why Feature Scaling is important for K-Means.
6. Applied Min-Max Scaling to Age and Income features.
7. Compared clustering before and after feature scaling.
8. Understood the Elbow Method for selecting the number of clusters.
9. Learned about inertia and Within-Cluster Sum of Squares (WCSS).
10. Practiced implementing K-Means using Scikit-learn.

## 📁 Project Structure

```text
KMeans-Clustering/
│
├── KMeans_Clustering.ipynb
├── income.csv
└── README.md
```

## 🚀 Future Improvements

- Experiment with different numbers of clusters.
- Compare clustering results before and after feature scaling.
- Identify the optimal K using the Elbow Method.
- Experiment with different centroid initialization methods.
- Use Silhouette Score to evaluate clustering quality.
- Apply K-Means to other real-world datasets.
- Compare K-Means with DBSCAN and Hierarchical Clustering.