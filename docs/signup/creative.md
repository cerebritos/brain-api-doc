# Sign-Up Creative

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
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
```
## Response Success

### Registered

HTTP Code: `200`

```json
{
	"message":"success",
	"context":[],
}
```

## Response Errors

### Already registered

HTTP Code: `402`

```json
{
	"message":"already registered",
	"context":[],
}
```

### Banned registration

HTTP Code: `402`

```json
{
	"message":"banned registration",
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
	"phone":"most numbers",
	"email":"already registred"
	}
	]
}
```