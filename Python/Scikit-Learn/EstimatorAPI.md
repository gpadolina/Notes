## Scikit-Learn's Estimator API

### Basics of the API
The steps in using the Scikit-Learn estimator API are as follows:

1. Choose a class of model by importing the appropriate estimator class from Scikit-Learn.
2. Choose model hyperparameters by instantiating this class with desired values.
3. Arrange data into a features matrix and target vector.
4. Fit the model to your data by calling the `fit()` method of the model instance.
5. Apply the model to new data:
  
   a. For supervised learning, predict labels for unknown data using the `predict()` method.
   
   b. For unsupervised learning, transform or infer properties of the data using the `transform()` or `predict()` method.
