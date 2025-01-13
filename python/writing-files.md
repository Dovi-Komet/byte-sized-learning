---
layout: default
title: "Writing Files"
order: 28
---

Python makes it easy to write data to files using the `open()` function in write (`"w"`) or append (`"a"`) mode. Writing to a file creates a new file if it doesn’t already exist or overwrites its content if it does.

## Writing to a File

To write to a file, open it in `"w"` mode and use the `write()` method.

### Example:
```python
with open("example.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a new line of text.")
```

### Result:
The file `example.txt` will contain:
```plaintext
Hello, World!
This is a new line of text.
```

---

## Appending to a File

To add content to an existing file without overwriting it, use `"a"` mode.

### Example:
```python
with open("example.txt", "a") as file:
    file.write("\nThis line is appended.")
```

### Result:
If `example.txt` initially contains:
```plaintext
Hello, World!
This is a new line of text.
```

It will now contain:
```plaintext
Hello, World!
This is a new line of text.
This line is appended.
```

---

## Writing Lists to Files

You can write a list of strings to a file using the `writelines()` method.

### Example:
```python
lines = ["Line 1\n", "Line 2\n", "Line 3\n"]
with open("example.txt", "w") as file:
    file.writelines(lines)
```

### Result:
The file `example.txt` will contain:
```plaintext
Line 1
Line 2
Line 3
```

---

## Handling Errors

Always handle errors to avoid crashes during file operations.

### Example:
```python
try:
    with open("example.txt", "w") as file:
        file.write("Writing to file safely!")
except IOError:
    print("An error occurred while writing to the file.")
```

### Output:
```plaintext
Writing to file safely!
```

---

## Writing JSON Data

Python’s `json` module allows you to write structured data to files in JSON format.

### Example:
```python
import json

data = {"name": "Alice", "age": 25, "city": "New York"}
with open("data.json", "w") as file:
    json.dump(data, file, indent=4)
```

### Result:
The file `data.json` will contain:
```json
{
    "name": "Alice",
    "age": 25,
    "city": "New York"
}
```

---

Writing files is essential for saving data and sharing results. In the next lesson, we’ll explore error handling basics to make your programs more robust.
