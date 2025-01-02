---
layout: default
title: "FastAPI REST APIs"
order: 88
---

FastAPI is a modern framework for building APIs with Python.

### Installing FastAPI

Install FastAPI and a server:

```plaintext
pip install fastapi uvicorn
```

### Building a Simple FastAPI Application

Example:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, FastAPI!"}

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str = None):
    return {"item_id": item_id, "query": q}

if __name__ == "__main__":
    import uvicorn
    uvicorn.run(app, host="127.0.0.1", port=8000)
```

### Expected Output

When you visit `http://127.0.0.1:8000`, you'll see:

```plaintext
{"message": "Hello, FastAPI!"}
```

FastAPI is efficient for creating production-ready APIs.
