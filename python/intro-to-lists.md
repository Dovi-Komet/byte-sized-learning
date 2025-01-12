---
layout: default
title: "Intro to Lists"
order: 19
---

Lists in Python are one of the most versatile and commonly used data structures. They are used to store multiple items in a single variable and can hold elements of different data types.

## What is a List?

A list is an ordered, mutable collection of elements enclosed in square brackets `[]`, with each element separated by a comma.

### Example:
```python
# A list of integers
numbers = [1, 2, 3, 4, 5]

# A list of strings
fruits = ["apple", "banana", "cherry"]

# A mixed list
mixed = [1, "apple", True]
```

### Output:
```plaintext
[1, 2, 3, 4, 5]
["apple", "banana", "cherry"]
[1, "apple", True]
```

## Accessing Elements in a List

You can access elements in a list using their index. Python uses zero-based indexing, meaning the first element has an index of `0`.

### Example:
```python
fruits = ["apple", "banana", "cherry"]

# Access the first element
print(fruits[0])

# Access the second element
print(fruits[1])
```

### Output:
```plaintext
apple
banana
```

## Negative Indexing

Python allows negative indexing, where `-1` refers to the last element, `-2` to the second last, and so on.

### Example:
```python
fruits = ["apple", "banana", "cherry"]

# Access the last element
print(fruits[-1])

# Access the second last element
print(fruits[-2])
```

### Output:
```plaintext
cherry
banana
```

## Why Use Lists?

1. **Ordered**: Lists maintain the order of elements, making them predictable.
2. **Mutable**: You can modify elements after creating the list.
3. **Versatile**: They can store elements of any data type, including other lists.

---

In the next lesson, we’ll learn about common operations you can perform on lists.
