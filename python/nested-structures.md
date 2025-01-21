---
title: "Nested Structures"
order: 18
---

# Nested Structures

**Nested structures** in Python refer to data structures that contain other data structures as their elements. This allows you to represent and work with more complex data.

---

## Nested Lists

A **nested list** is a list where each element can also be a list.

### Example:
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Accessing elements
print(matrix[0])       # Output: [1, 2, 3]
print(matrix[0][1])    # Output: 2
```

### Iterating Through Nested Lists:
```python
for row in matrix:
    for element in row:
        print(element, end=" ")
# Output: 1 2 3 4 5 6 7 8 9
```

---

## Nested Dictionaries

A **nested dictionary** is a dictionary where values are dictionaries.

### Example:
```python
students = {
    "Alice": {"age": 25, "grade": "A"},
    "Bob": {"age": 22, "grade": "B"},
}

# Accessing nested elements
print(students["Alice"]["grade"])  # Output: A
```

### Modifying Nested Dictionaries:
```python
students["Bob"]["grade"] = "A"
print(students["Bob"])  # Output: {'age': 22, 'grade': 'A'}
```

### Iterating Through Nested Dictionaries:
```python
for student, details in students.items():
    print(f"{student}:")
    for key, value in details.items():
        print(f"  {key}: {value}")
```

---

## Nested Lists and Dictionaries

You can combine lists and dictionaries for complex data structures.

### Example:
```python
classroom = [
    {"name": "Alice", "age": 25, "grades": [85, 90, 95]},
    {"name": "Bob", "age": 22, "grades": [80, 85, 88]},
]

# Accessing elements
print(classroom[0]["name"])        # Output: Alice
print(classroom[1]["grades"][2])  # Output: 88
```

---

## Use Cases of Nested Structures

1. **Matrices and Tables**:
   - Nested lists are useful for representing grids or matrices.
   - Example: A chessboard or a 2D table of data.

2. **Hierarchical Data**:
   - Nested dictionaries can represent objects with multiple attributes.
   - Example: JSON-like structures.

3. **Combining Data**:
   - Use nested lists and dictionaries for more complex data models.
   - Example: Managing data for students, employees, or products.

---

## Example: Representing a Directory

A nested dictionary can represent a file directory:
```python
directory = {
    "Folder1": {
        "File1.txt": "Contents of File1",
        "File2.txt": "Contents of File2",
    },
    "Folder2": {
        "File3.txt": "Contents of File3",
    },
}

print(directory["Folder1"]["File1.txt"])  # Output: Contents of File1
```

---

## Best Practices for Working with Nested Structures

1. **Clarity**: Use meaningful variable names to improve readability.
2. **Access Safely**: Use `get()` to avoid errors when keys are missing in nested dictionaries.
3. **Break Down**: When dealing with deeply nested structures, break them into smaller pieces for easier handling.

---

## Practice Exercises

1. **Matrix Operations**:
   - Create a 3x3 nested list.
   - Write a function `print_diagonal(matrix)` to print the diagonal elements.

2. **Student Data**:
   - Create a nested dictionary for students with keys `"name"`, `"age"`, and `"grades"`.
   - Add a new student to the dictionary.

3. **Store Inventory**:
   - Create a nested dictionary to represent a store's inventory where:
     - Each key is a category (e.g., `"Electronics"`).
     - Each value is another dictionary containing items and their prices.

Nested structures allow you to represent complex data and provide powerful ways to organize and process information in Python!