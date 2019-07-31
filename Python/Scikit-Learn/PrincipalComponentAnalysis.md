Principal component Analysis (PCA) is a fast and flexible method and one of the most broadly used unsupervised algorithms. PCA is
fundamentally a dimensionality reduction algorithmm but it can also be useful as a tool for visualization, noise filtering, 
feature extraction and engineering, and much more.
```
from sklearn.decomposition import PCA
pca = PCA(n_components=2)
pca.fit(X)
```
PCA quantifies the relationship between x and y values by finding a list of the principal axes in the data rather than attempting to
predict the y values from the x values. To get the components and explained variance:
```
pca.components_
pca.explained_variance_
```
### PCA as dimensionality reduction
Using PCA for dimensionality reduction involves zeroing out one or more of the smallest principal components, resulting in a
lower-dimensional projection of the data that preserves the maximal data variance/
```
pca = PCA(n_components=1)
pca.fit(X)
X_pca = pca.transform(X)
```
PCA as dimensionality reduction removes the information along the least important principal axes, leaving only the components with the
highest variance.

### Choosing the number of components
We can determine the number of components needed to describe the data by plotting the *cumulative explained variance*, which measures how
well PCA preserves the contents of the data.

#### Disadvantage
It tends to be highly affected by outliers in the data and it does not perform well when there are nonlinear relatationships within
the data.
