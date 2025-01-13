---
layout: default
title: "Nested Structures"
order: 26
---

Nested structures in Python are collections within collections. They allow you to organize data in complex and hierarchical ways. You can nest lists, dictionaries, tuples, and sets inside each other to represent structured data like tables, trees, or graphs.

## Nested Lists

A nested list is a list containing other lists as elements.

### Example:
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
print(matrix[0])      # Access the first row
print(matrix[1][2])   # Access the element at row 2, column 3
```

### Output:
```plaintext
[1, 2, 3]
6
```

### Iterating Through Nested Lists
You can use nested loops to iterate through a nested list.

```python
for row in matrix:
    for item in row:
        print(item, end=" ")
```

### Output:
```plaintext
1 2 3 4 5 6 7 8 9
```

---

## Nested Dictionaries

A nested dictionary is a dictionary where values are dictionaries themselves.

### Example:
```python
students = {
    "Alice": {"age": 25, "grade": "A"},
    "Bob": {"age": 22, "grade": "B"},
}
print(students["Alice"])        # Access Alice's data
print(students["Bob"]["grade"]) # Access Bob's grade
```

### Output:
```plaintext
{'age': 25, 'grade': 'A'}
B
```

### Iterating Through Nested Dictionaries
Use loops to iterate through the keys and values of nested dictionaries.

```python
for name, details in students.items():
    print(f"Student: {name}")
    for key, value in details.items():
        print(f"  {key}: {value}")
```

### Output:
```plaintext
Student: Alice
  age: 25
  grade: A
Student: Bob
  age: 22
  grade: B
```

---

## Nested Tuples

Tuples can also be nested, though their immutability means they’re often used for structured data that shouldn’t change.

### Example:
```python
coordinates = ((1, 2), (3, 4), (5, 6))
print(coordinates[0])  # Access the first tuple
print(coordinates[1][1])  # Access the second element of the second tuple
```

### Output:
```plaintext
(1, 2)
4
```

---

## Nested Sets

Sets can contain other sets only if the nested sets are frozen (immutable).

### Example:
```python
outer_set = {frozenset({1, 2}), frozenset({3, 4})}
print(outer_set)
```

### Output:
```plaintext
{frozenset({1, 2}), frozenset({3, 4})}
```

---

Nested structures are a powerful way to represent and manipulate complex data. They are commonly used in applications such as data parsing, JSON manipulation, and more.

---

In the next lesson, we’ll learn how to read files in Python.
