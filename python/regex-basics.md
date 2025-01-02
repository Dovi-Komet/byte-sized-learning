---
layout: default
title: "Regex Basics"
order: 65
---

Regular expressions (regex) are powerful for pattern matching in strings. Python provides the `re` module for regex operations.

### Basic Regex Operations

Example:

```python
import re

text = "The rain in Spain"
match = re.search("rain", text)
if match:
    print("Pattern found!")
```

### Expected Output

```plaintext
Pattern found!
```

### Common Methods in `re`

- `search()`: Searches for a pattern in a string.
- `findall()`: Returns all matches in a string.
- `match()`: Checks if the string starts with the pattern.

Example:

```python
matches = re.findall("ain", text)
print(matches)
```

### Expected Output

```plaintext
['ain', 'ain']
```

Regex is useful for text processing, validation, and parsing.
