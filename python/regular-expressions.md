---
title: "Regular Expressions"
order: 32
---

# Regular Expressions in Python

Regular expressions (regex) are a powerful tool for pattern matching and text processing. Python provides the **`re`** module to work with regular expressions.

---

## Importing the `re` Module
```python
import re
```

---

## Basic Functions in the `re` Module

### `re.search()`
Searches for the first occurrence of a pattern in a string.

```python
text = "Hello, world!"
match = re.search(r"world", text)

if match:
    print("Found:", match.group())  # Output: Found: world
```

### `re.match()`
Checks if the pattern matches the start of the string.

```python
text = "Hello, world!"
match = re.match(r"Hello", text)

if match:
    print("Matched:", match.group())  # Output: Matched: Hello
```

### `re.findall()`
Finds all occurrences of a pattern in a string.

```python
text = "apple banana apple grape"
matches = re.findall(r"apple", text)

print(matches)  # Output: ['apple', 'apple']
```

### `re.sub()`
Replaces occurrences of a pattern with a specified string.

```python
text = "123-456-7890"
formatted = re.sub(r"-", ".", text)

print(formatted)  # Output: 123.456.7890
```

---

## Regular Expression Syntax

| Syntax   | Description                      |
|----------|----------------------------------|
| `.`      | Any character except newline     |
| `\d`     | Digit (0-9)                      |
| `\D`     | Non-digit                        |
| `\w`     | Word character (letters, digits, _) |
| `\W`     | Non-word character               |
| `\s`     | Whitespace (space, tab, newline) |
| `\S`     | Non-whitespace                   |
| `^`      | Start of string                  |
| `$`      | End of string                    |
| `*`      | Zero or more occurrences         |
| `+`      | One or more occurrences          |
| `?`      | Zero or one occurrence           |
| `{n}`    | Exactly n occurrences            |
| `{n,}`   | At least n occurrences           |
| `{n,m}`  | Between n and m occurrences      |
| `|`      | Logical OR                       |
| `(...)`  | Grouping                         |

---

## Pattern Examples

### Match Email Addresses
```python
text = "Contact us at support@example.com"
email_pattern = r"[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}"

match = re.search(email_pattern, text)
if match:
    print("Email:", match.group())  # Output: support@example.com
```

### Validate a Phone Number
```python
phone_pattern = r"\d{3}-\d{3}-\d{4}"
text = "Call me at 123-456-7890."

if re.search(phone_pattern, text):
    print("Valid phone number found")
```

### Extract Numbers
```python
text = "The price is 100 dollars"
numbers = re.findall(r"\d+", text)

print(numbers)  # Output: ['100']
```

---

## Working with Groups

### Capturing Groups
```python
text = "Date: 2025-01-16"
pattern = r"(\d{4})-(\d{2})-(\d{2})"

match = re.search(pattern, text)
if match:
    print("Year:", match.group(1))  # Output: 2025
    print("Month:", match.group(2))  # Output: 01
    print("Day:", match.group(3))    # Output: 16
```

### Named Groups
```python
text = "Date: 2025-01-16"
pattern = r"(?P<year>\d{4})-(?P<month>\d{2})-(?P<day>\d{2})"

match = re.search(pattern, text)
if match:
    print("Year:", match.group("year"))  # Output: 2025
```

---

## Compiling Regular Expressions

For better performance when using the same pattern multiple times, compile the regex.

```python
pattern = re.compile(r"\d+")
text = "There are 123 apples and 456 oranges."

matches = pattern.findall(text)
print(matches)  # Output: ['123', '456']
```

---

## Flags in Regular Expressions

### Common Flags
- `re.IGNORECASE` (**`re.I`**): Ignore case in matching.
- `re.MULTILINE` (**`re.M`**): Enable multi-line matching.
- `re.DOTALL` (**`re.S`**): Allow `.` to match newline characters.

### Example: Ignore Case
```python
text = "Hello, World!"
match = re.search(r"hello", text, re.IGNORECASE)

if match:
    print("Matched:", match.group())  # Output: Hello
```

---

## Practical Examples

### Replace Sensitive Data
```python
text = "My phone number is 123-456-7890."
redacted = re.sub(r"\d{3}-\d{3}-\d{4}", "[REDACTED]", text)

print(redacted)  # Output: My phone number is [REDACTED].
```

### Validate a Password
```python
password = "P@ssw0rd2025"

pattern = r"^(?=.*[A-Z])(?=.*[a-z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$"
if re.match(pattern, password):
    print("Password is valid")
else:
    print("Password is invalid")
```

---

## Best Practices

1. **Escape Special Characters**:
   - Use `\` to escape special regex characters (e.g., `\.` for a literal dot).

2. **Use Raw Strings**:
   - Always use raw strings (e.g., `r"pattern"`) to avoid issues with Python's string escaping.

3. **Break Down Complex Patterns**:
   - Use comments with the `re.VERBOSE` flag for readability.

---

## Practice Exercises

1. **Extract Hashtags**:
   - Write a regex to find all hashtags in a tweet.

2. **Validate an Email**:
   - Create a regex to validate an email address.

3. **Replace URLs**:
   - Replace all URLs in a string with `[LINK]`.

4. **Find Dates**:
   - Extract all dates in the format `YYYY-MM-DD` from a text.

Regular expressions are a versatile tool for pattern matching and text processing. With practice, they become an invaluable skill for handling strings in Python.