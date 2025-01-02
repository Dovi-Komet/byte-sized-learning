---
layout: default
title: "Intro to Lists"
order: 18
---

A list is a collection of items that can be stored in a single variable. Lists are one of the most versatile data types in Python.

### Creating a List

You can create a list by placing items inside square brackets `[]`, separated by commas.

Example:

```python
fruits = ["apple", "banana", "cherry"]
print(fruits)
```

### Expected Output

```plaintext
['apple', 'banana', 'cherry']
```

### Accessing List Items

You can access items in a list using their index. Remember, indexing starts at 0.

Example:

```python
print(fruits[0])  # First item
print(fruits[1])  # Second item
```

### Expected Output

```plaintext
apple
banana
```

### Modifying List Items

Lists are mutable, meaning you can change their items.

Example:

```python
fruits[1] = "blueberry"
print(fruits)
```

### Expected Output

```plaintext
['apple', 'blueberry', 'cherry']
```