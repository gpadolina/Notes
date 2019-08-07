Matplotlib is a data visualization library built on NumPy arrays.

By convention, we `import maplotlib.pyplot as plt` and `seaborn as sns`.

## General
| Syntax | Description |
| --- | --- |
| `plt.style.use('name')` | Use to choose appripriate aesthetic styles for figures |
| `plt.show()` | Produce an output window using matplotlib from within a script |
| `%matplotlib inline` | Use in Jupyter notebooks to have visuals inline |
| `fig.savefig('name.png')` | Save the figure as a file |
| `plt.plot()` | Plot x versus y values |
| `plt.xlabel()` | Make a label for x axis |
| `plt.ylabel()` | Make a label for y axis |
| `plt.title()` | Make a title for the graph |
| `plt.subplot()` | Plot multi-plot figure |

### Subplots
```
# Create plots
fig, ax = plt.subplots(3)

# Plot using plot()
ax[0].plot(x, np.cos(x))
ax[1].plot(x, np.sin(x))
ax[2].plot(x, np.tan(x))
```

## Object-oriented method
Define `fig = plt.figure()` as a blank figure.

```
#Create empty gridded axes
fig = plt.figure()
ax = plt.axes()

x = np.linspace(0, 10, 50)    # (start, stop, num)
ax.plot(x, np.cos(x))

# Adjusting the plot
plt.plot(x, y, color=)        # Adjust color
plt.plot(x, y, linestyle=)    # Line style
plt.plot(x, y, '-r')          # Combine color and linetyle - solid red
plt.xlim(0, 10)               # X-axis limit
plt.ylim(-5, 5)               # Y-axis limit
plt.axis([0, 10, -5, 5])      # [xmin, xmax, ymin, ymax]
plt.title('name here')        # Add a title to the figure
plt.xlabel('name here')       # Add a label to x-axis
plt.ylabel('name here')       # Add a label to y-axis
plt.legend()                  # Helpful when plotting multiple lines

# Setup the axes for the plot
ax = fig.add_axes([1, 1, 8, 8]) # (left, bottom, width, height)

# Some functions can also be done by doing the following
ax.set_xlim(0, 10)             # X-axis limit
ax.set_ylim(-5, 5)             # Y-axis limit
ax,set_title('name here')      # Add a title to the figure
ax.set_xlabel('name here')     # Add a label to x-axis
ax.set_ylabel('name here')     # Add a label to y-axis
ax.plot(x, y, label='legend')
ax.plot(x, x**2, label='legend2')
ax.legend(loc=, frameon=, ncol=, framealpha=, shadow=)
```

### Sample plots

```
# Scatter plot
x = np.linspace(0, 5, 20)
y = np.cos(x)
plt.plot(x, y, 'o', color='red)

# Scatter plot using plt.scatter()
plt.scatter(x, y, marker='o')

# Errorbars
plt.errorbar(x, y, fmt=)

# Contour - 3D
plt.contour(X, Y, Z, colors=)

# Colorbar
# Can be combined with other plots
plt.colorbar()

# Histograms
plt.hist(data, bins=, normed=, alpha=, histtype=, color=, edgecolor=)

# Histograms - 2D
plt.hist2d(x, y, bins=, cmap=)
```

### Upper and lower bounds
```
fig = plt.figure(figsize=(10, 6))
ax = fig.add_axes([0, 0, 1, 1])

ax.plot(x, y, label='name')
ax.set_xlim([0, 3]) # (lower, upper)
ax.set_ylim([0, 3]) # (lower, upper)
```

## Class methods and parameters
| Syntax | Description |
| --- | --- |
| `plt.tight_layout` | Fix overlapping parameters by expanding |
| `plt.xticks()` | Set the current tick locations and labels of the x axis |
| `plt.figure(figsize=(width, height))` | Give the figure dimensions |
| `.plot(color=)` | Color can be names or hex codes |
| `.plot(linewidth=)` | Set the line width |
| `.plot(alpha=)` | Transparency of the plot |
| `.plot(linestyle=)` | Set the style of lines like solid or dashed |
| `.plot(marker=)` | Set the style of marker use to make the plot |
