# 查询订单

`GET` /v1/future-u/trade/order/list

## 请求参数

| 名称          | 位置  | 类型    | 必选 | 说明                                                         |
| ------------- | ----- | ------- | ---- | ------------------------------------------------------------ |
| page          | query | integer | 否   | 页码                                                         |
| size          | query | integer | 否   | page size                                                       |
| symbol        | query | string  | 否   | 交易对                                                       |
| startTime     | query | integer | 否   | 开始时间                                                     |
| endTime       | query | integer | 否   | 结束时间                                                     |
| forceClose    | query | boolean | 否   | 是否强平                                                     |
| state         | query | string  | 否   | 订单状态 NEW：新建订单（未成交）；PARTIALLY_FILLED：部分成交；FILLED：全部成交；CANCELED：用户撤销；REJECTED：下单失败；EXPIRED：已过期；UNFINISHED：未完成；HISTORY：（历史） |
| clientOrderId | query | string  | 否   | 自定义订单id                                                 |

> 请求示例

```shell
curl --location --request GET 'https://api.bitradex.com/v1/future-u/trade/order/list?page&size&symbol&startTime&endTime&forceClose&state&clientOrderId=23121' \
--header 'validate-algorithms: HmacSHA256' \
--header 'validate-appkey: 2fa91add-388c-44f2-8365-f4b72886c135' \
--header 'validate-recvwindow: 60000' \
--header 'validate-timestamp: 1725689464716' \
--header 'validate-signature: 57a6f876933928306fe037130aae9d94fd844a55c0226a896c8e93e22eb7e65e' \
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
        "page": 1,
        "ps": 10,
        "total": 1,
        "items": [
            {
                "orderId": "402317447495209024",
                "clientOrderId": "23121",
                "symbol": "btc_usdt",
                "orderType": "LIMIT",
                "orderSide": "BUY",
                "positionSide": "LONG",
                "timeInForce": "GTC",
                "closePosition": false,
                "price": "50000",
                "origQty": "10",
                "avgPrice": "0",
                "executedQty": "0",
                "marginFrozen": "2.53",
                "remark": null,
                "sourceId": null,
                "sourceType": "DEFAULT",
                "forceClose": false,
                "closeProfit": null,
                "closeProfitForBonus": null,
                "state": "CANCELED",
                "createdTime": 1725621954179,
                "updatedTime": 1725621978700,
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
            }
        ]
    },
    "ts": 1725689467410
}
```

