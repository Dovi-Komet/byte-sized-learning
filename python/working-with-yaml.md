---
layout: default
title: "Working with YAML"
order: 91
---

YAML is a human-readable data serialization format. The `PyYAML` library allows you to work with YAML files.

### Installing PyYAML

Install with pip:

```plaintext
pip install pyyaml
```

### Reading and Writing YAML Files

Example:

```python
import yaml

# Reading YAML
yaml_data = """
name: Alice
age: 25
skills:
  - Python
  - Data Science
"""
data = yaml.safe_load(yaml_data)
print("Name:", data["name"])
print("Skills:", data["skills"])

# Writing YAML
output_data = {"project": "Python Course", "level": "Advanced"}
with open("output.yaml", "w") as file:
    yaml.dump(output_data, file)
```

### Expected Output

```plaintext
Name: Alice
Skills: ['Python', 'Data Science']
```

PyYAML makes it simple to handle YAML in Python.
