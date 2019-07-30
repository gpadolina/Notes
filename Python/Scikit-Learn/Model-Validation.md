# Model Validation

### Holdout Sets
Hold out some subset of the data from the training of the model and then use this holdout set to check the model of performance.
```
from sklearn.model_selection import train_test_split
# split the data with 50% in each set
X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=0,
                                                train_size=0.5)
```
### Cross-validation
Sequence of fits where each subsets of the data is used both as a training set and as a validation set.

### n-fold cross-validation
Same as above. But repeating the validation across different subsets of the data gives an even better idea of the performance of the algorithm.
```
from sklearn.model_selection import cross_val_score
cross_val_score(model, X, y, cv=n)
```
### Leave-one-out cross-validation
The number of folds is equal to the number of data points.
```
from sklearn.model_selection import LeaveOneOut
scores = cross_val_score(model, X, y, cv=LeaveOneOut(len(X)))
scores
```
# Model Selection

### Underfitting (or has high bias)
Model does not enough have flexibility to account for all the features in the data.

### Overfitting (or has high variance)
Model has so much flexibility that the model ends up accounting for random errors as well as the underlying data distribution.

### Validation curve
  1. The training score is everywhere higher than the validation curve. Generally, the model will be a better fit to data it has seen than to data it has not seen.
  2. For very low model complexity (a high-bias model), the training data is underfit, which means that the model is a poor predictor both for the training data and for any previously unseen data.
  3. For very high model complexity (a hgih-variance model), the training data is ovefit, which means that the model predicts the training data very well, but fails for any previously unseen data.
  4. For some intermediate value, the validation curve has a maximum. This level of complexity indicates a suitable trade-off between bias and variance.
  
# Learning curves

General behavior of a learning curve:
  1. A model of a given complexity will oversit a small dataset meaning the training score will be relatively high, while the validation score will be relatively low.
  2. A model wof a given complexity will underfit a large dataset meaning the training score will decrease, but the validation score will increase.
  3. A model will never, except by chance, give a better score to the validation set than the training set meaning the curves should keep getting closer together but never cross.
