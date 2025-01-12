---
layout: default
title: "Strings"
order: 9
---

Strings are sequences of characters enclosed in quotes. They are used to represent text in Python.

## Creating Strings

You can create strings using single quotes, double quotes, or triple quotes.

```python
# Single-quoted string
single = 'Hello'

# Double-quoted string
double = "World"

# Triple-quoted string (used for multi-line strings)
triple = """This is a
multi-line string."""
print(single, double, triple)
```

## String Operations

Strings in Python support many operations, including concatenation, repetition, and indexing.

### Concatenation

You can combine strings using the `+` operator.

```python
greeting = "Hello, " + "World!"
print(greeting)  # Output: Hello, World!
```

### Repetition

Use the `*` operator to repeat a string multiple times.

```python
repeat = "ha" * 3
print(repeat)  # Output: hahaha
```

### Indexing and Slicing

Strings are indexed starting from `0`. You can access individual characters or slices (substrings) of a string.

```python
text = "Python"

# Indexing
print(text[0])  # Output: P
print(text[-1]) # Output: n (last character)

# Slicing
print(text[0:3])  # Output: Pyt (characters from index 0 to 2)
print(text[3:])   # Output: hon (characters from index 3 to end)
```

## Common String Methods

Python provides several built-in methods to manipulate strings:

| Method          | Description                                     | Example                               |
|------------------|-------------------------------------------------|---------------------------------------|
| `lower()`       | Converts all characters to lowercase.           | `"PYTHON".lower()` → `"python"`      |
| `upper()`       | Converts all characters to uppercase.           | `"python".upper()` → `"PYTHON"`      |
| `strip()`       | Removes leading and trailing whitespace.        | `"  hello  ".strip()` → `"hello"`    |
| `replace(a, b)` | Replaces all occurrences of `a` with `b`.       | `"hello".replace("e", "a")` → `"hallo"` |
| `split(delim)`  | Splits a string into a list using `delim`.      | `"a,b,c".split(",")` → `['a', 'b', 'c']` |
| `join(list)`    | Joins a list of strings into one string.         | `",".join(['a', 'b', 'c'])` → `"a,b,c"` |

### Examples
```python
text = " Python Programming "
print(text.lower())     # Output: python programming
print(text.upper())     # Output: PYTHON PROGRAMMING
print(text.strip())     # Output: Python Programming
print(text.replace("Python", "Java"))  # Output: Java Programming
```

## String Formatting

String formatting allows you to create dynamic strings by including variable values.

### Using f-strings (Recommended)

```python
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
# Output: My name is Alice and I am 25 years old.
```

### Using `.format()`

```python
template = "My name is {} and I am {} years old."
print(template.format("Alice", 25))
# Output: My name is Alice and I am 25 years old.
```

---

In the next lesson, we’ll explore slicing and indexing in greater depth.
