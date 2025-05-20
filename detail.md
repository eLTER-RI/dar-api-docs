[Back to API Menu](api.md)

# Record Detail API
The Record Detail API allows you to retrieve the details of a specific record in the system. 
You can access both published and draft records, depending on your permissions.

## Types
- published
- draft - This requires permissions to read draft records.

## Published detail request

```http request
GET /api/<model_name>/<record_id>
```

## Draft detail request

```http request
GET /api/<model_name>/<record_id>/draft
Authorization: Bearer <authToken>
```

[Back to API Menu](api.md)