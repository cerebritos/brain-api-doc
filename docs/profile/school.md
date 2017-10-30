# Information School Creative

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
https://www.cerebritos.mx/mapi/v1/school
```

`POST` Content:
```json
[{
		"name": "intituto albert smith state",
		"certificate": true,
		"title": "systems engineer",
		"startYear": "2012-01-31T08:59:19 +06:00",
		"endYear": "2015-01-31T08:59:19 +06:00",
		"truncated career": false
	},
	{
		"name": "universidad panamericana",
		"certificate": false,
		"title": "none",
		"startYear": "2016-01-31T08:59:19 +06:00",
		"endYear": "2016-01-31T08:59:19 +06:00",
		"truncated career": true
	}
]
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
		"skills": [{
				"0": "intituto albert smith state",
				"1": true,
				"2": "systems engineer",
				"3": "2012-01-31T08:59:19 +06:00",
				"4": "2015-01-31T08:59:19 +06:00",
				"truncatedCareer": false
			},
			{
				"name": "universidad panamericana",
				"certificate": false,
				"title": "none",
				"startYear": "2016-01-31T08:59:19 +06:00",
				"endYear": "2016-01-31T08:59:19 +06:00",
				"truncatedCareer": true
			}
		]
	}]
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

### Incorrect information / Missing fields

HTTP Code: `400`

```json
{
	"message":"missing fields",
	"context":[
	{
	"skills":"missing data"
	}
	]
}
```