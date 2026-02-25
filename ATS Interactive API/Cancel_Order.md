# Cancel Order

---

## Cancel Order Request

> Request Type: `3021` - Cancel Order Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 3021,
    "connectionId": "<connection-id>"
  },
  "exchange": "<exchange-segment>",
  "token": <instrument-token-id>,
  "side": <side>,
  "order-type": <order-type>,
  "quantity": <quantity>,
  "price": "<price>",
  "portfolio-id": "far-otm-pe",
  "appOrderIdentifier": <app-order-identifier>,
  "exchangeOrderId": <exchange-order-id>,
  "atsOrderId": <ats-order-id>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Order Types:** `1` - LIMIT, `3` - IOC, `4` - SL

**Side:** `1` - BUY, `2` - SELL

---

## Cancel Confirmation

> Response Type: `3003` - Cancel Confirmation

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 3003
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
  "price": "<price>",
  "quantity": <quantity>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Order Types:** `1` - LIMIT, `3` - IOC, `4` - SL

**Side:** `1` - BUY, `2` - SELL

---

## Cancel Reject

> Response Type: `3024` - Cancel Reject

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 3024
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
  "price": "<price>",
  "quantity": <quantity>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Order Types:** `1` - LIMIT, `3` - IOC, `4` - SL

**Side:** `1` - BUY, `2` - SELL