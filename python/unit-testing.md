---
layout: default
title: "Unit Testing"
order: 70
---

Python's `unittest` module is used for writing and running tests.

### Basic Test Case

Example:

```python
import unittest

def add(a, b):
    return a + b

class TestMath(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)

if __name__ == "__main__":
    unittest.main()
```

### Expected Output

```plaintext
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
```

### Running Multiple Tests

Add more test methods for comprehensive testing.

Example:

```python
class TestMath(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)

    def test_add_negative(self):
        self.assertEqual(add(-1, -1), -2)
```

Unit testing ensures your code works as expected.
