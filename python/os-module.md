---
layout: default
title: "os Module"
order: 36
---

The `os` module allows you to interact with the operating system. It provides functions to work with directories, files, and environment variables, making it a versatile tool for file system management.

---

## Importing the `os` Module

To use the `os` module, you must import it:

```python
import os
```

---

## Getting the Current Working Directory

The `os.getcwd()` function retrieves the current working directory (the folder your Python script is running in).

### Example: Getting the Current Directory

```python
import os

print("Current directory:", os.getcwd())
```

### Output (varies based on your system):

```plaintext
Current directory: /path/to/your/directory
```

---

## Listing Files and Directories

Use the `os.listdir()` function to list all files and subdirectories in a directory.

### Example: Listing Files

```python
files = os.listdir()
print("Files and directories:", files)
```

### Output (varies based on your system):

```plaintext
Files and directories: ['file1.py', 'file2.txt', 'example.py']
```

---

## Creating and Removing Directories

The `os.mkdir()` function creates a new directory, while `os.rmdir()` removes an empty directory.

### Example: Creating and Removing Directories

```python
os.mkdir("test_folder")  # Create a new directory
print("After creation:", os.listdir())

os.rmdir("test_folder")  # Remove the directory
print("After removal:", os.listdir())
```

### Output (before and after):

```plaintext
After creation: ['test_folder', 'file1.py', 'file2.txt']
After removal: ['file1.py', 'file2.txt']
```

---

## Checking If a Path Exists

Use the `os.path.exists()` function to check if a file or directory exists.

### Example: Checking Path Existence

```python
path = "file1.py"
if os.path.exists(path):
    print(f"{path} exists.")
else:
    print(f"{path} does not exist.")
```

### Output (varies based on your system):

```plaintext
file1.py exists.
```

---

## Summary

- **`os.getcwd()`**: Get the current working directory.
- **`os.listdir()`**: List files and directories in a folder.
- **`os.mkdir()` and `os.rmdir()`**: Create and remove directories.
- **`os.path.exists()`**: Check if a path exists.

The `os` module is a powerful tool for interacting with the file system. Practice these functions to understand how to navigate and manipulate files and directories programmatically.
