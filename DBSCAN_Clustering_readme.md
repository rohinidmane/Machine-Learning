# 🔍 DBSCAN Clustering – Density-Based Clustering

## 📌 Introduction
DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is an unsupervised machine learning algorithm used for clustering data points based on their density.

Unlike K-Means, DBSCAN does not require the number of clusters to be specified in advance. It can also identify noise points and discover clusters with irregular shapes.

## 📊 What This Project Does
- Generates sample datasets using `make_moons()` and `make_circles()`.
- Applies the DBSCAN clustering algorithm.
- Groups data points based on density.
- Identifies noise and outliers.
- Visualizes the clustering results using Matplotlib.
- Counts the number of unique cluster labels.

## 🔄 DBSCAN Workflow

Generate Dataset  
        ↓  
Visualize Original Data  
        ↓  
Initialize DBSCAN Model  
        ↓  
Apply `fit_predict()`  
        ↓  
Assign Cluster Labels  
        ↓  
Visualize Clusters  
        ↓  
Count Unique Labels

## 📊 Dataset Information

This project uses two synthetic datasets from Scikit-learn:

### 1. Make Moons Dataset
- Generates 300 data points.
- Noise level: `0.07`
- Random state: `0`
- Creates two interleaving half-moon-shaped clusters.

### 2. Make Circles Dataset
- Generates 300 data points.
- Factor: `0.5`
- Noise level: `0.05`
- Random state: `0`
- Creates two concentric circular clusters.

## 🧠 Key Concepts Covered

- **DBSCAN:** Density-based clustering algorithm.
- **Epsilon (`eps`):** Maximum distance between two points for them to be considered neighbors.
- **Min Samples (`min_samples`):** Minimum number of neighboring points required to form a dense region.
- **Core Points:** Points having at least the minimum number of points within their epsilon neighborhood.
- **Border Points:** Points located near a core point but having fewer neighbors.
- **Noise Points:** Data points that do not belong to any cluster.
- **Cluster Labels:** Labels assigned to each data point by DBSCAN.

## 🛠️ Tech Stack

- Python
- NumPy
- Matplotlib
- Scikit-learn

## 📈 Operations Performed

| Operation                       | Description                                 |
|---------------------------------|---------------------------------------------|
| `make_moons()`                  | Generates a moon-shaped dataset.            |
| `make_circles()`                | Generates a circular dataset.               |
| `DBSCAN()`                      | Initializes the DBSCAN clustering model.    |
| `fit_predict()`                 | Fits the model and predicts cluster labels. |
| `plt.scatter()`                 | Visualizes data points and clusters.        |
| `cmap`                          | Applies different colors to clusters.       |
| `set(labels)`                   | Finds unique cluster labels.                |
| `len()`                         | Counts the number of unique labels.         |
| `plt.title()`                   | Adds a title to the visualization.          |
| `plt.xlabel()` / `plt.ylabel()` | Adds axis labels.                           |
| `plt.show()`                    | Displays the plot.                          |

## 💡 Key Learnings

1. Understood the working of the DBSCAN clustering algorithm.
2. Learned how to generate synthetic datasets using Scikit-learn.
3. Understood the importance of `eps` and `min_samples` parameters.
4. Learned how DBSCAN identifies clusters based on data density.
5. Understood how DBSCAN detects noise and outliers.
6. Practiced visualizing clustering results using Matplotlib.
7. Learned to count unique cluster labels.

## 📁 Project Structure

```
DBSCAN-Clustering/
│
├── DBSCAN.ipynb
└── README.md
```

## 🚀 Future Improvements

- Experiment with different `eps` and `min_samples` values.
- Compare DBSCAN with K-Means and Hierarchical Clustering.
- Apply DBSCAN to real-world datasets.
- Explore how changing noise levels affects clustering.
- Evaluate clustering performance using suitable clustering metrics.
