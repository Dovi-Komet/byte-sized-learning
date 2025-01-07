---
layout: default
title: "Intro to Sets"
order: 24
---

A set is an unordered collection of unique items. Sets are useful when you need to store distinct elements and perform operations like unions, intersections, and differences.

## Creating a Set

You can create a set by placing items inside curly braces `{}`. Duplicate items are automatically removed, and the order of elements is not guaranteed.

### Example: Creating a Set

```python
unique_numbers = {1, 2, 3, 4, 4, 5}
print(unique_numbers)
```

### Output

```plaintext
{1, 2, 3, 4, 5}
```

### Creating an Empty Set

To create an empty set, use the `set()` function. Using `{}` will create an empty dictionary instead.

```python
empty_set = set()
print(empty_set)
```

### Output

```plaintext
set()
```

## Adding and Removing Items

You can modify sets by adding or removing items.

### Adding Items

Use the `add()` method to add a single item to a set.

```python
unique_numbers.add(6)
print(unique_numbers)
```

### Output

```plaintext
{1, 2, 3, 4, 5, 6}
```

### Removing Items

Use the `remove()` method to remove a specific item. If the item does not exist, it raises a `KeyError`.

```python
unique_numbers.remove(3)
print(unique_numbers)
```

### Output

```plaintext
{1, 2, 4, 5, 6}
```

### Using `discard()`

If you want to remove an item without raising an error if it doesn’t exist, use the `discard()` method.

```python
unique_numbers.discard(10)  # No error if 10 is not in the set
```

## Checking Membership

You can check if an item exists in a set using the `in` keyword.

### Example: Membership Test

```python
if 4 in unique_numbers:
    print("4 is in the set.")
```

### Output

```plaintext
4 is in the set.
```

## Key Characteristics of Sets

1. **Unordered**: Sets do not preserve the order of elements.
2. **Unique**: Duplicate items are automatically removed.
3. **Mutable**: You can add or remove items, but the set itself is immutable if it contains immutable elements.

## Summary

- Create sets with `{}` or the `set()` function for empty sets.
- Use `add()` to add items and `remove()` or `discard()` to remove them.
- Check for membership with the `in` keyword.
- Sets are ideal for tasks requiring uniqueness or performing mathematical set operations.

In the next lesson, we’ll explore set operations like union, intersection, and difference.
