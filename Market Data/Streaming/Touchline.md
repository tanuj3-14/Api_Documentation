# Touch Line

---

## Touch Line Request — Single Token

> HTTP GET Request

```
http://ip:port/touchline/<exchange-segment>/<instrument-token-id>
```

## Touch Line Response — Single Token

```json
{
  "TouchLine": [
    {
      "token": <instrument-token-id>,
      "bid": <bid-price>,
      "ask": <ask-price>,
      "bidQ": <bid-quantity>,
      "askQ": <ask-quantity>,
      "ts": <timestamp>
    }
  ]
}
```

---

## Touch Line Request — Multiple Tokens

> HTTP POST Request (maximum 32 tokens per request)

```
http://ip:port/touchlines
```

```json
{
  "exchange": "<exchange-segment>",
  "tokens": [
    <instrument-token-id>,
    <instrument-token-id>
  ]
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, `BSEFO`, etc.

## Touch Line Response — Multiple Tokens

```json
{
  "TouchLine": [
    {
      "token": <instrument-token-id>,
      "bid": <bid-price>,
      "ask": <ask-price>,
      "bidQ": <bid-quantity>,
      "askQ": <ask-quantity>,
      "ts": <timestamp>
    },
    {
      "token": <instrument-token-id>,
      "bid": <bid-price>,
      "ask": <ask-price>,
      "bidQ": <bid-quantity>,
      "askQ": <ask-quantity>,
      "ts": <timestamp>
    }
  ]
}
```