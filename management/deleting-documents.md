# Deleting documents

## Deleting document by ID

```
DELETE /product/_doc/1
```

## Adding test documents

Creat the `product` index
```
DELETE /product
PUT /product?pretty
```

Index two documents into `product`:
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

Delete all documents falling into the category of `book`
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

As a result, only one document is left in `product` index:
```
GET /product/_doc/_search
{
    "query": {
        "match_all": {}
    }
}
```
