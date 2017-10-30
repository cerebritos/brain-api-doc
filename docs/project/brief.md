# Brief

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/mapi/v1/brief
```

`POST` Content:
```json
{
	"businessId": "1313",
	"title": "Nescafe para todos",
	"category": [{
		"0": "creative",
		"1": "coffee",
		"2": "video",
		"3": "music",
		"4": "orchesta"
	}],
	"objectGoal": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam et convallis erat, sit amet sodales metus. Nullam molestie gravida nisl, ac maximus augue eleifend ac.",
	"messageTone": "Praesent maximus ex ante. Sed fermentum sagittis est, eu sollicitudin ligula faucibus non. Mauris mollis placerat bibendum.",
	"uniqueSellingPoint": "Morbi finibus augue sit amet sollicitudin dignissim. Pellentesque vulputate augue ornare, imperdiet mi eget, consectetur enim.",
	"budget": "100000000",
	"deadLine": "1989-01-31T08:59:19 +06:00",
	"typeFile": 1,
	"technicalSpecification": "Sed sit amet ipsum ac ante ultrices fringilla. Quisque metus sapien, ornare a mollis quis, sagittis aliquam urna. Donec ipsum sem, auctor non tortor at, ullamcorper ornare metus. Integer eu erat elit.",
	"wellBeing": "Phasellus ac efficitur erat. Donec consequat nec ligula sed finibus. Vestibulum odio lacus, commodo non turpis scelerisque, ultricies elementum est.",
	"competition": "Praesent ut arcu imperdiet, ultricies sem eu, ultrices neque.",
	"customerInsight": "In mollis, tortor a aliquet vulputate, orci ex viverra eros, nec euismod ipsum ex non felis. Phasellus vel commodo lectus. Sed purus nisl, porttitor et facilisis a, venenatis non sapien.",
	"expectations": "Aliquam quis suscipit libero, ut malesuada diam. Nulla commodo congue velit vel sodales. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Duis semper egestas lectus eu elementum. Phasellus sed lacinia justo, eu tincidunt risus."
}
```

## Response Success

### Brief published

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[],
}
```

### Brief save

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[],
}
```

### Brief updated

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[],
}
```

### Brief found

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[
		{
			"Id":"1313",
			"brainId":"1313",
			"businessId":"1313",
			"title":"Nescafe para todos",
			"category":[
				{
				"0":"creative",
				"1":"coffee",
				"2":"video",
				"3":"music",
				"4":"orchesta",
				}
			],
			"objectGoal":"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam et convallis erat, sit amet sodales metus. Nullam molestie gravida nisl, ac maximus augue eleifend ac.",
			"messageTone":"Praesent maximus ex ante. Sed fermentum sagittis est, eu sollicitudin ligula faucibus non. Mauris mollis placerat bibendum.",
			"uniqueSellingPoint":"Morbi finibus augue sit amet sollicitudin dignissim. Pellentesque vulputate augue ornare, imperdiet mi eget, consectetur enim.",
			"budget":"100000000",
			"deadLine":"1989-01-31T08:59:19 +06:00",
			"typeFile":1,
			"technicalSpecification":"Sed sit amet ipsum ac ante ultrices fringilla. Quisque metus sapien, ornare a mollis quis, sagittis aliquam urna. Donec ipsum sem, auctor non tortor at, ullamcorper ornare metus. Integer eu erat elit.",
			"wellBeing":"Phasellus ac efficitur erat. Donec consequat nec ligula sed finibus. Vestibulum odio lacus, commodo non turpis scelerisque, ultricies elementum est.",
			"competition":"Praesent ut arcu imperdiet, ultricies sem eu, ultrices neque.",
			"customerInsight":"In mollis, tortor a aliquet vulputate, orci ex viverra eros, nec euismod ipsum ex non felis. Phasellus vel commodo lectus. Sed purus nisl, porttitor et facilisis a, venenatis non sapien.",
			"expectations":"Aliquam quis suscipit libero, ut malesuada diam. Nulla commodo congue velit vel sodales. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Duis semper egestas lectus eu elementum. Phasellus sed lacinia justo, eu tincidunt risus.",
		}
	],
}
```

## Response Errors

### Brief expired

HTTP Code: `400`

```json
{
	"message":"brief expired",
	"context":[],
}
```

### Brief Already registered

HTTP Code: `400`

```json
{
	"message":"brief Already registered",
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
	"budget":"is't number"
	}
	]
}
```

### Brief not found

HTTP Code: `400`

```json
{
	"message":"brief not found",
	"context":[],
}
```