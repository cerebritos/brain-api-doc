# Information Project Bag Creative / Business

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
https://www.cerebritos.mx/mapi/v1/project_bag
```

## Response Success

### Profile found

HTTP Code: `200`

```json

{
	"message": "success",
	"context": [{
		"id": "1313",
		"projects": {
			"finalized": [{
					"status": "paid",
					"tittle": "Nulla sodales, tortor ut efficitur mollis.",
					"shortDescription": "Praesent ut arcu imperdiet, ultricies sem eu, ultrices neque. Morbi ut tempor dolor. Suspendisse rutrum, est sed egestas condimentum, risus diam tempus lectus, at bibendum libero felis vel nisl.",
					"review": "Praesent ut arcu imperdiet, ultricies sem eu.",
					"comment": "In mollis, tortor a aliquet vulputate, orci ex viverra eros, nec euismod ipsum ex non felis."
				},
				{
					"status": "paid",
					"tittle": "Nulla sodales, tortor ut efficitur mollis.",
					"shortDescription": "Praesent ut arcu imperdiet, ultricies sem eu, ultrices neque. Morbi ut tempor dolor. Suspendisse rutrum, est sed egestas condimentum, risus diam tempus lectus, at bibendum libero felis vel nisl.",
					"review": "Praesent ut arcu imperdiet, ultricies sem eu.",
					"comment": "In mollis, tortor a aliquet vulputate, orci ex viverra eros, nec euismod ipsum ex non felis."
				}
			],
			"pitch": {
				"status": "bid",
				"linkBrief": "http://www.cerebritos.mx/b/312313",
				"tittle": "Nulla sodales, tortor ut efficitur mollis.",
				"hook": "Praesent ut arcu imperdiet, ultricies sem eu, ultrices neque. Morbi ut tempor dolor. Suspendisse rutrum, est sed egestas condimentum, risus diam tempus lectus, at bibendum libero felis vel nisl."
			}
		}
	}]
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

### Token expired

HTTP Code: `400`

```json
{
	"message":"token expired",
	"context":[]
}
```