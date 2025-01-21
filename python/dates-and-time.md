---
title: "Dates and Time"
order: 29
---

# Dates and Time in Python

Python provides the **`datetime`** module for working with dates and times. It allows you to manipulate, format, and perform calculations on date and time data.

---

## Importing the `datetime` Module
```python
from datetime import datetime, timedelta, date
```

---

## Current Date and Time

### Get the Current Date and Time
```python
now = datetime.now()
print(now)  # Output: Current date and time
```

### Get the Current Date
```python
today = date.today()
print(today)  # Output: Current date
```

---

## Formatting Dates and Times

### Default String Representation
```python
now = datetime.now()
print(str(now))  # Output: "2025-01-16 10:15:30.123456"
```

### Custom Formatting with `strftime`
```python
formatted = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted)  # Output: "2025-01-16 10:15:30"
```

#### Common Formatting Codes:
- `%Y`: Year (e.g., 2025)
- `%m`: Month (01 to 12)
- `%d`: Day of the month (01 to 31)
- `%H`: Hour (00 to 23)
- `%M`: Minute (00 to 59)
- `%S`: Second (00 to 59)
- `%A`: Full weekday name (e.g., Monday)
- `%B`: Full month name (e.g., January)

---

## Parsing Strings to Dates

### Convert a String to a `datetime` Object
```python
date_string = "2025-01-16 10:15:30"
parsed_date = datetime.strptime(date_string, "%Y-%m-%d %H:%M:%S")
print(parsed_date)  # Output: 2025-01-16 10:15:30
```

---

## Date Arithmetic

### Adding and Subtracting Time
```python
now = datetime.now()
future_date = now + timedelta(days=7)
past_date = now - timedelta(days=30)

print(future_date)  # Output: Date 7 days from now
print(past_date)    # Output: Date 30 days ago
```

---

## Comparing Dates
```python
date1 = datetime(2025, 1, 1)
date2 = datetime(2025, 12, 31)

if date1 < date2:
    print("date1 is earlier than date2")
```

---

## Working with Time Zones

### Using `pytz` for Time Zones
The `pytz` library provides support for time zones.

```python
import pytz

utc = pytz.UTC
eastern = pytz.timezone("US/Eastern")

now = datetime.now(utc)
eastern_time = now.astimezone(eastern)

print(eastern_time)  # Output: Current time in US/Eastern timezone
```

---

## Practical Examples

### Calculate Age from a Birthdate
```python
from datetime import date

def calculate_age(birthdate):
    today = date.today()
    return today.year - birthdate.year - ((today.month, today.day) < (birthdate.month, birthdate.day))

birthdate = date(1990, 5, 20)
print(calculate_age(birthdate))  # Output: Age in years
```

### Countdown to a Specific Date
```python
from datetime import datetime

target_date = datetime(2025, 12, 31)
now = datetime.now()
remaining = target_date - now

print(f"Days remaining: {remaining.days}")
```

### Log with Timestamps
```python
now = datetime.now()
log_message = f"[{now.strftime('%Y-%m-%d %H:%M:%S')}] Application started."
print(log_message)
```

---

## Best Practices

1. **Use `datetime` for Date and Time**:
   - Use `datetime` objects instead of strings for date and time operations.

2. **Avoid Hardcoding Time Zones**:
   - Use libraries like `pytz` or `zoneinfo` (Python 3.9+) for managing time zones.

3. **Error Handling for Parsing**:
   - Use `try-except` blocks when parsing strings to dates to handle invalid formats.

---

## Practice Exercises

1. **Date Formatting**:
   - Format the current date as `"Day: Monday, Date: 2025-01-16"`.

2. **Date Parsing**:
   - Parse the string `"16-01-2025"` into a `datetime` object.

3. **Date Arithmetic**:
   - Write a script that calculates the number of days between two user-provided dates.

4. **Age Calculator**:
   - Create a program that calculates a person's age based on their birthdate.

The `datetime` module is an essential tool for handling dates and times in Python. Its versatility and wide range of features make it ideal for a variety of applications.