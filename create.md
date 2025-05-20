[Back to API Menu](api.md)

# Create a new record
This endpoint allows you to create a new record in the draft state. While the record is in the draft state,
you can modify it (add metadata or files).

Record has to be created under specified model. Model represents a type of record (e.g. dataset, software, etc.)
and its metadata.

Record has to be created by user with specified role in the community assigned in the body of the request. 
This rule doesn't apply for the external-datasets model, where the record can be created only by user with
the administrator role.

## Request

### Body
`externalWorkflow.defaultWorkflowTemplateId` - defines quality checks id for the record.
`metadata` - any default metadata during creation of the record.
`parent.communities.default` - defines the community where the record will be created.
`files.enabled` - defines if the files are enabled for the record. 
If the files are enabled, the record will require any files to be uploaded before it can be published.

```http request
POST /api/<model_name>/
Content-Type: application/json
Authorization: Bearer <authToken>

{
  "files": {
    "enabled": true
  },
  "metadata": {
    "titles": [
      {
        "titleLanguage": "eng",
        "titleText": "This is test title"
      }
    ]
  },
  "parent": {
    "communities": {
      "default": <community_name (elter)>
    }
  },
  "externalWorkflow": {
    "defaultWorkflowTemplateId": "basic-ingest"
  }
}
```

## Response
TODO

[Back to API Menu](api.md)
