---
layout: default
title: "Intro to Lists"
order: 18
---

A list is a collection of items that can be stored in a single variable. Lists are one of the most versatile and commonly used data types in Python.

## Creating a List

You can create a list by placing items inside square brackets `[]`, separated by commas. Lists can contain any type of data, including strings, numbers, or even other lists.

### Example: Creating a List

```python
fruits = ["apple", "banana", "cherry"]
print(fruits)
```

### Expected Output

```plaintext
['apple', 'banana', 'cherry']
```

## Accessing List Items

You can access individual items in a list using their index. Indexing starts at `0` for the first item, and you can use negative indices to access items from the end of the list.

### Example: Accessing Items by Index

```python
print(fruits[0])  # First item
print(fruits[1])  # Second item
print(fruits[-1])  # Last item
```

### Expected Output

```plaintext
apple
banana
cherry
```

## Modifying List Items

Lists are mutable, meaning you can change their contents after they are created.

### Example: Changing an Item

```python
fruits[1] = "blueberry"
print(fruits)
```

### Expected Output

```plaintext
['apple', 'blueberry', 'cherry']
```

## Checking the Length of a List

You can find the number of items in a list using the `len()` function.

### Example: Getting List Length

```python
print(len(fruits))
```

### Expected Output

```plaintext
3
```

## Summary

- Lists are collections of items stored in square brackets `[]`.
- Items in a list can be accessed by their index, starting at `0`.
- Lists are mutable, allowing you to modify their contents.
- Use `len()` to determine the number of items in a list.

Lists are a powerful and flexible tool in Python. Practice creating, accessing, and modifying lists to understand their versatility!
