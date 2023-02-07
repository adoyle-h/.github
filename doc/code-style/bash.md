---
parent: Code Styles
---
# Bash Code Style

Generally follows <https://google.github.io/styleguide/shellguide.html>

And the following rules have higher priority.

## Editor Settings

- Your editor must be able to recognize the [`.editorconfig`](http://editorconfig.org/) file in project.
- [Shellcheck](https://github.com/koalaman/shellcheck) must be installed, and your editor must support it.

## File naming

- All filenames must match the regex `[-_a-z0-9]`, except `Dockerfile` and other particular files.
- All script filenames must end with `.bash`.

## File Header

- For executable files, put `#!/usr/bin/env bash` at the top of file.
- For `.bats` files, put `#!/usr/bin/env bats` at the top of file.
- No shebang for non-executable files.

## Test

- Use [bats](https://github.com/bats-core/bats-core) for unit testing.

## Rules

- No `function` key. Function declaration `func() {...}` is preferred over `function func() {...}`.
