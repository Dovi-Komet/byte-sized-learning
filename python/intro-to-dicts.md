---
layout: default
title: "Intro to Dicts"
order: 21
---

A dictionary is a collection of key-value pairs. Each key maps to a specific value, making dictionaries a versatile data type for storing and retrieving data efficiently.

## Creating a Dictionary

You can create a dictionary using curly braces `{}`. Each key is unique and is paired with a value, separated by a colon `:`.

### Example: Creating a Dictionary

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

## Accessing Values

To access a value in a dictionary, use its key inside square brackets `[]`.

### Example: Accessing Values by Key

```python
print(person["name"])  # Access the value associated with the key 'name'
print(person["age"])   # Access the value associated with the key 'age'
```

### Expected Output

```plaintext
Alice
30
```

## Adding or Updating Key-Value Pairs

You can add a new key-value pair or update an existing one using the assignment operator `=`.

### Example: Adding and Updating

```python
person["job"] = "Engineer"  # Add a new key-value pair
person["age"] = 31         # Update the value of an existing key
print(person)
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 31, 'city': 'New York', 'job': 'Engineer'}
```

## Removing Key-Value Pairs

Use the `del` statement to remove a key-value pair from a dictionary.

### Example: Removing a Key-Value Pair

```python
del person["city"]
print(person)
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 31, 'job': 'Engineer'}
```

## Summary

- Dictionaries are collections of key-value pairs, created using curly braces `{}`.
- Access values by referencing their keys inside square brackets `[]`.
- Add or update key-value pairs using the assignment operator `=`.
- Remove key-value pairs with the `del` statement.

Dictionaries are an essential tool for storing and managing data in Python. Understanding how to use them effectively will enhance your ability to write flexible and powerful programs.
