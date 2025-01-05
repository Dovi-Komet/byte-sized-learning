---
layout: default
title: "Slicing and Indexing"
order: 11
---

Slicing and indexing allow you to access parts of strings and other sequences like lists in Python.

## Indexing

Indexing retrieves individual elements from a sequence using their position. Python uses zero-based indexing, meaning the first element is at position `0`. Negative indices count from the end of the sequence.

### Example: Indexing Strings

```python
word = "Python"
print(word[0])  # First character: 'P'
print(word[-1])  # Last character: 'n'
```

### Expected Output

```plaintext
P
n
```

## Slicing

Slicing extracts a portion of a sequence using the syntax `[start:end:step]`. 
- **start**: The index to start from (inclusive).
- **end**: The index to stop at (exclusive).
- **step**: The interval between indices (optional).

### Default Behavior in Slicing

- If `start` is omitted, slicing starts from the beginning of the sequence.
- If `end` is omitted, slicing goes to the end of the sequence.
- If `step` is omitted, the default step is `1`.

### Example: Default Behavior in Slicing

```python
word = "Python"
print(word[:4])   # From the start to index 3: 'Pyth'
print(word[2:])   # From index 2 to the end: 'thon'
print(word[:])    # The entire string: 'Python'
print(word[::2])  # Every second character: 'Pto'
```

### Expected Output

```plaintext
Pyth
thon
Python
Pto
```

Slicing and indexing are powerful tools that make it easy to manipulate strings and other sequences. Practice these operations to become comfortable with sequence handling in Python!
