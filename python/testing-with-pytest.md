---
layout: default
title: "Testing with pytest"
order: 97
---

`pytest` is a popular testing framework that is more flexible than `unittest`.

### Installing pytest

Install with pip:

```plaintext
pip install pytest
```

### Writing a Simple Test with pytest

Example:

```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
    assert add(-1, 1) == 0

# Run with: pytest script.py
```

### Expected Output

```plaintext
================== test session starts ==================
collected 1 item

script.py .                                          [100%]

================== 1 passed in 0.01s ==================
```

pytest simplifies testing and offers advanced features like fixtures.
