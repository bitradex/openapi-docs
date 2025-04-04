# Create Stop Limit

`POST` /v1/future-u/trade/v2/entrust/create-profit

## Request Parameters

| name                        | location   | type      | required    | Description                                                            |
|---------------------------|------|---------|-------|---------------------------------------------------------------|
| symbol                    | body | string  | true  | symbol                                                           |
| triggerPriceType          | body | string  | false | 触发价格type：INDEX_PRICE(指数价格); MARK_PRICE(标记价格)；LATEST_PRICE(最新价格) |
| triggerProfitPrice        | body | number  | false | 止盈触发价                                                         |
| triggerStopPrice          | body | number  | false | 止损触发价                                                         |
| origQty                   | body | number  | false | 数量（张）                                                         |
| positionSide              | body | string  | true  | 持仓方向：LONG;SHORT                                               |
| expireTime                | body | integer | false | 过期时间                                                          |

> Request Example

```shell
curl --location --request POST 'https://api.bitradex.com/v1/future-u/trade/v2/entrust/create-profit' \
--header 'Content-Type: application/json' \
--header 'validate-algorithms: HmacSHA256' \
--header 'validate-appkey: 2fa91add-388c-44f2-8365-f4b72886c135' \
--header 'validate-recvwindow: 60000' \
--header 'validate-timestamp: 1725874904394' \
--header 'validate-signature: b7536773e073a44b6915c02a0b99d659b27946c5bbce6da3020fdbdef6a71c17' \
--header 'Accept: */*' \
--header 'Host: api.bitradex.com' \
--header 'Connection: keep-alive' \
--data-raw '{"symbol":"btc_usdt","origQty":1,"triggerPriceType":"INDEX_PRICE","triggerProfitPrice":56300,"triggerStopPrice":52000,"positionSide":"LONG"}'
```

## Response Result

```json
{
    "code": 0,
    "msg": "success",
    "msgInfo": null,
    "data": "403378398671664192",//止盈止损ID
    "ts": 1725874904699
}
```

