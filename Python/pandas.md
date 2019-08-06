# pandas

pandas contain high-level data structures and manipulation tools designed to make data analysis fast and easy.
  ```
  import pandas as pd
  ```
## pandas Data Structures

### Series

Series is a one-dimensional array-like object containing an array of data and an associated array of data labels, called *index*. It's a
fixed-length, ordered dict, as it is a mapping of index values to data values.
  ```
  obj = Series ([1, 2, 3, 4])
  ```
Often it's desirable to create a Series with an index identifying each data point:
  ```
  obj2 = Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])
  ```
Notes:
1. You can use values in the index when selecting single values or a set of values.
2. NumPy array operations will preserve the index-value link.
3. Python dict can be turned to a Series by passing the dict, `Series(dict)`
4. A Series' index can be altered in place by assignment, `obj.index = ['assign']

#### Categorical methods for Series

| Method | Description |
| --- | --- |
| add_categories | Append new categories at end of existing categories |
| as_ordered | Make categories ordered |
| as_unordered | Opposite of `as_unordered` |
| remove_categories | Remove categories, setting any removed values to null |
| remove_unused_categories | Remove any category values which do not appear in the data |
| rename_categories | Replace categories with indicated set of new category names |
| reorder_categories | Like `rename_categories` but can also change the result to have ordered categories |
| set_categories | Replace the categories with the indicated set of new categories |

### DataFrame

DataFrame represents a tabular, spreadsheet-like data structure containing an ordered collection of columns, each of which can be a
different value type. DataFrame has both a row and column index; it can be thought of as a dict of Series.

Notes:
1. One of the most common ways to construct a DataFrame is from a dict of equal-length lists or NumPy arrays.
2. Columns can be specified in the DataFrame.
3. A column in a DataFrame can be retrieved as a Series either by dict-like notation or by attribute.
4. Rows can also be retrieved by position such as using the `iloc` indexing field.
5. **del** keyword will delete columns as with a dict.

#### Data inputs to DataFrame constructor
| Type | Description |
| --- | --- |
| 2D ndarray | A matrix of data with row and column labels optional |
| dict of arrays, lists, or tuple | Becomes a column in the DataFrame. Must be the same length |
| dict of Series | Each value becomes a column. Indexes from each Series are unioned together |
| dict of dicts | Each inner dict becomes a column 
| list of dicts or Series | Each item becomes a row in the DataFrame |
| list of lists or tuples | Treated as the "2D ndarray" case |

### Index Objects

#### Index methods and properties

| Method | Description |
| --- | --- |
| append | Concatenate with additional Index objects, producing a new index |
| diff | Compute set difference as an Index |
| intersection | Compute set intersection |
| union | Compute set union |
| isin | Compute boolean array whether each value is contained in the passed collection |
| delete | Comput new Index with element at index i deleted |
| drop | Compute new Index by deleted passed value |
| insert | Compute new Index by inserting element at index i |
| is_unique | Returns True if the Index has no duplicate values |
| unique | Compute the array of unique values in the Index |

## Functionality

### Reindexing

Reindex create a new object with the data *conformed* to a new index. From a dataframe `df`:

| Argument | Description |
| --- | --- |
| `df.reindex()` | Rearranges the data according to the new index |
| `df.reindex(method=ffill)` | Fill values forward |
| `df.reindex(method=bfill)` | Fill values backward |

Notes:
1. **reindex** can alter either the index(row), columns, or both.

#### reindex function arguments
| Argument | Description |
| --- | --- |
| index | New sequence to use as index. Can be Index instance or any other sequence-like Python data structure |
| method | Interpolation method. See above |
| fill_value | Substitute value to use when introducing missing data by reindexing |
| limit | Maximum size gap to fill when forward or backfilling |
| level | Match simple Index on level of MultiIndex |

### Indexing, selection, and filtering

#### Indexing options with DataFrame

| Type | Description |
| --- | --- |
| obj[val] | Select single column or sequence of columns from the DataFrame |
| obj.iloc[val] | Select single row of subset of rows from the DataFrame |
| obj.iloc[:, val] | Select single column of subsets of columns |
| obj.iloc[val, val2] | Select both rows and columns |
| reindex method | Conform one or more axes to new indexes |
| xs method | Select single row or column as a Series by label |
| icol, irow method | Select single column or row as a Series by integer location |
| *get_value, set_value* methods | Select single value by row and column label |

## Missing Data

#### NA handling methods

| Argument | Description |
| --- | --- |
| dropna | Filter axis labels based on whether values for each label have missing data |
| fillna | Fill in missing data with some value or using an interpolation method |
| isnull | Return object containing boolean values indicating which values are missing |
| notnull | Negation of isnull |

#### fillna function arguments

| Argument | Description |
| --- | --- |
| value | Scalar value or dict-like object to use to fill mising values |
| method | Interpolation, by default is *ffill* |
| axis | Axis to fill on, by default axis=0 |
| inplace | Modify the calling object without producing a copy |
| limit | Maximum number of consecutive periods for forward and backward filling |

## General

| Example | Description |
| --- | --- |
| `df.set_index` | Create a new DataFrame using one or more of its column as the index |
| `df.reset_index` | Opposite of `set_index` |
| `df.swaplevel` | Takes two level numbers or names and returns a new object with the level interchanged |
| `df.sortlevel` | Sorts the data using only the values in a single level |
| `df.pivot` | Create a pivot table without aggregation. Useful for transforming column data into rows |
| `df.pivot_table` | Create a spreadsheet-style pivot table as a DataFrame. Can take multiple indices |
| `df.describe` | Generate descriptive statistics excluding NaN values |
| `df.info` | Generate a summary of a DataFrame |
| `df.transpose` | Transpose index and columns |
| `df.join` | Join columns with other DataFrame either on index or on a key column |
| `df.head` | Return the top ten rows for each column |
| `df.concat` | Concatenate pandas objects along a particular axis |
| `df.stack` | Pivot a level of column labels to rows |
| `df.unstack` | Pivot a level of row labels to columns |
| `df.groupby` | Create an object that can be used to split a DataFrame into groups based on a column or row label. Useful for categorical features |
