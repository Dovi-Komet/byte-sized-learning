---
layout: default
title: "Lambda Functions"
order: 63
---

Lambda functions are anonymous, single-expression functions in Python.

### Syntax of Lambda Functions

```python
lambda arguments: expression
```

Example:

```python
square = lambda x: x**2
print(square(5))
```

### Expected Output

```plaintext
25
```

### Lambda Functions with `map()`, `filter()`, and `reduce()`

- **`map()`** applies a function to all items in an iterable.
- **`filter()`** filters items based on a condition.
- **`reduce()`** reduces a sequence to a single value (from `functools` module).

Example:

```python
from functools import reduce

numbers = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, numbers))
even = list(filter(lambda x: x % 2 == 0, numbers))
product = reduce(lambda x, y: x * y, numbers)

print(squared)
print(even)
print(product)
```

### Expected Output

```plaintext
[1, 4, 9, 16]
[2, 4]
24
```

Lambda functions are widely used for short, throwaway functions.