# Information Membership Creative / Business

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
https://www.cerebritos.mx/mapi/v1/membership
```

## Response Success

### Profile found

HTTP Code: `200`

```json
{
	"message": "success",
	"context": [{
		"id": "123124",
		"idBrain": "832952",
		"typeUser": 1,
		"idTypeMembership": 3,
		"startDate": "2017-01-31T08:59:19 +06:00",
		"endDate": "2018-01-31T08:59:19 +06:00"
	}]
}
```

## Response Errors

### Profile not found

HTTP Code: `400`

```json
{
	"message":"Profile not found",
	"context":[]
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