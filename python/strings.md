---
layout: default
title: "Strings"
order: 10
---

Strings are one of the most commonly used data types in Python. A string is a sequence of characters enclosed in either single quotes (`'`) or double quotes (`"`). Strings can represent text such as words, sentences, or any combination of characters.

## Combining Strings (Concatenation)

You can combine two or more strings using the `+` operator.

### Example

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

## String Length

Use the `len()` function to find the number of characters in a string.

### Example

```python
message = "Hello"
print(len(message))
```

### Expected Output

```plaintext
5
```

Strings are incredibly versatile and will be used extensively in this course. In the next lesson, we’ll learn how to work with slices and indices to manipulate strings further.
