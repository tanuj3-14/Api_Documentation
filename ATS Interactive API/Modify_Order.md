# Modify Order

---

## Modify Order Request

> Request Type: `3011` - Modify Order Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 3011,
    "connectionId": "<connection-id>"
  },
  "exchange": "<exchange-segment>",
  "token": <instrument-token-id>,
  "triggerPrice": "<trigger-price>",
  "side": <side>,
  "order-type": <order-type>,
  "modifiedQuantity": <quantity>,
  "modifiedPrice": "<price>",
  "portfolio-id": "stradle-nifty-atm",
  "appOrderIdentifier": <incremental-number-starting-with-000001>,
  "exchangeOrderId": <exchange-order-id>,
  "atsOrderId": <ats-order-id>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Order Types:** `1` - LIMIT, `3` - IOC, `4` - SL

**Side:** `1` - BUY, `2` - SELL

> `triggerPrice` is required only for order type `4` (SL)

---

## Response - Modify Confirmed

> Response Type: `3012` - Modify Confirmed

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 3012
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
  "modifiedQuantity": <modified-quantity>,
  "modifiedPrice": "<modified-price>"
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Order Types:** `1` - LIMIT, `3` - IOC, `4` - SL

**Side:** `1` - BUY, `2` - SELL

---

## Response - Modify Reject

> Response Type: `3014` - Modify Reject

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 3014
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
  "modifiedQuantity": <modified-quantity>,
  "modifiedPrice": "<modified-price>"
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Side:** `1` - BUY, `2` - SELL

