---
layout: default
title: "Slicing and Indexing"
order: 11
---

Slicing and indexing allow you to access parts of lists and strings.

### Indexing

Use brackets `[]` to access elements by position:

Example:

```python
my_list = [10, 20, 30, 40, 50]
print(my_list[0])  # 10
print(my_list[-1])  # 50
```

### Slicing

Use the syntax `[start:end]` to get a subset:

Example:

```python
my_list = [10, 20, 30, 40, 50]
print(my_list[1:4])  # [20, 30, 40]
print(my_list[:3])   # [10, 20, 30]
print(my_list[::2])  # [10, 30, 50]
```

### Expected Output

```plaintext
10
50
[20, 30, 40]
[10, 20, 30]
[10, 30, 50]
```

Understanding slicing is crucial for efficient data manipulation.
