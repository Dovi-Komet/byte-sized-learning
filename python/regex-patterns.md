---
layout: default
title: "Regex Patterns"
order: 66
---

Regular expressions can match complex patterns using special symbols and groups.

### Special Characters

- `.`: Matches any character.
- `*`: Matches zero or more occurrences.
- `+`: Matches one or more occurrences.
- `[]`: Matches any character inside the brackets.

Example:

```python
import re

text = "bat, cat, mat"
pattern = "[bcm]at"
matches = re.findall(pattern, text)
print(matches)
```

### Expected Output

```plaintext
['bat', 'cat', 'mat']
```

### Grouping and Escaping

- Use `()` to group parts of patterns.
- Escape special characters with `\`.

Example:

```python
pattern = r"\d{3}-\d{2}-\d{4}"
text = "123-45-6789"
match = re.match(pattern, text)
if match:
    print("Valid format!")
```

### Expected Output

```plaintext
Valid format!
```

Regex helps identify and extract complex text patterns.
