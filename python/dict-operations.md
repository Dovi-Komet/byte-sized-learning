---
layout: default
title: "Dict Operations"
order: 22
---

Dictionaries in Python offer various operations for managing key-value pairs. Let’s explore some of them.

### Adding Key-Value Pairs

You can add a new key-value pair to a dictionary by assigning a value to a new key.

Example:

```python
person = {"name": "Alice", "age": 30}
person["city"] = "New York"
print(person)
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
```

### Modifying Values

You can modify the value associated with an existing key.

Example:

```python
person["age"] = 31
print(person)
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 31, 'city': 'New York'}
```

### Removing Key-Value Pairs

Use the `del` keyword to remove a key-value pair.

Example:

```python
del person["city"]
print(person)
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 31}
```

### Looping Through a Dictionary

You can loop through the keys, values, or both in a dictionary.

Example:

```python
for key, value in person.items():
    print(key, ":", value)
```

### Expected Output

```plaintext
name : Alice
age : 31
```