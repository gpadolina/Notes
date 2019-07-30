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
Its features are assumed to be generated from a simple multinomial distribution. Multinomial distribution describes the probability of
observing counts among a number of categories, which makes it most appropriate for features that represent counts or count rates. Often
used in text classification.
```
from sklearn.naive_bayes import MultinomialNB
```

## When to Use Naive Bayes
  1. For very well-separated categories, when model complexity is less import
  2. For very high-dimensional data, when model complexity is less important
  
Naive Bayes do not perform well as more complicated model but they have advantages:
  1. They are extremely fast for both training and prediction
  2. They provide straightforward probabilistic prediction
  3. They are often very easily interpretable
  4. They have very few tunable parameters
