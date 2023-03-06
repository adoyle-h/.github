# Developer Certificate of Origin

[English](./dco.md) | [中文](./dco.zh.md)

---

The project uses a mechanism known as a Developer Certificate of Origin (DCO) to manage process.

A DCO is a lightweight way for a developer to certify that they wrote or otherwise have the right to submit code or documentation to a project.

The full text of the DCO can be found at <https://developercertificate.org> . It reads:

```
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.


Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

If you are willing to agree to these terms, you just add a line to every git commit message:

```
Signed-off-by: Some Developer somedev@example.com
```

When you do this, you are agreeing to the DCO.

## Sign DCO with Git

If you set your user.name and user.email as part of your git configuration,
you can sign your commit automatically with `git commit -sS`.

An example signed commit message might look like:

```
An example commit message

Signed-off-by: Some Developer somedev@example.com
```

If more than one person works on something it’s possible for more than one person to sign off on it. For example,

```
An example commit message

Signed-off-by: Some Developer somedev@example.com
Signed-off-by: Another Developer anotherdev@example.com
```


See `git help commit`,

```
-s, --signoff
    Add Signed-off-by line by the committer at the end of the commit log message. The meaning of a signoff depends on the
    project, but it typically certifies that committer has the rights to submit this work under the same license and
    agrees to a Developer Certificate of Origin (see http://developercertificate.org/ for more information).

-S[<keyid>], --gpg-sign[=<keyid>]
    GPG-sign commits. The keyid argument is optional and defaults to the committer identity; if specified, it must be
    stuck to the option without a space.
```
