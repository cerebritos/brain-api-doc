# Pitch

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/p/<idPitch>
```

`POST` Content:
```json
{
	"userId":"1313",
	"title":"Nescafe para todos",
	"hook":"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam et convallis erat, sit amet sodales metus. Nullam molestie gravida nisl, ac maximus augue eleifend ac.",
	"typeFile":1,
	"uniqSellingPoint":"Praesent maximus ex ante. Sed fermentum sagittis est, eu sollicitudin ligula faucibus non. Mauris mollis placerat bibendum.",
	"compensation":"Morbi finibus augue sit amet sollicitudin dignissim. Pellentesque vulputate augue ornare, imperdiet mi eget, consectetur enim.",
	"category":[
		{
		"0":"creative",
		"1":"coffee",
		"2":"video",
		"3":"music",
		"4":"orchesta",
		}
	],
	"expectations":"100000000",
	"deadLine":"1989-01-31T08:59:19 +06:00"
}
```

## Response Success

### Pitch published

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[],
}
```

### Pitch save

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[],
}
```

### Pitch updated

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[],
}
```

### Pitch found

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[
		{
			"Id":"1313",
			"brainId":"1313",
			"userId":"1313",
			"title":"Nescafe para todos",
			"hook":"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam et convallis erat, sit amet sodales metus. Nullam molestie gravida nisl, ac maximus augue eleifend ac.",
			"typeFile":1,
			"uniqSellingPoint":"Praesent maximus ex ante. Sed fermentum sagittis est, eu sollicitudin ligula faucibus non. Mauris mollis placerat bibendum.",
			"compensation":"Morbi finibus augue sit amet sollicitudin dignissim. Pellentesque vulputate augue ornare, imperdiet mi eget, consectetur enim.",
			"category":[
				{
				"0":"creative",
				"1":"coffee",
				"2":"video",
				"3":"music",
				"4":"orchesta",
				}
			],
			"expectations":"100000000",
			"deadLine":"1989-01-31T08:59:19 +06:00"
		}
	]
}
```

## Response Errors

### Pitch expired (1)

HTTP Code: `402`

```json
{
	"message":"pitch expired",
	"context":[],
}
```

### Pitch Already registered

HTTP Code: `402`

```json
{
	"message":"pitch Already registered",
	"context":[],
}
```

### Brief not available (2)

HTTP Code: `402`

```json
{
	"message":"brief not available",
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
	"title":"missing",
	"hook":"very long"
	}
	]
}
```

### Pitch not found

HTTP Code: `400`

```json
{
	"message":"pitch not found",
	"context":[],
}
```

* (1) In Review.
* (2) Time expired for the brief.