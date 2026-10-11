# ESX Legacy Snippets

ESX Legacy snippets for Lua files in [Zed](https://zed.dev).

Snippets live in `snippets/lua.json` and are registered from `extension.toml`.

## Install

1. In Zed, run `zed: install dev extension`.
2. Select this repository folder.
3. Open a `.lua` file.

If a published copy of this extension is already installed, Zed uses this dev extension instead.

## Use a snippet

Type a prefix in a Lua file, then pick the snippet from the completion list.

| Type | Inserts |
| --- | --- |
| `ESX.RegisterCommand` | An `ESX.RegisterCommand` command |
| `ESX:playerloaded` | The `esx:playerLoaded` event |
| `ESX.SharedObject` | `exports['es_extended']:getSharedObject()` |
| `xPlayer.addMoney` | `xPlayer.addMoney(money)` |

Some snippets include `$0`. That is the final cursor position. Press Tab to move to the next stop.

## Edit snippets

Edit `snippets/lua.json`. Each snippet needs a name and a `body`. `prefix` is the text you type to trigger it. When `prefix` is omitted, Zed uses the snippet name.

```json
{
  "Get shared object": {
    "prefix": "ESX.SharedObject",
    "body": ["ESX = exports['es_extended']:getSharedObject()", "$0"],
    "description": "ESX shared object"
  }
}
```

A `$` that is not a tab stop must be written as `\\$`.
