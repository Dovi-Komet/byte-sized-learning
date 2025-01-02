---
layout: default
title: "Config Files"
order: 100
---

Configuration files allow you to separate configuration data from code. Python’s `configparser` module makes it easy to work with `.ini` files.

### Reading Config Files

Example:

```python
import configparser

config = configparser.ConfigParser()
config.read("settings.ini")

print("Database:", config["database"]["name"])
print("Host:", config["database"]["host"])
```

### Writing Config Files

Example:

```python
config["database"] = {
    "name": "my_database",
    "host": "localhost",
    "port": "3306"
}

with open("settings.ini", "w") as configfile:
    config.write(configfile)
```

### Expected Output

```plaintext
Database: my_database
Host: localhost
```

Config files make managing settings easier and more organized.
