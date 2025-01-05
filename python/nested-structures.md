---
layout: default
title: "Nested Structures"
order: 25
---

Nested data structures like lists of dictionaries or dictionaries of lists are common in real-world applications. They allow you to organize complex data hierarchically and access it efficiently.

## Lists of Dictionaries

A list of dictionaries is useful when you need to store multiple records, where each record is a dictionary.

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

### Accessing Nested Data

You can access specific data by combining list and dictionary indexing.

```python
print(students[0]["name"])  # Access the name of the first student
```

### Output

```plaintext
Alice
```

## Dictionaries of Lists

A dictionary of lists is useful when you need to group multiple items under specific categories.

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

### Accessing Nested Data

You can access specific items in the lists by combining dictionary and list indexing.

```python
print(grades["math"][0])  # Access the first score in math
```

### Output

```plaintext
90
```

## Mixed Nested Structures

You can combine lists and dictionaries to create more complex structures, such as a dictionary of lists containing dictionaries.

### Example: Mixed Structure

```python
class_data = {
    "math": [
        {"name": "Alice", "score": 90},
        {"name": "Bob", "score": 85}
    ],
    "science": [
        {"name": "Alice", "score": 92},
        {"name": "Bob", "score": 80}
    ]
}

for subject, records in class_data.items():
    print(subject)
    for record in records:
        print(f"  {record['name']} scored {record['score']}")
```

### Output

```plaintext
math
  Alice scored 90
  Bob scored 85
science
  Alice scored 92
  Bob scored 80
```

## Summary

- **Lists of Dictionaries**: Store multiple records, each as a dictionary, within a list.
- **Dictionaries of Lists**: Group multiple items under categories represented as keys.
- **Mixed Structures**: Combine lists and dictionaries for hierarchical or complex data needs.

Understanding how to work with nested structures allows you to manage and manipulate complex data efficiently. Practice creating and accessing nested data structures to develop your skills further.
