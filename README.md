# KMeans - Wine data clustering
#### Dataset
The used [dataset](https://www.kaggle.com/datasets/harrywang/wine-dataset-for-clustering) is downloaded from Kaggle. This dataset gives
information about various parameters of wine. The data needs to be grouped into different clusters based on its values.
Dataset has 178 rows and 13 columns. All columns have numerical values and no values are missing.
___
#### KMeans
KMeans works by randomly selecting n data points to be the initial cluster centers. 
The rest of the data are then grouped into clusters to which they are closest.

When all the data are classified into clusters, the mean of each cluster
is observed and the data is regrouped by clusters depending on the distance from its center. 
The procedure is repeated until every cluster remains the same as in the previous step.
___
#### Elbow method
Elbow method is used to determine the optimal number of clusters. A KMeans model is created for each number of clusters 
and the sum of squared errors (SSE) is determined.

The optimal number of clusters is the one where the change in SSE is significantly smaller than 
the previous ones, which is shown in the shape of an elbow on the graph.

In this example, elbow is noticeable at 6 clusters.

![Elbow method](https://github.com/mato-m/kmeans-wine/assets/64593617/0aa0af44-7ab4-42c0-a677-d24686b38f38)


#### Sillhouette score

The Silhouette score ranges between 1 and -1.

A score closer to 1 indicates that the cluster is well defined,

while a score closer to -1 indicates that the data are probably in the wrong clusters.

Using the silhouette score we can also see that the optimal number of clusters is 6.

![Sillhouette score](https://github.com/mato-m/kmeans-wine/assets/64593617/b077b27a-54c3-4f9f-af1f-cc146aa9c90b)

#### Principal Component Analysis (PCA)

In order to provide a simple visual representation of the data, the dimensionality of the data is reduced using Principal Component Analysis (PCA).

In this case, PCA will split the existing 13 columns into two columns, which are then clustered into the optimal number of clusters.

The following chart shows clustered data that was reduced to two dimensions using PCA. The red crosses represent centroids of each cluster.

![Clustered data](https://github.com/mato-m/kmeans-wine/assets/64593617/cda72233-5a70-4bcd-b8d9-8e93c617da9a)

