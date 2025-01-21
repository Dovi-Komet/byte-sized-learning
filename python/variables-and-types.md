---
title: "Variables and Types"
order: 5
---

# Variables and Types

Variables are used to store data in Python programs. They act as containers for values that can be used and manipulated.

## What is a Variable?

- A variable is a name that refers to a value.
- You can think of it as a label attached to a value.

### Example:
```python
name = "Alice"
age = 25
height = 5.6
```

In this example:
- `name` stores the string `"Alice"`.
- `age` stores the integer `25`.
- `height` stores the floating-point number `5.6`.

## Variable Naming Rules

1. Names can contain letters, numbers, and underscores (`_`).
2. Names must start with a letter or an underscore, not a number.
3. Names cannot be the same as Python's reserved keywords (e.g., `if`, `for`, `class`).

### Valid and Invalid Names:
```python
# Valid
first_name = "Alice"
_age = 30
user2 = "Bob"

# Invalid
2name = "Error"  # Starts with a number
first-name = "Error"  # Contains a hyphen
class = "Error"  # Reserved keyword
```

## Data Types in Python

Python is dynamically typed, which means you don’t need to declare the type of a variable. The type is determined by the value assigned.

### Common Data Types:

| Data Type     | Description                          | Example                  |
|---------------|--------------------------------------|--------------------------|
| `int`         | Integer numbers                     | `10`, `-5`, `100`        |
| `float`       | Decimal numbers                     | `3.14`, `-0.01`, `2.0`   |
| `str`         | Strings (text)                      | `"hello"`, `'world'`     |
| `bool`        | Boolean (True or False)             | `True`, `False`          |
| `list`        | Ordered collection of values        | `[1, 2, 3]`, `["a", "b"]`|
| `tuple`       | Immutable ordered collection        | `(1, 2, 3)`              |
| `dict`        | Key-value pairs (dictionary)        | `{"key": "value"}`       |

### Checking the Type of a Variable

Use the `type()` function to check a variable's type:
```python
x = 42
print(type(x))  # Output: <class 'int'>
```

## Reassigning Variables

Variables can be reassigned to values of different types:
```python
x = 10  # x is an integer
x = "Python"  # x is now a string
```

## Multiple Assignments

You can assign multiple variables in a single line:
```python
a, b, c = 1, 2, 3
```

Or assign the same value to multiple variables:
```python
x = y = z = 0
```

## Constants

Constants are variables meant to remain unchanged. By convention, their names are written in uppercase:
```python
PI = 3.14159
```

## Practice Exercises

1. Create variables for:
   - Your name.
   - Your age.
   - Your favorite number.
2. Print the type of each variable using `type()`.
3. Reassign one variable to a new value of a different type and print the result.

With this knowledge, you're ready to start working with data in Python!
