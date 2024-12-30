---
layout: default
title: "File Handling: Writing to Files"
order: 24
---

You can write data to a file in Python using the `write()` method.

### Writing to a File

Use the `open()` function with the `"w"` mode to write to a file. If the file doesn’t exist, it will be created.

Example:

```python
with open("output.txt", "w") as file:
    file.write("This is some text.")
```

### Expected Output

A file named `output.txt` will be created with the following content:

```plaintext
This is some text.
```

### Appending to a File

Use the `"a"` mode to append data to an existing file.

Example:

```python
with open("output.txt", "a") as file:
    file.write("\nThis is additional text.")
```