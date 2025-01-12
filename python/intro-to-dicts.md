---
layout: default
title: "Intro to Dicts"
order: 22
---

Dictionaries in Python are powerful data structures that store data as key-value pairs. They are mutable and allow for efficient data retrieval based on unique keys.

## What is a Dictionary?

A dictionary is an unordered collection of key-value pairs, where each key must be unique. Keys act as identifiers for their associated values.

### Example:
```python
# A dictionary with strings as keys and values
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

# A dictionary with mixed types
product = {
    "id": 101,
    "name": "Laptop",
    "price": 799.99
}
```

### Output:
```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
{'id': 101, 'name': 'Laptop', 'price': 799.99}
```

## Key Characteristics of Dictionaries

1. **Key-Value Pairs**: Each key maps to a specific value.
2. **Keys Must Be Unique**: Duplicate keys are not allowed.
3. **Values Can Be Any Type**: Values can be strings, numbers, lists, or even other dictionaries.
4. **Unordered**: As of Python 3.7+, dictionaries preserve insertion order, but this is not guaranteed in earlier versions.

## Creating a Dictionary

### Empty Dictionary:
```python
empty_dict = {}
print(empty_dict)
```

### Output:
```plaintext
{}
```

### Pre-Filled Dictionary:
```python
car = {
    "brand": "Toyota",
    "model": "Corolla",
    "year": 2020
}
print(car)
```

### Output:
```plaintext
{'brand': 'Toyota', 'model': 'Corolla', 'year': 2020}
```

## Accessing Values in a Dictionary

You can access values by referencing their keys.

### Example:
```python
person = {"name": "Alice", "age": 30, "city": "New York"}

# Access the value associated with the key 'name'
print(person["name"])

# Access the value associated with the key 'city'
print(person["city"])
```

### Output:
```plaintext
Alice
New York
```

## Why Use Dictionaries?

1. **Fast Lookups**: Retrieve values quickly using keys.
2. **Flexible**: Store diverse types of data.
3. **Descriptive**: Keys provide context to the values they store.

---

In the next lesson, we’ll learn more about performing operations on dictionaries.
