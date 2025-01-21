---
title: "Strings"
order: 7
---

# Strings

Strings are sequences of characters enclosed in quotes. They are one of the most commonly used data types in Python, allowing you to work with text.

## Creating Strings

1. **Single Quotes**:
   ```python
   single_quote = 'Hello, World!'
   ```

2. **Double Quotes**:
   ```python
   double_quote = "Hello, Python!"
   ```

3. **Triple Quotes**:
   Used for multi-line strings or docstrings:
   ```python
   multi_line = """This is
   a multi-line
   string."""
   ```

## Common String Operations

| Operation          | Example                          | Result                   |
|--------------------|----------------------------------|--------------------------|
| Concatenation      | `'Hello' + ' World'`            | `'Hello World'`          |
| Repetition         | `'Python' * 3`                  | `'PythonPythonPython'`   |
| Length             | `len('Python')`                 | `6`                      |
| Access by Index    | `'Python'[0]`                   | `'P'`                    |
| Slicing            | `'Python'[0:3]`                 | `'Pyt'`                  |
| Check Substring    | `'Py' in 'Python'`              | `True`                   |

### Examples:
```python
greeting = "Hello"
name = "Alice"

# Concatenation
print(greeting + " " + name)  # Hello Alice

# Repetition
print(name * 3)  # AliceAliceAlice

# Length
print(len(greeting))  # 5

# Access by Index
print(greeting[1])  # e

# Slicing
print(greeting[1:4])  # ell

# Check Substring
print("lo" in greeting)  # True
```

## String Methods

Python provides several built-in methods to work with strings:

| Method             | Description                              | Example                        | Result                 |
|--------------------|------------------------------------------|--------------------------------|------------------------|
| `lower()`          | Converts to lowercase                   | `'PYTHON'.lower()`            | `'python'`            |
| `upper()`          | Converts to uppercase                   | `'python'.upper()`            | `'PYTHON'`            |
| `strip()`          | Removes whitespace                      | `'  hello  '.strip()`         | `'hello'`             |
| `replace(a, b)`    | Replaces substring `a` with `b`          | `'hello'.replace('e', 'a')`   | `'hallo'`             |
| `split(delim)`     | Splits string into a list               | `'a,b,c'.split(',')`          | `['a', 'b', 'c']`     |
| `join(iterable)`   | Joins elements with a delimiter          | `','.join(['a', 'b', 'c'])`   | `'a,b,c'`             |

### Examples:
```python
text = "  Python is Fun!  "

# Convert to lowercase
print(text.lower())  # python is fun!

# Convert to uppercase
print(text.upper())  # PYTHON IS FUN!

# Remove whitespace
print(text.strip())  # Python is Fun!

# Replace substring
print(text.replace("Fun", "Awesome"))  # Python is Awesome!

# Split and join
words = text.strip().split(" ")  # ['Python', 'is', 'Fun!']
print("-".join(words))  # Python-is-Fun!
```

## Escape Characters

Special characters in strings can be included using backslashes (`\`):

| Escape Character | Description               | Example         | Result          |
|------------------|---------------------------|-----------------|-----------------|
| `\'`            | Single quote              | `'It\'s OK'`    | `It's OK`       |
| `\"`            | Double quote              | `"He said \"Hi\""` | `He said "Hi"` |
| `\\`            | Backslash                 | `'C:\\path'`    | `C:\path`       |
| `\n`            | Newline                   | `'Hello\nWorld'`| `Hello↵World`   |
| `\t`            | Tab                       | `'Hello\tWorld'`| `Hello    World`|

### Example:
```python
print("It's a beautiful day!")
print("Line1\nLine2")
print("Path: C:\\Users\\Alice")
```

## Practice Exercises

1. Create a string variable containing your full name.
   - Print the length of the string.
   - Extract your first and last names using slicing.
2. Take a string `"Hello, World!"`:
   - Convert it to lowercase.
   - Replace `"World"` with `"Python"`.
   - Split it into a list of words.
3. Print a multi-line string using triple quotes.

Strings are an essential part of Python and understanding them will help you work with text-based data effectively!