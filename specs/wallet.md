# Wallet (in 3bot itself)

## Architecture

![Android app architecture](./images/androidapp.svg)

## Functionality

![Initialize mockups](./images/tbotWallet1.png)

 * Add / upload wallet
 * Buy tft
 * Sell tft
 * view open orders
 * view order history

 * Overiew wallets
 * Orders
 * Order history


## User stories

### As a user, Show your wallets

![Initialize mockups](./images/tbotWallet2.png)

GET /tfgrid/3bot/{doublename}/wallets

```
{
    [
        {"CoinName": "Bitcoin",
        "CoinAbbreviation": "BTC'
        "Amount":"1.31",
        "Address":"asdfqawfwqaf",
        },
        {"CoinName": "Threefold token",
        "CoinAbbreviation": "TFT'
        "Amount":"13100",
        "Address":"asfqfqfnjutyd"
        }
    ]
}
```

### As a user, Show your open orders

GET /tfgrid/3bot/{doublename}/orders

```
{
    [
        {
            "CoinSellName": "Bitcoin",
            "CoinSellAbbreviation": "BTC'
            "CoinSellAmountAmount":"1.31",
            "CoinBuyName": "Threefoldtoken",
            "CoinBuyAbbreviation": "TFT'
            "CoinBuyAmountAmount":"1310000",
        },
        {
            "CoinSellName": "Bitcoin",
            "CoinSellAbbreviation": "BTC'
            "CoinSellAmountAmount":"1.61",
            "CoinBuyName": "Threefoldtoken",
            "CoinBuyAbbreviation": "TFT'
            "CoinBuyAmountAmount":"1510000",
        }
    ]
}
```

### As a user, Show your order history


GET /tfgrid/3bot/{doublename}/orderHistofy

```
{
    [
        {
            "CoinSellName": "Bitcoin",
            "CoinSellAbbreviation": "BTC'
            "CoinSellAmountAmount":"1.31",
            "CoinBuyName": "Threefoldtoken",
            "CoinBuyAbbreviation": "TFT'
            "CoinBuyAmountAmount":"1310000",
        },
        {
            "CoinSellName": "Bitcoin",
            "CoinSellAbbreviation": "BTC'
            "CoinSellAmountAmount":"1.61",
            "CoinBuyName": "Threefoldtoken",
            "CoinBuyAbbreviation": "TFT'
            "CoinBuyAmountAmount":"1510000",
        }
    ]
}
```

### As a user, Buy btc





