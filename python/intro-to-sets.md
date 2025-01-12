---
layout: default
title: "Intro to Sets"
order: 24
---

Sets in Python are an unordered collection of unique elements. They are useful for storing data without duplicates and for performing mathematical set operations like union, intersection, and difference.

## What is a Set?

A set is defined using curly braces `{}` or the `set()` constructor. Unlike lists or tuples, sets do not allow duplicate elements, and their elements are unordered.

### Example:
```python
# Creating a set with unique elements
fruits = {"apple", "banana", "cherry", "apple"}
print(fruits)

# Using the set() constructor
numbers = set([1, 2, 3, 2, 1])
print(numbers)
```

### Output:
```plaintext
{'apple', 'banana', 'cherry'}
{1, 2, 3}
```

## Key Characteristics of Sets

1. **Unique Elements**: Duplicate elements are automatically removed.
2. **Unordered**: Sets do not preserve the order of elements.
3. **Mutable**: You can add or remove elements from a set.

## Creating Sets

### Empty Set
An empty set must be created using the `set()` constructor because `{}` creates an empty dictionary.

```python
empty_set = set()
print(empty_set)
```

### Output:
```plaintext
set()
```

### Pre-Filled Set
```python
colors = {"red", "blue", "green"}
print(colors)
```

### Output:
```plaintext
{'red', 'blue', 'green'}
```

## Accessing Elements

Since sets are unordered, you cannot access elements by index. Instead, you can iterate over the set.

```python
colors = {"red", "blue", "green"}
for color in colors:
    print(color)
```

### Output:
```plaintext
red
blue
green
```

(Note: The order of elements in the output may vary.)

## Why Use Sets?

1. **Duplicate Removal**: Automatically removes duplicate items.
2. **Membership Testing**: Quickly check if an item exists in the set using the `in` keyword.
3. **Set Operations**: Perform mathematical operations like union, intersection, and difference.

---

In the next lesson, we’ll dive deeper into performing operations on sets.
