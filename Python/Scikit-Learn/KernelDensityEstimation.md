KDE is an algorithm that takes the mixture of Gaussians idea to its logical extreme: it uses a mixture consisting of one Gaussian component per point, resulting in an essentially nonparametric estimator of density.

## Histograms
A density estimaor is an algorithm that seeks to model the probability distribution that generated a dataset. A histogram divides the data into discrete bins, counts the number of points that fall in each bin, and then visualizes the results in an intuitive manner.
```
hist = plt.hist()
```
## In practice
The free parameters of kernel density estimation are the kernel, which specifies the shape of the distribution placed at each point, and the kernel bandwidth, which controls the size of the kernel at each point. Scikit-Learn's KDE estimator uses a tree-based algorithm and can trade off computation time for accuracy using the `atol` (absolute tolerance) and `rtol` (relative tolerance) parameters.
```
from sklearn.neighbors import KernelDensity
kde = KernelDensity()
kde.fit()
```
