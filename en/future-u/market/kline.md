# Get Trading Pair Information of Kline

`GET` /v1/future-u/market/public/q/kline

## Request Parameters

| name      | location  | type    | required | Description                                                         |
| --------- | ----- | ------- | ---- | ------------------------------------------------------------ |
| symbol    | query | string  | Yes   | symbol                                                       |
| interval  | query | string  | Yes   | 时间间隔支持1m，3m,5m,15m,30m,1h,2h,4h,6h,8h,12h,1d,2d,3d,1w,1M |
| startTime | query | integer | No   | Start Time                                                     |
| endTime   | query | integer | No   | End Time                                                     |
| limit     | query | integer | No   | 限制Page Limit                                                     |


Note：This method does not require a signature.

> Request Example

```shell
curl --location --request GET 'https://api.bitradex.com/v1/future-u/market/public/q/kline?symbol=btc_usdt&interval=1m&startTime&endTime&limit=5' \
--header 'Accept: */*' \
--header 'Host: api.bitradex.com' \
--header 'Connection: keep-alive'
```

## Response Result

```json
{
    "code": 0,
    "msg": "success",
    "msgInfo": null,
    "data": [
        {
            "s": "btc_usdt",
            "p": "btc_usdt",
            "t": 1725625680000,
            "o": "56020.55",
            "c": "56020.55",
            "h": "56020.55",
            "l": "56020.55",
            "a": "29063",
            "v": "162812.524465"
        },
        {
            "s": "btc_usdt",
            "p": "btc_usdt",
            "t": 1725625620000,
            "o": "56044.85",
            "c": "56032.95",
            "h": "56085.95",
            "l": "56020.55",
            "a": "1242311",
            "v": "6963240.668650"
        },
        {
            "s": "btc_usdt",
            "p": "btc_usdt",
            "t": 1725625560000,
            "o": "55981.45",
            "c": "56039.95",
            "h": "56039.95",
            "l": "55979.85",
            "a": "947381",
            "v": "5307817.605915"
        },
        {
            "s": "btc_usdt",
            "p": "btc_usdt",
            "t": 1725625500000,
            "o": "55986.05",
            "c": "55986.25",
            "h": "56004.85",
            "l": "55974.85",
            "a": "368317",
            "v": "2062299.880420"
        },
        {
            "s": "btc_usdt",
            "p": "btc_usdt",
            "t": 1725625440000,
            "o": "55966.25",
            "c": "55986.05",
            "h": "55992.95",
            "l": "55945.65",
            "a": "468955",
            "v": "2624767.175930"
        }
    ],
    "ts": 1725625687109
}
```

