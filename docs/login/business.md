# Login Business

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`POST` Content:
```json

```
## Response Success

### LoggedIn

HTTP Code: `200`

```json

```

## Response Errors

### Bad credentials

HTTP Code: `402`

```json

```

### Banned LoggedIn

HTTP Code: `402`

```json

```

### Token expired

HTTP Code: `402`

```json

```