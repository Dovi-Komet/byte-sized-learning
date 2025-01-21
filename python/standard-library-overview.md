---
title: "Standard Library Overview"
order: 26
---

# Standard Library Overview

Python's **standard library** is a collection of modules and packages that come pre-installed with Python. It provides a wealth of functionality, enabling developers to perform a variety of tasks without installing external packages.

---

## Categories of Modules

### 1. **File and Directory Management**
- **os**: Interact with the operating system.
- **shutil**: High-level file operations.
- **glob**: Find files by patterns.

#### Examples:
```python
import os

print(os.getcwd())  # Get current working directory
os.mkdir("new_folder")  # Create a new directory
```

---

### 2. **Data and Time Handling**
- **datetime**: Work with dates and times.
- **time**: Time-related functions.
- **calendar**: Generate and manipulate calendars.

#### Examples:
```python
from datetime import datetime

now = datetime.now()
print(now)  # Output: Current date and time
```

---

### 3. **Mathematics**
- **math**: Mathematical functions.
- **random**: Generate random numbers.
- **statistics**: Statistical functions.

#### Examples:
```python
import math

print(math.sqrt(16))  # Output: 4.0
```

---

### 4. **String Handling**
- **string**: Constants and utility functions for strings.
- **re**: Regular expressions for advanced string processing.

#### Examples:
```python
import re

pattern = r"\d+"
match = re.search(pattern, "There are 123 apples")
print(match.group())  # Output: 123
```

---

### 5. **Internet and Web Services**
- **urllib**: Work with URLs.
- **http.client**: HTTP protocol client.
- **json**: Parse and generate JSON data.

#### Examples:
```python
import json

data = {"name": "Alice", "age": 30}
json_data = json.dumps(data)
print(json_data)  # Output: {"name": "Alice", "age": 30}
```

---

### 6. **System Utilities**
- **sys**: System-specific parameters and functions.
- **argparse**: Command-line argument parsing.
- **logging**: Logging utility.

#### Examples:
```python
import sys

print(sys.version)  # Python version
```

---

### 7. **Concurrency and Parallelism**
- **threading**: Thread-based parallelism.
- **multiprocessing**: Process-based parallelism.

#### Examples:
```python
import threading

def worker():
    print("Thread is running")

thread = threading.Thread(target=worker)
thread.start()
```

---

### 8. **Data Persistence**
- **pickle**: Serialize and deserialize Python objects.
- **shelve**: Persistent, dictionary-like objects.

#### Examples:
```python
import pickle

data = {"name": "Alice", "age": 30}
with open("data.pkl", "wb") as file:
    pickle.dump(data, file)
```

---

### 9. **Testing and Debugging**
- **unittest**: Unit testing framework.
- **pdb**: Python debugger.

#### Examples:
```python
import unittest

class TestExample(unittest.TestCase):
    def test_addition(self):
        self.assertEqual(1 + 1, 2)

unittest.main()
```

---

### 10. **Compression and Archiving**
- **zipfile**: Work with ZIP files.
- **tarfile**: Work with TAR files.

#### Examples:
```python
import zipfile

with zipfile.ZipFile("example.zip", "r") as zip_ref:
    zip_ref.extractall("output_folder")
```

---

### 11. **Email and Communication**
- **smtplib**: Send emails using SMTP.
- **email**: Create and parse email messages.

#### Examples:
```python
import smtplib

# Connect to SMTP server
server = smtplib.SMTP("smtp.example.com", 587)
server.starttls()
server.login("user@example.com", "password")
server.quit()
```

---

### 12. **Development Tools**
- **abc**: Abstract base classes.
- **inspect**: Inspect live objects.

#### Examples:
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass
```

---

## Benefits of Using the Standard Library

1. **No Installation Required**: Comes with Python by default.
2. **Reliable and Well-Maintained**: Built and maintained by Python developers.
3. **Cross-Platform**: Works across operating systems.

---

## Practice Exercises

1. **File Management**:
   - Use the `os` and `shutil` modules to create a directory, move a file into it, and then delete the directory.

2. **Data Handling**:
   - Write a script that uses `json` to read a JSON file and print its contents.

3. **String Processing**:
   - Use the `re` module to find all numbers in a given string.

4. **Datetime**:
   - Create a script that calculates the number of days until the next year using `datetime`.

5. **Testing**:
   - Write a simple unit test using the `unittest` module.

Python's standard library provides all the tools you need to perform common programming tasks effectively and efficiently.