---
layout: default
title: "os Module"
order: 35
---

The `os` module allows you to interact with the operating system.

### Getting the Current Working Directory

Use the `os.getcwd()` function to get the current working directory.

Example:

```python
import os
print("Current directory:", os.getcwd())
```

### Expected Output (varies based on your system)

```plaintext
Current directory: /path/to/your/directory
```

### Listing Files in a Directory

Use the `os.listdir()` function to list all files and directories.

Example:

```python
files = os.listdir()
print("Files:", files)
```

### Expected Output (varies based on your system)

```plaintext
Files: ['file1.py', 'file2.txt', 'example.py']
```

The `os` module is powerful for performing file and directory operations.