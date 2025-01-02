---
layout: default
title: "Intro to Sets"
order: 23
---

A set is an unordered collection of unique items. Sets are useful for tasks involving uniqueness and set operations.

### Creating a Set

You can create a set by placing items inside curly braces `{}`.

Example:

```python
unique_numbers = {1, 2, 3, 4, 4, 5}
print(unique_numbers)
```

### Expected Output

```plaintext
{1, 2, 3, 4, 5}
```

Notice that duplicate items (`4`) are automatically removed.

### Adding and Removing Items

You can add items to a set using the `add()` method and remove them using the `remove()` method.

Example:

```python
unique_numbers.add(6)
unique_numbers.remove(3)
print(unique_numbers)
```

### Expected Output

```plaintext
{1, 2, 4, 5, 6}
```