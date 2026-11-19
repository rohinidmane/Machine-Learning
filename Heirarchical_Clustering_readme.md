# 🌳 Hierarchical Clustering – Unsupervised Machine Learning

## 📌 Introduction
Hierarchical Clustering is an unsupervised machine learning algorithm used to group similar data points into clusters based on their distance or similarity.

It creates a hierarchy of clusters represented using a tree-like diagram called a Dendrogram.

This project explores Hierarchical Clustering using SciPy and Agglomerative Clustering using Scikit-learn. It also demonstrates data scaling, cluster formation, and visualization using sample datasets.

## 📊 What This Project Does
- Creates sample datasets using NumPy and Scikit-learn.
- Applies Hierarchical Clustering using the Ward linkage method.
- Generates and visualizes dendrograms.
- Uses horizontal lines to identify possible cluster divisions.
- Assigns cluster labels using `fcluster()`.
- Implements Agglomerative Clustering.
- Generates synthetic data using `make_blobs()`.
- Applies Standard Scaling before clustering.
- Visualizes the final clusters using Matplotlib.

## 🔄 Hierarchical Clustering Workflow

Generate Sample Dataset  
        ↓  
Scale the Data (where required)  
        ↓  
Calculate Linkage Matrix  
        ↓  
Generate Dendrogram  
        ↓  
Choose Number of Clusters  
        ↓  
Assign Cluster Labels  
        ↓  
Visualize Clusters

## 📊 Dataset Information

This project uses two types of sample datasets.

### 1. Manually Created Dataset

A small dataset created using NumPy containing six data points.

```python
X = np.array([
    [1, 2], [2, 3], [3, 2],
    [8, 7], [7, 8], [8, 8]
])
```

- Number of data points: 6
- Number of features: 2
- Number of clusters: 2

### 2. Make Blobs Dataset

A synthetic dataset generated using Scikit-learn.

- Number of samples: 100
- Number of centers: 3
- Cluster standard deviation: 1.2
- Random state: 42
- Number of features: 2

The dataset is scaled using StandardScaler before applying Hierarchical Clustering.

## 🧠 Key Concepts Covered

### 1. Hierarchical Clustering
- An unsupervised learning algorithm.
- Groups similar data points based on distance.
- Creates a hierarchy of clusters.
- Does not require specifying the number of clusters when building the full hierarchy.

### 2. Agglomerative Clustering
- A bottom-up approach to Hierarchical Clustering.
- Initially treats every data point as an individual cluster.
- Repeatedly merges the closest clusters until the required number of clusters is reached.

### 3. Dendrogram
- A tree-like diagram representing the merging of clusters.
- Helps understand relationships between data points.
- Helps choose an appropriate number of clusters by cutting the tree at a selected height.

### 4. Linkage Methods

Different linkage methods calculate the distance between clusters differently.

- **Ward:** Merges clusters while minimizing the increase in within-cluster variance.
- **Single:** Uses the minimum distance between points in two clusters.
- **Complete:** Uses the maximum distance between points in two clusters.
- **Average:** Uses the average distance between points in two clusters.

### 5. Standard Scaling
- Standardizes features using mean and standard deviation.
- Helps prevent features with larger scales from dominating distance calculations.
- Produces features with approximately zero mean and unit variance.

### 6. Cluster Labels
- Assigns each data point to a cluster.
- Helps identify groups formed by the clustering algorithm.

## 🛠️ Tech Stack

- Python
- NumPy
- Pandas
- Matplotlib
- SciPy
- Scikit-learn

## 📈 Operations Performed

| Operation                  | Description                                      |
|----------------------------|--------------------------------------------------|
| `np.array()`               | Creates sample datasets.                         |
| `make_blobs()`             | Generates synthetic clustering data.             |
| `StandardScaler()`         | Standardizes numerical features.                 |
| `fit_transform()`          | Fits the scaler and transforms the data.         |
| `linkage()`                | Creates the hierarchical linkage matrix.         |
| `dendrogram()`             | Visualizes the hierarchy of clusters.            |
| `fcluster()`               | Forms flat clusters from the linkage matrix.     |
| `AgglomerativeClustering()`| Initializes the Agglomerative Clustering model.  |
| `fit_predict()`            | Fits the model and assigns cluster labels.       |
| `plt.axhline()`            | Draws a horizontal line on the dendrogram.       |
| `plt.scatter()`            | Visualizes data points and clusters.             |
| `plt.legend()`             | Displays cluster labels.                         |
| `plt.grid()`               | Adds grid lines to the plot.                     |
| `plt.show()`               | Displays the visualizations.                     |

## 💡 Key Learnings

1. Understood the working of Hierarchical Clustering.
2. Learned the difference between Agglomerative and other hierarchical approaches.
3. Understood how dendrograms represent cluster relationships.
4. Practiced creating linkage matrices using SciPy.
5. Learned different linkage methods such as Ward, Single, Complete, and Average.
6. Understood how to select the number of clusters using dendrograms.
7. Learned to assign cluster labels using `fcluster()`.
8. Practiced implementing Agglomerative Clustering using Scikit-learn.
9. Understood the importance of feature scaling in distance-based clustering.
10. Learned to visualize clusters using Matplotlib.

## 📁 Project Structure

```
Hierarchical-Clustering/
│
├── Hierarchical_Clustering.ipynb
└── README.md
```

## 🚀 Future Improvements

- Experiment with different linkage methods.
- Compare Ward, Single, Complete, and Average linkage.
- Experiment with different numbers of clusters.
- Compare Hierarchical Clustering with K-Means and DBSCAN.
- Apply Hierarchical Clustering to real-world datasets.
- Explore different distance metrics.
- Evaluate clustering quality using Silhouette Score.
