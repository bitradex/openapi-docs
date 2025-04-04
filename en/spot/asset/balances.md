# Get a list of currency assets

`GET` /v1/spot/balances

## Request Parameters

| name         | location    | type     | required | Description          |
|------------|-------|--------|----|-------------|
| currencies | query | string | No  | coin：usdt,btc |

> Request Example

```shell
curl --location --request GET 'https://api.bitradex.com/v1/spot/balances?currencies=usdt&filterIsDisplayFalse=false' \
--header 'validate-algorithms: HmacSHA256' \
--header 'validate-appkey: 2fa91add-388c-44f2-8365-f4b72886c135' \
--header 'validate-recvwindow: 6000' \
--header 'validate-timestamp: 1725531972816' \
--header 'validate-signature: 6ad1d98c3ee09fd78035340e2946bd14b0ce61251da58b546d955bba258c63d6' \
--header 'Accept: */*' \
--header 'Host: api.bitradex.com' \
--header 'Connection: keep-alive'
```

## Response Result

```json
{
    "code": 0,
    "msg": "success",
    "msgInfo": [],
    "data": {
        "totalUsdtAmount": "8884630.6354",
        "totalBtcAmount": "156.49121429",
        "assets": [
            {
                "currency": "usdt",
                "currencyId": 11,
                "frozenAmount": "180524.40000000",
                "availableAmount": "8704106.23547842",
                "totalAmount": "8884630.63547842",
                "convertBtcAmount": "156.49121429",
                "convertUsdtAmount": "8884630.6354",
                "withdraw": null
            }
        ]
    },
    "ts": 1725531972901
}
```

