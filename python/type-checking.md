---
layout: default
title: "Type Checking"
order: 90
---

The `typing` module allows you to add type hints to your Python code.

### Adding Type Hints

Example:

```python
from typing import List

def greet(name: str) -> str:
    return f"Hello, {name}!"

def sum_numbers(numbers: List[int]) -> int:
    return sum(numbers)

print(greet("Alice"))
print(sum_numbers([1, 2, 3]))
```

### Expected Output

```plaintext
Hello, Alice!
6
```

Type hints improve code readability and help with static analysis.
