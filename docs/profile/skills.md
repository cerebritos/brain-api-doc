# Information General Creative / Business

## Request

Headers:
```
	X-Auth-Country: mx
	X-Auth: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXUyJ9...
	Content-Type: application/json
	Accept: application/json
```

`POST` Url Create / Update:
```url
https://www.cerebritos.mx/mapi/v1/creative/skills
```

`POST` Url Get:
```url
https://www.cerebritos.mx/mapi/v1/creative/getSkills
```

`POST` Content:
```json
{
	"skills": {
	    "typesOffers": "IT - Networking",
	    "experienceLevel": "Noob",
	    "typesAreas": {
	        "0": "serivice network",
	        "1": "develop",
	        "2": "support",
	        "3": "analitics",
	        "4": "community manager",
	        "5": "downLoad",
	        "6": "slide"
	    },
	    "skills": {
	        "0": "PHP",
	        "1": "SCRUM",
	        "2": "SLACK",
	        "3": "WATCH TV",
	        "4": "PIZZA",
	        "5": "WORD"
	    }
	}
}
```
## Response Success

### Profile found

HTTP Code: `200`

```json
{
    "typesOffers": "IT - Networking",
    "experienceLevel": "Noob",
    "typesAreas": [
        "serivice network",
        "develop",
        "support",
        "analitics",
        "community manager",
        "downLoad"
    ],
    "skills": [
        "PHP",
        "SCRUM",
        "SLACK",
        "WATCH TV",
        "PIZZA",
        "WORD"
    ]
}
```

### Updated profile

HTTP Code: `200`

```json
{
    "message": "success",
    "context": "Add o Update skills in profile"
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

### Incorrect information / Same Data

HTTP Code: `400`

```json
{
    "message": "Error Grave",
    "context": {
        "warning": "Same or Problems Data"
    }
}
```