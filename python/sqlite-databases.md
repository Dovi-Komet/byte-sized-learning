---
layout: default
title: "SQLite Databases"
order: 70
---

Python's `sqlite3` module allows you to work with SQLite databases.

### Connecting to a Database

Example:

```python
import sqlite3

connection = sqlite3.connect("example.db")
cursor = connection.cursor()
cursor.execute("CREATE TABLE IF NOT EXISTS users (id INTEGER PRIMARY KEY, name TEXT)")
connection.commit()
connection.close()
```

### Inserting Data

Example:

```python
connection = sqlite3.connect("example.db")
cursor = connection.cursor()
cursor.execute("INSERT INTO users (name) VALUES (?)", ("Alice",))
connection.commit()
connection.close()
```

### Retrieving Data

Example:

```python
connection = sqlite3.connect("example.db")
cursor = connection.cursor()
cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()
for row in rows:
    print(row)
connection.close()
```

SQLite is a lightweight, file-based database ideal for small projects.
