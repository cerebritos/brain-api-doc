# Information School Creative

## Request

Headers:
```
	X-Auth-Country: mx
	X-Auth: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXUyJ9...
	Content-Type: application/json
	Accept: application/json
```

`POST` Url Create School:
```url
https://www.cerebritos.mx/mapi/v1/creative/school
```

`POST` Url Delete School:
```url
https://www.cerebritos.mx/mapi/v1/mapi/v1/creative/school/delete/7
```

`POST` Url Get School:
```url
https://www.cerebritos.mx/mapi/v1/creative/school/8
```

`POST` Url Get Schools:
```url
https://www.cerebritos.mx/mapi/v1/creative/schools
```


`POST` Content Create:
```json

{
	"school_register":{
		"instituteName": "intituto albert smith state",
		"certificate": true,
		"title": "systems engineer",
		"startYear":{
        	"year":"2012",
        	"month":"5",
        	"day":"2"
        },
		"endYear":{
        	"year":"1915",
        	"month":"5",
        	"day":"2"
        }
	}
}
```
## Response Success

### Profile found

HTTP Code: `200`

```json
{
    "instituteName": "intituto albert smith state",
    "certificate": true,
    "title": "systems engineer",
    "startYear": "2012-05-02",
    "endYear": "1915-05-02"
}
```

### Profile found Bulk

HTTP Code: `200`

```json
[
    {
        "instituteName": "intituto albert smith state",
        "certificate": true,
        "title": "systems engineer",
        "startYear": "2012-05-02",
        "endYear": "1915-05-02"
    },
    {
        "instituteName": "intituto albert smith state",
        "certificate": true,
        "title": "systems engineer",
        "startYear": "2012-05-02",
        "endYear": "1915-05-02"
    },
    {
        "instituteName": "intituto albert smith state",
        "certificate": true,
        "title": "systems engineer",
        "startYear": "2012-05-02",
        "endYear": "1915-05-02"
    },
    {
        "instituteName": "intituto albert smith state",
        "certificate": true,
        "title": "systems engineer",
        "startYear": "2012-05-02",
        "endYear": "1915-05-02"
    },
    {
        "instituteName": "intituto albert smith state",
        "certificate": true,
        "title": "systems engineer",
        "startYear": "2012-05-02",
        "endYear": "1915-05-02"
    },
    {
        "instituteName": "intituto albert smith state",
        "certificate": true,
        "title": "systems engineer",
        "startYear": "2012-05-02",
        "endYear": "1915-05-02"
    }
]
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