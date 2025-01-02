---
layout: default
title: "Nested Structures"
order: 25
---

Nested data structures like lists of dictionaries or dictionaries of lists are common in real-world applications.

### Lists of Dictionaries

Example:

```python
students = [
    {"name": "Alice", "age": 20},
    {"name": "Bob", "age": 22}
]

for student in students:
    print(f"{student['name']} is {student['age']} years old")
```

### Dictionaries of Lists

Example:

```python
grades = {
    "math": [90, 85, 88],
    "science": [92, 80, 85]
}

for subject, scores in grades.items():
    print(f"{subject}: {scores}")
```

### Expected Output

```plaintext
Alice is 20 years old
Bob is 22 years old
math: [90, 85, 88]
science: [92, 80, 85]
```

Nested structures allow for flexible and efficient data organization.
