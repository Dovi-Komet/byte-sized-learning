---
layout: default
title: "Modules: Introduction"
order: 28
---

Modules allow you to organize your code into separate files and reuse functionality. Python comes with many built-in modules, and you can also create your own.

### Importing a Module

Use the `import` statement to bring in a module.

Example:

```python
import math
print(math.sqrt(16))
```

### Expected Output

```plaintext
4.0
```

### Importing Specific Functions

You can import specific functions from a module.

Example:

```python
from math import pi, sqrt
print("Value of pi:", pi)
print("Square root of 25:", sqrt(25))
```

### Expected Output

```plaintext
Value of pi: 3.141592653589793
Square root of 25: 5.0
```

Modules make it easier to structure and reuse your code.