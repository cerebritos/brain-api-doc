# Sign-Up Business

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

### Registered

HTTP Code: `200`

```json

```

## Response Errors

### Already registered

HTTP Code: `402`

```json

```

### Banned registration

HTTP Code: `402`

```json

```

### Incorrect information / Missing fields

HTTP Code: `400`

```json

```