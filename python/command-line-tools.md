---
layout: default
title: "Command-Line Tools"
order: 77
---

The `argparse` module helps you create command-line tools.

### Basic Example

Example:

```python
import argparse

parser = argparse.ArgumentParser(description="A simple CLI tool")
parser.add_argument("name", help="Your name")

args = parser.parse_args()
print(f"Hello, {args.name}!")
```

Run the script from the terminal:

```plaintext
python script.py Alice
```

### Expected Output

```plaintext
Hello, Alice!
```

The `argparse` module makes it easy to handle command-line arguments.
