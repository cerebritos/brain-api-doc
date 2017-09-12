# Login Business

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
   "password":"Password0fa4664e99c2",
   "passwordDoubleCheck":"Password0fa4664e99c2",
}
```
## Response Success

### LoggedIn

HTTP Code: `200`

```json
{
	"message":"success LoggedIn",
	"context":[],
}
```

## Response Errors

### Bad credentials

HTTP Code: `402`

```json
{
	"message":"bad credentials",
	"context":[],
}
```

### Banned LoggedIn

HTTP Code: `402`

```json
{
	"message":"banned LoggedIn",
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