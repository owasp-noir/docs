---
layout: page
title: How to Contribute
permalink: /contribute/how-to-contribute
parent: Contribute
nav_order: 1
---

## ❤️ Contribute
1. Write code in forked repo
2. Make Pull Request to `dev` branch
3. Finish :D

![](https://github.com/hahwul/noir/assets/13212227/23989dab-6b4d-4f18-904f-7f5cfd172b04)

## 🧭 Code structure
- spec (for `crystal spec`)
  - unit_test: unit-test codes
  - functional_test: functional test codes
- src
  - analyzer: Code analyzers for Endpoint URL and Parameter analysis
  - detector: Codes for language, framework identification 
  - models: Everything for the model, such as class, structure, etc
  - utils: Utility codes
  - etc...
- noir.cr: main and command-line parser

## References
- https://github.com/noir-cr/noir/blob/main/CONTRIBUTING.md