---
layout: default
title: "Intro to Tuples"
order: 20
---

A tuple is similar to a list, but it is immutable, meaning its items cannot be changed after creation.

### Creating a Tuple

You can create a tuple by placing items inside parentheses `()`.

Example:

```python
coordinates = (10, 20)
print(coordinates)
```

### Expected Output

```plaintext
(10, 20)
```

### Accessing Tuple Items

You can access items in a tuple using their index, just like a list.

Example:

```python
print(coordinates[0])  # First item
print(coordinates[1])  # Second item
```

### Expected Output

```plaintext
10
20
```

### Why Use Tuples?

Tuples are often used to represent data that should not change, like geographic coordinates or RGB color values.