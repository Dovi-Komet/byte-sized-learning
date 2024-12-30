---
layout: default
title: "Generators"
order: 57
---

Generators are functions that yield values one at a time using the `yield` keyword, providing memory efficiency for large datasets.

### Creating a Generator Function

Example:

```python
def countdown(start):
    while start > 0:
        yield start
        start -= 1

for number in countdown(5):
    print(number)
```

### Expected Output

```plaintext
5
4
3
2
1
```

### Generator Expressions

Similar to list comprehensions but produce values lazily.

Example:

```python
squares = (x**2 for x in range(5))
print(next(squares))
print(next(squares))
```

### Expected Output

```plaintext
0
1
```

Generators are useful for handling large datasets efficiently.
