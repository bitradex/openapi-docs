# Get Trading Pair Currency 

`GET` /v1/future-u/market/public/symbol/coins

## Request Parameters

Note：This method does not require a signature.

> Request Example

```shell
curl --location --request GET 'https://api.bitradex-test.com/v1/future-u/market/public/symbol/coins' \
--header 'Accept: */*' \
--header 'Host: api.bitradex-test.com' \
--header 'Connection: keep-alive'
```

## Response Result

```json
{
    "code": 0,
    "msg": "success",
    "msgInfo": null,
    "data": [
        "usdt"
    ],
    "ts": 1725507804044
}
```

