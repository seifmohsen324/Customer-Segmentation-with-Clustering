# Customer Segmentation with Clustering

An unsupervised learning notebook that explores customer groups in the supplied mall-customer dataset using K-Means, Agglomerative Clustering, and DBSCAN.

## Project files

```text
.
├── Customer_Segmentation_with_Clustering (1).ipynb
├── Mall_Customers.csv
└── README.md
```

The notebook uses the annual income and spending-score features for clustering and also explores demographic distributions. It scales data for the clustering methods, considers K-Means cluster counts using inertia and silhouette scores, profiles the resulting groups, compares algorithms, uses PCA for a two-dimensional view, and exports analysis outputs when run.

## Requirements and usage

Python and Jupyter are required. The notebook imports pandas, NumPy, Matplotlib, Seaborn, and scikit-learn.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook
```

Open `Customer_Segmentation_with_Clustering (1).ipynb` from the repository root and run the cells in order. The notebook reads `Mall_Customers.csv` using a relative path.

## Interpretation

Cluster labels describe similarity within this dataset; they are not pre-existing customer categories or proof of customer intent. Silhouette scores and visualizations are exploratory and should be evaluated against the intended business use before drawing conclusions.
