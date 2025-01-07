---
layout: default
title: "Sorting & Keys"
order: 65
---

The `sorted()`, `min()`, and `max()` functions can sort or evaluate data using custom criteria.

### Sorting with `key`

Example:

```python
names = ["Alice", "Bob", "Charlie"]
sorted_names = sorted(names, key=lambda x: len(x))
print(sorted_names)
```

### Min/Max with `key`

Example:

```python
numbers = [-10, -20, 15, 5]
max_num = max(numbers, key=abs)
print(max_num)
```

### Expected Output

```plaintext
['Bob', 'Alice', 'Charlie']
-20
```

Custom keys make sorting and comparisons powerful and flexible.
