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

## Random Forests
Random forests is an ensemble of randomized decision trees. To find a better classification, multiple overfitting estimators can be combined
and averaged, a method called bagging.
```
from sklearn.tree import DecisionTreeClassifier
from sklearn.tree import BaggingClassifier

tree = DecisitionTreeClassifier()
bag  = BaggingClassifier(tree, etc.)

bag.fit(X, y)
```
For an optimized ensemble of randomized decision trees, implement:
```
from sklearn.ensemble import RandomForestClassifier
model = RandomForestCLassifer()
```
By averaging random models, we end up with an overall model that is much closer about how the parameter space should be split.

## Random Forest Regression
Random forest can also be used in the case of regression - continuous rather than categorical variables. We can find the best-fit
curve as follows:
```
from sklearn.ensemble import RandomForestRegressor
forest = RandomForestRegressor()
forest.fit()
```

#### Disadvantage of using random forests
Random forests results are not easily interpretable.
