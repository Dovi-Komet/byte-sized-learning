---
layout: default
title: "Strings"
order: 10
---

Strings are one of the most commonly used data types in Python. Let’s explore some basic string operations.

### Combining Strings (Concatenation)

You can combine two or more strings using the `+` operator.

Example:

```python
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name
print(full_name)
```

### Expected Output

```plaintext
John Doe
```

### String Length

Use the `len()` function to find the number of characters in a string.

Example:

```python
message = "Hello"
print(len(message))
```

### Expected Output

```plaintext
5
```

### Accessing Characters in a String

You can access specific characters in a string using their index. Remember, indexing starts at 0.

Example:

```python
word = "Python"
print(word[0])  # First character
print(word[-1])  # Last character
```

### Expected Output

```plaintext
P
n
```