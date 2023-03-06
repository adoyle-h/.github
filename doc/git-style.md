---
parent: Code Styles
---
# Git Commit Message Style

[English](./git-style.md) | [中文](./git-style.zh.md)

---

Generally follows the [Conventional Commits v1.0.0](https://www.conventionalcommits.org/en/v1.0.0/).

And the following rules have higher priority.

## Commit Message Format

```
<type>[(scope)][!]: <description>

[body]

[footer]
```

- `<type>`, `<description>` are required.
- `[(scope)]`, `[body]`, `[footer]` are optional.
- If the commit has [breaking change](#breaking-change), `!` is required.

## Type

The `<type>` must be one of the following:

- **build**: Changes that affect the build system or external dependencies.
- **ci**: Changes to CI configuration files and scripts.
- **docs**: Only changes documentation and comments.
- **feat**: A new feature.
- **fix**: A bug fix.
- **perf**: A code change that improves performance.
- **refactor**: A code change that neither fixes a bug nor adds a feature.
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
- **test**: Adding missing tests or correcting existing tests.
- **chore**: Other changes that don't modify src or test files.


## Breaking Change

The commit message with optional `!` to draw attention to breaking change.

```
chore!: drop Node 6 from testing matrix

BREAKING CHANGE: dropping Node 6 which hits end of life in April
```

A commit that has the text `BREAKING CHANGE:` at the beginning of its optional body or footer section
introduces a breaking change. Please read the [Semantic Versioning](https://semver.org/).

A BREAKING CHANGE can be part of commits of any type.

## Sign the DCO for PR

Please sign [our Developer Certificate of Origin (DCO)](./dco.md) before sending pull requests.
For any code changes to be accepted, the DCO must be signed.

## One git commit for PR

Each Pull Request should be in only one commit.

You can use `git rebase -i` to squash some commits into one.
