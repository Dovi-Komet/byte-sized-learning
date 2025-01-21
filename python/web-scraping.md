---
title: "Web Scraping"
order: 37
---

# Web Scraping with Python

Web scraping is the process of extracting data from websites automatically. Python provides several powerful libraries for web scraping, such as `BeautifulSoup`, `requests`, and `Selenium`.

---

## When to Use Web Scraping

Web scraping is useful for:

1. **Data Collection:** Gathering information for analysis (e.g., stock prices, news articles).
2. **Monitoring Websites:** Tracking changes on competitors' sites.
3. **Automation:** Extracting repetitive data without manual effort.
4. **Data Aggregation:** Collecting data from multiple sources into a single repository.

**Important:** Always check a website's `robots.txt` file and terms of service before scraping.

---

## Setting Up the Environment

Install the required libraries:

```bash
pip install requests beautifulsoup4 lxml
```

---

## Using `requests` to Fetch Web Pages

The `requests` library is used to download web pages as HTML.

```python
import requests

url = "https://example.com"
response = requests.get(url)

if response.status_code == 200:
    print(response.text[:500])  # Print first 500 characters of the page
else:
    print(f"Failed to retrieve page, status code: {response.status_code}")
```

### Handling Common Issues:

- **Headers:** Some websites block requests without headers.
  
  ```python
  headers = {"User-Agent": "Mozilla/5.0"}
  response = requests.get(url, headers=headers)
  ```

- **Timeouts:** Avoid hanging requests.

  ```python
  response = requests.get(url, timeout=10)
  ```

---

## Parsing HTML with BeautifulSoup

`BeautifulSoup` helps extract data from HTML content.

```python
from bs4 import BeautifulSoup

html_content = "<html><body><h1>Hello, World!</h1></body></html>"
soup = BeautifulSoup(html_content, "html.parser")

print(soup.h1.text)  # Output: Hello, World!
```

### Extracting Elements

```python
response = requests.get("https://example.com")
soup = BeautifulSoup(response.text, "html.parser")

# Find elements
title = soup.find("title").text
all_links = soup.find_all("a")

print("Page Title:", title)
for link in all_links:
    print("Link:", link.get('href'))
```

---

## Navigating the HTML Structure

BeautifulSoup provides methods to navigate through the HTML structure:

- `soup.title.text` – Gets the text of the `<title>` tag.
- `soup.find("div", class_="content")` – Finds a `<div>` with a specific class.
- `soup.find_all("p")` – Finds all paragraph tags.

Example:

```python
content = soup.find("div", {"id": "main-content"})
paragraphs = content.find_all("p")

for p in paragraphs:
    print(p.text)
```

---

## Handling Pagination

Many websites display data across multiple pages. You can scrape multiple pages using loops.

```python
base_url = "https://example.com/page="
for page in range(1, 6):
    url = f"{base_url}{page}"
    response = requests.get(url)
    soup = BeautifulSoup(response.text, "html.parser")
    print(soup.title.text)
```

---

## Scraping Tables

Web pages often contain structured data in tables.

```python
import pandas as pd

table = soup.find("table")
rows = table.find_all("tr")

data = []
for row in rows:
    cols = row.find_all("td")
    data.append([col.text.strip() for col in cols])

df = pd.DataFrame(data, columns=["Column1", "Column2"])
print(df)
```

---

## Web Scraping with Selenium

For dynamic websites that rely on JavaScript, Selenium can be used to interact with the page.

### Installation:

```bash
pip install selenium webdriver-manager
```

### Example:

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from webdriver_manager.chrome import ChromeDriverManager

driver = webdriver.Chrome(ChromeDriverManager().install())

driver.get("https://example.com")
print(driver.title)

element = driver.find_element(By.TAG_NAME, "h1")
print(element.text)

driver.quit()
```

### Interacting with Elements:

- Clicking buttons: `element.click()`
- Typing into fields: `element.send_keys("Python")`
- Submitting forms: `element.submit()`

---

## Handling Common Challenges

1. **Dynamic Content:** Use Selenium or wait for JavaScript to load.
2. **CAPTCHAs:** Some sites block bots with CAPTCHAs.
3. **IP Blocking:** Rotate proxies or use a delay between requests.
4. **Session Handling:** Use cookies and authentication tokens.

---

## Ethical Web Scraping Guidelines

1. **Respect `robots.txt`:** Check if scraping is allowed.
2. **Avoid Overloading Servers:** Use delays between requests.
3. **Give Credit:** Respect data ownership and licensing.
4. **Don't Harvest Personal Data:** Ensure compliance with regulations like GDPR.

Example of checking `robots.txt`:

```python
response = requests.get("https://example.com/robots.txt")
print(response.text)
```

---

## Storing Scraped Data

Once data is extracted, it can be stored in various formats:

- **CSV File:**
  
  ```python
  import csv

  with open("data.csv", "w", newline="") as f:
      writer = csv.writer(f)
      writer.writerow(["Name", "Price"])
      writer.writerow(["Item1", "$10"])
  ```

- **JSON File:**
  
  ```python
  import json

  data = {"name": "Item1", "price": "$10"}
  with open("data.json", "w") as f:
      json.dump(data, f)
  ```

- **Database (SQLite Example):**
  
  ```python
  import sqlite3

  conn = sqlite3.connect("data.db")
  c = conn.cursor()
  c.execute("CREATE TABLE IF NOT EXISTS products (name TEXT, price TEXT)")
  c.execute("INSERT INTO products VALUES ('Item1', '$10')")
  conn.commit()
  conn.close()
  ```

---

## Practice Exercises

1. Scrape the titles of articles from a news website.
2. Extract product names and prices from an e-commerce website.
3. Use Selenium to interact with a login form and scrape data post-login.
4. Store scraped data in a CSV file.

---

## Summary

- **requests**: Fetch web pages.
- **BeautifulSoup**: Parse HTML and extract data.
- **Selenium**: Handle dynamic web pages.
- **Ethics**: Always follow best practices to avoid legal issues.

With these tools, you can automate data extraction and build powerful data-driven applications.