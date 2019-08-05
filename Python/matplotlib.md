Matplotlib is a data visualization library built on NumPy arrays.

By convention, we `import maplotlib.pyplot as plt` and `seaborn as sns`.

## Basic methods
| Syntax | Description |
| --- | --- |
| `plt.show()` | Produce an output window using matplotlib from within a script |
| `%matplotlib inline` | Use in Jupyter notebooks to have visuals inline |
| `plt.plot()` | Plot x versus y values |
| `plt.xlabel()` | Make a label for x axis |
| `plt.ylabel()` | Make a label for y axis |
| `plt.title()` | Make a title for the graph |
| `plt.subplot()` | Plot multi-plot figure |

## Object oriented method
Define `fig = plt.figure()` as a blank figure.

```
x = np.linspace(0, 5, 10)
y = x ** 2

# Create empty gridded axes
fig = plt.figure()
ax = plt.axes()

# Setup the axes for the plot
ax = fig.add_axes([0.1, 0.1, 0.8, 0.8]) # (left, bottom, width, height)

# Manipulating the axes
axes.plot(x, y) # Self-explanatory
axes.set_xlabel = ('label') # Set label for x axis
axes.set_ylabel = ('label') # Set label for y axis
axes.set_title = ('title') # Set title for the figure
```

### Subplots
```
fig, axes = plt.subplots(1, 2) # (row by column)

# Manipulating the axes
axes[0].plot(x, y)
axes[0].set_xlabel('label')
axes[0].set_ylabel('label')

axes[1].plot(x, y)
axes[1].set_xlabel('label')
axes[1].set_ylabel('label')
```

### Legend
```
fig = plt.figure(figsize=(10, 6))
ax = fig.add_axes([0, 0, 1, 1])

ax.plot(x, y, label='legend')
ax.plot(x, x**3, label='legend2')
ax.legend()
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
| `fig.savefig('name.png')` | Save the figure as a file |
| `.plot(color=)` | Color can be names or hex codes |
| `.plot(linewidth=)` | Set the line width |
| `.plot(alpha=)` | Transparency of the plot |
| `.plot(linestyle=)` | Set the style of lines like solid or dashed |
| `.plot(marker=)` | Set the style of marker use to make the plot |
