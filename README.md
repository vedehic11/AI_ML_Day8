# Customer Segmentation with K-Means Clustering

## Overview
This notebook implements K-Means clustering to segment mall customers based on their demographics and spending patterns. The analysis identifies natural groupings of customers that can inform targeted marketing strategies.

## Dataset
- **Source**: Mall Customer Segmentation Data (Kaggle)
- **Features**: Age, Annual Income (k$), Spending Score (1-100)
- **Access Method**: KaggleHub API

## Methodology

### Data Preprocessing
- Data loaded and checked for missing values (none found)
- Feature selection focusing on demographic and spending attributes
- Standardization applied to normalize features

### Dimensionality Reduction
- Principal Component Analysis (PCA) implemented to reduce dimensions to 2D
- Initial visualization of unclustered data in reduced space

### Cluster Analysis
- **Optimal Cluster Determination**:
  - Elbow method applied with K ranging from 1 to 10
  - Inertia (within-cluster sum of squares) plotted against K values
  - K=5 selected as the optimal number of clusters

- **Model Implementation**:
  - K-Means algorithm with 5 clusters and fixed random state
  - Cluster assignments applied to the dataset

### Evaluation and Visualization
- **Cluster Quality Assessment**:
  - Silhouette score calculated to measure clustering quality
  - Visual inspection of cluster separation in PCA space
  
- **Cluster Profiling**:
  - Mean values calculated for each feature across clusters
  - Radar chart visualization showing distinctive characteristics of each segment

## Key Results
- Five distinct customer segments identified with clear pattern differences
- Silhouette score indicates fair clustering quality with some potential overlap
- Visual inspection confirms meaningful separation in reduced feature space
- Each segment shows unique combinations of age, income, and spending behavior

## Output
- Clustered dataset saved as "Clustered_Mall_Customers.csv"
- Comprehensive visualization of customer segments
- Detailed cluster profiles for business insights

## Dependencies
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- kagglehub

## Business Applications
The identified customer segments can be used for:
- Personalized marketing campaigns
- Product recommendation systems
- Store layout optimization
- Targeted promotional strategies
