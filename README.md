# mindcycle.dev builder tools cli

This CLI provides opinionated automations and tools for mindcycle software development and systems administration operations. It provides opinionated starter kits for common software design patterns, simple testing tools and scripts, and automations for frequent workflows.

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->

- [Usage](#usage)
- [Commands](#commands)
<!-- tocstop -->

# Usage

<!-- usage -->

```sh-session
$ npm install -g mindcycle-cli
$ mcl COMMAND
running command...
$ mcl (--version)
mindcycle-cli/0.0.0 darwin-x64 node-v19.2.0
$ mcl --help [COMMAND]
USAGE
  $ mcl COMMAND
...
```

<!-- usagestop -->

# Commands

<!-- commands -->

- [mindcycle.dev builder tools cli](#mindcycledev-builder-tools-cli)
- [Usage](#usage)
- [Commands](#commands)
  - [`mcl hello PERSON`](#mcl-hello-person)
  - [`mcl hello world`](#mcl-hello-world)
  - [`mcl help [COMMANDS]`](#mcl-help-commands)
  - [`mcl plugins`](#mcl-plugins)
  - [`mcl plugins:install PLUGIN...`](#mcl-pluginsinstall-plugin)
  - [`mcl plugins:inspect PLUGIN...`](#mcl-pluginsinspect-plugin)
  - [`mcl plugins:install PLUGIN...`](#mcl-pluginsinstall-plugin-1)
  - [`mcl plugins:link PLUGIN`](#mcl-pluginslink-plugin)
  - [`mcl plugins:uninstall PLUGIN...`](#mcl-pluginsuninstall-plugin)
  - [`mcl plugins:uninstall PLUGIN...`](#mcl-pluginsuninstall-plugin-1)
  - [`mcl plugins:uninstall PLUGIN...`](#mcl-pluginsuninstall-plugin-2)
  - [`mcl plugins update`](#mcl-plugins-update)

## `mcl hello PERSON`

Say hello

```
USAGE
  $ mcl hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/swbmindcycle/mindcycle-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `mcl hello world`

Say hello world

```
USAGE
  $ mcl hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ mcl hello world
  hello world! (./src/commands/hello/world.ts)
```

## `mcl help [COMMANDS]`

Display help for mcl.

```
USAGE
  $ mcl help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for mcl.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.12/src/commands/help.ts)_

## `mcl plugins`

List installed plugins.

```
USAGE
  $ mcl plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ mcl plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.4.7/src/commands/plugins/index.ts)_

## `mcl plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ mcl plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ mcl plugins add

EXAMPLES
  $ mcl plugins:install myplugin

  $ mcl plugins:install https://github.com/someuser/someplugin

  $ mcl plugins:install someuser/someplugin
```

## `mcl plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ mcl plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ mcl plugins:inspect myplugin
```

## `mcl plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ mcl plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ mcl plugins add

EXAMPLES
  $ mcl plugins:install myplugin

  $ mcl plugins:install https://github.com/someuser/someplugin

  $ mcl plugins:install someuser/someplugin
```

## `mcl plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ mcl plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ mcl plugins:link myplugin
```

## `mcl plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mcl plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mcl plugins unlink
  $ mcl plugins remove
```

## `mcl plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mcl plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mcl plugins unlink
  $ mcl plugins remove
```

## `mcl plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mcl plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mcl plugins unlink
  $ mcl plugins remove
```

## `mcl plugins update`

Update installed plugins.

```
USAGE
  $ mcl plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

<!-- commandsstop -->
