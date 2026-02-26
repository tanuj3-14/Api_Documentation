# Portfolio Subscription

## Portfolio Subscription Request

> Request Type: `2001` - Subscription Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 2001,
    "connectionId": "<connection-id>"
  },
  "portfolio-id": "stradle-nifty-atm",
  "exchange": "NSEFO",
  "tokens": [
    234567,
    234568
  ],
  "max-new-order": 1000,
  "max-quantity-per-order": 50
}
```

---

## Spread Contract Subscription Request

> Request Type: `2001` - Spread Contract Subscription Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 2001,
    "connectionId": "<connection-id>"
  },
  "portfolio-id": "stradle-nifty-atm",
  "spreadToken": true,
  "exchange": "NSEFO",
  "tokens": [
    [234567, 234568],
    [2334, 5454]
  ],
  "max-new-order": 1000,
  "max-quantity-per-order": 50
}
```
**Max New Order:** Max number of orders for the portfolio \
**Max Qty per order:** Max quantity that can fired per order