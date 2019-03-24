# Deleting documents

## Deleting document by ID

```
DELETE /product/_doc/1
```

## Adding test documents

```
DELETE /product
PUT /product?pretty
```

```
POST /product/_doc
{
  "name": "Processing Events with Logstash",
  "category": "course"
}
```

```
POST /product/_doc
{
  "name": "The Art of Scalability",
  "category": "book"
}
```

```
GET /product/_doc/_search
{
    "query": {
        "match_all": {}
    }
}
```

## Deleting documents by query

```
POST /product/_delete_by_query
{
  "query": {
    "match": {
      "category": "book"
    }
  }
}
```

```
GET /product/_doc/_search
{
    "query": {
        "match_all": {}
    }
}
```
