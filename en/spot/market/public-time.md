# Get server time

`GET` /v1/spot/public/time

## Request Parameters

Note：This method does not require a signature.

> Request Example

```shell
curl --location --request GET 'https://api.noahex-test.com/v1/spot/public/time' \
--header 'Accept: */*' \
--header 'Host: api.noahex-test.com' \
--header 'Connection: keep-alive' 
```

## Response Result

```json
{
    "code": 0,
    "msg": "success",
    "msgInfo": [],
    "data": {
        "serverTime": 1725523397172
    },
    "ts": 1725523397172
}
```

