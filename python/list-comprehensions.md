---
layout: default
title: "List Comprehensions"
order: 56
---

List comprehensions offer a concise way to create lists in Python.

### Basic List Comprehension

Syntax:

```python
new_list = [expression for item in iterable]
Example:
squares = [x**2 for x in range(5)]
print(squares)
```

### Expected Output

```plaintext
[0, 1, 4, 9, 16]
```

### Conditional List Comprehension

Add conditions to filter items.

Example:

```python
even_squares = [x**2 for x in range(10) if x % 2 == 0]
print(even_squares)
```

### Expected Output

```plaintext
[0, 4, 16, 36, 64]
```

List comprehensions improve code readability and reduce the need for loops.
