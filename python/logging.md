---
layout: default
title: "Logging"
order: 72
---

The `logging` module provides a flexible way to log messages for debugging and monitoring.

### Basic Logging

Example:

```python
import logging

logging.basicConfig(level=logging.INFO)
logging.info("This is an info message.")
logging.warning("This is a warning message.")
logging.error("This is an error message.")
```

### Expected Output

```plaintext
INFO:root:This is an info message.
WARNING:root:This is a warning message.
ERROR:root:This is an error message.
```

Logging provides better control over message levels than `print()` statements.
