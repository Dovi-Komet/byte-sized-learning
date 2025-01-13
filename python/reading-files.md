---
layout: default
title: "Reading Files"
order: 27
---

Python provides built-in functions for working with files, allowing you to read data from files for further processing. The `open()` function is commonly used to open files.

## Opening a File

To read a file, use the `open()` function. It requires the file name and mode. The most common mode for reading is `"r"` (read mode).

### Example:
```python
file = open("example.txt", "r")  # Open file in read mode
content = file.read()           # Read the entire file
print(content)
file.close()                    # Close the file
```

### Output:
Assuming `example.txt` contains:
```plaintext
Hello, World!
This is a sample file.
```

The output would be:
```plaintext
Hello, World!
This is a sample file.
```

### Best Practice: Using `with` Statement
The `with` statement ensures that the file is properly closed after its block of code is executed.

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

---

## Reading Line by Line

Use the `readline()` method to read one line at a time.

### Example:
```python
with open("example.txt", "r") as file:
    line1 = file.readline()
    line2 = file.readline()
    print(line1)
    print(line2)
```

### Output:
```plaintext
Hello, World!
This is a sample file.
```

---

## Reading All Lines as a List

Use the `readlines()` method to read all lines at once and return them as a list.

### Example:
```python
with open("example.txt", "r") as file:
    lines = file.readlines()
    print(lines)
```

### Output:
```plaintext
['Hello, World!\n', 'This is a sample file.\n']
```

### Stripping Newlines
You can remove newline characters using a list comprehension.

```python
with open("example.txt", "r") as file:
    lines = [line.strip() for line in file.readlines()]
    print(lines)
```

### Output:
```plaintext
['Hello, World!', 'This is a sample file.']
```

---

## Handling File Not Found Errors

If the file does not exist, Python raises a `FileNotFoundError`. You can handle this using a `try` block.

### Example:
```python
try:
    with open("nonexistent.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("The file does not exist.")
```

### Output:
```plaintext
The file does not exist.
```

---

Reading files is a crucial skill for processing and analyzing data. In the next lesson, we’ll learn how to write data to files.
