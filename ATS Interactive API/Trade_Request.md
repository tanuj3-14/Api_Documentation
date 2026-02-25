# Trade Request

---

## Trade Request

> Request Type: `6001` - Trade Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 6001,
    "connectionId": "<connection-id>"
  },
  "portfolio-id": "<portfolio-id>"
}
```

---

## Trade Response

> Response Type: `6002` - Trade Response

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 6002,
    "tradesCountLeft": <trades-count-left>
  },
  "exchange": "<exchange-segment>",
  "exchangeTimeStamp": <exchange-timestamp>,
  "exchangeOrderId": <exchange-order-id>,
  "atsOrderId": <ats-order-id>,
  "token": <instrument-token-id>,
  "side": <side>,
  "appOrderIdentifier": <app-order-identifier>,
  "errorCode": <error-code>,
  "margin": [
    <margin-value>
  ],
  "type": <order-type>,
  "triggerPrice": "<trigger-price>",
  "portfolio-id": "<portfolio-id>",
  "remainingQuantity": <remaining-quantity>,
  "fillPrice": "<fill-price>",
  "fillQuantity": <fill-quantity>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Side:** `1` - BUY, `2` - SELL

**tradesCountLeft:** `0` - No more trades left, `-1` - No trades available