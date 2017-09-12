# Information Membership Creative / Business

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/p/membership/<idCreative>
```

## Response Success

### Profile found

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[
    {
	   "id":"123124",
	   "idBrain":"832952",
	   "typeUser":1,
	   "idTypeMembership":3,
	   "startDate":"2017-01-31T08:59:19 +06:00",
	   "endDate":"2018-01-31T08:59:19 +06:00",
	}
	],
}
```

## Response Errors

### Profile not found

HTTP Code: `404`

```json
{
	"message":"Profile not found",
	"context":[],
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