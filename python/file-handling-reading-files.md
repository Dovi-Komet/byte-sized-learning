---
layout: default
title: "File Handling: Reading Files"
order: 23
---

Python allows you to read data from files, which is useful for working with external data sources.

### Reading a File

Use the `open()` function to open a file and the `read()` method to read its contents.

Example:

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

### Expected Output (if `example.txt` contains "Hello, World!")

```plaintext
Hello, World!
```

### Why Use `with`?

The `with` statement ensures the file is properly closed after it is read, even if an error occurs.