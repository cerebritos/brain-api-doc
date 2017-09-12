# Pitch

## Request

Headers:
```
	Authorization: Bearer <token>
	Location: mx
```

`GET` Url:
```url
https://www.cerebritos.mx/p/<idPitch>
```

`POST` Content:
```json

```

## Response Success

### Pitch published

HTTP Code: `200`

```json

```

### Pitch save

HTTP Code: `200`

```json

```

### Pitch updated

HTTP Code: `200`

```json

```

### Pitch found

HTTP Code: `200`

```json

```

## Response Errors

### Pitch expired*

HTTP Code: `402`

```json

```

### Pitch Already registered

HTTP Code: `402`

```json

```

### Brief not available

HTTP Code: `402`

```json

```

### Incorrect information / Missing fields

HTTP Code: `400`

```json

```

### Pitch not found

HTTP Code: `400`

```json

```

(*) In Review.