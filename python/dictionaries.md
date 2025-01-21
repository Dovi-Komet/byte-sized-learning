---
title: "Dictionaries"
order: 17
---

# Dictionaries

A **dictionary** in Python is a collection of key-value pairs. Each key maps to a specific value, and dictionaries are optimized for fast lookups.

---

## Creating a Dictionary

You can create a dictionary using curly braces `{}` or the `dict()` constructor.

### Example:
```python
# Using curly braces
person = {"name": "Alice", "age": 25, "city": "New York"}

# Using dict()
person = dict(name="Alice", age=25, city="New York")
```

---

## Accessing Values

You can access values by their keys.

### Example:
```python
print(person["name"])  # Output: Alice
```

### Using `get()`:
The `get()` method is safer because it does not raise an error if the key is missing.
```python
print(person.get("name"))  # Output: Alice
print(person.get("job", "Not found"))  # Output: Not found
```

---

## Modifying a Dictionary

### Adding or Updating Key-Value Pairs:
```python
person["job"] = "Engineer"  # Add a new key-value pair
person["age"] = 26          # Update an existing key-value pair
```

### Removing Key-Value Pairs:
- **`pop(key)`**: Removes a key and returns its value.
- **`popitem()`**: Removes and returns the last inserted key-value pair.
- **`del`**: Deletes a key-value pair.
- **`clear()`**: Empties the dictionary.

```python
person.pop("age")          # Removes "age"
del person["city"]         # Removes "city"
person.clear()             # Empties the dictionary
```

---

## Iterating Through Dictionaries

You can iterate through keys, values, or both.

### Example:
```python
person = {"name": "Alice", "age": 25, "city": "New York"}

# Iterate through keys
for key in person:
    print(key)

# Iterate through values
for value in person.values():
    print(value)

# Iterate through key-value pairs
for key, value in person.items():
    print(f"{key}: {value}")
```

---

## Dictionary Methods

| Method               | Description                                         |
|----------------------|-----------------------------------------------------|
| `keys()`             | Returns a view object of all keys.                  |
| `values()`           | Returns a view object of all values.                |
| `items()`            | Returns a view object of key-value pairs.           |
| `update(other_dict)` | Merges another dictionary into the current one.     |
| `copy()`             | Returns a shallow copy of the dictionary.           |

---

## Nested Dictionaries

A dictionary can contain other dictionaries, enabling you to create complex data structures.

### Example:
```python
students = {
    "student1": {"name": "Alice", "age": 25},
    "student2": {"name": "Bob", "age": 22},
}

print(students["student1"]["name"])  # Output: Alice
```

---

## Common Use Cases

1. **Storing Mappings**:
   ```python
   capitals = {"France": "Paris", "Japan": "Tokyo", "India": "New Delhi"}
   ```

2. **Counting Items**:
   ```python
   word_count = {}
   for word in ["apple", "banana", "apple"]:
       word_count[word] = word_count.get(word, 0) + 1
   print(word_count)  # Output: {'apple': 2, 'banana': 1}
   ```

3. **Representing Objects**:
   ```python
   person = {"name": "Alice", "age": 25, "job": "Engineer"}
   ```

---

## Practice Exercises

1. Create a dictionary `person` with the keys: `"name"`, `"age"`, and `"city"`. 
   - Access and print the `"city"` value.
   - Add a new key `"job"` with a value.

2. Write a function `count_occurrences(items)` that:
   - Takes a list as input.
   - Returns a dictionary where the keys are the items, and the values are the number of occurrences.

3. Create a nested dictionary `classroom` where:
   - Each key represents a student name.
   - Each value is another dictionary containing `"age"` and `"grade"`.
   - Access and print the grade of a specific student.

Dictionaries are a powerful and versatile tool for organizing data in Python!