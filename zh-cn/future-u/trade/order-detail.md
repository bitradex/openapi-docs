# 根据id查询订单

`GET` /v1/future-u/trade/order/detail

## 请求参数

| 名称          | 位置  | 类型    | 必选 | 说明 |
| ------------- | ----- | ------- | ---- | ---- |
| orderId       | query | integer | 否   | none |
| clientOrderId | query | string  | 否   | none |

> 请求示例

```shell
curl --location --request GET 'https://api.bitradex.com/v1/future-u/trade/order/detail?orderId=401302995278811200&clientOrderId' \
--header 'validate-algorithms: HmacSHA256' \
--header 'validate-appkey: 2fa91add-388c-44f2-8365-f4b72886c135' \
--header 'validate-recvwindow: 6000' \
--header 'validate-timestamp: 1725512343034' \
--header 'validate-signature: d023479f5ef89b2f6caacfddc8be19430c2d29deaee3f8c3d874a5d4ebe5e15a' \
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
    "data": {
        "orderId": "401302995278811200",
        "clientOrderId": null,
        "symbol": "btc_usdt",
        "orderType": "LIMIT",
        "orderSide": "BUY",
        "positionSide": "LONG",
        "timeInForce": "GTC",
        "closePosition": false,
        "price": "26972.9",
        "origQty": "4",
        "avgPrice": "0",
        "executedQty": "0",
        "marginFrozen": "0.5459315",
        "remark": null,
        "sourceId": null,
        "sourceType": "DEFAULT",
        "forceClose": false,
        "closeProfit": null,
        "closeProfitForBonus": null,
        "state": "CANCELED",
        "createdTime": 1725380089923,
        "updatedTime": 1725511966321,
        "welfareAccount": false,
        "triggerPriceType": null,
        "triggerProfitPrice": null,
        "profitDelegateOrderType": null,
        "profitDelegateTimeInForce": null,
        "profitDelegatePrice": null,
        "triggerStopPrice": null,
        "stopDelegateOrderType": null,
        "stopDelegateTimeInForce": null,
        "stopDelegatePrice": null,
        "leverage": 20,
        "profit": false
    },
    "ts": 1725512343581
}
```

