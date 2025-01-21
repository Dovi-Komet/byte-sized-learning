---
title: "Reading and Writing Files"
order: 20
---

# Reading and Writing Files

Python provides powerful built-in functions for reading from and writing to files. File handling is an essential skill for interacting with external data.

---

## Opening a File

Use the `open()` function to open a file. The mode determines how the file is accessed.

### Common Modes:
- `"r"`: Read (default).
- `"w"`: Write (overwrites the file).
- `"a"`: Append (adds to the end of the file).
- `"b"`: Binary mode (e.g., `"rb"`, `"wb"`).
- `"x"`: Create (fails if the file exists).

### Example:
```python
# Open a file for reading
file = open("example.txt", "r")

# Close the file
file.close()
```

---

## Reading a File

### Read Entire File:
```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

### Read Line by Line:
```python
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())  # Removes trailing newline
```

### Read Specific Number of Characters:
```python
with open("example.txt", "r") as file:
    content = file.read(10)  # Read the first 10 characters
    print(content)
```

---

## Writing to a File

### Writing Text:
```python
with open("output.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a new file.")
```

### Appending to a File:
```python
with open("output.txt", "a") as file:
    file.write("\nAppending this line.")
```

---

## Working with Files Using `with`

Using the `with` statement ensures the file is properly closed, even if an error occurs.

### Example:
```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
# File is automatically closed here
```

---

## File Methods

| Method              | Description                              |
|---------------------|------------------------------------------|
| `read()`            | Reads the entire file as a string.       |
| `readline()`        | Reads one line at a time.                |
| `readlines()`       | Reads all lines as a list of strings.    |
| `write(text)`       | Writes the specified text to the file.   |
| `writelines(lines)` | Writes a list of strings to the file.    |

---

## Working with Binary Files

For non-text files like images or audio, use binary mode (`"b"`).

### Example:
```python
# Copy an image
with open("source.jpg", "rb") as source:
    content = source.read()

with open("copy.jpg", "wb") as target:
    target.write(content)
```

---

## Checking if a File Exists

Use the `os` module to check for a file's existence.

### Example:
```python
import os

if os.path.exists("example.txt"):
    print("File exists!")
else:
    print("File not found!")
```

---

## Practice Exercises

1. **Read a File**:
   - Create a file `data.txt` with some text.
   - Write a script to read and print its contents.

2. **Write to a File**:
   - Create a file `notes.txt` and write three lines of text.
   - Append two more lines to the same file.

3. **Copy a File**:
   - Write a script to copy the contents of one file to another.

4. **File Checker**:
   - Write a script that checks if a file exists and prints its size if it does.

---

File handling in Python is essential for working with data from external sources, saving results, and managing files efficiently!