Conditional statements are often called as *if-then* statements.

### if, elif, and else
```
x = -2

if x==0:
  print(x, "is zero")
elif x > 0:
  print(x, "is positive")
else x < 0:
  print(x, "is negative")
```

### for loops
A way to repeatedly execute some code statement.
```
for N in range(15):
  print(N, end=' ')
```

### while loops
```
i = 0
while i < 5:
  print(i, end=' ')
  i += 1
```

### Example
```
m, n = 1, 2
max = 50
N = []

while True:
  (m, n) = (n, m + n)
  if m > max:
      break/continue
  N.append(m)

print(N)
```

## Iterators
```
for i in range(15):
  print(i, end=' ')
```

### enumarate
Use when there is a need to iterate the values and index in an array.
```
X = [3, 6, 9, 12, 15]

for i, val in enumerate(X):
  print(i, val)
```

### zip
Use to iterate over multiple lists simultaneously.
```
X = [3, 6, 9, 12, 15]
Y = [1, 2, 3, 4, 5]
for xval, rval in zip(X, Y):
  print(xval, rval)
```

## Comprehensions
A way to compress a list-building *for loop* into a single short readable line.
```
[expr for var in iterable]            # syntax

[i for i in range(10) if i % 2 > 0]
```
