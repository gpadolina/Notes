Manifold learning is a class of unsupervised estimators that seeks to describe datasets as low-dimensional manifolds embedded in high-
dimensional spaces.

## Multidimensional Scaling (MDS)
In MDS, the x and y values are not necessarily fundamental to the relationships in the data. What is fundamental is the distance between
each point and the other points in the dataset. Using distance matrix, for N points, construct an *N x N* array such that entry *(i, j)
contains the distance between point i and point j.
```
from sklearn.metrics import pairwise_distances
D = pairwise_distances(X)
D.shape
```
MDS aims to recover a D-dimensional coordinate representation of the data given a distance matrix between points.
```
from sklearn.manifold import MDS
model = MDS()
```
#### Disadvantage
MDS fails when the embedding of the dataset is nonlinear.

## Locally Linear Embedding (LLE)
Rather than preserving all distances, LLE tries to preserve only the distances between *neighboring points*. Modified LLE does better than
other types of LLE at recovering well-defined manifolds from a nonlinear embedded input.
```
from sklearn.manifold import LocallyLinearEmbedding
model = LocallyLinearEmbedding()
out = model.fit_transform()
```

#### Disadvantage
  1. Manifold learning tends to be finicky that it is rarely used for anything other than visualization.
  2. There is no good framework for handling missing data.
  3. Result is highly dependent on the number of neighbors chosen but there is no solid way to choose an optimal number of neighbors.
  4. The computational expense of manifold learning scales as <img src="https://latex.codecogs.com/svg.latex?O[N^{2}]" title="O[N^{2}]" />
  or <img src="https://latex.codecogs.com/svg.latex?O[N^{3}]" title="O[N^{3}]" />.
  
