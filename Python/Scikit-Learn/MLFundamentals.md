* *Training Set* - The examples that the system uses to learn. Use to train the model.
* *Test Set* - Use to test the model.
* *Sample* - Each training example is called sample (or training instance).
* *Data mining* - The application of ML techniques to dig into large amounts of data to discover patterns that 
were not immediately apparent.
* *Types of Machine Learning Systems*
  * *Supervised learning* - The training data included the desired solutions, called *labels*. Typical supervised learning task are
  classification and regression.
    * k-Nearest Neighbors
    * Linear Regression
    * Logistic Regression
    * Support Vector Machines (SVMs)
    * Decision Trees and Random Forests
    * Neural Network
  * *Unsupervised learning* - The training data is unlabeled.
    * k-Means
    * Hierarchical Cluster Analysis (HCA)
    * Expectation Maximization
    * Principal Component Analysis (PCA)
    * Kernel PCA
    * Locally-Linear Embedding (LLE)
    * t-Distributed Stochastic Neighbor Embedding (t-SNE)
  * *Semisupervised learning* - Partially labeled training data, usually a lot of unlabeled data and a little bit of labeled data.
  * *Reinforcement learning* - The learning system, called an *agent*, can observe the environment, select and perform actions and get
  *rewards* in return or *penalties* in the form of negative rewards. It must learn by itself what is the best strategy called a *policy*.
* *Dimensionality Reduction* - Simplify the data without losing too much information by merging several correlated features into one.
* *Feature Extraction* - Combining existing features to produce a more useful one.
* *Feature Selection* - Selecting the most useful features to train on among existing features.
* *Generalization* - The model's ability to react to new data.
* *Overfitting* - Modelling error which occurs when a function is too closely fit to a limited set of data points. The model performs well
on the training data, but it does not generalize well. If the training error is low (model makes few mistakes on the training set) but the generalization error is high, it means that the model is overfitting the training data.
* *Underfitting* - The opposite of overfitting. It occurs when the model is too simple to learn the underlying structure of the data.
* *Regularization* - Constraining a model to make it simpler and reducing the risk of overfitting.
* *Hyperparameter* - A hyperparameter is a parameter of a learning algorithm, not the model.
* *Cross-validation* - The training set is split into complementary subsets, and each model is trained against a different cobination of these subsets and validated against the remaining parts.
* *Pipeline* - A sequence of data processing components.
* Performance Measures
  * *RMSE* - Typical performance measure for regression problems is the Root Mean Square Error. It measures the standard deviation of the errors the system makes in its predictions.
  * *MAE* - Another way to measure the distance between two vectors: prediction vector and target values vector.
