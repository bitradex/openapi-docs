# 查询当前挂单

`GET` /v1/spot/open-order

## 请求参数

| 名称      | 位置    | 类型     | 必选 | 说明                      |
|---------|-------|--------|----|-------------------------|
| symbol  | query | string | 是  | 交易对，不传代表所有	             |
| bizType | query | string | 是  | 业务类型 SPOT-现货 |
| side    | query | string | 是  | BUY-买,SELL-卖	           |
| limit   | query | string | 是  | 条数                      |

> 请求示例

```shell
curl --location --request GET 'https://api.bitradex.com/v1/spot/open-order?symbol=btc_usdt&bizType=SPOT&side=BUY&limit=10' \
--header 'validate-algorithms: HmacSHA256' \
--header 'validate-appkey: 2fa91add-388c-44f2-8365-f4b72886c135' \
--header 'validate-recvwindow: 6000' \
--header 'validate-timestamp: 1725547662850' \
--header 'validate-signature: 7601e09ff34960a24376e779f49e939cfc887757a3be9b62c0963f25b2387413' \
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
  "data": [
    {
      "symbol": "btc_usdt",
      "orderId": "401876438755871040",
      "clientOrderId": "16559590087220001",
      "baseCurrency": "btc",
      "quoteCurrency": "usdt",
      "side": "BUY",
      "type": "LIMIT",
      "timeInForce": "GTC",
      "price": "40000.00",
      "origQty": "0.500010",
      "origQuoteQty": "20000.40",
      "executedQty": "0.000000",
      "leavingQty": "0.500010",
      "tradeBase": "0.000000",
      "tradeQuote": "0.00",
      "avgPrice": null,
      "fee": null,
      "feeCurrency": null,
      "closed": false,
      "state": "NEW",
      "time": 1725516809502,
      "updatedTime": 1725516809657
    },
    {
      "symbol": "btc_usdt",
      "orderId": "401653869310150976",
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
      "leavingQty": "2.000000",
      "tradeBase": "0.000000",
      "tradeQuote": "0.00",
      "avgPrice": null,
      "fee": null,
      "feeCurrency": null,
      "closed": false,
      "state": "NEW",
      "time": 1725463744811,
      "updatedTime": 1725463744873
    }
  ],
  "ts": 1725547662970
}
```

