# Clustering-Based Semi-Supervised Classification

This Python script demonstrates the use of clustering for semi-supervised classification. It's based on the idea of assigning labels to unlabeled data points based on their proximity to cluster centers.

## Data Preparation

The code begins by loading labeled and unlabeled data from CSV files, `train_labeled.csv` and `train_unlabeled.csv`, respectively. The labeled data is used to perform clustering and assign labels to the unlabeled data.

## Clustering with Elbow Method

The Elbow Method is applied to determine the optimal number of clusters. It calculates the Sum of Squared Errors (SSE) for different numbers of clusters, helping you identify an appropriate cluster count. The results are plotted to visualize the elbow point.

## Clustering

After determining the optimal number of clusters (e.g., 4 clusters), the code proceeds with clustering. It randomly initializes cluster centers, assigns data points to the nearest cluster, and updates cluster centers iteratively until convergence.

## Assigning Labels to Clusters

Once clustering is complete, labels are assigned to clusters based on the majority vote from the labeled data. This step aims to identify the most likely label for each cluster.

## Test Data Prediction

Finally, the code reads test data from `test_data.csv`, finds the nearest cluster center for each test data point, and assigns predicted labels based on the clustering results.
