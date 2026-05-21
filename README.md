# 🛍️ Customer Segmentation with Clustering

An unsupervised machine learning project that segments mall customers into meaningful groups based on income and spending behavior using K-Means, Agglomerative, and DBSCAN clustering.

---

## 📋 Overview

This project applies clustering techniques to identify distinct customer segments from a mall dataset. The goal is to uncover natural groupings — such as "Premium", "Budget", or "Value Seekers" — that can inform targeted marketing strategies and business decisions.

---

## 📂 Project Structure

```
├── Customer_Segmentation_with_Clustering.ipynb   # Main notebook
├── Mall_Customers.csv                            # Dataset (200 customers)
├── mall_customers_clustered.csv                  # Output: data with cluster labels
├── kmeans_centers.csv                            # Output: cluster centers
├── cluster_profile.csv                           # Output: per-cluster stats
├── segment_summary.csv                           # Output: stakeholder summary
├── method_comparison.csv                         # Output: algorithm comparison
├── kmeans_clusters.png                           # Figure: K-Means scatter plot
├── agg_clusters.png                              # Figure: Agglomerative scatter plot
├── dbscan_clusters.png                           # Figure: DBSCAN scatter plot
├── pca_kmeans.png                                # Figure: PCA projection
└── README.md
```

---

## 📊 Dataset

**Source:** [Mall Customers — Kaggle](https://www.kaggle.com/)

| Property | Value |
|---|---|
| Records | 200 customers |
| Target variable | None (unsupervised) |
| Features used | `Annual Income (k$)`, `Spending Score (1-100)` |

**All columns:**
`CustomerID`, `Gender`, `Age`, `Annual Income (k$)`, `Spending Score (1-100)`

---

## 🔧 Workflow

1. **Data Loading & Cleaning** — rename columns, strip whitespace, check for nulls
2. **EDA** — distribution plots for income, spending, and age; income vs. spending scatter by gender
3. **Feature Scaling** — StandardScaler for K-Means/Agglomerative; MinMaxScaler for DBSCAN
4. **Optimal k Selection** — Elbow method (inertia) + Silhouette score across k = 2–10
5. **K-Means Clustering** — fit with best k, visualize with cluster centers
6. **Cluster Profiling** — mean/median/min/max per cluster; semantic segment labels
7. **Alternative Algorithms** — Agglomerative (Ward linkage) and DBSCAN (k-distance plot for eps)
8. **Method Comparison** — silhouette scores across all three algorithms
9. **PCA Projection** — 2D visualization of clusters via PCA
10. **Export** — clustered CSV, centers, profiles, and figures saved to disk

---

## 🏷️ Customer Segments

Clusters are automatically labeled based on median income and spending thresholds:

| Segment | Description |
|---|---|
| **Premium** | High income, high spending |
| **Cautious** | High income, low spending |
| **Value Seekers** | Low income, high spending |
| **Budget** | Low income, low spending |

---

## 📈 Models & Evaluation

| Algorithm | Notes |
|---|---|
| K-Means | Optimal k via elbow + silhouette |
| Agglomerative (Ward) | Hierarchical, compared via silhouette |
| DBSCAN | Density-based; handles noise points (label = -1) |

All three are compared using the **Silhouette Score** at the end of the notebook.

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data loading and manipulation
- **NumPy** — numerical operations
- **Matplotlib / Seaborn** — visualizations
- **Scikit-learn** — clustering, scaling, PCA, and evaluation metrics

---

## 🚀 Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/your-username/customer-segmentation.git
cd customer-segmentation

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# 3. Launch the notebook
jupyter notebook Customer_Segmentation_with_Clustering.ipynb
```

Make sure `Mall_Customers.csv` is in the same directory as the notebook before running.

---

## 📌 Topics Covered

- Unsupervised learning and clustering
- K-Means, Agglomerative, and DBSCAN algorithms
- Optimal cluster selection (Elbow method, Silhouette score)
- Feature scaling strategies (StandardScaler vs. MinMaxScaler)
- Dimensionality reduction with PCA
- Customer profiling and semantic segment labeling
