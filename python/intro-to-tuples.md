---
layout: default
title: "Intro to Tuples"
order: 21
---

Tuples in Python are similar to lists but have one key difference: they are immutable. Once a tuple is created, its elements cannot be changed. Tuples are often used to store data that shouldn’t be modified.

## What is a Tuple?

A tuple is an ordered collection of elements, enclosed in parentheses `()` and separated by commas.

### Example:
```python
# A tuple of integers
numbers = (1, 2, 3)

# A tuple of strings
fruits = ("apple", "banana", "cherry")

# A mixed tuple
mixed = (1, "apple", True)
```

### Output:
```plaintext
(1, 2, 3)
("apple", "banana", "cherry")
(1, "apple", True)
```

## Key Characteristics of Tuples

1. **Ordered**: Tuples maintain the order of their elements.
2. **Immutable**: Once created, elements cannot be modified.
3. **Allow Duplicates**: Tuples can contain duplicate values.

### Example:
```python
duplicates = (1, 1, 2, 2, 3)
print(duplicates)
```

### Output:
```plaintext
(1, 1, 2, 2, 3)
```

## Creating a Tuple

### Empty Tuple:
```python
empty_tuple = ()
print(empty_tuple)
```

### Output:
```plaintext
()
```

### Single-Element Tuple:
When creating a tuple with one element, include a trailing comma.

```python
single_element = (42,)
print(single_element)
```

### Output:
```plaintext
(42,)
```

## Accessing Tuple Elements

You can access elements in a tuple using their index, just like lists.

### Example:
```python
fruits = ("apple", "banana", "cherry")

# Access the first element
print(fruits[0])

# Access the last element
print(fruits[-1])
```

### Output:
```plaintext
apple
cherry
```

## Why Use Tuples?

1. **Immutability**: Protects data from accidental modification.
2. **Performance**: Tuples are faster than lists for fixed data.
3. **Keys in Dictionaries**: Tuples can be used as keys in dictionaries, unlike lists.

---

In the next lesson, we’ll explore dictionaries and how to work with key-value pairs in Python.
