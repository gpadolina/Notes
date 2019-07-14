# NumPy

NumPy library provides the ndarray object for efficient storage and manipulation of homogenous(the same type) multidimensional 
dense data arrays in Python.

  ```
  import numpy as np
  ```

## The NumPy ndarray

Arrays enable you to perform mathematical operations on whole blocks of data using similar syntax to the equivalent operations between
scalar elements.

### Array creation functions
| Syntax | Description|
| --- | --- |
| `np.shape` | Indicate the size of each dimension |
| `np.reshape(m, n)` | Reshape a 1-d array to 2-d array |
| `np.dtype` | Describe the *data type* of the array |
| `np.array(list)` | Create a one-dimensional array from the input data |
| `np.array(listoflist)` | Create a two-dimensional array from the input data |
| `np.zeros(m)` | Create an m-vector of zeros (1-d) |
| `np.zeros(m, n)` | Create an m by n array of zeros (2-d) |
| `np.ones()` | Like the zeros but producing arrays of one's instead |
| `np.empty((m, n, x))` | Create an array but do not populate any values. x creates a higher dimensional array |
| `np.arange()` | NumPy version of built-in Python *range* that returns an ndarray instead of a list |
| `np.eye()` | Create a 2-d N x N identity matrix |
| `.astype(np.type)` | Convert or casts an array from one dtype to another |
| `arr[m:n]` or `arr[m1:m2, n1:n2]` | Create a slice from row m1 to m2 (exclusive) to column n1 to n2 (exclusive) |
| `.copy()` | Produce a copy of an array. If you want to make a change in an array such as `arr`, use `arr2 = arr.copy()`. If `arr2 = arr`, changes will be made to `arr` |
| `arr[m, n]` or `arr[m][n]` | Select invididual elements at row `m` column `n` |
| `np.<TAB>` | Display all the contents of the numpy namespace |
| `np?` | Display NumPy's built-in documentation |

### Operations between Arrays and Scalars

Usually called *vectorization*, arrays enable you to express scalar arithmetics on arrays to arrays or scalars without writing any *for loops*

Example:
  ```
  arr = np.array([[1, 2, 3], [4, 5, 6]])
  
  arr
  arr * arr
  arr - arr
  1 - arr
  arr ** 2
  ```
### Unary functions

| Function | Description |
| --- | --- |
| abs | Compute the absolute value element-wise |
| sqrt | Compute the square root of each element |
| sign | Compute the sign of each element: 1(positive), 0(zero), or -1(negative) |
| ceil | Compute the ceiling of each element |
| floor | Compute the floor of each element |
| rint | Round elements to the nearest integer |
| isnan | Return boolean array indicating whether each value is NaN |

### Binary functions

| Function | Description |
| --- | --- |
| add | Add corresponding elements in arrays |
| subtract | Subtract elements in second array from first array |
| multiply | Multiple array elements |
| divide, floor_divide | Divide or floor divide, which truncates the remainder |
| mod | Return modulus (division remainder) |

### Statistical methods

| Method | Description |
| --- | --- |
| sum | Sum of all the elements in the array or along an axis |
| mean | Return mean |
| std | Return standard deviation |
| var | Return variance |
| min | Return minimum |
| max | Return maximum |
| argmin | Return indices of minimum |
| argmax | Return indices of maximum |
| cumsum | Give cumulative sum of elements |
| cumprod | Give cumulative product of elements from 1 |

### Linear Algebra functions

| Function | Description |
| --- | --- |
| diag | Return the diagonal of a square matrix |
| dot | Matrix multiplication |
| trace | Compute the sum of the diagonal elements |
| det | Compute the matrix determinant |
| eig | Compute the eigenvalues and eigenvectors of a square matrix |
| inv | Comput the inverse of a square matrix |
| qr | Compute the QR decomposition |
| solve | Compute the linear systems Ax = b for x where A is a square matrix |
