---
layout: default
title: "datetime Module"
order: 37
---

The `datetime` module allows you to work with dates and times, making it easy to handle tasks like displaying the current time, formatting dates, or performing calculations with time.

---

## Getting the Current Date and Time

Use `datetime.now()` to get the current date and time.

### Example: Getting Current Date and Time

```python
from datetime import datetime

now = datetime.now()
print("Current date and time:", now)
```

### Output (varies based on your system):

```plaintext
Current date and time: 2024-12-29 14:35:00.123456  # (The actual output will vary.)
```

---

## Formatting Dates

Use the `strftime()` method to format dates and times into a readable string based on a specified pattern.

### Example: Formatting Dates

```python
formatted_date = now.strftime("%Y-%m-%d %H:%M:%S")
print("Formatted date:", formatted_date)
```

### Output:

```plaintext
Formatted date: 2024-12-29 14:35:00  # (The format will match the string pattern.)
```

### Common Formatting Codes:

- `%Y`: Year with century (e.g., `2024`).
- `%m`: Month as a zero-padded decimal number (e.g., `01`).
- `%d`: Day of the month (e.g., `29`).
- `%H`: Hour (24-hour clock) (e.g., `14`).
- `%M`: Minute (e.g., `35`).
- `%S`: Second (e.g., `00`).

---

## Parsing Dates from Strings

Use the `strptime()` method to convert a date string into a `datetime` object.

### Example: Parsing a Date String

```python
date_string = "2024-12-29 14:35:00"
parsed_date = datetime.strptime(date_string, "%Y-%m-%d %H:%M:%S")
print("Parsed date:", parsed_date)
```

### Output:

```plaintext
Parsed date: 2024-12-29 14:35:00
```

---

## Performing Date Arithmetic

The `timedelta` class allows you to perform operations like adding or subtracting days, hours, or minutes.

### Example: Adding Days to a Date

```python
from datetime import timedelta

future_date = now + timedelta(days=7)
print("Date one week from now:", future_date)
```

### Output:

```plaintext
Date one week from now: 2025-01-05 14:35:00.123456  # (The actual output will vary.)
```

---

## Summary

- **`datetime.now()`**: Get the current date and time.
- **`strftime()`**: Format dates and times into a readable string.
- **`strptime()`**: Parse a date string into a `datetime` object.
- **`timedelta`**: Perform arithmetic with dates and times.

The `datetime` module is a versatile tool for working with dates and times. Practice formatting, parsing, and manipulating dates to handle time-based operations effectively.
