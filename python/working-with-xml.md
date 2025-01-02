---
layout: default
title: "Working with XML"
order: 86
---

Python provides libraries like `xml.etree.ElementTree` for working with XML.

### Parsing an XML File

Example:

```python
import xml.etree.ElementTree as ET

xml_data = '''<data>
    <item>
        <name>Alice</name>
        <age>25</age>
    </item>
</data>'''

root = ET.fromstring(xml_data)
for item in root.findall("item"):
    name = item.find("name").text
    age = item.find("age").text
    print(f"Name: {name}, Age: {age}")
```

### Expected Output

```plaintext
Name: Alice, Age: 25
```

The `xml` module makes it simple to parse and manipulate XML data.
