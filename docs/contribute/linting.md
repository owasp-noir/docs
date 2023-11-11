---
layout: page
title: Formatting and Linting
permalink: /contribute/formatting_linting
parent: Contribute
nav_order: 5
---

## Formatting
```bash
crystal tool format
```

## Linting
You align code conventions using Ameba. Refer to the link [https://github.com/crystal-ameba/ameba#installation](https://github.com/crystal-ameba/ameba#installation) to install Ameba.

```bash
# Basic
ameba

# Auto fix
ameba --fix
```

*Ameba conf: [.ameba.yml](https://github.com/noir-cr/noir/blob/main/.ameba.yml)*