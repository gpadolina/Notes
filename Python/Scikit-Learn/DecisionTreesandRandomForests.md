Random forest is another powerful non-parametric algorithm. It is an example of an ensemble method that relies on aggregating the results of
an ensemble of simpler estimators.

## Decision Trees
Extremely intuite ways to classify or label objects by simply asking a series of questions designed to zero in on the classification.
In a well-constructed tree, each question will cut the number of options by approximately half, very quickly narrowing the options even
among a large numbers of classes.
```
from sklearn.tree import DecisionTreeClassifier
tree = DecisionTreeClassifier().fit(X, y)
```
### Overfitting
Overfitting turns out to be a general property of decision trees as it is very easy to go too deep in the tree.
