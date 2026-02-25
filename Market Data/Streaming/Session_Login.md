# Mkt Data Session Login

## WebSocket Connection

To establish a WebSocket connection with the ATS Mkt Data Streaming Service, use the following URL:

`ws://mkt-data-streaming-service-ip:port`

---

## Mkt Data Login Request

> Request Type: `10001` - Mkt Data Login Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 10001
  }
}
```

---

## Mkt Data Login Response

> Response Type: `10002` - Mkt Data Login Response

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 10002,
    "status": <status>
  }
}
```

**Status Codes:** `1` - Success, `0` - Failure