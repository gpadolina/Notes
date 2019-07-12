# Data Structures and Sequences

## Tuple

A tuple is one-dimensional, fixed-length, *immutable* sequence of Python objects. The easiest way to create one is with a 
comma-separated sequence of values:

  `tup = 1, 2, 3`
  
It's often necessary to enclose the values in parentheses, as in this example of creating a tuple of tuples:

  `nested_tup = (1, 2, 3), (4, 5)`
  
Note:
1. Any sequences of iterator can be converted to a tuple by invoking tuple:

  ``` 
  tuple([1, 2, 3])
  
  tup = tuple('string')
  ```

## List

Lists are variable-length and their contents can be modified. They can be defined using square brackets [] or using the *list*
type function:

  ```
  a_list = [1, 2, 3, None]
  
  tup = ('cat, 'dog', 'monkey)
  b_list = list(tup)
  b_list[1] = 'bird'
  ```
  
| Syntax | Description |
| --- | --- |
| `list.append(x)` | Add an item to the end of the list. Equivalent to `a[len(a):] = [x]` |
| `list.extend(iterable)` | Extend the list by appending all the items from the iterable. |
| `list.insert(i, x)` | Insert an item at a given position. *i = index* |
| `list.remove(x)` | Remove the first item from the list whose value is equal to x. |
| `list.pop([i])` | Remove the item at the given position in the list and return it. |
| `list.clear()` | Remove all items from the list. Equivalent to `del a[:]`. |
| `list.index(x[, start[, end]])` | Return zero-based index in the list of the first tiem whose value is equal to x.|
| `list.count(x)` | Return the number of times x appears in the list. |
| `list.sort(key=None, reverse=False)` | Sort the items of the list in place. Also see *sorted().* |
| `list.reverse()` | Reverse the elements of the list in place. |
| `list.copy()` | Return a shallow copy of the list. |

## Dictionary

Likely the most important built-in Python data structure. It is a collection of *key-value* pairs, where *key* and *value* are Python
objects. One way to creat one is by using curly braces {} and using colons to separate keys and values:

  ```
  empty_dict = {}
  
  dict1 = {'a': 'hello', 'b': [1, 2, 3]}
  ```
Note:
1. Elements can be accessed and inserted or set using the same syntax as accessing elements of a list or tuple:
  ```
  dict1[1] = 'hi there'
  ```
