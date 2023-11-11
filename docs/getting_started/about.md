---
layout: page
title: What is Noir?
permalink: /getting-started/about/
parent: Getting Started
nav_order: 1
---

Noir is developed with the goal of enabling security engineers and pentesters to easily identify endpoints in source code. 

It serves as an Attack Surface Detector, conducting static analysis on the source code and various files within the target directory to identify endpoints such as URLs, headers, and parameters. This facilitates the easy identification of endpoints within source code, enabling the transmission of results to other tools or parsing for integration with DAST or logging systems in a DevSecOps environment.

## Key Features

- Automatically identify language and framework from source code.
- Find API endpoints and web pages through code analysis.
- Load results quickly through interactions with proxy tools such as ZAP, Burpsuite, Caido and More Proxy tools.
- That provides structured data such as JSON and YAML for identified Attack Surfaces to enable seamless interaction with other tools. Also provides command line samples to easily integrate and collaborate with other tools, such as curls or httpie.

## Showcase