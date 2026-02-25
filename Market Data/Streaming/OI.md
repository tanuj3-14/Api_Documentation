# Open Interest (OI)

---

## OI Request — Single Token

> HTTP GET Request

```
http://ip:port/oi/<exchange-segment>/<instrument-token-id>
```

## OI Response — Single Token

```json
{
  "OI": [
    {
      "token": <instrument-token-id>,
      "oi": <open-interest>,
      "ts": <timestamp>
    }
  ]
}
```

---

## OI Request — Multiple Tokens

> HTTP POST Request (maximum 32 tokens per request)

```
http://ip:port/ois
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

## OI Response — Multiple Tokens

```json
{
  "OI": [
    {
      "token": <instrument-token-id>,
      "oi": <open-interest>,
      "ts": <timestamp>
    },
    {
      "token": <instrument-token-id>,
      "oi": <open-interest>,
      "ts": <timestamp>
    }
  ]
}
```