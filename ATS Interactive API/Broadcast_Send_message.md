# Broadcast Message

---

## Broadcast Message Request by Group Creator

> Request Type: `1017` - Broadcast Message Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "groupKey": "<group-key>",
    "requestType": 1017
  },
  "broadCastMsg": "<broadcast-message>",
  "broadCastMsgCode": <broadcast-message-code>
}
```

---

## Broadcast Message Response

> Response Type: `1018` - Broadcast Message received by all sessions joined for the group

```json
{
  "ResponseHeader": {
    "groupKey": "<group-key>",
    "responseType": 1018
  },
  "BroadCastMsg": "<broadcast-message>",
  "BroadCastMsgCode": <broadcast-message-code>
}
```