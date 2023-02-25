# launch-gen

This plugin serves as a fast way to start generic project-specific launch.json configs without needing to open the nvim-dap wiki pages.

nvim-dap can load launch configurations with the following (example):

```lua
require("dap.ext.vscode").load_launchjs(nil, { cppdbg = { "c", "cpp", "rust" } })
```

## Commands

```lua
:lua require("launch-gen").NewLaunchConfig({path}, {formatOutputJSON})
```

1. `{path}` defaults to `vim.fn.getcwd()/.vscode/launch.json`
2. `{formatOutputJSON}` defaults to `true`

## Configs

Configs are loaded from `./lua/configs.lua`, which are manually created from the [nvim-dap wiki on adapter installation](https://github.com/mfussenegger/nvim-dap/wiki/Debug-Adapter-installation).

As more configs are needed/requested, they will be added.
