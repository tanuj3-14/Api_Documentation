# Subscription

---

## Subscription Request

> Request Type: `20001` - Subscription Request

```json
{
  "RequestHeader": {
    "userId": "<user-id>",
    "apiKey": "<api-key>",
    "connectionId": "<connection-id>",
    "requestType": 20001
  },
  "exchange": "<exchange-segment>",
  "portfolio-id": "<portfolio-id>",
  "tokens": [
    <instrument-token-id>
  ]
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, `BSEFO`, etc.

---

## Book Depth Streaming Response

> Response Type: `20003` - Book Depth Streaming Response (every 1 second)

```json
{
  "ResponseHeader": {
    "responseType": 20003
  },
  "TOUCHLINE": [
    {
      "token": <instrument-token-id>,
      "ltp": <ltp>,
      "totalBuyQty": <total-buy-quantity>,
      "totalSellQty": <total-sell-quantity>,
      "prevClosePrice": <previous-close-price>,
      "exchange": "<exchange-segment>",
      "ts": <timestamp>
    },
    [
      {
        "bidP": <bid-price-1>,
        "askP": <ask-price-1>,
        "bidQ": <bid-quantity-1>,
        "askQ": <ask-quantity-1>
      },
      {
        "bidP": <bid-price-2>,
        "askP": <ask-price-2>,
        "bidQ": <bid-quantity-2>,
        "askQ": <ask-quantity-2>
      },
      {
        "bidP": <bid-price-3>,
        "askP": <ask-price-3>,
        "bidQ": <bid-quantity-3>,
        "askQ": <ask-quantity-3>
      },
      {
        "bidP": <bid-price-4>,
        "askP": <ask-price-4>,
        "bidQ": <bid-quantity-4>,
        "askQ": <ask-quantity-4>
      },
      {
        "bidP": <bid-price-5>,
        "askP": <ask-price-5>,
        "bidQ": <bid-quantity-5>,
        "askQ": <ask-quantity-5>
      }
    ]
  ]
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, `BSEFO`, etc.

> `TOUCHLINE` contains a touchline object followed by an array of 5 bid/ask depth levels.

---

## Candle Streaming Response

> Response Type: `20002` - Candle Streaming Response (every 1 minute)

```json
{
  "ResponseHeader": {
    "responseType": 20002
  },
  "CANDLE": [
    {
      "token": <instrument-token-id>,
      "ltp": <ltp>,
      "open": <open-price>,
      "high": <high-price>,
      "low": <low-price>,
      "close": <close-price>,
      "volume": <volume>,
      "exchange": "<exchange-segment>",
      "ts": <timestamp>,
      "OI": <open-interest>
    }
  ]
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, `BSEFO`, etc.