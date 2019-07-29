Naive Bayes models are a group of extremely fast and simple classifcation algorithms that are often suitable for very high-dimensional
datasets. They are useful as a quick and dirty baseline for a classification problem because they are so fast and have so few tunable
parameters.

## Bayesian Classification

<img src="https://latex.codecogs.com/svg.latex?\fn_phv&space;P(L&space;|&space;features)&space;=&space;\frac{P(features|L)P(L)}{P(features)}" title="P(L | features) = \frac{P(features|L)P(L)}{P(features)}" />

<img src="https://latex.codecogs.com/svg.latex?\fn_phv&space;\frac{P(L_{1}|features)}{P(L_{1}|features)}&space;=&space;\frac{P(features|L_{1})P(L_{1})}{P(features|L_{2})P(L_{2})}" title="\frac{P(L_{1}|features)}{P(L_{1}|features)} = \frac{P(features|L_{1})P(L_{1})}{P(features|L_{2})P(L_{2})}" />

## Gaussian Naive Bayes
Assume that *data from each label is drawn from a simple Gaussian distribution.*
```
from sklearn.datasets import make_blobs
X, y = make_blobs(100, 2, centers=2, random_state=2, cluster_std=1.5)
plt.scatter(X[:, 0], X[:, 1], c=y, s=50, cmap='RdBu')

from sklearn.naive_bayes import GaussianNB
model = GaussianNB()
model.fit(X, y)
```
In general, the boundary in Gaussian is quadratic.

## Multinomial Naive Bayes

