# Portfolio List Request

---

## Portfolio List Request

> Request Type: `7003` - Portfolio List Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 7003,
    "connectionId": "<connection-id>"
  }
}
```

---

## Portfolio List Response

> Response Type: `7004` - Portfolio List Response

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "responseType": 7004,
    "connectionId": "<connection-id>"
  },
  "portfolio-list": [
    "<portfolio-id-1>",
    "<portfolio-id-2>"
  ]
}
```