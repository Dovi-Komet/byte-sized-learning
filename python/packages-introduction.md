---
layout: default
title: "Packages: Introduction"
order: 30
---

A package is a collection of modules organized into directories with a special `__init__.py` file. Packages help you structure larger projects.

### Creating a Package

1. Create a directory for your package.
2. Add an `__init__.py` file (even if it's empty) to make the directory a package.
3. Add modules to the package.

Example directory structure:

```bash
my_package/ 
    init.py 
    math_utils.py 
    string_utils.py
```

### Using a Package

You can import modules from your package.

Example:

```python
from my_package import math_utils
result = math_utils.add(2, 3)
print(result)
```

### Expected Output (if `add(2, 3)` is defined to return 5)

```plaintext
5
```

Packages make it easier to manage large codebases by organizing related functionality.