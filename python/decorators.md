---
layout: default
title: "Decorators"
order: 61
---

Decorators are functions that modify the behavior of another function or method.

### Basic Decorator

Example:

```python
def decorator(func):
    def wrapper():
        print("Before function call")
        func()
        print("After function call")
    return wrapper

@decorator
def greet():
    print("Hello!")

greet()
```

### Expected Output

```plaintext
Before function call
Hello!
After function call
```

Decorators are used for logging, enforcing access control, memoization, and more.