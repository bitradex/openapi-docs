# 获取持仓爆仓信息

`GET` /v1/future-u/trade/position/break-list

## 请求参数

| 名称     | 位置    | 类型     | 必选 | 说明  |
|--------|-------|--------|----|-----|
| symbol | query | string | 否  | 交易对 |

> 请求示例

```shell
curl --location --request GET 'https://api.bitradex.com/v1/future-u/trade/position/break-list?symbol=btc_usdt' \
--header 'validate-algorithms: HmacSHA256' \
--header 'validate-appkey: 2fa91add-388c-44f2-8365-f4b72886c135' \
--header 'validate-recvwindow: 60000' \
--header 'validate-timestamp: 1725637136325' \
--header 'validate-signature: 32dbee4689743aca63c9f809c9e3b23e16784c3dad95b438c1ad89ea6b587617' \
--header 'Accept: */*' \
--header 'Host: api.bitradex.com' \
--header 'Connection: keep-alive'
```

## 响应结果

```json
{
  "code": 0,
  "msg": "success",
  "msgInfo": null,
  "data": [
    {
      "symbol": "btc_usdt",
      "positionType": "CROSSED",
      "positionSide": "LONG",
      "contractType": "PERPETUAL",
      "positionSize": "2157",
      "entryPrice": "56160.43",
      "isolatedMargin": "605.690232",
      "leverage": 20,
      "breakPrice": "47054.09",
      "calMarkPrice": "54236.05"
    },
    {
      "symbol": "btc_usdt",
      "positionType": "CROSSED",
      "positionSide": "SHORT",
      "contractType": "PERPETUAL",
      "positionSize": "200",
      "entryPrice": "56037.65",
      "isolatedMargin": "56.03765",
      "leverage": 20,
      "breakPrice": "47054.09",
      "calMarkPrice": "54236.05"
    }
  ],
  "ts": 1725637136443
}
```

