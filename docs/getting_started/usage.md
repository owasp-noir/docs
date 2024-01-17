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

  Output:
    -f FORMAT, --format json         Set output format
                                       * plain yaml json jsonl markdown-table
                                       * curl httpie oas2 oas3
                                       * only-url only-param only-header only-cookie
    -o PATH, --output out.txt        Write result to file
    --set-pvalue VALUE               Specifies the value of the identified parameter
    --include-path                   Include file path in the plain result
    --no-color                       Disable color output
    --no-log                         Displaying only the results

  Deliver:
    --send-req                       Send results to a web request
    --send-proxy http://proxy..      Send results to a web request via an HTTP proxy
    --send-es http://es..            Send results to Elasticsearch
    --with-headers X-Header:Value    Add custom headers to be included in the delivery
    --use-matchers string            Send URLs that match specific conditions to the Deliver
    --use-filters string             Exclude URLs that match specified conditions and send the rest to Deliver

  Technologies:
    -t TECHS, --techs rails,php      Specify the technologies to use
    --exclude-techs rails,php        Specify the technologies to be excluded
    --list-techs                     Show all technologies

  Config:
    --concurrency 100                Set concurrency

  Others:
    -d, --debug                      Show debug messages
    -v, --version                    Show version
    -h, --help                       Show help
```

## Example
```bash
# noir -b my_sources

[*] Detecting technologies to base directory.
[I] Detected 1 technologies.
    ruby_rails
[*] Initiate code analysis based on the detected technology.
[*] Starting analysis of endpoints.
    19 Analyzers initialized
    Analysis to 1 technologies
    6 endpoints found
[*] Optimizing endpoints.
[I] Finally identified 6 endpoints.
[*] Generating Report.
GET /secret.html
GET /posts
GET /posts/1
POST /posts {"id":"","title":"","context":""} X-API-KEY:
PUT /posts/1 {"id":"","title":"","context":""} X-API-KEY:
DELETE /posts/1
```