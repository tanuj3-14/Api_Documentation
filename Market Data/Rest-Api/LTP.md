# Last Traded Price

---

## LTP Request — Single Token



```
http://ip:port/ltp/<exchange-segment>/<instrument-token-id>
```

## LTP Response — Single Token

```json
{
  "LTP": [
    {
      "token": <instrument-token-id>,
      "ltp": <last-traded-price>,
      "ts": <timestamp>
    }
  ]
}
```

---

## LTP Request — Multiple Tokens


```
http://ip:port/ltps
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

## LTP Response — Multiple Tokens

```json
{
  "LTP": [
    {
      "token": <instrument-token-id>,
      "ltp": <last-traded-price>,
      "ts": <timestamp>
    },
    {
      "token": <instrument-token-id>,
      "ltp": <last-traded-price>,
      "ts": <timestamp>
    }
  ]
}
```