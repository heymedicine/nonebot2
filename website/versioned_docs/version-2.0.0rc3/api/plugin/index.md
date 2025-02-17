---
sidebar_position: 0
description: nonebot.plugin 模块
---

# nonebot.plugin

本模块为 NoneBot 插件开发提供便携的定义函数。

## 快捷导入

为方便使用，本模块从子模块导入了部分内容，以下内容可以直接通过本模块导入:

- `on` => [`on`](./on.md#on)
- `on_metaevent` => [`on_metaevent`](./on.md#on_metaevent)
- `on_message` => [`on_message`](./on.md#on_message)
- `on_notice` => [`on_notice`](./on.md#on_notice)
- `on_request` => [`on_request`](./on.md#on_request)
- `on_startswith` => [`on_startswith`](./on.md#on_startswith)
- `on_endswith` => [`on_endswith`](./on.md#on_endswith)
- `on_fullmatch` => [`on_fullmatch`](./on.md#on_fullmatch)
- `on_keyword` => [`on_keyword`](./on.md#on_keyword)
- `on_command` => [`on_command`](./on.md#on_command)
- `on_shell_command` => [`on_shell_command`](./on.md#on_shell_command)
- `on_regex` => [`on_regex`](./on.md#on_regex)
- `on_type` => [`on_type`](./on.md#on_type)
- `CommandGroup` => [`CommandGroup`](./on.md#CommandGroup)
- `Matchergroup` => [`MatcherGroup`](./on.md#MatcherGroup)
- `load_plugin` => [`load_plugin`](./load.md#load_plugin)
- `load_plugins` => [`load_plugins`](./load.md#load_plugins)
- `load_all_plugins` => [`load_all_plugins`](./load.md#load_all_plugins)
- `load_from_json` => [`load_from_json`](./load.md#load_from_json)
- `load_from_toml` => [`load_from_toml`](./load.md#load_from_toml)
- `load_builtin_plugin` => [`load_builtin_plugin`](./load.md#load_builtin_plugin)
- `load_builtin_plugins` => [`load_builtin_plugins`](./load.md#load_builtin_plugins)
- `require` => [`require`](./load.md#require)
- `PluginMetadata` => [`PluginMetadata`](./plugin.md#PluginMetadata)

## _def_ `get_plugin(name)` {#get_plugin}

- **说明**

  获取已经导入的某个插件。

  如果为 `load_plugins` 文件夹导入的插件，则为文件(夹)名。

- **参数**

  - `name` (str): 插件名，即 [Plugin.name](./plugin.md#Plugin-name)。

- **返回**

  - Plugin | None

## _def_ `get_plugin_by_module_name(module_name)` {#get_plugin_by_module_name}

- **说明**

  通过模块名获取已经导入的某个插件。

  如果提供的模块名为某个插件的子模块，同样会返回该插件。

- **参数**

  - `module_name` (str): 模块名，即 [Plugin.module_name](./plugin.md#Plugin-module_name)。

- **返回**

  - Plugin | None

## _def_ `get_loaded_plugins()` {#get_loaded_plugins}

- **说明**

  获取当前已导入的所有插件。

- **返回**

  - set[Plugin]

## _def_ `get_available_plugin_names()` {#get_available_plugin_names}

- **说明**

  获取当前所有可用的插件名（包含尚未加载的插件）。

- **返回**

  - set[str]
