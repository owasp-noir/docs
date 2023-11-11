---
layout: page
title: Debugging
permalink: /contribute/debugging
parent: Contribute
nav_order: 6
---

## With noir's debug flag
Using the `--debug` flag provides detailed information when running Noir.

```bash
noir -b . --debug
```

```bash
[D] Start Debug mode
[D] Noir version: 0.10.0
[D] Noir options from arguments:
    base: .
    url:
    format: plain
    output:
    techs:
    debug: yes
    color: yes
    send_proxy:
    send_req: no
# ....
[D] Baking endpoint /posts with 4 params.
[D] Baked endpoint /posts with {"id":"","title":"","context":""} body and 1 headers.
POST /posts {"id":"","title":"","context":""} X-API-KEY:
[D] Baking endpoint /posts/1 with 4 params.
[D] Baked endpoint /posts/1 with {"id":"","title":"","context":""} body and 1 headers.
PUT /posts/1 {"id":"","title":"","context":""} X-API-KEY:
# ....
```

## With LLDB
And, with tools like [CodeLLDB](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb), a VSCode extension, you can debug Crystal-lang-based applications like Noir.

LLDB Config (`.vscode/launch.json`)

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "lldb",
      "request": "launch",
      "name": "crystal: debug current file",
      "preLaunchTask": "crystal: build current file (debug)",
      "program": "${workspaceFolder}/bin/${fileBasenameNoExtension}",
      "args": [],
      "cwd": "${workspaceFolder}",
      "initCommands": [
        "command script import /path/to/crystal/etc/lldb/crystal_formatters.py"
      ]
    }
  ]
}
```
*[https://github.com/crystal-lang/crystal/blob/master/etc/lldb/crystal_formatters.py](https://github.com/crystal-lang/crystal/blob/master/etc/lldb/crystal_formatters.py)*