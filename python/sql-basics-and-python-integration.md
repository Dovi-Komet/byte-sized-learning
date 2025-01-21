---
title: "SQL Basics and Python Integration"
order: 38
---

# SQL Basics and Python Integration

Structured Query Language (SQL) is used to manage and manipulate relational databases. Python provides libraries like `sqlite3`, `mysql-connector-python`, and `SQLAlchemy` to interact with databases efficiently.

---

## Why Use SQL with Python?

- Store and manage structured data efficiently.
- Perform complex queries and data manipulations.
- Integrate with web applications, data analysis, and automation tasks.

---

## Setting Up SQLite in Python

SQLite is a lightweight, serverless database that comes with Python by default.

### Checking SQLite Installation

```python
import sqlite3
print(sqlite3.sqlite_version)
```

---

## Creating an SQLite Database

```python
import sqlite3

# Connect to a database (or create one)
conn = sqlite3.connect("my_database.db")

# Create a cursor object to execute SQL commands
cursor = conn.cursor()

# Create a table
cursor.execute("""
    CREATE TABLE IF NOT EXISTS users (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        name TEXT NOT NULL,
        age INTEGER
    )
""")

# Commit changes and close the connection
conn.commit()
conn.close()
```

---

## Inserting Data into the Database

```python
conn = sqlite3.connect("my_database.db")
cursor = conn.cursor()

cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Alice", 25))
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Bob", 30))

conn.commit()
conn.close()
```

---

## Querying Data

```python
conn = sqlite3.connect("my_database.db")
cursor = conn.cursor()

cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()

for row in rows:
    print(row)

conn.close()
```

**Output:**
```
(1, 'Alice', 25)
(2, 'Bob', 30)
```

---

## Updating Data

```python
conn = sqlite3.connect("my_database.db")
cursor = conn.cursor()

cursor.execute("UPDATE users SET age = ? WHERE name = ?", (26, "Alice"))

conn.commit()
conn.close()
```

---

## Deleting Data

```python
conn = sqlite3.connect("my_database.db")
cursor = conn.cursor()

cursor.execute("DELETE FROM users WHERE name = ?", ("Bob",))

conn.commit()
conn.close()
```

---

## Using Parameterized Queries to Prevent SQL Injection

Always use parameterized queries to avoid SQL injection vulnerabilities.

```python
name = input("Enter user name: ")
cursor.execute("SELECT * FROM users WHERE name = ?", (name,))
```

---

## Using SQLAlchemy for Advanced Database Interaction

SQLAlchemy is a popular Python ORM (Object Relational Mapper) that simplifies database interactions.

### Install SQLAlchemy

```bash
pip install sqlalchemy
```

### Using SQLAlchemy with SQLite

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker

# Database setup
engine = create_engine("sqlite:///my_database.db")
Base = declarative_base()

# Define model
class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    age = Column(Integer)

# Create tables
Base.metadata.create_all(engine)

# Add data
Session = sessionmaker(bind=engine)
session = Session()
new_user = User(name="Charlie", age=29)
session.add(new_user)
session.commit()

# Query data
users = session.query(User).all()
for user in users:
    print(user.name, user.age)

session.close()
```

---

## Connecting to MySQL Databases

To connect to MySQL databases, install the connector:

```bash
pip install mysql-connector-python
```

### Example: Connecting to a MySQL Database

```python
import mysql.connector

conn = mysql.connector.connect(
    host="localhost",
    user="root",
    password="yourpassword",
    database="test_db"
)

cursor = conn.cursor()

cursor.execute("SELECT * FROM employees")
for row in cursor.fetchall():
    print(row)

conn.close()
```

---

## Common SQL Commands

| Command        | Description                        |
|----------------|------------------------------------|
| `SELECT`       | Retrieve data from a table        |
| `INSERT`       | Add new records to a table        |
| `UPDATE`       | Modify existing records           |
| `DELETE`       | Remove records from a table       |
| `CREATE TABLE` | Define a new table                |
| `DROP TABLE`   | Delete a table                    |
| `ALTER TABLE`  | Modify a table structure          |
| `JOIN`         | Combine rows from multiple tables |

---

## SQL Joins

SQL joins allow combining data from multiple tables.

### Example:

```sql
SELECT users.name, orders.amount 
FROM users 
JOIN orders ON users.id = orders.user_id;
```

### Types of Joins:

1. **INNER JOIN:** Returns records with matching values in both tables.
2. **LEFT JOIN:** Returns all records from the left table and matching ones from the right.
3. **RIGHT JOIN:** Returns all records from the right table and matching ones from the left.
4. **FULL JOIN:** Returns all records when there is a match in either table.

---

## Using SQLite with Pandas

Python’s Pandas library can interact with SQLite databases for data analysis.

```python
import pandas as pd
import sqlite3

conn = sqlite3.connect("my_database.db")

df = pd.read_sql_query("SELECT * FROM users", conn)
print(df)

conn.close()
```

---

## Best Practices for Using SQL with Python

1. **Use parameterized queries to avoid SQL injection.**
2. **Close connections after queries to free up resources.**
3. **Use ORM like SQLAlchemy for complex applications.**
4. **Normalize database schema to avoid redundancy.**
5. **Index columns used in queries for better performance.**

---

## Practice Exercises

1. Create a Python script to store user information in an SQLite database.
2. Write a query to find users older than 30 from the database.
3. Integrate SQLite with Pandas to analyze the stored data.
4. Use SQLAlchemy to insert, update, and delete records.

---

SQL is a powerful tool for managing data, and integrating it with Python allows for robust, scalable, and efficient data-driven applications.