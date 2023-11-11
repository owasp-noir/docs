---
layout: page
title: Set up Build Environment
permalink: /contribute/build
parent: Contribute
nav_order: 2
---

## Install Crystal
Before getting started with building Noir, you'll need to install Crystal-lang. Refer to the link below for installation guidance.

> https://crystal-lang.org/install/

If you're using macOS or Linux, you can easily install it through Homebrew.

```bash
brew install crystal
```

## Clone noir

```bash
# Clone this repo
git clone https://github.com/noir-cr/noir
cd noir
```

## Build
### Install Dependencies
```bash
shards install
```

### Build
```bash
shards build
```

By default, Crystal builds including debugging information. For release, build with the flags --release --no-debug to exclude debug info.