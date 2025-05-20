[Back to API Menu](api.md)

# Search API
The Search API allows you to search for datasets, publications, and files in the DataCite Commons. 
You can use various parameters to filter your search results.

The search is based on the opensearch engine - 
you can use official opensearch documentation for more details and possibilities.

## Types of Searches
- **Model**: Search for records with specified model.
- **Global Search**: Search for records with any model.
- **User Search**: Search of records for user. 
- This search is limited for records that the user has access to. Need authToken.

## Search Parameters (some)
- **q**: The search query string.
- **size**: The number of results to return (default is 25).
- **page**: The page number of results to return (default is 1).
- **sort**: The field to sort the results by (default is "newest").
- **f**: The field for facets. Here you can find [list of assets](facets_list.md).

## Model Search Request
```http request
GET /api/<model_name>/?q=f=metadata_keywords_keywordLabel:test
```

## Global Search Request
```http request
GET /api/search/?q=f=metadata_keywords_keywordLabel:test
```

## User Search Request
```http request
GET /api/user/search/?q=f=metadata_keywords_keywordLabel:test
Authorization: Bearer <authToken>
```

## Response
TODO


[Back to API Menu](api.md)
