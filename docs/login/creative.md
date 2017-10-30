# Login Creative

## Request

Headers:
```
	X-Auth-Country: mx
	Content-Type: application/json
	Accept: application/json
```

## Login
`Post` Url:
```url
https://www.cerebritos.mx/mapi/v1/auth/login
```

`POST` Content:
```json
{
   "username": "functional.test8@cerebritos.com",
   "password": "abcd1234"
}
```
## Response Success

### LoggedIn

HTTP Code: `200`

```json
{
    "token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXUyJ9...",
    "id": "3",
    "cerebritosId": "38a300f32b75e9e56f9ae68c1c5e155d",
    "username": "test@cerebritos.com",
    "firstName": "Functional",
    "lastName": "Test"
}
```

## Response Errors

### Bad credentials

HTTP Code: `400`

```json
{
	"message":"bad credentials",
	"context":[]
}
```

### Banned LoggedIn

HTTP Code: `400`

```json
{
	"message":"banned LoggedIn",
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