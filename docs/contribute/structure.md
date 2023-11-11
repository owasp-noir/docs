---
layout: page
title: Struct of Project
permalink: /contribute/structure
parent: Contribute
nav_order: 3
---

## Detector
The Detector in Noir investigates the programming languages, frameworks, and specification documents present in the source code at the base path.

## Analyzer
The Analyzer in Noir works based on the information gathered by the Detector to identify actual endpoints. It finding methods, paths, parameters, and more.

## Deliver
The Deliver feature in Noir handles the transmission of the endpoints identified by the Analyzer. While Noir typically outputs via stdout, using Deliver enables additional transmission to tools like Proxy or ElasticSearch.

## Output Builder
The Output Builder feature is responsible for generating results. It transforms the object containing discovered endpoints into formats like JSON, YAML, and Curl.