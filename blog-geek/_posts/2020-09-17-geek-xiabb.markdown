---
layout: post
title:  "Geek XiaBB"
date:   2020-09-17 11:02:24
category: geek
---

### 2020-09-17 Second

* 在PowerShell播放音乐的命令如下：

``` powershell
$arr =@(".\Joel Santos feat Foundeur (BACHATA) - Por Que.mp3", ".\Los ángeles Azules - Acarí?ame feat. Julieta Venegas, Juan Ingaramo, Jay de la Cueva.mp3", ".\Shawn Mendes, Camila Cabello - Se?orita (DJ Tronky Bachata Remix).mp3", ".\Tito el Bambino,Daddy Yankee - Chequea CoI mo Se Siente.mp3")
for ($i=0;$i -lt $arr.Length; $i++) {ffplay $arr[$i] -nodisp -autoexit}
```

### 2020-09-17 First

* 下面这个命令是在Powershell上面打印一个文件，并从中match一个关键词，用了正则表达式。

``` powershell
Get-Content -Path ./autosave.xmi | Where-Object {$_ -match "View"}
```