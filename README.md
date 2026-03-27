# Chainstock Exchange API Documentation

**Base URL:** `https://api.chainstock.org`

---

## Summary

Returns market summary for all trading pairs.

**Endpoint:** `GET /api/currency/summary`

**Response Example:**
```json
{
  "success": true,
  "data": {
    "CS_USDT": {
      "base_id": 1,
      "base_name": "Chainstock",
      "base_symbol": "CS",
      "quote_id": 101,
      "quote_name": "Tether",
      "quote_symbol": "USDT",
      "last_price": "0.27200000",
      "base_volume": "2841891.06",
      "quote_volume": "783240.56",
      "isFrozen": 0
    }
  }
}
```

---

## Ticker

Returns ticker data for all trading pairs.

**Endpoint:** `GET /api/currency/ticker`

**Response Example:**
```json
{
  "success": true,
  "data": {
    "CS_USDT": {
      "last_price": "0.27200000",
      "base_volume": "2841891.06",
      "quote_volume": "783240.56",
      "isFrozen": 0
    }
  }
}
```

---

## Trades

Returns recent trades for a trading pair.

**Endpoint:** `GET /api/currency/trades?market_pair={market_pair}`

**Parameters:**
| Name | Type | Required | Description |
|------|------|----------|-------------|
| market_pair | string | Yes | e.g. `CS_USDT` |

**Response Example:**
```json
{
  "success": true,
  "data": [
    {
      "trade_id": 414,
      "price": "0.27200000",
      "base_volume": "100.00",
      "target_volume": "27.20",
      "timestamp": 1774622587,
      "type": "buy"
    }
  ]
}
```

---

## Orderbook

Returns current orderbook for a trading pair.

**Endpoint:** `GET /api/currency/orderbook?market_pair={market_pair}`

**Parameters:**
| Name | Type | Required | Description |
|------|------|----------|-------------|
| market_pair | string | Yes | e.g. `CS_USDT` |

**Response Example:**
```json
{
  "success": true,
  "data": {
    "timestamp": 1774622587,
    "bids": [
      ["0.27100000", "500.00"],
      ["0.27000000", "1000.00"]
    ],
    "asks": [
      ["0.27300000", "300.00"],
      ["0.27400000", "800.00"]
    ]
  }
}
```

---

## Supported Trading Pairs

| Pair | Base | Quote |
|------|------|-------|
| CS_USDT | CS (Chainstock) | USDT |

---

*For support, contact: support@chainstock.org*
