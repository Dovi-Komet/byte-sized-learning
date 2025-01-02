---
layout: default
title: "CLI with Click"
order: 92
---

Click is a library for building command-line interfaces.

### Installing Click

Install with pip:

```plaintext
pip install click
```

### Creating a CLI Application

Example:

```python
import click

@click.command()
@click.option("--name", default="World", help="Name to greet")
def greet(name):
    print(f"Hello, {name}!")

if __name__ == "__main__":
    greet()
```

### Expected Output

Run the script:

```plaintext
python script.py --name Alice
```

Output:

```plaintext
Hello, Alice!
```

Click simplifies building user-friendly command-line tools.
