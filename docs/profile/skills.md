# Information General Creative / Business

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
https://www.cerebritos.mx/mapi/v1/skills
```

`POST` Content:
```json
{
	"typesOffers": 3,
	"typesAreas": [{
		"0": "serivice network",
		"1": "develop",
		"2": "support",
		"3": "analitics",
		"4": "community manager"
	}],
	"skills": [{
		"0": "PHP",
		"1": "SCRUM",
		"2": "SLACK",
		"3": "WATCH TV",
		"4": "PIZZA",
		"5": "WORD"
	}],
	"experienceLevel": 3
}
```
## Response Success

### Profile found

HTTP Code: `200`

```json
{
	"message": "success",
	"context": [{
		"typesOffers": 3,
		"typesAreas": [{
			"0": "serivice network",
			"1": "develop",
			"2": "support",
			"3": "analitics",
			"4": "community manager"
		}],
		"skills": [{
			"0": "PHP",
			"1": "SCRUM",
			"2": "SLACK",
			"3": "WATCH TV",
			"4": "PIZZA",
			"5": "WORD"
		}],
		"experienceLevel": 3
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
	"typesOffers":3,
	"experienceLevel":3
	}
	]
}
```