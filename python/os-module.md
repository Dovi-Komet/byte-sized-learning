---
layout: default
title: "os Module"
order: 36
---

The `os` module in Python provides a way to interact with the operating system. It offers functionality for file and directory management, environment variables, and executing system commands. This module is part of the Python Standard Library and is available without any additional installation.

---

## Importing the `os` Module

To use the `os` module, you need to import it into your Python program:

```python
import os
```

---

## Commonly Used Functions in the `os` Module

### Get Current Working Directory

The `os.getcwd()` function returns the current working directory.

```python
import os

# Get and print the current working directory
current_dir = os.getcwd()
print("Current Directory:", current_dir)
```

### Change Directory

The `os.chdir(path)` function changes the current working directory.

```python
# Change to a new directory
os.chdir("/path/to/new/directory")
print("Directory changed to:", os.getcwd())
```

### List Files and Directories

The `os.listdir(path)` function lists all files and directories in the specified path.

```python
# List files and directories in the current directory
contents = os.listdir(".")
print("Contents:", contents)
```

---

## Creating and Removing Directories

### Create a Directory

Use `os.mkdir(path)` to create a new directory.

```python
# Create a new directory
os.mkdir("example_directory")
print("Directory 'example_directory' created!")
```

### Remove a Directory

Use `os.rmdir(path)` to remove an empty directory.

```python
# Remove the directory
os.rmdir("example_directory")
print("Directory 'example_directory' removed!")
```

---

## Environment Variables

The `os.environ` object allows you to access environment variables.

```python
# Get the value of the PATH environment variable
path_env = os.environ.get("PATH")
print("PATH:", path_env)
```

---

## Executing System Commands

The `os.system(command)` function runs a system command.

```python
# Execute a system command
os.system("echo Hello from the os module!")
```

---

## Documentation

For a full list of functions provided by the `os` module, visit the [official Python documentation](https://docs.python.org/3/library/os.html){:target="_blank"}.

---

The `os` module is a powerful tool for interacting with the operating system. In the next lesson, we’ll explore the `datetime` module, which provides tools for working with dates and times.
