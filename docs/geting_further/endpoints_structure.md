---
layout: page
title: Endpoints Structure
permalink: /getting-further/endpoints/
parent: Getting Further
nav_order: 1
---

| Name              | Desc                | Examples                                  |
|-------------------|---------------------|-------------------------------------------|
| protocol          | Endpoint's protocol | http                                      |
| method            | Endpoint's Method   | POST                                      |
| url               | Base URL + Path     | https://testapp.internal.domains/comments |
| params            | Parameters (Array)  | []                                        |
| params.name       | Parameter's name    | title                                     |
| params.param_type | Parameter's type    | json                                      |
| params.value      | Parameter's value   | this_is_value                             |

```json
[
  ...
  {
    "method": "POST",
    "params": [
      {
        "name": "article_slug",
        "param_type": "json",
        "value": ""
      },
      {
        "name": "title",
        "param_type": "json",
        "value": ""
      },
      {
        "name": "id",
        "param_type": "json",
        "value": ""
      }
    ],
    "protocol": "http",
    "url": "https://testapp.internal.domains/comments"
  }
]
```