---
layout: post
title:  "Geek XiaBB"
date:   2020-09-17 11:02:24
category: geek
---

### 2020-09-17

* 下面这个命令是在Powershell上面打印一个文件，并从中match一个关键词，用了正则表达式。
* Get-Content -Path ./autosave.xmi | Where-Object {$_ -match "View"}