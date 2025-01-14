---
layout: default
title: "APIs with requests"
order: 54
---

An API (Application Programming Interface) allows different software systems to communicate with each other. Python's `requests` library is a powerful tool for sending HTTP requests to interact with APIs. It simplifies working with APIs by handling details like making requests, sending data, and parsing responses.

---

## Installing `requests`

First, install the `requests` library using `pip`:

```bash
pip install requests
```

---

## Making a Basic GET Request

A GET request is used to retrieve data from a server. You can make a GET request to an API endpoint using `requests.get()`.

### Example: Fetching Data from an API

```python
import requests

# Make a GET request to a public API
response = requests.get("https://jsonplaceholder.typicode.com/posts")

# Check if the request was successful
if response.status_code == 200:
    data = response.json()  # Parse the JSON data from the response
    print(data)
else:
    print(f"Error: {response.status_code}")
```

### Explanation:
- `requests.get()` makes the request to the specified URL.
- `response.status_code` checks the HTTP status code (e.g., 200 means success).
- `response.json()` converts the returned JSON data into a Python dictionary.

---

## Sending Data with POST Requests

A POST request is used to send data to the server. This is useful for creating or updating resources.

### Example: Sending Data with a POST Request

```python
import requests

# API endpoint
url = "https://jsonplaceholder.typicode.com/posts"

# Data to send (in the form of a dictionary)
data = {
    "title": "New Post",
    "body": "This is a new post.",
    "userId": 1
}

# Make a POST request
response = requests.post(url, json=data)

# Check if the request was successful
if response.status_code == 201:
    print("Post created successfully!")
    print(response.json())  # Print the response data
else:
    print(f"Error: {response.status_code}")
```

### Explanation:
- `requests.post()` sends the data as a JSON object.
- The `json=data` argument automatically converts the dictionary into a JSON format.

---

## Handling Query Parameters

You can pass query parameters in the URL to filter or modify the data requested from the API.

### Example: Sending Query Parameters with GET Request

```python
import requests

# API endpoint with query parameters
url = "https://jsonplaceholder.typicode.com/posts"

# Define query parameters
params = {"userId": 1}

# Make the GET request with query parameters
response = requests.get(url, params=params)

# Check if the request was successful
if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f"Error: {response.status_code}")
```

### Explanation:
- `params` is a dictionary of key-value pairs that get appended to the URL as query parameters.
- For example, `userId=1` will filter the posts to only show those by user 1.

---

## Handling Errors

APIs may return error messages if something goes wrong. Use `response.status_code` to check for errors and handle them accordingly.

### Example: Handling Errors

```python
import requests

# Make a GET request to a non-existent endpoint
response = requests.get("https://jsonplaceholder.typicode.com/invalid-endpoint")

if response.status_code == 200:
    print(response.json())
else:
    print(f"Error {response.status_code}: {response.text}")
```

### Explanation:
- `response.status_code` helps you check if the request was successful.
- `response.text` contains the error message returned by the API.

---

## Key Takeaways

1. **GET Requests**: Used to retrieve data from an API.
2. **POST Requests**: Used to send data to an API.
3. **Handling Responses**: Use `response.status_code` and `response.json()` to handle and process data.
4. **Error Handling**: Check `status_code` to handle any issues in the response.

---

In the next lesson, we’ll explore the basics of version control with Git.
