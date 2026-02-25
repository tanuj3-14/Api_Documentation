# Session Login

## Overview

The Session Login process allows you to establish a WebSocket connection to the ATS Execution Service and manage session login and logout requests.

## WebSocket Connection

To establish a WebSocket connection with the ATS Execution Service, use the following URL:
```json
ws://execution-streaming-service-ip:port

---

## Body of Request and Response:

### Session Login Request (1001 - Login Request)

```json
{
    "RequestHeader": {
        "userId": "<user-id>",
        "apiKey": "<api-key>",
        "requestType": 1001
    }
}