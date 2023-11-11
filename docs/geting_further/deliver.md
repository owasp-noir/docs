---
layout: page
title: Deliver
permalink: /getting-further/deliver/
parent: Getting Further
nav_order: 2
---

## Flags

```
  Deliver:
    --send-req                       Send the results to the web request
    --send-proxy http://proxy..      Send the results to the web request via http proxy
    --send-es http://es..            Send the results to elasticsearch
    --with-headers X-Header:Value    Add Custom Headers to be Used in Deliver
    --use-matchers string            Delivers URLs that match a specific condition
    --use-filters string             Excludes URLs that match a specific condition
```

## Example
### Send to proxy
```bash
noir -b . -u http://localhost:4000 --send-proxy http://localhost:8090
```

![](/docs/assets/images/contents/send-proxy.png)

### Send to Elastic Search
```bash
# noir -b <BASE-PATH> --send-es http://<ES-ENDPOINT>/<INDEX>/<TYPE>
noir -b ./app/ --send-es http://localhost:9200/noir/url
```

![](https://github.com/hahwul/noir/assets/13212227/4ee8d7ab-4a90-45df-9a79-293390b5d505)

### Send with Headers

Command
```bash
noir -b . -u http://localhost:4000 \
     --send-proxy http://localhost:8090 \
     --with-headers "X-API-Key: abcdefg" \
     --with-headers "Device-ID: 1290874198274"
```

Request
```http
GET http://localhost:4000/secret.html HTTP/1.1
X-API-Key: abcdefg
Device-ID: 1290874198274
User-Agent: Noir/0.10.0
Accept: */*
host: localhost:4000
```