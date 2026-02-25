# LPP

---

## LPP Request — Single Token

```
http://ip:port/lpp/<exchange-segment>/<instrument-token-id>
```

## LPP Response — Single Token

```json
{
  "LPP": [
    {
      "token": <instrument-token-id>,
      "lppHigh": <lpp-high>,
      "lppLow": <lpp-low>,
      "ts": <timestamp>
    }
  ]
}
```

**Exchange Segments:** `NSEFO`, `NSECM`, `BSEFO`, etc.