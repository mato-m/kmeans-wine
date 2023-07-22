# KMeans in wine clustering
#### Dataset
The used [dataset](https://www.kaggle.com/datasets/harrywang/wine-dataset-for-clustering) is downloaded from Kaggle. This dataset gives
information about various parameters of wine. The data needs to be grouped into different clusters based on its values.
Dataset has 178 rows and 13 columns.
___
#### Kmeans
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

![Elbow method](https://github.com/mato-m/kmeans-wine/assets/64593617/dc5c388e-4789-4686-b903-6d6783cb4208)

#### Sillhouete score
