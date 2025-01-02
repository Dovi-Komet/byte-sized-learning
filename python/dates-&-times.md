---
layout: default
title: "Dates & Times"
order: 81
---

The `time` and `calendar` modules help manage date and time operations.

### Using the `time` Module

Example:

```python
import time

current_time = time.time()
print("Current timestamp:", current_time)
local_time = time.localtime(current_time)
print("Local time:", time.strftime("%Y-%m-%d %H:%M:%S", local_time))
```

### Expected Output

```plaintext
Current timestamp: 1693409000.123456
Local time: 2024-08-30 10:30:00
```

### Using the `calendar` Module

Example:

```python
import calendar

print(calendar.month(2024, 8))
```

### Expected Output

```plaintext
    August 2024
Mo Tu We Th Fr Sa Su
           1  2  3  4
 5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28 29 30 31
```

These modules are useful for working with time-based data.
