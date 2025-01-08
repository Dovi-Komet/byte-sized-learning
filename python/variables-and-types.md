---
layout: default
title: "Variables and Types"
order: 7
---

Variables are used to store data in a Python program. They act as placeholders for values that can change during the execution of the program.

## Creating Variables

In Python, creating a variable is simple. You just need to assign a value to a name using the `=` operator.

```python
# Assigning values to variables
name = "Alice"  # A string
age = 25        # An integer
height = 5.8    # A float
```

### Explanation
- **`name`**: Stores a text value (string).
- **`age`**: Stores a whole number (integer).
- **`height`**: Stores a decimal number (float).

## Variable Naming Rules

1. Must start with a letter or an underscore (`_`).
2. Cannot start with a number.
3. Can only contain alphanumeric characters and underscores (`_`).
4. Are case-sensitive (`name` and `Name` are different).

### Examples
```python
valid_name = "John"
_valid_name = "Jane"
name1 = "Doe"
```

```python
# Invalid examples (uncommenting will cause an error):
# 1name = "Error"  # Starts with a number
# name@ = "Error"  # Contains a special character
```

## Types of Data

Python automatically assigns the type of a variable based on its value. Common data types include:

### String (`str`)

Text enclosed in quotes.

```python
text = "Hello, World!"
```

### Integer (`int`)

Whole numbers.

```python
number = 42
```

### Float (`float`)

Decimal numbers.

```python
pi = 3.14
```

### Boolean (`bool`)

True or False values.

```python
is_active = True
```

## Checking Variable Types

You can use the `type()` function to check the type of a variable:

```python
x = 10
print(type(x))  # Output: <class 'int'>
```

## Changing Variable Values

Variables can be reassigned to new values, even of a different type:

```python
variable = 10       # Initially an integer
print(variable)     # Output: 10
variable = "Python" # Now a string
print(variable)     # Output: Python
```

---

In the next lesson, we’ll explore numbers and mathematical operations in Python.
