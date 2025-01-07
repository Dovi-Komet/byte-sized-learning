---
layout: default
title: "Intro to Tuples"
order: 21
---

A tuple is a collection of items similar to a list, but it is immutable, meaning its items cannot be changed after creation. Tuples are useful for representing fixed sets of data.

## Creating a Tuple

You can create a tuple by placing items inside parentheses `()`. Tuples can contain any type of data and can even mix types.

### Example: Creating a Tuple

```python
coordinates = (10, 20)
print(coordinates)
```

### Expected Output

```plaintext
(10, 20)
```

If your tuple contains only one item, include a trailing comma to differentiate it from a regular value.

### Example: Single-Item Tuple

```python
single_value = (42,)  # Trailing comma makes it a tuple
print(single_value)
```

### Expected Output

```plaintext
(42,)
```

## Accessing Tuple Items

Like lists, you can access items in a tuple using their index. Remember, indexing starts at `0`.

### Example: Accessing Tuple Items

```python
coordinates = (10, 20)
print(coordinates[0])  # First item
print(coordinates[1])  # Second item
```

### Expected Output

```plaintext
10
20
```

## Why Use Tuples?

Tuples are often used for data that should remain constant, making them ideal for representing fixed sets of related information.

### Common Use Cases for Tuples

1. **Geographic Coordinates**:
   ```python
   location = (40.7128, -74.0060)  # Latitude and longitude
   print("Location:", location)
   ```

2. **RGB Color Values**:
   ```python
   color = (255, 0, 0)  # Red color
   print("Color:", color)
   ```

3. **Key-Value Pairs in Data**:
   ```python
   item = ("apple", 3.99)  # Name and price
   print("Item:", item)
   ```

### Expected Output for All Examples

```plaintext
Location: (40.7128, -74.0060)
Color: (255, 0, 0)
Item: ('apple', 3.99)
```

## Key Features of Tuples

- **Immutable**: Once created, items cannot be added, removed, or modified.
- **Efficient**: Tuples use less memory and are faster to access compared to lists.
- **Hashable**: Tuples can be used as keys in dictionaries, unlike lists.

## Summary

- Tuples are immutable collections created with parentheses `()`.
- Access tuple items using indexing, just like lists.
- Use tuples to represent fixed or constant data, such as coordinates or color values.
- Their immutability ensures data integrity in your programs.

Tuples are a fundamental data type in Python. Understanding their features and use cases will help you decide when they are the right tool for managing your data.