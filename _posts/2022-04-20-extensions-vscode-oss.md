---
layout: post
title: How to Get Any Extension to Work With VSCodium
slug: extensions-vscodium
author: Florent Dufour
date: 2022-02-20
#modified: 2022-02-20
location: München
category: ["development"]
---

A student recently asked me how I managed to get the "Remote Development Extension Pack" provided by Microsoft to work with the open source software [VSCodium](https://vscodium.com)<!--more-->[^1]. The trick is underwhelming.

I have both Visual Studio Code (VS Code) and VSCodium installed on my machine. From the terminal:

```shell
~$ cd ~/.vscode-oss
~$ ln -s ../.vscode/extensions extensions
```

creates a symbolic link VSCodium will follow to initialize the extensions from the VS Code folder. This is much easier than compiling extensions into `.vsix` archives (when it is even possible). VS Code is now relegated to a mere store front I use to install extensions.

[^1]: While VSCodium is point to point VS Code (except the Microsoft telemetry and branding), it does not tap into the Microsoft license protected store. Instead, only a limited set of extensions are made available via the [Open VSX Registry](https://open-vsx.org).