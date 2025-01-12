---
layout: default
title: "Slicing and Indexing"
order: 10
---

Slicing and indexing allow you to access specific parts of a sequence, such as a string or a list. This lesson focuses on how to use these features effectively.

## Indexing

Indexing retrieves a single element from a sequence. Python uses zero-based indexing, meaning the first element has an index of `0`.

### Example:
```python
text = "Python"

# Accessing characters by index
print(text[0])   # Output: P (first character)
print(text[1])   # Output: y (second character)
print(text[-1])  # Output: n (last character)
print(text[-2])  # Output: o (second to last character)
```

### Key Points:
- Positive indices count from the start (0, 1, 2, ...).
- Negative indices count from the end (-1, -2, -3, ...).

## Slicing

Slicing retrieves a portion (substring or sublist) of a sequence. Use the syntax `sequence[start:end]`, where:
- `start` is the index where the slice begins (inclusive).
- `end` is the index where the slice ends (exclusive).

### Example:
```python
text = "Python"

# Slicing the string
print(text[0:3])  # Output: Pyt (characters at indices 0, 1, 2)
print(text[2:5])  # Output: tho (characters at indices 2, 3, 4)
```

### Omitting Start or End
- If you omit `start`, Python assumes the slice begins at the start of the sequence.
- If you omit `end`, Python assumes the slice ends at the last element.

```python
text = "Python"

print(text[:3])   # Output: Pyt (from start to index 2)
print(text[3:])   # Output: hon (from index 3 to the end)
```

### Using Step
You can include a third parameter, `step`, to specify the interval between indices.

```python
text = "Python"

print(text[::2])  # Output: Pto (every second character)
print(text[::-1]) # Output: nohtyP (reversed string)
```

## Practical Examples

### Extracting Substrings
```python
url = "https://example.com"
domain = url[8:]  # Extract everything after the 8th character
print(domain)  # Output: example.com
```

### Modifying a Sequence
While strings are immutable (cannot be modified directly), you can create a new string using slicing.

```python
text = "Jython"
corrected_text = "P" + text[1:]  # Replace the first character
print(corrected_text)  # Output: Python
```

---

In the next lesson, we’ll learn how to gather input from users with the `input()` function.
