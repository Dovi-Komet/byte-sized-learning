---
title: "Lists, Sets, and Tuples"
order: 16
---

# Lists, Sets, and Tuples

**Lists**, **sets**, and **tuples** are fundamental data structures in Python. They allow you to store and manage collections of data.

---

## Lists

A **list** is an ordered, mutable (modifiable) collection that allows duplicate elements.

### Creating a List:
```python
fruits = ["apple", "banana", "cherry"]
```

### Accessing Elements:
```python
print(fruits[0])  # Output: apple
```

### Modifying a List:
```python
fruits[1] = "blueberry"
print(fruits)  # Output: ['apple', 'blueberry', 'cherry']
```

### Common Methods:
- **`append(item)`**: Add an item to the end.
- **`extend(iterable)`**: Add multiple items.
- **`insert(index, item)`**: Insert at a specific position.
- **`remove(item)`**: Remove the first occurrence.
- **`pop(index)`**: Remove and return an item by index.
- **`sort()`**: Sort the list in-place.

### Example:
```python
numbers = [3, 1, 4, 1, 5]
numbers.append(9)
numbers.sort()
print(numbers)  # Output: [1, 1, 3, 4, 5, 9]
```

---

## Sets

A **set** is an unordered, mutable collection of unique elements. Duplicate elements are automatically removed.

### Creating a Set:
```python
numbers = {1, 2, 3, 3}
print(numbers)  # Output: {1, 2, 3}
```

### Adding and Removing Elements:
- **`add(item)`**: Add an element.
- **`remove(item)`**: Remove an element (raises an error if not found).
- **`discard(item)`**: Remove an element (does not raise an error if not found).

### Set Operations:
- **Union** (`|` or `union()`): Combine sets.
- **Intersection** (`&` or `intersection()`): Common elements.
- **Difference** (`-` or `difference()`): Elements in one set but not the other.
- **Symmetric Difference** (`^` or `symmetric_difference()`): Elements in either set but not both.

### Example:
```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

print(set_a | set_b)  # Output: {1, 2, 3, 4, 5}
print(set_a & set_b)  # Output: {3}
print(set_a - set_b)  # Output: {1, 2}
```

---

## Tuples

A **tuple** is an ordered, immutable (unchangeable) collection. It allows duplicate elements.

### Creating a Tuple:
```python
coordinates = (10, 20)
```

### Accessing Elements:
```python
print(coordinates[0])  # Output: 10
```

### Tuples are Immutable:
```python
# coordinates[0] = 30  # This will raise an error
```

### Tuple Unpacking:
```python
x, y = coordinates
print(x)  # Output: 10
print(y)  # Output: 20
```

### Single-Element Tuple:
To create a tuple with one element, include a trailing comma:
```python
single = (42,)
print(type(single))  # Output: <class 'tuple'>
```

---

## Comparison of Lists, Sets, and Tuples

| Feature       | List        | Set         | Tuple       |
|---------------|-------------|-------------|-------------|
| Ordered       | ✅          | ❌          | ✅          |
| Mutable       | ✅          | ✅          | ❌          |
| Allows Duplicates | ✅       | ❌          | ✅          |

---

## Common Use Cases

1. **Lists**:
   - Storing ordered collections like a shopping list.
   - Dynamic resizing and frequent modifications.

2. **Sets**:
   - Removing duplicates from a collection.
   - Mathematical set operations (union, intersection).

3. **Tuples**:
   - Representing fixed collections like coordinates or RGB values.
   - Using as dictionary keys (since they are immutable).

---

## Practice Exercises

1. **List Practice**:
   - Create a list of 5 numbers.
   - Replace the second number with `10`.
   - Append `20` to the list.
   - Print the list.

2. **Set Practice**:
   - Create two sets: `A = {1, 2, 3}` and `B = {3, 4, 5}`.
   - Print their union, intersection, and difference.

3. **Tuple Practice**:
   - Create a tuple representing a point `(x, y)`.
   - Unpack the tuple into `x` and `y` variables.
   - Print the values of `x` and `y`.

Lists, sets, and tuples are versatile tools that enable you to handle collections of data effectively in Python!