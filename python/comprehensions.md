---
title: "Comprehensions"
order: 19
---

# Comprehensions

**Comprehensions** in Python are concise and expressive ways to create collections like lists, dictionaries, and sets. They are used to generate new collections from existing ones in a single line of code.

---

## List Comprehensions

A **list comprehension** is used to create a new list by applying an expression to each item in an iterable.

### Syntax:
```python
[expression for item in iterable if condition]
```

### Example:
```python
# Create a list of squares
squares = [x**2 for x in range(10)]
print(squares)  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Filter even numbers
evens = [x for x in range(10) if x % 2 == 0]
print(evens)  # Output: [0, 2, 4, 6, 8]
```

---

## Dictionary Comprehensions

A **dictionary comprehension** is used to create dictionaries in a concise way.

### Syntax:
```python
{key_expression: value_expression for item in iterable if condition}
```

### Example:
```python
# Create a dictionary of squares
squares_dict = {x: x**2 for x in range(5)}
print(squares_dict)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

# Filter and create a dictionary
filtered_dict = {x: x**2 for x in range(10) if x % 2 == 0}
print(filtered_dict)  # Output: {0: 0, 2: 4, 4: 16, 6: 36, 8: 64}
```

---

## Set Comprehensions

A **set comprehension** is similar to a list comprehension but creates a set instead of a list. Sets do not allow duplicate values.

### Syntax:
```python
{expression for item in iterable if condition}
```

### Example:
```python
# Create a set of squares
unique_squares = {x**2 for x in [1, 2, 2, 3, 3]}
print(unique_squares)  # Output: {1, 4, 9}
```

---

## Nested Comprehensions

You can use comprehensions inside other comprehensions to work with nested structures.

### Example:
```python
# Create a 2D grid
grid = [[x * y for x in range(3)] for y in range(3)]
print(grid)
# Output: [[0, 0, 0], [0, 1, 2], [0, 2, 4]]
```

---

## Generator Expressions

A **generator expression** is similar to a list comprehension but generates items lazily, saving memory.

### Syntax:
```python
(expression for item in iterable if condition)
```

### Example:
```python
# Create a generator for squares
squares_gen = (x**2 for x in range(5))
print(next(squares_gen))  # Output: 0
print(next(squares_gen))  # Output: 1
```

---

## Use Cases for Comprehensions

1. **Data Transformation**:
   - Converting a list of strings to uppercase.
   - Generating a list of squared numbers.

2. **Filtering**:
   - Extracting items based on conditions (e.g., even numbers, positive numbers).

3. **Flattening Nested Data**:
   - Simplifying nested structures into a single collection.

---

## Practice Exercises

1. **List Comprehensions**:
   - Create a list of the first 10 odd numbers using a list comprehension.
   - Create a list of squares for numbers divisible by 3 from 0 to 20.

2. **Dictionary Comprehensions**:
   - Create a dictionary where the keys are numbers from 1 to 5, and the values are their cubes.
   - Create a dictionary of characters and their ASCII values for letters in the string `"Python"`.

3. **Set Comprehensions**:
   - Create a set of unique squares for numbers from 1 to 10.

4. **Nested Comprehensions**:
   - Create a 3x3 matrix using a nested list comprehension.
   - Flatten the matrix into a single list.

Comprehensions are a powerful feature in Python that make your code more concise, readable, and efficient!