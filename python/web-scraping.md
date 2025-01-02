---
layout: default
title: "Web Scraping"
order: 74
---

`BeautifulSoup` is a library for web scraping.

### Installing BeautifulSoup

Install using pip:

```plaintext
pip install beautifulsoup4 requests
```

### Basic Scraping

Example:

```python
import requests
from bs4 import BeautifulSoup

response = requests.get("https://example.com")
soup = BeautifulSoup(response.text, "html.parser")

print(soup.title.string)
```

### Expected Output (example site content)

```plaintext
Example Domain
```

Web scraping allows you to extract data from websites programmatically.
