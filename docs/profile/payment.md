# Information Payment Creative / Business

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/p/payment/<idCreative>
```

`POST` Content:
```json
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
	],
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
	"context":[],
}
```

## Response Errors

### Profile not found

HTTP Code: `404`

```json
{
	"message":"profile not found",
	"context":[],
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
	],
}
```

### Token expired

HTTP Code: `402`

```json
{
	"message":"token expired",
	"context":[],
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