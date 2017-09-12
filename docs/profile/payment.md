# Information Payment Creative / Business

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/p/payment/<idCreative>
```

`POST` Content:
```json

```
## Response Success

### Profile found

HTTP Code: `200`

```json

```

### Updated profile

HTTP Code: `200`

```json

```

## Response Errors

### Profile not found

HTTP Code: `404`

```json

```

### Card validation failed

HTTP Code: `400`

```json

```

### Token expired

HTTP Code: `402`

```json

```

### Incorrect information / Missing fields

HTTP Code: `400`

```json

```