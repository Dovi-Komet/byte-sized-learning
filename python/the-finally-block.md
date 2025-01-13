---
layout: default
title: "The finally Block"
order: 31
---

The `finally` block in Python is used to execute code that should run regardless of whether an exception occurs in the `try` block. It’s commonly used for cleanup tasks like closing files, releasing resources, or disconnecting from a database.

---

## Structure of `finally`

The `finally` block is used alongside `try` and optionally with `except` or `else`.

### Syntax:
```python
try:
    # Code that might raise an exception
except SomeException:
    # Code to handle the exception
else:
    # Code that runs if no exceptions occur
finally:
    # Code that always runs
```

---

## Using `finally`

The `finally` block ensures that the code within it runs no matter what happens in the `try` block.

### Example:
```python
try:
    file = open("example.txt", "r")
    content = file.read()
    print(content)
except FileNotFoundError:
    print("File not found!")
finally:
    print("Closing file.")
```

### Output (if file does not exist):
```plaintext
File not found!
Closing file.
```

### Output (if file exists):
```plaintext
<contents of the file>
Closing file.
```

---

## `finally` with Exceptions

Even if an exception occurs and isn’t caught, the `finally` block will execute.

### Example:
```python
try:
    print(10 / 0)  # This will raise ZeroDivisionError
finally:
    print("This will always run.")
```

### Output:
```plaintext
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
ZeroDivisionError: division by zero
This will always run.
```

---

## Practical Use Case: Resource Cleanup

The `finally` block is useful for cleaning up resources like closing files or releasing locks.

### Example:
```python
try:
    file = open("data.txt", "w")
    file.write("Writing some data.")
finally:
    file.close()
    print("File closed.")
```

### Output:
```plaintext
File closed.
```

---

The `finally` block ensures that critical cleanup tasks are executed, making your code more robust. In the next lesson, we’ll learn about Python modules and how to use them to organize and reuse code.
