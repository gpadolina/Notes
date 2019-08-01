Gaussian mixture model (GMM) attempts to find a mixture of multidimensional Gaussian probability distributions that best model any input
dataset. GMMs can be used for finding clusters in the same manner as k-means.
```
from sklearn.mixture import GMM
gmm = GMM().fit(X)
labels = gmm.predict(X)
```
Because GMM contains a probabilistic model, it is possible to find probabilistic cluster assignments using `predict_proba` method.
```
probs = gmm.predict_proba(X)
```
GMM uses an expectation-maximization approach like k-means by doing the following:
  1. Choose starting guesses for the location and shape.
  2. Repeat until converged:
     a. *E-step*: for each point, find weights encoding the probability of membership in each cluster.
     b. *M-step*: for each cluster, update its location, normalization, and shape based on all data points, making use of the weights.
     
## GMM as Density Estimation
The result of a GMM fit to some data is technically not a clustering model, but a generative probabilistic model describing the distribution of the data.
