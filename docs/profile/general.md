# Information General Creative / Business

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/p/general/<idCreative>
```

`POST` Content:
```json
{
   "email":"demo@mail.com",
   "emailDoubleCheck":"demo@mail.com",
   "password":"Password0fa4664e99c2",
   "newPassword":false,
   "passwordDoubleCheck":"Password0fa4664e99c2",
   "name":"cerebritos inc.",
   "agentName":"Jonh smith jonnes",
   "bornDate":"1989-01-31T08:59:19 +06:00",
   "nationalIdentificationNumber":"FASDFAS123123R",
   "phoneNumber":"01325534363754",
   "acceptTerms":true,
   "taxIdentificationNumber":"TAXDFAS123123R",
   "projectPerYear":3,
   "teamSize":2
}
```

## Response Success

### Profile found

HTTP Code: `200`

Response business:
```json
{
	"message":"success",
	"context":[
    {
	   "id":"123124",
	   "idBrain":"832952",
	   "email":"demo@mail.com",
	   "emailDoubleCheck":"demo@mail.com",
	   "password":"Password0fa4664e99c2",
	   "newPassword":false,
	   "passwordDoubleCheck":"Password0fa4664e99c2",
	   "name":"cerebritos inc.",
	   "agentName":"Jonh smith jonnes",
	   "bornDate":"1989-01-31T08:59:19 +06:00",
	   "nationalIdentificationNumber":"FASDFAS123123R",
	   "phoneNumber":"01325534363754",
	   "acceptTerms":true,
	   "taxIdentificationNumber":"TAXDFAS123123R",
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
	   "projectPerYear":3,
	   "teamSize":2
	}
	],
}
```

Response creative:
```json
{
	"message":"success",
	"context":[
    {
	   "id":"123124",
	   "idBrain":"832952",
	   "email":"demo@mail.com",
	   "emailDoubleCheck":"demo@mail.com",
	   "password":"Password0fa4664e99c2",
	   "newPassword":false,
	   "passwordDoubleCheck":"Password0fa4664e99c2",
	   "name":"cerebritos inc.",
	   "lastName":"Jonh smith jonnes",
	   "bornDate":"1989-01-31T08:59:19 +06:00",
	   "nationalIdentificationNumber":"FASDFAS123123R",
	   "phoneNumber":"01325534363754",
	   "acceptTerms":true,
	   "taxIdentificationNumber":"TAXDFAS123123R",
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
	   "hourlyRate":3,
	   "experienceLevel":2
	}
	],
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

### Token expired

HTTP Code: `402`

```json
{
	"message":"token expired",
	"context":[],
}
```

### Incorrect information / Missing fields

HTTP Code: `402`

```json
{
	"message":"missing fields",
	"context":[
	{
	"phone":"most numbers",
	"email":"already registred"
	}
	]
}
```