---
layout: default
title: "Custom Modules"
order: 32
---

You can create your own module by saving Python code in a `.py` file and importing it into another file.

### Creating a Module

Save the following code in a file called `my_module.py`:

```python
def greet(name):
    return f"Hello, {name}!"
```

### Using Your Module

Create another file and import your module:

```python
import my_module
message = my_module.greet("Alice")
print(message)
```

### Expected Output

```plaintext
Hello, Alice!
```

Creating your own modules allows you to organize and reuse your code effectively.