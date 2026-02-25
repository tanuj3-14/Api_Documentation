# Session Login

## Overview

The Session Login process allows you to establish a WebSocket connection to the ATS Execution Service and manage session login and logout requests.

## WebSocket Connection

To establish a WebSocket connection with the ATS Execution Service, use the following URL:

`ws://execution-streaming-service-ip:port`

---

## Body of Request and Response

### Session Login Request

> Request Types: `1001` - Login Request, `1003` - Logout Request, `1005` - UI Login Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 1001
  }
}
```

### Session Login Response

> Response Types: `1002` - Login Response, `1004` - Logout Response, `1006` - UI Login Response

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<unique-connection-id>",
    "responseType": 1002,
    "status": 1
  }
}
```

**Status Codes:** `1` - Success, `0` - Failure