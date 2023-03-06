---
parent: Code Styles
---
# Git Commit Message 风格

[English](./git-style.md) | [中文](./git-style.zh.md)


通常情况下，遵循风格 [Conventional Commits v1.0.0](https://www.conventionalcommits.org/en/v1.0.0/)。

以下规则的权重更高。

## Commit Message 格式

```
<type>[(scope)][!]: <description>

[body]

[footer]
```

- `<type>`, `<description>` 是必要的。
- `[(scope)]`, `[body]`, `[footer]` 是可选的。
- 如果 Commit 包含[破坏性修改](#破坏性修改)，`!` 是必要的。

## Type

`<type>` 必须是以下之一。

- **build**: 改变了构建用的系统或其外部依赖。
- **ci**: 改变了持续集成的配置文件或自动化脚本。
- **docs**: 只修改了文档或注释。
- **feat**: 新增功能。
- **fix**: 修复错误。
- **perf**: 提高性能。
- **refactor**: 既不修复错误也不增加功能的代码变化。
- **style**。不影响代码含义的改变（白空间、格式化、缺少分号等）。
- **test**。增加缺失的测试，或纠正现有的测试。
- **chore**: 其他不修改源码以及测试文件的改动。

## 破坏性修改

Commit Message 中包含可选的 `!`，以引起用户对破坏性修改的注意。

```
chore!: drop Node 6 from testing matrix

BREAKING CHANGE: dropping Node 6 which hits end of life in April
```

一个提交如果有 `BREAKING CHANGE:` 出现在正文 (body) 或页脚 (footer) 的开头。这表示该提交引入了一个破坏性修改。详见[语义化版本](https://semver.org/lang/zh-CN/)。

`BREAKING CHANGE` 可以出现在任何类型的提交。

## 提交 PR 前，签署 DCO

提交 PR 前，请签署[我们的开发者起源证书 (DCO)](./dco.zh.md)。
为了使任何代码修改被接受，DCO 必须被签署。

## PR 只包含一个 Git Commit

每个 Pull Request 应该只有一个 Git Commit。

你可以用`git rebase -i` 把一些 commit 压缩 (squash) 成一个。
