---
layout: default
title: "Logging"
order: 53
---

Logging is a way to record messages about your program’s execution, which helps in debugging, monitoring, and troubleshooting. Python’s built-in `logging` module provides a flexible framework for adding log messages to your code.

---

## Why Use Logging?

1. **Debugging**: Identify and fix issues in your code.
2. **Monitoring**: Track application performance and behavior.
3. **Error Tracking**: Record errors and exceptions for analysis.

---

## Basic Logging

The `logging` module can be used to log messages at different severity levels. The levels, in increasing order of severity, are:

- `DEBUG`: Detailed information for debugging.
- `INFO`: General messages about program execution.
- `WARNING`: Indication of potential problems.
- `ERROR`: A serious issue that has occurred.
- `CRITICAL`: A very severe error that may require immediate attention.

### Example: Basic Logging

```python
import logging

# Configure logging
logging.basicConfig(level=logging.DEBUG)

# Log messages
logging.debug("This is a debug message")
logging.info("This is an info message")
logging.warning("This is a warning message")
logging.error("This is an error message")
logging.critical("This is a critical message")
```

### Output Example

When you run this code, you’ll see:

```plaintext
DEBUG:root:This is a debug message
INFO:root:This is an info message
WARNING:root:This is a warning message
ERROR:root:This is an error message
CRITICAL:root:This is a critical message
```

---

## Configuring Logging

You can customize the logging output, including its format and where it’s written (e.g., console, file).

### Example: Logging to a File

```python
import logging

# Configure logging to write to a file
logging.basicConfig(
    filename="app.log",
    level=logging.INFO,
    format="%(asctime)s - %(levelname)s - %(message)s"
)

logging.info("This message will be written to the file")
```

This creates a file `app.log` with log entries formatted with a timestamp, severity level, and message.

---

## Using Logger Objects

The `logging` module allows you to create custom logger objects for more control.

```python
import logging

# Create a logger
logger = logging.getLogger("my_logger")
logger.setLevel(logging.DEBUG)

# Create a console handler
console_handler = logging.StreamHandler()
console_handler.setLevel(logging.INFO)

# Set the format for the handler
formatter = logging.Formatter("%(name)s - %(levelname)s - %(message)s")
console_handler.setFormatter(formatter)

# Add the handler to the logger
logger.addHandler(console_handler)

logger.debug("This is a debug message")
logger.info("This is an info message")
```

---

## Best Practices for Logging

1. **Log at Appropriate Levels**: Use `DEBUG` for development, `INFO` for general events, and `WARNING` or higher for issues.
2. **Don’t Overuse Logs**: Log important events but avoid excessive logging, which can clutter your output.
3. **Secure Logs**: Avoid logging sensitive information like passwords or personal data.

---

In the next lesson, we’ll explore how to interact with APIs using Python’s `requests` library.
