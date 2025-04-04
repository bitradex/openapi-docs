# 单笔查询

`GET` /v1/spot/order

## 请求参数

| 名称            | 位置    | 类型     | 必选 | 说明     |
|---------------|-------|--------|----|--------|
| orderId       | query | string | 否  | 订单ID   |
| clientOrderId | query | string | 否  | 客户端订单号 |

> 请求示例

```shell
curl --location --request GET 'https://api.bitradex.com/v1/spot/order?orderId=401878710881651008&clientOrderId' \
--header 'validate-algorithms: HmacSHA256' \
--header 'validate-appkey: 2fa91add-388c-44f2-8365-f4b72886c135' \
--header 'validate-recvwindow: 6000' \
--header 'validate-timestamp: 1725546767779' \
--header 'validate-signature: d0abc4c3c907c75f5ba3c72c08c8166429ab9c7c608cff39171c7f1bdd255884' \
--header 'Accept: */*' \
--header 'Host: api.bitradex.com' \
--header 'Connection: keep-alive'
```

## 响应结果

```json
{
  "code": 0,
  "msg": "success",
  "msgInfo": [],
  "data": {
    "symbol": "btc_usdt",
    "orderId": "401878710881651008",
    "clientOrderId": "16559590087220001",
    "baseCurrency": "btc",
    "quoteCurrency": "usdt",
    "side": "BUY",
    "type": "LIMIT",
    "timeInForce": "GTC",
    "price": "40000.00",
    "origQty": "2.000000",
    "origQuoteQty": "80000.00",
    "executedQty": "0.000000",
    "leavingQty": "0.000000",
    "tradeBase": "0.000000",
    "tradeQuote": "0.00",
    "avgPrice": null,
    "fee": null,
    "feeCurrency": null,
    "closed": true,
    "state": "CANCELED",
    "time": 1725517351219,
    "updatedTime": 1725522979707
  },
  "ts": 1725546768350
}
```

