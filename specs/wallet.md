# Wallet (in 3bot itself)

## Assumptions
- The default wallet shares it key with the 3bot itself
- TODO: add default wallet, not no wallet
- Doing trades is not specific to one wallet, it uses all wallets to do possible exchanges. Need work on this
## Architecture


## Functionality

![Initialize mockups](./images/tbotWallet1.png)

 * Add / upload wallet
 * Buy tft
 * Sell tft
 * View open orders
 * View order history
 * Cancel open orders

 * Overview wallets
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





