# Adding multi-fields mappings

## Managing index

```
DELETE /product
PUT /product?pretty
```

## Adding mappings

```
PUT /product/_doc/_mapping
{
  "properties": {
    "description": {
      "type": "text"
    },
    "name": {
      "type": "text",
      "fields": {
        "keyword": {
          "type": "keyword"
        }
      }
    },
    "tags": {
      "type": "text",
      "fields": {
        "keyword": {
          "type": "keyword"
        }
      }
    }
  }
}
```

## Retrieving mapping

```
GET /product/_doc/_mapping
```
