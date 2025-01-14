---
layout: default
title: "datetime Module"
order: 37
---

The `datetime` module in Python provides classes and functions for working with dates and times. It allows you to handle operations like getting the current date and time, formatting dates, and performing date arithmetic.

---

## Importing the `datetime` Module

To use the `datetime` module, import it into your program:

```python
import datetime
```

---

## Commonly Used Classes in the `datetime` Module

### `datetime.datetime`: Working with Dates and Times

#### Get the Current Date and Time

The `now()` method returns the current local date and time.

```python
import datetime

# Get the current date and time
current_time = datetime.datetime.now()
print("Current Date and Time:", current_time)
```

#### Create a Specific Date and Time

You can create a custom date and time using the `datetime()` constructor.

```python
# Create a custom date and time
custom_date = datetime.datetime(2025, 1, 1, 10, 30)
print("Custom Date and Time:", custom_date)
```

#### Format Dates and Times

The `strftime()` method formats a `datetime` object into a string.

```python
# Format the current date and time
formatted_time = current_time.strftime("%Y-%m-%d %H:%M:%S")
print("Formatted Date and Time:", formatted_time)
```

---

### `datetime.date`: Working with Dates

#### Get the Current Date

The `today()` method returns the current date.

```python
# Get the current date
current_date = datetime.date.today()
print("Current Date:", current_date)
```

#### Create a Specific Date

You can create a custom date using the `date()` constructor.

```python
# Create a custom date
custom_date = datetime.date(2025, 1, 1)
print("Custom Date:", custom_date)
```

---

### `datetime.timedelta`: Performing Date Arithmetic

The `timedelta` class represents a duration or difference between two dates or times.

#### Add or Subtract Days

```python
# Add 7 days to the current date
future_date = current_date + datetime.timedelta(days=7)
print("Date After 7 Days:", future_date)

# Subtract 7 days from the current date
past_date = current_date - datetime.timedelta(days=7)
print("Date 7 Days Ago:", past_date)
```

---

## Common Formatting Codes for `strftime`

Here are some useful formatting codes for dates and times:

- `%Y`: Year (e.g., 2025)
- `%m`: Month (01-12)
- `%d`: Day of the month (01-31)
- `%H`: Hour (00-23)
- `%M`: Minute (00-59)
- `%S`: Second (00-59)

For a complete list, refer to the [official Python documentation](https://docs.python.org/3/library/datetime.html){:target="_blank"}.

---

The `datetime` module is essential for handling dates and times in Python. In the next lesson, we’ll dive into the `json` module, which is used for working with JSON data.
