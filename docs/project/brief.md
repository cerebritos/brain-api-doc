# Brief

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/b/<idBrief>
```

`POST` Content:
```json

```

## Response Success

### Brief published

HTTP Code: `200`

```json

```

### Brief save

HTTP Code: `200`

```json

```

### Brief updated

HTTP Code: `200`

```json

```

### Brief found

HTTP Code: `200`

```json

```

## Response Errors

### Brief expired

HTTP Code: `402`

```json

```

### Brief Already registered

HTTP Code: `402`

```json

```

### Incorrect information / Missing fields

HTTP Code: `400`

```json

```

### Brief not found

HTTP Code: `400`

```json

```