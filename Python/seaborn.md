## Seaborn
By convention, we `import matplotlib.pyplot as plt` and `import seaborn as sns`.

## Distribution Plots
| Syntax | Description |
| --- | --- |
| `data = sns.load_dataset('name')` | Load a data set |
| `sns.head()` | Similar to pandas `head()` method |
| `sns.distplot(data['factor'])` | Plot a univariate distribution of 'factor' observations |
| `sns.kdeplot()` | Plot a univariate or bivariate distribution with kernel density estimation | 
| `sns.rugplot()` | Show small vertical lines to show each observation in a distribution |
| `sns.jointplot(x, y, data=None)` | Plot two variables with bivariate and univariate graphs |
| `sns.pairplot()` | Plot pairwise relationships or every possible 2-way comparison in a dataset |

## Categorical Plots
| Syntax | Description |
| --- | --- |
| `sns.barplot(x, y, data=None)` | Treat `x` as categorical and `y` as numeric and show plot as rectangular bars |
| `sns.countplot(x, data=None)` | Plot the counts of observations in each categorical variable |
| `sns.pointplot(x, y, data=None)` | Plot confidence intervals using scatter plot |
| `sns.boxplot(x, y, data=None)` | Plot distributions with respect to categories |
| `sns.boxenplot(x, y, data=None)` | Plot an enhanced box plot for larger data sets |
| `sns.violinplot(x, y, data=None)` | Plot a combination of boxplot and KDEs |
| `sns.stripplot(x, y, data=None)` | Plot a scatterplot with one variable as categorical | 
| `sns.swarmplot(x, y, data=None)` | Similar to stripplot but the points are adjusted to avoid overlapping |

## Matrix Plots
The data for matrix plots needs to be in matrix form.
| Syntax | Description |
| --- | --- |
| `sns.heatmap()` | Plot a rectangular data as color-encoded matrix. Provides an easy magnitude comparison using color difference. |
| `sns.clustermap()` | Similar to heatmap but with arranged the rows and columns |

## Grid Plots

### PairGrid
Specialized version of `sns.pairplot`.
```
g = sns.PairGrid(data)
g.map_offdiag(plt.scatter) # Plot a scatter plot above and below the diagonal
g.map_diag(sns.distplot) # Plot distribution plot along the diagonal
g.map_lower(sns.kdeplot) # Plot KDE plots below the diagonal
g.map_upper(plt.scatter) # Plot a scatter plot above the diagonal
g.add_legend() # Add a legend to the graph
```

### FacetGrid
Kind of like PairGrid but separates the data in multiple plots.
```
# Separate the data into multiple plots in separate axes
g = sns.FacetGrid(data, col='category1', row='category2')
g.map(sns.distplot, 'factor') # Some factor where category1 and category2 are separated
g.map(plt.scatter, 'factor1', 'factor2') # Basically like above but added factor2 (or y-axis)
g = sns.FacetGrid(data, hue="class") # This differenntiates variables by color
g = g.map(plt.hist,'factor',bins=10,alpha=0.5) # This is most useful in plotting multiple histograms
```
