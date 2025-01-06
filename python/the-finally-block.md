---
layout: default
title: "The finally Block"
order: 30
---

The `finally` block allows you to execute code regardless of whether an exception occurs. It is typically used for cleanup tasks like closing files or releasing resources.

## Using `finally`

The `finally` block always runs after the `try` and any associated `except` blocks, even if an exception is raised.

### Example: Using `finally`

```python
try:
    file = open("example.txt", "r")
    content = file.read()
    print(content)
except FileNotFoundError:
    print("File not found.")
finally:
    print("Execution completed.")
```

### Output (if `example.txt` does not exist)

```plaintext
File not found.
Execution completed.
```

In this example:
- If the file does not exist, the `except` block runs to handle the error.
- Regardless of the outcome, the `finally` block executes, printing "Execution completed."

---

## Using `finally` for Cleanup

The `finally` block is ideal for tasks like closing files or releasing resources to ensure they are handled properly.

### Example: Closing a File Safely

```python
try:
    file = open("example.txt", "r")
    content = file.read()
    print(content)
except FileNotFoundError:
    print("File not found.")
finally:
    if 'file' in locals() and not file.closed:
        file.close()
        print("File closed.")
```

### Output (if `example.txt` does not exist)

```plaintext
File not found.
File closed.
```

### Output (if `example.txt` exists and contains `"Hello, World!"`)

```plaintext
Hello, World!
File closed.
```

---

## Summary

- The `finally` block runs code after the `try` and `except` blocks, regardless of whether an exception occurs.
- It is commonly used for cleanup tasks such as closing files or releasing resources.
- Using `finally` ensures your program maintains proper resource management and avoids issues like unclosed files.

Practice using the `finally` block with different tasks to understand its importance in maintaining program reliability.
