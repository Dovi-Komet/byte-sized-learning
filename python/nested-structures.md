---
layout: default
title: "Nested Structures"
order: 25
---

Nested data structures like lists of dictionaries, dictionaries of lists, and lists of lists are common in real-world applications. They allow for flexible and efficient data organization.

## Lists of Lists

A list of lists is useful when you need to organize data in a grid-like or tabular structure.

### Example: Lists of Lists

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in matrix:
    print(row)
```

### Output

```plaintext
[1, 2, 3]
[4, 5, 6]
[7, 8, 9]
```

### Accessing Nested Items with Two Indices

You can use two indices to access specific elements in a list of lists:
- The **first index** specifies the position of the sub-list (row) in the main list.
- The **second index** specifies the position of the element (column) in the chosen sub-list.

#### Example: Accessing Specific Elements

```python
print(matrix[0][1])  # Element in the first row, second column
print(matrix[2][0])  # Element in the third row, first column
```

### Output

```plaintext
2
7
```

## Lists of Dictionaries

A list of dictionaries is useful for storing multiple records, where each record is represented as a dictionary.

### Example: Lists of Dictionaries

```python
students = [
    {"name": "Alice", "age": 20},
    {"name": "Bob", "age": 22}
]

for student in students:
    print(f"{student['name']} is {student['age']} years old")
```

### Output

```plaintext
Alice is 20 years old
Bob is 22 years old
```

### Accessing Nested Items

You can access specific data in a list of dictionaries using both list indexing and dictionary keys.

```python
print(students[0]["name"])  # Access the name of the first student
```

### Output

```plaintext
Alice
```

## Dictionaries of Lists

A dictionary of lists groups multiple items under specific categories represented as keys.

### Example: Dictionaries of Lists

```python
grades = {
    "math": [90, 85, 88],
    "science": [92, 80, 85]
}

for subject, scores in grades.items():
    print(f"{subject}: {scores}")
```

### Output

```plaintext
math: [90, 85, 88]
science: [92, 80, 85]
```

### Accessing Nested Items with Two Indices

You can access specific items in a list within a dictionary by using a key and an index.

```python
print(grades["math"][1])  # Access the second score in math
```

### Output

```plaintext
85
```

## Summary

- **Lists of Lists**: Organize data in a grid-like structure and access specific elements using two indices.
- **Lists of Dictionaries**: Store multiple records, each as a dictionary, and access elements with list indices and dictionary keys.
- **Dictionaries of Lists**: Group items under categories, accessed using a key and list index.

Understanding nested structures and indexing with multiple levels is essential for managing complex data. Practice these concepts to strengthen your ability to work with structured data.
