---
layout: default
title: "Exceptions"
order: 29
---

In Python, exceptions are errors that occur during program execution. Knowing the most common exceptions helps you identify and handle errors effectively.

## What Are Exceptions?

Exceptions are events that interrupt the normal flow of a program. They can occur due to various reasons, such as invalid user input, file not found, or division by zero. Python provides built-in exception types to describe specific error conditions.

### Common Exceptions in Python

Here are some of the most common exceptions and when they occur:

### 1. `ValueError`

Occurs when an operation or function receives an argument of the correct type but an inappropriate value.

#### Example:

```python
try:
    number = int("abc")  # Cannot convert "abc" to an integer
except ValueError:
    print("This is a ValueError!")
```

### Output:

```plaintext
This is a ValueError!
```

---

### 2. `TypeError`

Occurs when an operation or function is applied to an object of an inappropriate type.

#### Example:

```python
try:
    result = "abc" + 123  # Cannot add a string and an integer
except TypeError:
    print("This is a TypeError!")
```

### Output:

```plaintext
This is a TypeError!
```

---

### 3. `IndexError`

Occurs when trying to access an index that is out of range in a sequence (like a list or string).

#### Example:

```python
try:
    my_list = [1, 2, 3]
    print(my_list[5])  # Index 5 does not exist
except IndexError:
    print("This is an IndexError!")
```

### Output:

```plaintext
This is an IndexError!
```

---

### 4. `KeyError`

Occurs when trying to access a key that does not exist in a dictionary.

#### Example:

```python
try:
    my_dict = {"name": "Alice"}
    print(my_dict["age"])  # Key "age" does not exist
except KeyError:
    print("This is a KeyError!")
```

### Output:

```plaintext
This is a KeyError!
```

---

### 5. `ZeroDivisionError`

Occurs when attempting to divide by zero.

#### Example:

```python
try:
    result = 10 / 0  # Division by zero
except ZeroDivisionError:
    print("This is a ZeroDivisionError!")
```

### Output:

```plaintext
This is a ZeroDivisionError!
```

---

### 6. `FileNotFoundError`

Occurs when trying to open a file that does not exist.

#### Example:

```python
try:
    with open("nonexistent_file.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("This is a FileNotFoundError!")
```

### Output:

```plaintext
This is a FileNotFoundError!
```

---

### 7. `AttributeError`

Occurs when trying to access an attribute that does not exist on an object.

#### Example:

```python
try:
    number = 123
    number.append(4)  # Integers do not have an "append" method
except AttributeError:
    print("This is an AttributeError!")
```

### Output:

```plaintext
This is an AttributeError!
```

---

## Summary

Understanding these common exceptions helps you:
1. Diagnose errors during program execution.
2. Write more effective error-handling code.
3. Build robust programs that can handle unexpected situations gracefully.

Practice writing `try` and `except` blocks to handle these exceptions and improve the reliability of your programs.
