# Sign-Up Business

## Request

Headers:
```
	X-Auth-Country: mx
	Content-Type: application/json
	Accept: application/json
```
Url:
```url
https://www.cerebritos.mx/mapi/creative
```

`POST` Content:
```json
{
    "registration": {
        "email": "functional.test8@cerebritos.com",
        "typeUser": 2,
        "firstName": "Functional",
        "lastName": "Test",
        "agentName": "",
        "bornDate": {
        	"year":"1989",
        	"month":"5",
        	"day":"2"
        },
        "gender": "male",
        "password": "abcd1234",
        "nationalIdentificationNumber":"FASDFAS123123D",
        "taxIdentificationNumber":"TAXDFAS123123R",
        "phoneNumber": "55 3436 5887",
        "hourlyRate":3,
        "experienceLevel":2,
        "acceptTerms": true
    }
}
```
## Response Success

### Registered

HTTP Code: `200`

```json
{
    "token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXUyJ9.eyJleHAi"
}
```

## Response Errors

### Already registered

HTTP Code: `400`

```json
{
    "message": "El email ya existe",
    "context": null
}
```

### Banned registration

HTTP Code: `400`

```json
{
	"message":"Este email esta Baneado",
	"context":[]
}
```

### Incorrect information / Missing fields

HTTP Code: `400`

```json
{
    "message": "Hubo un problema al registrar el usuario.",
    "context": {
        "firstName": [
            "Este valor no debería estar vacío."
        ]
    }
}
```