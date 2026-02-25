# Position Request

---

## Position Request

> Request Type: `7001` - Position Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "requestType": 7001,
    "connectionId": "<connection-id>"
  },
  "portfolio-id": "<portfolio-id>"
}
```

---

## Position Response

> Response Type: `7002` - Position Response

```json
{
  "ResponseHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "responseType": 7002,
    "connectionId": "<connection-id>",
    "positionCountLeft": <position-count-left>
  },
  "exchange": "<exchange-segment>",
  "token": <instrument-token-id>,
  "portfolio-id": "<portfolio-id>",
  "totalBuyQuantity": <total-buy-quantity>,
  "AvgBuyPrice": "<avg-buy-price>",
  "totalSellQuantity": <total-sell-quantity>,
  "AvgSellPrice": "<avg-sell-price>",
  "netQuantity": <net-quantity>
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, etc.

**positionCountLeft:** `0` - Last position response