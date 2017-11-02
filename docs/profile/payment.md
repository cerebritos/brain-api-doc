# Information Payment Creative / Business

## Request

Headers:
```
	X-Auth-Country: mx
	X-Auth: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXUyJ9...
	Content-Type: application/json
	Accept: application/json
```

`POST` Url Create CreditCard:
```url
https://www.cerebritos.mx/mapi/v1/creative/creditcard
```

`POST` Url Delete CreditCard:
```url
https://www.cerebritos.mx/mapi/v1/mapi/v1/creative/creditcard/delete/7
```

`POST` Url Get CreditCard:
```url
https://www.cerebritos.mx/mapi/v1/creative/creditcards
```

`POST` Content:
```json
{
	"creditcard_register":{
		"brand": "bancomer",
		"cardholderFirstName": "Jesus",
		"cardholderLastName": "Lopez Lopez",
		"cardNumber": "1232123334541234",
		"expirationDate": "2020-03"
	}
}
```
## Response Success

### Profile found

HTTP Code: `200`

```json
[
    {
        "id": "1",
        "brand": "bancomer",
        "cardholderName": "Jesus Lopez Lopez",
        "cardholderFirstName": "Jesus",
        "cardholderLastName": "Lopez Lopez",
        "cardNumber": "970e70061f4498b048a6a1aeb111cb36",
        "expirationDate": "2020-03-01"
    },
    {
        "id": "2",
        "brand": "bancomer",
        "cardholderName": "Jesus Lopez Lopez",
        "cardholderFirstName": "Jesus",
        "cardholderLastName": "Lopez Lopez",
        "cardNumber": "970e70061f4498b048a6a1aeb111cb36",
        "expirationDate": "2020-03-01"
    }
]
```

### Delete profile

HTTP Code: `200`

```json
{
    "message": "success",
    "context": "creditcard save"
}
```

## Response Errors

### Profile not found

HTTP Code: `400`

```json
{
	"message":"profile not found",
	"context":[]
}
```

### Card validation failed

HTTP Code: `400`

```json
{
	"message":"card validation failed",
	"context":[
	{
	"error":"banned credit card number"
	}
	]
}
```

### Token expired

HTTP Code: `400`

```json
{
	"message":"token expired",
	"context":[]
}
```

### Incorrect information / Missing fields

HTTP Code: `400`

```json
{
	"message":"missing fields",
	"context":[
	{
	"ccn":"invalid number"
	}
	]
}
```