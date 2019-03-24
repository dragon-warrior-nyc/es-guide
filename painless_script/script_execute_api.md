```
POST /_scripts/painless/_execute
{
  "script": {
    "source": "params.count / params.total",
    "params": {
      "count": 100.0,
      "total": 1000.0
    }
  }
}
```

```
POST /_scripts/painless/_execute
{
  "script":{
    "source": """
      long u = params.q ^ params.b; 
      long uCount = u - ((u >> 1) & -5270498306774157605L) - ((u >> 2) & -7905747460161236407L); 
      return ((uCount + (uCount >> 3)) & 8198552921648689607L) % 63;
      """,
    "params": {"q": 1357974856, "b": -1357974856}
  }
}
```

```
POST /_scripts/painless/_execute
{
  "script":{
    "source": """
      long u = params.q ^ params.b; 
      long uCount = u - ((u >>> 1) & -5270498306774157605L) - ((u >>> 2) & -7905747460161236407L); 
      return ((uCount + (uCount >>> 3)) & 8198552921648689607L) % 63;
      """,
    "params": {"q": 1357974856, "b": -1357974856}
  }
}
```
