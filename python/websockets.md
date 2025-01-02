---
layout: default
title: "WebSockets"
order: 93
---

The `websockets` library allows real-time communication with WebSocket servers.

### Installing websockets

Install with pip:

```plaintext
pip install websockets
```

### Creating a WebSocket Client

Example:

```python
import asyncio
import websockets

async def hello():
    async with websockets.connect("ws://example.com/socket") as websocket:
        await websocket.send("Hello, Server!")
        response = await websocket.recv()
        print("Response from server:", response)

asyncio.run(hello())
```

### Expected Output

```plaintext
Response from server: (depends on server response)
```

WebSockets are great for real-time communication in Python.
