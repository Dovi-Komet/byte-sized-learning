---
layout: default
title: "Flask REST APIs"
order: 87
---

Flask is a micro web framework for building web applications and APIs.

### Installing Flask

Install using pip:

```plaintext
pip install flask
```

### Creating a Simple REST API

Example:

```python
from flask import Flask, jsonify

app = Flask(__name__)

@app.route('/api', methods=['GET'])
def api():
    return jsonify({"message": "Hello, World!"})

if __name__ == "__main__":
    app.run(debug=True)
```

### Expected Output

When you visit `http://127.0.0.1:5000/api`, you'll see:

```plaintext
{"message": "Hello, World!"}
```

Flask is ideal for quickly building small web applications and APIs.
