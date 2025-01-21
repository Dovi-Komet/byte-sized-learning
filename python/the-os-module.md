---
title: "The os Module"
order: 27
---

# The `os` Module

The **`os` module** in Python provides functions to interact with the operating system. It allows you to perform tasks like handling directories, working with file paths, and accessing system information.

---

## Key Features of `os`

### 1. Working with Directories

#### Get the Current Working Directory
```python
import os

print(os.getcwd())  # Output: Current working directory
```

#### Change the Current Working Directory
```python
os.chdir("/path/to/directory")
print(os.getcwd())  # Output: Updated working directory
```

#### Create a Directory
```python
os.mkdir("new_folder")  # Creates a single directory
```

#### Create Nested Directories
```python
os.makedirs("parent_folder/child_folder")  # Creates directories recursively
```

#### Remove a Directory
```python
os.rmdir("new_folder")  # Removes an empty directory
```

#### Remove Nested Directories
```python
os.removedirs("parent_folder/child_folder")  # Removes directories recursively
```

---

### 2. Working with Files

#### Check if a File or Directory Exists
```python
print(os.path.exists("example.txt"))  # Output: True or False
```

#### Rename a File
```python
os.rename("old_name.txt", "new_name.txt")
```

#### Remove a File
```python
os.remove("example.txt")
```

---

### 3. Path Operations with `os.path`

The `os.path` module provides functions to work with file paths.

#### Join Paths
```python
path = os.path.join("folder", "subfolder", "file.txt")
print(path)  # Output: folder/subfolder/file.txt
```

#### Split a Path
```python
directory, file = os.path.split("/folder/file.txt")
print(directory)  # Output: /folder
print(file)       # Output: file.txt
```

#### Get File Extension
```python
_, extension = os.path.splitext("file.txt")
print(extension)  # Output: .txt
```

---

### 4. System Information

#### Get the Operating System Name
```python
print(os.name)  # Output: 'posix' (Linux/Mac), 'nt' (Windows)
```

#### Get Environment Variables
```python
print(os.environ)  # Dictionary of environment variables
print(os.environ.get("PATH"))  # Access a specific environment variable
```

#### Execute a System Command
```python
os.system("ls")  # Runs the `ls` command (Unix) or `dir` (Windows)
```

---

### 5. Traversing the File System

#### Walk Through a Directory Tree
The `os.walk()` function generates the file names in a directory tree.

```python
for root, dirs, files in os.walk("example_folder"):
    print("Root:", root)
    print("Directories:", dirs)
    print("Files:", files)
```

---

### 6. File Permissions

#### Change Permissions of a File
```python
os.chmod("example.txt", 0o644)  # Change file permissions
```

#### Get File Metadata
```python
info = os.stat("example.txt")
print(info.st_size)  # File size in bytes
print(info.st_mtime)  # Last modified time
```

---

## Practical Example

### Script to Organize Files by Extension
```python
import os

def organize_files(directory):
    os.chdir(directory)
    for file in os.listdir():
        if os.path.isfile(file):
            ext = os.path.splitext(file)[1][1:]  # Get the extension without the dot
            if not os.path.exists(ext):
                os.mkdir(ext)
            os.rename(file, os.path.join(ext, file))

organize_files("downloads_folder")
```

This script moves files into subfolders based on their extensions.

---

## Best Practices

1. **Error Handling**:
   - Always handle exceptions when performing file or directory operations.
   ```python
   try:
       os.remove("nonexistent_file.txt")
   except FileNotFoundError:
       print("File not found!")
   ```

2. **Use `os.path` for Portability**:
   - Avoid hardcoding file paths. Use `os.path` functions to make your code work across different operating systems.

3. **Clean Up Resources**:
   - Ensure files and directories are closed or properly cleaned up after operations.

---

## Practice Exercises

1. **Directory Management**:
   - Write a script that creates a nested directory structure and then removes it.

2. **File Organization**:
   - Write a script that organizes all files in a directory into subdirectories based on their extensions.

3. **System Commands**:
   - Use `os.system()` to execute a system command and capture its output.

The `os` module is a powerful tool for managing the file system and interacting with the operating system in a Pythonic way.