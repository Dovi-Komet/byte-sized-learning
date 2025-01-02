---
layout: default
title: "Task Automation"
order: 82
---

Selenium is a library for automating web browser interactions.

### Installing Selenium

Install using pip:

```plaintext
pip install selenium
```

### Automating a Simple Task

Example:

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()  # Ensure you have the ChromeDriver installed
driver.get("https://example.com")
print(driver.title)
driver.quit()
```

### Expected Output

```plaintext
Example Domain
```

Selenium is useful for testing and automating web applications.
