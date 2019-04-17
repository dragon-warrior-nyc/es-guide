# Introducing the Query Domain-Specific Language (DSL)

## Matching all documents

```
GET /product/_doc/_search
{
  "query": {
    "match_all": {}
  }
}
```
