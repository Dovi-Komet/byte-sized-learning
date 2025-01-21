---
title: "Logging"
order: 36
---

# Logging in Python

Logging is an essential tool for tracking the execution of an application, diagnosing issues, and gaining insights into its behavior. Python’s built-in `logging` module provides a flexible and powerful way to generate logs.

---

## Why Use Logging?

1. **Better than Print Statements:** Persistent and configurable logging avoids cluttering the code with `print()` statements.
2. **Debugging and Troubleshooting:** Helps identify issues by tracking program execution.
3. **Performance Monitoring:** Logs can provide valuable performance metrics.
4. **Security Audits:** Tracks actions and access within applications.
5. **Persistence:** Logs can be saved to files for future analysis.

---

## Basic Logging Example

Python provides a straightforward way to log messages.

```python
import logging

logging.basicConfig(level=logging.INFO)
logging.info("This is an informational message")
```

### Output:
```
INFO:root:This is an informational message
```

---

## Logging Levels

Python's logging module provides several log levels to indicate the severity of messages:

| Level      | Description                                | Numeric Value |
|------------|--------------------------------------------|---------------|
| DEBUG      | Detailed information for diagnosing issues | 10            |
| INFO       | General operational messages              | 20            |
| WARNING    | Something unexpected, but the program continues | 30            |
| ERROR      | A more serious issue that prevents execution of some parts | 40            |
| CRITICAL   | A severe error that might halt the application | 50            |

### Example of Different Log Levels:

```python
logging.debug("This is a debug message")
logging.info("This is an info message")
logging.warning("This is a warning")
logging.error("This is an error")
logging.critical("This is a critical error")
```

---

## Configuring Logging

The `basicConfig()` method allows configuring the logging behavior such as:

- Setting log levels
- Formatting log messages
- Specifying output files

### Example Configuration:

```python
logging.basicConfig(
    filename='app.log',
    level=logging.DEBUG,
    format='%(asctime)s - %(levelname)s - %(message)s'
)

logging.info("This message will be logged to a file")
```

#### Log File Output Example (`app.log`):
```
2025-01-21 12:34:56,789 - INFO - This message will be logged to a file
```

---

## Formatting Log Messages

Customizing log messages helps provide useful contextual information.

### Common Formatting Options:

- `%(asctime)s` – Timestamp
- `%(levelname)s` – Log level (DEBUG, INFO, etc.)
- `%(message)s` – Actual log message
- `%(name)s` – Logger's name
- `%(lineno)d` – Line number where log was created
- `%(filename)s` – Source file name

### Example with Custom Format:

```python
logging.basicConfig(
    format='%(levelname)s: %(name)s - %(message)s',
    level=logging.DEBUG
)

logging.debug("Debugging message")
```

#### Output:
```
DEBUG: root - Debugging message
```

---

## Logging to a File

Instead of logging to the console, logs can be saved to a file for later analysis.

```python
logging.basicConfig(
    filename='error.log',
    level=logging.ERROR,
    format='%(asctime)s - %(levelname)s - %(message)s'
)

logging.error("This is logged to the error.log file")
```

---

## Using Logger Objects

Instead of using the root logger, creating custom loggers gives more control.

```python
logger = logging.getLogger('my_logger')
logger.setLevel(logging.INFO)

handler = logging.FileHandler('my_log.log')
formatter = logging.Formatter('%(asctime)s - %(levelname)s - %(message)s')
handler.setFormatter(formatter)

logger.addHandler(handler)

logger.info("This is an info message from my_logger")
```

---

## Logging Exceptions

Logging exceptions provides stack traces that help debug errors.

```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    logging.error("An exception occurred", exc_info=True)
```

#### Output:
```
ERROR:root:An exception occurred
Traceback (most recent call last):
  File "example.py", line 2, in <module>
    result = 10 / 0
ZeroDivisionError: division by zero
```

---

## Rotating Logs

Using rotating log handlers prevents log files from growing indefinitely.

### Using `RotatingFileHandler`:

```python
from logging.handlers import RotatingFileHandler

handler = RotatingFileHandler('app.log', maxBytes=2000, backupCount=3)
logger = logging.getLogger('rotating_logger')
logger.setLevel(logging.INFO)
logger.addHandler(handler)

for i in range(1000):
    logger.info(f"Log message {i}")
```

- `maxBytes`: Maximum size of the log file before rotation.
- `backupCount`: Number of backup files to keep.

---

## Using `TimedRotatingFileHandler`

Logs can rotate based on time intervals.

```python
from logging.handlers import TimedRotatingFileHandler

handler = TimedRotatingFileHandler('timed_app.log', when='midnight', interval=1, backupCount=7)
logger = logging.getLogger('timed_logger')
logger.setLevel(logging.INFO)
logger.addHandler(handler)

logger.info("Log message with time-based rotation")
```

---

## Disabling Logging

To disable logging temporarily:

```python
logging.disable(logging.CRITICAL)
logging.critical("This message will not be logged")
```

---

## Best Practices for Logging

1. **Log Strategically:** Avoid logging too much or too little.
2. **Use Appropriate Levels:** Choose log levels according to message importance.
3. **Avoid Sensitive Data:** Never log passwords or personal information.
4. **Implement Rotations:** Prevent unlimited log growth.
5. **Centralize Logs:** Consider log aggregation tools for analysis.
6. **Format Consistently:** Ensure log readability and structure.
7. **Use Contextual Information:** Add relevant metadata (e.g., request IDs).

---

## Common Tools for Log Management

1. **Log Aggregation Services:**
   - ELK Stack (Elasticsearch, Logstash, Kibana)
   - Splunk
   - Graylog

2. **Cloud Logging Solutions:**
   - AWS CloudWatch
   - Google Cloud Logging
   - Azure Monitor

---

## Practice Exercises

1. Configure logging to log warnings and higher-level messages to a file.
2. Create a rotating file logger that rotates logs every 1KB.
3. Write a program that logs exceptions using `exc_info=True`.
4. Use a custom logger to log different messages to the console and file.

---

Logging is an essential tool for maintaining, debugging, and monitoring Python applications effectively. Using the right logging strategy helps improve the maintainability and scalability of your projects.