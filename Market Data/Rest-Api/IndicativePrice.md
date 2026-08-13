# Indicative Price

---

## Indicative Price Request — Single Token

> HTTP GET Request

```
http://ip:port/indicativePrice/<exchange-segment>/<instrument-token-id>
```

## Indicative Price Response — Single Token

```json
{
  "INDICATIVEPRICE": [
    {
      "token": <instrument-token-id>,
      "indicativePrice": <indicative-price>,
      "ts": <timestamp>
    }
  ]
}
```

---

## Indicative Price Request — Multiple Tokens

> HTTP POST Request (maximum 32 tokens per request)

```
http://ip:port/indicativePrices
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

## Indicative Price Response — Multiple Tokens

```json
{
  "INDICATIVEPRICE": [
    {
      "token": <instrument-token-id>,
      "indicativePrice": <indicative-price>,
      "ts": <timestamp>
    },
    {
      "token": <instrument-token-id>,
      "indicativePrice": <indicative-price>,
      "ts": <timestamp>
    }
  ]
}
```