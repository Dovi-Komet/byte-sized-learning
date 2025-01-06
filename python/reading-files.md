---
layout: default
title: "Reading Files"
order: 26
---

Python allows you to read data from files, making it easy to work with external data sources such as text files, logs, or configuration files.

## Reading a File

To read a file, use the `open()` function and the `read()` method. The `open()` function requires the file name and mode. For reading, use mode `"r"`.

### Example: Reading a File

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

### Output (if `example.txt` contains `"Hello, World!"`)

```plaintext
Hello, World!
```

### Why Use `with`?

The `with` statement ensures the file is properly closed after it is read, even if an error occurs. This prevents resource leaks and keeps your code safe and efficient.

## Reading Line by Line

Use the `readline()` or `readlines()` methods to read files line by line, especially for large files.

### Example: Reading Lines with `readlines()`

```python
with open("example.txt", "r") as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())  # Remove extra whitespace
```

### Output (if `example.txt` contains two lines: `"Hello, World!"` and `"Python is fun!"`)

```plaintext
Hello, World!
Python is fun!
```

## File Modes for Reading

When opening files, you can specify modes to control how they are accessed:
- `"r"`: Read mode (default). Opens the file for reading and raises an error if the file does not exist.
- `"rb"`: Read mode in binary. Used for non-text files like images or PDFs.

## Handling Missing Files

If you try to open a file that does not exist, Python raises a `FileNotFoundError`. You can handle this error to make your program more robust.

### Example: Handling Missing Files

```python
try:
    with open("example.txt", "r") as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print("The file does not exist.")
```

### Output (if the file does not exist)

```plaintext
The file does not exist.
```

## Summary

- Use `open()` with mode `"r"` to read files.
- The `with` statement ensures files are closed properly after use.
- Read the entire file with `read()` or line by line with `readlines()` or `readline()`.
- Handle missing files with a `try` and `except` block to avoid program crashes.
- Understand file modes to handle text and binary files appropriately.

Reading files is a critical skill for working with external data. Practice with different file contents and methods to solidify your understanding.
