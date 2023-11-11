---
layout: page
title: Installation
permalink: /getting-started/installation/
parent: Getting Started
nav_order: 2
---

## Homebrew (macOS)
```bash
brew install noir

# https://formulae.brew.sh/formula/noir
```

## From Sources
```bash
# Install Crystal-lang
# https://crystal-lang.org/install/

# Clone this repo
git clone https://github.com/noir-cr/noir
cd noir

# Install Dependencies
shards install

# Build
shards build --release --no-debug

# Copy binary
cp ./bin/noir /usr/bin/
```

## Docker (GHCR)

```bash
docker pull ghcr.io/noir-cr/noir:main
``````