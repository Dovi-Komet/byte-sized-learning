---
layout: default
title: "Pickle Serialization"
order: 76
---

The `pickle` module serializes Python objects into byte streams.

### Saving an Object

Example:

```python
import pickle

data = {"name": "Alice", "age": 25}
with open("data.pkl", "wb") as file:
    pickle.dump(data, file)
```

### Loading an Object

Example:

```python
with open("data.pkl", "rb") as file:
    loaded_data = pickle.load(file)
    print(loaded_data)
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 25}
```

Pickle is useful for saving Python objects but should not be used with untrusted data.
