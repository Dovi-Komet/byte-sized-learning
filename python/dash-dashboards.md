---
layout: default
title: "Dash Dashboards"
order: 94
---

Dash is a Python framework for creating interactive web dashboards.

### Installing Dash

Install with pip:

```plaintext
pip install dash
```

### Creating a Basic Dashboard

Example:

```python
from dash import Dash, html

app = Dash(__name__)

app.layout = html.Div([
    html.H1("Welcome to My Dashboard"),
    html.P("This is a simple dashboard.")
])

if __name__ == "__main__":
    app.run_server(debug=True)
```

### Expected Output

Visit `http://127.0.0.1:8050` in your browser to view the dashboard.

Dash makes building data-driven dashboards simple and effective.
