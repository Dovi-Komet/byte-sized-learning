---
layout: default
title: "Dict Operations"
order: 23
---

Dictionaries in Python provide various operations for adding, updating, removing, and interacting with key-value pairs. These operations make dictionaries highly versatile.

## Adding and Updating Items

### Adding a New Key-Value Pair
You can add a new key-value pair by assigning a value to a key that doesn’t exist in the dictionary.

```python
person = {"name": "Alice", "age": 30}
person["city"] = "New York"
print(person)
```

### Output:
```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
```

### Updating an Existing Key
If the key already exists, assigning a value to it will update the value.

```python
person = {"name": "Alice", "age": 30}
person["age"] = 31
print(person)
```

### Output:
```plaintext
{'name': 'Alice', 'age': 31}
```

## Removing Items

### Using `pop()`
The `pop()` method removes a key-value pair and returns the value associated with the key.

```python
person = {"name": "Alice", "age": 30}
age = person.pop("age")
print(age)
print(person)
```

### Output:
```plaintext
30
{'name': 'Alice'}
```

### Using `del`
The `del` statement removes a key-value pair by key.

```python
person = {"name": "Alice", "age": 30}
del person["age"]
print(person)
```

### Output:
```plaintext
{'name': 'Alice'}
```

### Using `clear()`
The `clear()` method removes all items from the dictionary.

```python
person = {"name": "Alice", "age": 30}
person.clear()
print(person)
```

### Output:
```plaintext
{}
```

## Checking for Keys

You can check if a key exists in a dictionary using the `in` keyword.

```python
person = {"name": "Alice", "age": 30}
print("name" in person)
print("city" in person)
```

### Output:
```plaintext
True
False
```

## Iterating Over a Dictionary

### Iterating Over Keys
```python
person = {"name": "Alice", "age": 30}
for key in person:
    print(key)
```

### Output:
```plaintext
name
age
```

### Iterating Over Values
```python
person = {"name": "Alice", "age": 30}
for value in person.values():
    print(value)
```

### Output:
```plaintext
Alice
30
```

### Iterating Over Key-Value Pairs
```python
person = {"name": "Alice", "age": 30}
for key, value in person.items():
    print(f"{key}: {value}")
```

### Output:
```plaintext
name: Alice
age: 30
```

## Combining Dictionaries

You can combine two dictionaries using the `update()` method.

```python
dict1 = {"name": "Alice"}
dict2 = {"age": 30, "city": "New York"}
dict1.update(dict2)
print(dict1)
```

### Output:
```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
```

---

In the next lesson, we’ll explore Python sets and their operations.
