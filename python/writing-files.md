---
layout: default
title: "Writing Files"
order: 27
---

Python allows you to write data to files, making it easy to save output, logs, or processed data. You can create new files or modify existing ones using various modes.

## Writing to a File

To write to a file, use the `open()` function with the `"w"` mode. If the file doesn’t exist, it will be created. If it already exists, its contents will be overwritten.

### Example: Writing to a File

```python
with open("output.txt", "w") as file:
    file.write("This is some text.")
```

### Result

A file named `output.txt` will be created with the following content:

```plaintext
This is some text.
```

### Why Use `with`?

The `with` statement ensures the file is closed automatically after writing, even if an error occurs. This helps prevent data corruption or resource leaks.

## Appending to a File

Use the `"a"` mode to append data to an existing file. The new data is added to the end of the file without erasing its existing content.

### Example: Appending to a File

```python
with open("output.txt", "a") as file:
    file.write("\nThis is additional text.")
```

### Result

The file `output.txt` will now contain:

```plaintext
This is some text.
This is additional text.
```

## Writing Multiple Lines

You can write multiple lines to a file using a loop or the `writelines()` method.

### Example: Writing Multiple Lines

```python
lines = ["Line 1\n", "Line 2\n", "Line 3\n"]
with open("output.txt", "w") as file:
    file.writelines(lines)
```

### Result

The file `output.txt` will contain:

```plaintext
Line 1
Line 2
Line 3
```

## File Modes for Writing

- `"w"`: Write mode. Creates a new file or overwrites an existing file.
- `"a"`: Append mode. Adds data to the end of an existing file without overwriting its content.
- `"wb"` and `"ab"`: Write and append modes for binary data, such as images or files in non-text formats.

## Summary

- Use `"w"` mode to create or overwrite a file and `"a"` mode to append data.
- Write data with the `write()` method or multiple lines with `writelines()`.
- The `with` statement ensures files are properly closed after writing.
- Understand file modes to handle text and binary files appropriately.

Writing files is an essential skill for saving and managing data in Python. Experiment with writing and appending files to understand these operations better.
