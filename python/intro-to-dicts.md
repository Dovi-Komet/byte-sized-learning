---
layout: default
title: "Intro to Dicts"
order: 21
---

A dictionary is a collection of key-value pairs. Each key in a dictionary maps to a specific value.

### Creating a Dictionary

You can create a dictionary using curly braces `{}`.

Example:

```python
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
print(person)
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
```

### Accessing Values

You can access a value in a dictionary by using its key.

Example:

```python
print(person["name"])  # Access the value associated with the key 'name'
print(person["age"])   # Access the value associated with the key 'age'
```

### Expected Output

```plaintext
Alice
30
```