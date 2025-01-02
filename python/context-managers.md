---
layout: default
title: "Context Managers"
order: 62
---

Context managers handle setup and teardown actions using the `with` statement.

### Using the `with` Statement

Example:

```python
with open("example.txt", "w") as file:
    file.write("Hello, World!")
```

The `with` statement ensures resources are cleaned up, such as closing files.

### Custom Context Managers

Define your own context manager using `__enter__` and `__exit__` methods.

Example:

```python
class MyContext:
    def __enter__(self):
        print("Entering the context")
        return self

    def __exit__(self, exc_type, exc_value, traceback):
        print("Exiting the context")

with MyContext() as context:
    print("Inside the context")
```

### Expected Output

```plaintext
Entering the context
Inside the context
Exiting the context
```

Context managers ensure predictable resource management.
