# Reference Price

---

## Reference Price Request — Single Token

> HTTP GET Request

```
http://ip:port/referencePrice/<exchange-segment>/<instrument-token-id>
```

## Reference Price Response — Single Token

```json
{
  "REFERENCEPRICE": [
    {
      "token": <instrument-token-id>,
      "referencePrice": <reference-price>,
      "ts": <timestamp>
    }
  ]
}
```

---

## Reference Price Request — Multiple Tokens

> HTTP POST Request (maximum 32 tokens per request)

```
http://ip:port/referencePrices
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

## Reference Price Response — Multiple Tokens

```json
{
  "REFERENCEPRICE": [
    {
      "token": <instrument-token-id>,
      "referencePrice": <reference-price>,
      "ts": <timestamp>
    },
    {
      "token": <instrument-token-id>,
      "referencePrice": <reference-price>,
      "ts": <timestamp>
    }
  ]
}
```