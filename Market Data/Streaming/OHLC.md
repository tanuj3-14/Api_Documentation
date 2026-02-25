# OHLC

---

## OHLC Request — Single Token

> HTTP GET Request

```
http://ip:port/ohlc/<exchange-segment>/<instrument-token-id>
```

## OHLC Response — Single Token

```json
{
  "OHLC": [
    {
      "token": <instrument-token-id>,
      "o": <open-price>,
      "h": <high-price>,
      "l": <low-price>,
      "c": <close-price>,
      "v": <volume>,
      "ts": <timestamp>
    }
  ]
}
```

---

## OHLC Request — Multiple Tokens

> HTTP POST Request (maximum 32 tokens per request)

```
http://ip:port/ohlcs
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

## OHLC Response — Multiple Tokens

```json
{
  "OHLC": [
    {
      "token": <instrument-token-id>,
      "o": <open-price>,
      "h": <high-price>,
      "l": <low-price>,
      "c": <close-price>,
      "v": <volume>,
      "ts": <timestamp>
    },
    {
      "token": <instrument-token-id>,
      "o": <open-price>,
      "h": <high-price>,
      "l": <low-price>,
      "c": <close-price>,
      "v": <volume>,
      "ts": <timestamp>
    }
  ]
}
```