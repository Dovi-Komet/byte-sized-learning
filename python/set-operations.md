---
layout: default
title: "Set Operations"
order: 25
---

Sets in Python come with built-in methods to perform operations such as union, intersection, difference, and more. These operations are efficient and follow the principles of mathematical sets.

## Adding and Removing Elements

### Adding an Element
You can add a single element to a set using the `add()` method.

```python
numbers = {1, 2, 3}
numbers.add(4)
print(numbers)
```

### Output:
```plaintext
{1, 2, 3, 4}
```

### Removing an Element
The `remove()` method removes a specific element, but it raises an error if the element is not found.

```python
numbers = {1, 2, 3, 4}
numbers.remove(3)
print(numbers)
```

### Output:
```plaintext
{1, 2, 4}
```

The `discard()` method works like `remove()` but does not raise an error if the element is not found.

```python
numbers = {1, 2, 4}
numbers.discard(5)  # No error if 5 is not in the set
print(numbers)
```

### Output:
```plaintext
{1, 2, 4}
```

## Mathematical Set Operations

### Union
The union of two sets combines all unique elements from both sets. Use the `union()` method or the `|` operator.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
result = set1.union(set2)
print(result)
```

### Output:
```plaintext
{1, 2, 3, 4, 5}
```

### Intersection
The intersection contains only elements common to both sets. Use the `intersection()` method or the `&` operator.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
result = set1.intersection(set2)
print(result)
```

### Output:
```plaintext
{3}
```

### Difference
The difference contains elements in the first set but not in the second. Use the `difference()` method or the `-` operator.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
result = set1.difference(set2)
print(result)
```

### Output:
```plaintext
{1, 2}
```

### Symmetric Difference
The symmetric difference contains elements in either set but not in both. Use the `symmetric_difference()` method or the `^` operator.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
result = set1.symmetric_difference(set2)
print(result)
```

### Output:
```plaintext
{1, 2, 4, 5}
```

## Membership Testing

Use the `in` keyword to check if an element is in a set.

```python
numbers = {1, 2, 3}
print(2 in numbers)
print(4 in numbers)
```

### Output:
```plaintext
True
False
```

## Combining Sets

### Updating a Set
You can combine sets using the `update()` method, which adds all elements from another set to the current set.

```python
set1 = {1, 2, 3}
set2 = {4, 5}
set1.update(set2)
print(set1)
```

### Output:
```plaintext
{1, 2, 3, 4, 5}
```

---

In the next lesson, we’ll explore nested structures and how they can be used to organize data in Python.
