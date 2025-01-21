---
title: "APIs and Requests"
order: 31
---

# APIs and Requests

APIs (Application Programming Interfaces) allow applications to communicate with each other. In Python, the **`requests`** library is commonly used to interact with APIs for sending HTTP requests and receiving responses.

---

## Installing the `requests` Library
The `requests` library is not included in Python's standard library. Install it using `pip`:

```bash
pip install requests
```

---

## Basic HTTP Methods

### Sending a GET Request
```python
import requests

response = requests.get("https://jsonplaceholder.typicode.com/posts/1")
print(response.status_code)  # Output: 200 (HTTP status code)
print(response.json())       # Output: JSON data from the API
```

### Sending a POST Request
```python
data = {"title": "New Post", "body": "This is the content.", "userId": 1}
response = requests.post("https://jsonplaceholder.typicode.com/posts", json=data)

print(response.status_code)  # Output: 201 (Created)
print(response.json())       # Output: Newly created resource
```

### Other HTTP Methods
- **PUT**: Update a resource.
- **DELETE**: Remove a resource.

```python
# PUT request
response = requests.put("https://jsonplaceholder.typicode.com/posts/1", json={"title": "Updated Title"})
print(response.json())

# DELETE request
response = requests.delete("https://jsonplaceholder.typicode.com/posts/1")
print(response.status_code)  # Output: 200 (Success)
```

---

## Response Object

The response object returned by `requests` contains useful attributes:

```python
response = requests.get("https://jsonplaceholder.typicode.com/posts/1")

print(response.text)         # Raw response content
print(response.json())       # Parsed JSON data
print(response.status_code)  # HTTP status code
print(response.headers)      # Response headers
```

---

## Handling Query Parameters

Use the `params` argument to send query parameters in a GET request.

```python
params = {"userId": 1}
response = requests.get("https://jsonplaceholder.typicode.com/posts", params=params)

print(response.url)          # Output: URL with query parameters
print(response.json())       # Filtered JSON data
```

---

## Sending Headers

Add custom headers to your request.

```python
headers = {"Authorization": "Bearer YOUR_TOKEN_HERE"}
response = requests.get("https://api.example.com/resource", headers=headers)

print(response.status_code)
```

---

## Error Handling

### Check for Errors
Use `response.raise_for_status()` to raise an exception for HTTP errors.

```python
try:
    response = requests.get("https://jsonplaceholder.typicode.com/invalid-endpoint")
    response.raise_for_status()
except requests.exceptions.HTTPError as e:
    print("HTTP error:", e)
except requests.exceptions.RequestException as e:
    print("Error:", e)
```

---

## Advanced Topics

### Timeout
Set a timeout to avoid hanging requests.

```python
try:
    response = requests.get("https://jsonplaceholder.typicode.com/posts", timeout=5)
    print(response.json())
except requests.exceptions.Timeout:
    print("Request timed out")
```

### Session Objects
Reuse connections with a session object.

```python
session = requests.Session()
session.headers.update({"Authorization": "Bearer YOUR_TOKEN_HERE"})

response = session.get("https://api.example.com/resource")
print(response.json())
```

---

## Practical Examples

### Get Weather Data
```python
api_key = "YOUR_API_KEY"
city = "London"
url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}"

response = requests.get(url)
if response.status_code == 200:
    weather = response.json()
    print(f"Temperature: {weather['main']['temp']}K")
else:
    print("Failed to fetch weather data")
```

### Search GitHub Repositories
```python
url = "https://api.github.com/search/repositories"
params = {"q": "requests language:python", "sort": "stars"}
response = requests.get(url, params=params)

if response.status_code == 200:
    data = response.json()
    for repo in data["items"][:5]:
        print(repo["name"], "-", repo["html_url"])
```

---

## Best Practices

1. **Use Environment Variables**:
   - Store API keys and sensitive data in environment variables instead of hardcoding them.

2. **Handle Errors Gracefully**:
   - Always check the response status code and handle exceptions.

3. **Rate Limiting**:
   - Respect API rate limits to avoid being blocked.

4. **Use Secure Connections**:
   - Always use HTTPS for secure communication.

---

## Practice Exercises

1. **Simple GET Request**:
   - Fetch posts from `https://jsonplaceholder.typicode.com/posts` and display the titles.

2. **Weather API**:
   - Write a program that fetches weather data for a user-specified city.

3. **POST Request**:
   - Send a POST request to create a new resource and verify the response.

4. **Error Handling**:
   - Make a request to an invalid endpoint and handle the resulting error.

APIs are a powerful way to interact with external services and exchange data. Understanding how to use the `requests` library effectively will unlock endless possibilities for building dynamic applications.