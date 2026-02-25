# Open Order Request

---

## Open Order Request

> Request Type: `9001` - Open Order Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "requestType": 9001
  }
}
```

---

## Open Order Response

> Response Type: `9002` - Open Order Response (multiple responses until `openOrderCountLeft` becomes `0`)

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 9002,
    "openOrderCountLeft": 4
  },
  "exchange": "<exchange-segment>",
  "price": "<price>",
  "exchangeTimeStamp": <exchange-timestamp>,
  "exchangeOrderId": <exchange-order-id>,
  "atsOrderId": <ats-order-id>,
  "token": <instrument-token-id>,
  "side": <side>,
  "appOrderIdentifier": <incremental-number-starting-with-000001>,
  "errorCode": <error-code>,
  "portfolio-id": "<portfolio-id>",
  "remainingQuantity": <remaining-quantity>,
  "order-type": <order-type>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, `BSEFO`, etc.

**Order Types:** `1` - LIMIT, `3` - IOC, `4` - SL

**Side:** `1` - BUY, `2` - SELL

**openOrderCountLeft:** Decrements with each response; `0` indicates the last response