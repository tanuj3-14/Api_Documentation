# Span Margin

---

## Margin Request

> Request Type: `8001` - Margin Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 8001,
    "connectionId": "<connection-id>"
  },
  "exchange": "<exchange-segment>"
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

---

## Margin Response

> Response Type: `8002` - Margin Response

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 8002
  },
  "exchange": "<exchange-segment>",
  "margin": [
    <margin-value>
  ]
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.