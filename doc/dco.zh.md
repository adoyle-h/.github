# 开发者原创声明

[English](./dco.md) | [中文](./dco.zh.md)


该项目使用一种被称为开发者原创声明 (DCO) 的机制来管理流程。

DCO 让开发者简便地证明是他们自己编写了代码或文档，并具有向项目提交代码或文档的权利。

DCO 的全文可以在 <https://developercertificate.org> 阅读。它是这样写的：
（以下是中文翻译，可能翻译表达不到位，须以英文原文为准）

```
开发者原创声明
版本1.1

Copyright (C) 2004, 2006 Linux 基金会与其贡献者。

任何人均可复制和分发本许可文件副本，但不得修改。

开发者原创声明 1.1

向本项目提交贡献时，我保证

(a) 该贡献的全部或部分是由我创建的，并且我有权根据文件中注明的开放源码许可证提交该贡献；或

(b) 该贡献是基于以前的作品，据我所知，该作品是在适当的开放源码许可下进行的，
    而且根据该许可，我有权在文件中指出的相同的开放源码许可下提交该作品的修改，
    无论是全部还是部分由我创建（除非我被允许以不同的许可提交）；或

(c) 该贡献是由作出 (a)、(b) 或 (c) 声明的其他人直接提供给我，且我未对其进行修改。

(d) 我理解并同意，本项目和贡献是公开的，贡献的记录（包括我提交的所有个人信息，包括我的签名）
    将被无限期存档，并且可以与本项目或所涉开源许可证保持一致的情形下再被分发。
```

如果你愿意同意这些条款，你只需在每个 Git 提交信息中添加一行。

```
Signed-off-by: Some Developer somedev@example.com
```

当你这样做时，就代表同意了 DCO。

## 使用 Git 签署 DCO

如果你在 git 配置文件中设置了 `user.name` 和 `user.email`。
你可以用 `git commit -sS` 自动签署你的提交。

一个签名的提交信息的例子可能是这样的。

```
一个提交信息的例子

Signed-off-by: Some Developer somedev@example.com
```

如果不止一个人参与，就有可能有不止一个人在上面签名。比如说。

```
一个提交信息的例子

Signed-off-by: Some Developer somedev@example.com
Signed-off-by: Another Developer anotherdev@example.com
```


参见 `git help commit`,

```
-s, --签收
    在提交日志信息的末尾添加提交者的Signed-off-by行。签收的意义取决于
    项目，但它通常证明提交者有权在相同的许可下提交这项作品，并且
    同意开发者原创声明（更多信息见http://developercertificate.org/）。

-S[<keyid>], --gpg-sign[=<keyid>]
    GPG-sign 提交。keyid参数是可选的，默认为提交者的身份；
    如果指定，它必须与选项卡在一起，没有空格。粘在选项上，不能有空格。
```
