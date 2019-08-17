## Pipeline

Pipeline is a built-in scikit-learn function that allows streamlining functions one after another.

```
from sklearn.pipeline import make_pipeline

lm = make_pipeline(Imputer(missing_values='NaN', strategy='mean', axis=0),
                    PolynomialFeatures(degree=3),
                    LogisticRegression())
```
