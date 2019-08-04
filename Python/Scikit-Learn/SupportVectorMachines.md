Support vector machines (SVMs) are powerful and flexible class of supervised algorithms for both classification and regression. 

The objective of the SVM is to find a hyperplane in an N-dimensional space (N-number of features) that distinctly classifies the data
points.

## Maximizing the Margin
This means that rather than simply drawing a line between the classes, we can draw around each line a margin of some width, up to the
nearest point. The line that maximizes this margins is the optimal model.
```
from sklearn.svm import SVC # Support vector classifier
model = SVC()
model.fit(X, y)
```
The few points that touch the margin are called the *support vectors*. To get the identity of these points, use:
```
model.support_vectors_
```

## Kernel SVM
SVM becomes extremely powerful when combined with kernels. We can apply kernelized SVM by simply changing out linear kernel to a radial
basis function (RBF).
```
model = SVC(kernel='rbf')
model.fit(X, y)
```

## Optimal parameters
Use grid search cross-validation to find the optimal parameters for SVM.
```
from sklearn.grid_search import GridSearchCV
param_grid = {'C': [0.1, 1, 5, 10, 50, 100],          # C controls the margin hardness. High C provides high bias, low variance.
              'gamma': [1, 0.1, 0.01, 0.005, 0.0005]} # Gamma controls the size of radial basis function
grid = GridSearchCV(model, param_grid)
```

To get a better sense of our report:
```
from sklearn.metrics import classification_report, confusion_matrix
print(classification_report(ytest, yfit))
print(confusion_matrix(ytest, yfit))
```
