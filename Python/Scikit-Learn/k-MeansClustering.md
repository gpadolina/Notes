Clustering algorithms are unsupervised machine learning models that seek to learn an optimal division or discrete labeling of groups of
points from the properties of the data. The basis of k-means model are:
  1. The "cluster center" is the arithmetic mean of the all the points belonging to the cluster.
  2. Each point is closer to its own cluster center than to other cluster centers.
```
from sklearn.cluster import KMeans
kmeans = KMeans(n_cluster=2)
kmeans.fit(X)
y_kmeans = kmeans.predict(X)
```
