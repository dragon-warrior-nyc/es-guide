```
{
  "script": {
    "lang": "painless",
    "source": "long u = params.substring ^ doc[params.field].value; long uCount = u - ((u >>> 1) & -5270498306774157605L) - ((u >>> 2) & -7905747460161236407L); return ((uCount + (uCount >>> 3)) & 8198552921648689607L) % 63;"
  }
}
```
