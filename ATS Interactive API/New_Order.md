# New Order

---

## New Order Entry

> Request Type: `3001` - New Order Entry Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 3001,
    "connectionId": "<connection-id>"
  },
  "exchange": "<exchange-segment>",
  "token": "<instrument-token-id>",
  "order-type": <order-type>,
  "triggerPrice": "<trigger-price>",
  "side": <side>,
  "quantity": <quantity>,
  "price": "<price>",
  "portfolio-id": "stradle-nifty-atm",
  "appOrderIdentifier": <incremental-number-starting-with-000001>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Order Types:** `1` - LIMIT, `3` - IOC, `4` - SL

> `triggerPrice` is required only for order type `4` (SL)

**Side:** `1` - BUY, `2` - SELL

**appOrderIdentifier:** Unique incremental number throughout the session, starting with `000001`

---

## Response - Order Confirmation

> Response Type: `3002` - Order Confirmation

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 3002
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
  "price": "<price>",
  "quantity": <quantity>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Side:** `1` - BUY, `2` - SELL

**appOrderIdentifier:** Unique incremental number throughout the session, starting with `000001`

---

## Response - Cancel Confirmation

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

**Side:** `1` - BUY, `2` - SELL

---

## Response - Trade Confirmation

> Response Type: `4002` - Trade Confirmation

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 4002
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

---

## Response - New Order Reject

> Response Type: `3004` - New Order Reject

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "responseType": 3004
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
  "price": "<price>",
  "quantity": <quantity>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**Side:** `1` - BUY, `2` - SELL

