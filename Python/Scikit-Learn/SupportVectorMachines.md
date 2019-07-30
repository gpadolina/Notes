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
