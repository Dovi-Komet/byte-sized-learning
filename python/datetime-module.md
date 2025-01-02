---
layout: default
title: "datetime Module"
order: 36
---

The `datetime` module allows you to work with dates and times.

### Getting the Current Date and Time

Use `datetime.now()` to get the current date and time.

Example:

```python
from datetime import datetime
now = datetime.now()
print("Current date and time:", now)
```

### Expected Output

```plaintext
Current date and time: 2024-12-29 14:35:00.123456  # (The actual output will vary.)
```

### Formatting Dates

Use the `strftime()` method to format dates.

Example:

```python
formatted_date = now.strftime("%Y-%m-%d %H:%M:%S")
print("Formatted date:", formatted_date)
```

### Expected Output

```plaintext
Formatted date: 2024-12-29 14:35:00  # (The format will match the string pattern.)
```

Working with dates and times is made easy with the `datetime` module.