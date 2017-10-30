# Information General Creative / Business

## Request

Headers:
```
	X-Auth-Country: mx
	X-Auth: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXUyJ9...
	Content-Type: application/json
	Accept: application/json
```

## Obtain Creative Profile
`Post` Url:
```url
https://www.cerebritos.mx/mapi/v1/creative/profile
```

`POST` Content:
```json
{}
```

## Update Creative Profile
`Post` Url:
```url
https://www.cerebritos.mx/mapi/v1/creative/update-profile
```

`POST` Content:
```json
{
  "firstName": "test",
  "lastName": "test test",
  "gender": "male",
  "bornDate": {
        	"year":"1989",
        	"month":"5",
        	"day":"2"
        },
  "email": "test@cerebritos.com"
}
```

## Response Success

### Profile found

HTTP Code: `200`

Response business:
```json
{
    "id": "3",
    "cerebritos_id": "38a300f32b75e9e56f9ae68c1c5e155d",
    "email": "functional.test8@cerebritos.com",
    "first_name": "Functional",
    "last_name": "Test",
    "bornDate": "1989-05-02 00:00:00",
    "gender": "male",
    "nationalIdentificationNumber": "FASDFAS123123D",
    "taxIdentificationNumber": "TAXDFAS123123R"
}
```

Response creative:
```json
{
    "id": "3",
    "cerebritos_id": "38a300f32b75e9e56f9ae68c1c5e155d",
    "email": "functional.test8@cerebritos.com",
    "first_name": "Functional",
    "last_name": "Test",
    "bornDate": "1989-05-02 00:00:00",
    "gender": "male",
    "nationalIdentificationNumber": "FASDFAS123123D",
    "taxIdentificationNumber": "TAXDFAS123123R"
}
```

### Updated profile

HTTP Code: `200`

```json
{
    "message": "success",
    "context": "Tus datos han sido Actualizados"
}
```

## Response Errors

### Profile not found

HTTP Code: `400`

```json
{
	"message":"No se encontro ese Usuario",
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
    "message": "Hubo un problema al actualizar los datos del usuario.",
    "context": {
        "lastName": [
            "Este valor no debería estar vacío."
        ]
    }
}
```