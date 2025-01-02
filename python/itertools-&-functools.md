---
layout: default
title: "Itertools & Functools"
order: 96
---

The `itertools` and `functools` modules provide powerful tools for iterable manipulation and functional programming.

### Using itertools

Example: Generating combinations.

```python
import itertools

items = ["a", "b", "c"]
combinations = itertools.combinations(items, 2)
print(list(combinations))
```

### Using functools

Example: Using `reduce` to compute the product of a list.

```python
from functools import reduce

numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print(product)
```

### Expected Output

```plaintext
[('a', 'b'), ('a', 'c'), ('b', 'c')]
24
```

`itertools` and `functools` simplify complex operations on iterables.
