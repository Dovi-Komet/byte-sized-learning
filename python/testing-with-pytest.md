---
layout: default
title: "Testing with pytest"
order: 52
---

`pytest` is a popular Python testing framework that makes writing and running tests simple and efficient. It offers more flexibility than `unittest` and is widely used in the Python community.

---

## Why Use `pytest`?

1. **Simple Syntax**: No need to write test classes; use plain functions instead.
2. **Powerful Features**: Supports fixtures, parameterized tests, and plugins.
3. **Detailed Reporting**: Provides clear output and debugging information.

---

## Installing `pytest`

Install `pytest` using `pip`:

```bash
pip install pytest
```

---

## Writing Tests with `pytest`

Tests in `pytest` are simple functions that start with `test_`.

### Example: Basic Test

```python
# math_operations.py
def add(a, b):
    return a + b
```

```python
# test_math_operations.py
from math_operations import add

def test_add():
    assert add(2, 3) == 5  # Check if add(2, 3) returns 5
    assert add(-1, 1) == 0 # Check if add(-1, 1) returns 0
```

### Explanation:
- The `add` function is defined in `math_operations.py`.
- The test file, `test_math_operations.py`, contains tests for the `add` function.
- The `assert` keyword checks if the condition is true.

---

## Running Tests with `pytest`

Run tests in a directory or file by using the `pytest` command:

```bash
pytest
```

To run tests in a specific file:

```bash
pytest test_math_operations.py
```

---

### Output Example

If all tests pass, you’ll see:

```plaintext
============================= test session starts =============================
collected 2 items

test_math_operations.py ..                                            [100%]

============================== 2 passed in 0.01s ==============================
```

---

## Advanced Features of `pytest`

### Using Fixtures

Fixtures provide setup and teardown logic for tests.

```python
import pytest

@pytest.fixture
def sample_data():
    return {"a": 1, "b": 2, "c": 3}

def test_sample_data(sample_data):
    assert sample_data["a"] == 1
    assert "b" in sample_data
```

### Parameterized Tests

Run the same test with multiple inputs:

```python
import pytest

@pytest.mark.parametrize("a, b, expected", [(1, 2, 3), (2, 3, 5), (-1, -1, -2)])
def test_add(a, b, expected):
    assert a + b == expected
```

---

## Key Takeaways

- `pytest` simplifies writing and running tests.
- Use plain functions and `assert` statements for test cases.
- Leverage powerful features like fixtures and parameterized tests.

---

In the next lesson, we’ll explore logging in Python and how it helps in debugging and monitoring applications.
