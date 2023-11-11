---
layout: page
title: Usage
permalink: /getting-started/usage/
parent: Getting Started
nav_order: 3
---

## Basic
> noir -b `<base-path>` `<flags...>`

```shell
noir -b . -u https://www.hahwul.com
```

## Usage
```shell
Usage: noir <flags>
  Basic:
    -b PATH, --base-path ./app       (Required) Set base path
    -u URL, --url http://..          Set base url for endpoints
    -s SCOPE, --scope url,param      Set scope for detection

  Output:
    -f FORMAT, --format json         Set output format
                                     [plain/json/yaml/markdown-table/curl/httpie/oas2/oas3]
    -o PATH, --output out.txt        Write result to file
    --set-pvalue VALUE               Specifies the value of the identified parameter
    --no-color                       Disable color output
    --no-log                         Displaying only the results

  Deliver:
    --send-req                       Send the results to the web request
    --send-proxy http://proxy..      Send the results to the web request via http proxy
    --send-es http://es..            Send the results to elasticsearch
    --with-headers X-Header:Value    Add Custom Headers to be Used in Deliver
    --use-matchers string            Delivers URLs that match a specific condition
    --use-filters string             Excludes URLs that match a specific condition

  Technologies:
    -t TECHS, --techs rails,php      Specify the technologies to use
    --exclude-techs rails,php        Specify the technologies to be excluded
    --list-techs                     Show all technologies

  Others:
    -d, --debug                      Show debug messages
    -v, --version                    Show version
    -h, --help                       Show help
```