# Information Payment Creative / Business

## Request

Headers:
```
	X-Auth-Country: mx
	X-Auth: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXUyJ9...
	Content-Type: application/json
	Accept: application/json
```

`POST` Url:
```url
https://www.cerebritos.mx/mapi/v1/payment
```

`POST` Content:
```json
{
	"ccn": "42908304012957057",
	"cardType": 1,
	"expirationDate": "0220",
	"csc": 1312,
	"defaultAddess": false,
	"addresses": [{
		"street": "lorem impsu",
		"externalNumber": "12",
		"internalNumber": "1b",
		"city": "Mexico",
		"country": "Mexico",
		"municipality": "Ecatepec",
		"neighborhood": "Magdalena",
		"region": "32342",
		"defaultAddress": true
	}]
}
```
## Response Success

### Profile found

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[
		{
		"ccn":"42908304012957057",
		"cardType":1,
		"expirationDate":"0220",
		"csc":1312,
		"defaultAddess":false,
		"addresses":[
			{
			"street": "lorem impsu",
			"externalNumber": "12",
			"internalNumber": "1b",
			"city": "Mexico",
			"country": "Mexico",
			"municipality": "Ecatepec",
			"neighborhood": "Magdalena",
			"region": "32342",
			"defaultAddress": true
			}
		]
		}
	]
}
```

### Updated profile

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[]
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