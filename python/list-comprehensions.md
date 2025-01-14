---
layout: default
title: "List Comprehensions"
order: 49
---

List comprehensions in Python provide a concise way to create lists. They allow you to generate a new list by applying an expression to each item in an iterable, optionally filtering items with a condition.

---

## Syntax of List Comprehensions

```python
[expression for item in iterable if condition]
```

- **`expression`**: Defines how each element should be transformed or included in the new list.
- **`item`**: Represents the current element being processed.
- **`iterable`**: Any iterable (e.g., list, range, or string) to process.
- **`condition`** *(optional)*: A filter to include only certain items.

---

## Basic Examples

### Creating a List from a Range

```python
squares = [x ** 2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

---

### Filtering Items

```python
even_numbers = [x for x in range(10) if x % 2 == 0]
print(even_numbers)  # Output: [0, 2, 4, 6, 8]
```

---

### Transforming Items

```python
names = ["Alice", "Bob", "Charlie"]
uppercase_names = [name.upper() for name in names]
print(uppercase_names)  # Output: ['ALICE', 'BOB', 'CHARLIE']
```

---

## Nested List Comprehensions

List comprehensions can be nested to handle multi-dimensional data.

### Example: Flattening a List of Lists

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flattened = [num for row in matrix for num in row]
print(flattened)  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

---

## Conditional List Comprehensions

You can include an `if-else` expression within the list comprehension.

```python
numbers = [1, 2, 3, 4, 5]
result = ["Even" if x % 2 == 0 else "Odd" for x in numbers]
print(result)  # Output: ['Odd', 'Even', 'Odd', 'Even', 'Odd']
```

---

## Benefits of List Comprehensions

1. **Concise**: Shorter and more readable than traditional loops.
2. **Performance**: Faster than equivalent for-loops in many cases.
3. **Flexibility**: Can handle transformations and filtering in a single line.

---

## When to Avoid List Comprehensions

- Avoid using them for complex operations that reduce readability.
- Prefer traditional for-loops when more than one step is needed.

---

## Key Takeaways

- List comprehensions are a powerful feature for generating lists in Python.
- They enhance readability for simple transformations and filters.
- Use them wisely to balance conciseness and clarity.

---

In the next lesson, we’ll explore sorting techniques and how to use custom keys with the `sorted()` function.
