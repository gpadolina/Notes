## Simple Linear Regression
Most familiar linear regression form is a straight-line fit to data.
```
y = ax + b
```

### Train-test-split
```
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.5, random_state=1)
      # The test_size is the percentage of the data set you want allocated to the test data
      # The random_state is the number of random splits of that data
```
Then we instantiate and fit the model
```
from sklearn.linear_model import LinearRegression
model = LinearRegression(fit_intercept=True)
      # fit_intercept - The intercept of the data is contained in the model's parameter
model.fit(X_train, y_train)
```
To get the slope and intercept of the data, use:
```
model.coef_
model.intercept_
```

## Basis Function Regression
Use to adapt linear regression to nonlinear relationships between variables.

### Polynomial basis functions
```from sklearn.preprocessing import PolynomialFeatures
poly = PolynomialFeatures()
poly.fit_transform()
```
Generate a new feature matrix consisting of all polynomial combinations of the features. Note that high degrees can cause overfitting.

### Gaussian basis functions

## Regularization
