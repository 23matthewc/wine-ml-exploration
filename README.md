# Wine Dataset Exploration and Clustering Analysis

This project explores a curated dataset of 178 wines characterized by 13 chemical and physical attributes. The goal is to apply various unsupervised machine learning techniques — including dimensionality reduction and clustering — to uncover natural groupings in the data and better understand the underlying structure of the wine types.

---

## Dataset Description

The dataset contains 178 samples (wines), each described by 13 attributes:

1. Alcohol content (%)  
2. Malic acid concentration (g/L)  
3. Ash content (mg/L)  
4. Alkalinity of the Ash (g/L of potassium carbonate)  
5. Magnesium (mg/L)  
6. Total phenols (mg/L)  
7. Flavonoids (mg/L)  
8. Stilbenes (mg/L)  
9. Proanthocyanins (mg/L)  
10. Color intensity  
11. Hue  
12. OD280 (Protein concentration)  
13. Proline content (amino acid)  

The data is clean, with no missing values.

---

## Methods and Analyses

### Dimensionality Reduction

- **Principal Component Analysis (PCA):**  
  Used to reduce the data to principal components, identify how many components explain significant variance (eigenvalues > 1), and interpret the main axes of variation.

- **t-Distributed Stochastic Neighbor Embedding (t-SNE):**  
  Applied for nonlinear dimensionality reduction, visualizing clusters in 2D. The effect of perplexity on the Kullback-Leibler divergence was analyzed.

- **Multidimensional Scaling (MDS):**  
  A 2D embedding computed to compare with t-SNE results and analyze stress values indicating fit quality.

### Clustering

- **k-Means Clustering:**  
  Performed on a 2D embedding (chosen from PCA, t-SNE, or MDS) with the number of clusters optimized via the Silhouette method. Cluster quality assessed by within-cluster sum of distances.

- **Density-Based Spatial Clustering of Applications with Noise (DBSCAN):**  
  Used to identify clusters based on density with hyperparameters epsilon (radius) and minPoints (minimum points). The choice of parameters was justified by visual inspection and clustering performance.

---

## Key Questions Addressed

1. How many principal components have eigenvalues above 1? How much variance is explained by the first two PCs, and what do they represent?  
2. How does t-SNE’s KL-divergence depend on perplexity values from 5 to 150? What does the 2D t-SNE embedding look like at perplexity 20?  
3. What is the stress value of a 2D MDS embedding, and how does its visualization compare to t-SNE?  
4. Using a 2D embedding, what is the optimal number of clusters from the Silhouette method? How does k-Means perform with this k? What is the total within-cluster sum of distances?  
5. Using the same embedding, how does DBSCAN cluster the data? How were epsilon and minPoints selected and why?

---

## Results and Visualizations

The project includes detailed plots such as:

- Scree plot of PCA eigenvalues  
- 2D scatter plots of PCA, t-SNE, and MDS embeddings  
- Perplexity vs. KL-divergence plot for t-SNE  
- Clustered scatter plots from k-Means and DBSCAN with color-coded cluster labels

---

## Interpretation and Insights

These analyses shed light on the underlying groupings of the wines, indicating how many distinct wine types may exist based on chemical profiles. Differences in cluster assignments between methods are discussed, highlighting strengths and weaknesses of each approach.

---
