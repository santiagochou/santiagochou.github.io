---
layout: post
title:  "Geek XiaBB"
date:   2020-09-17 11:02:24
category: geek
---



### 2021-07-12

* 树立算法工程师和软件工程师，以及后面的会计师思想。用knowledge去解决问题。
* 猜想和证明是数学的本质。用分析的出来猜想，再用归纳来进行证明。
* 数学是一个实操的学问。

### 2021-04-29

* 构建软件的一般思路：
  * 先搭建骨架，再添加神经，最后补充血肉。

### 2021-01-06

* 在目录里递归查找关键字： ``` Select-String (Get-ChildItem -Recurse -Include "*" | ?{$_.Name -like "*"}) -pattern "PRESCRAM"  ```
* 在目录里递归查找文件名： ``` "Get-ChildItem -Recurse -Include *prcdata*" ```

### 2020-11-18

* I needed to check whether a DLL with particular name is registered and I used this command in my BAT: [ref](https://serverfault.com/questions/576831/how-do-i-know-if-a-dll-is-registered)

``` powershell
reg query HKLM\SOFTWARE\Classes /s /f whatever.dll
if errorlevel 1 goto DLL_MISSING
```

* If with errorlevel sent control to the label whenver reg query found nothing. You may need to change the part of the registry where you search (in my case HKLM'..., the more specific path the faster, otherwise it takes really long).

* The output can be processed if necessary, GUID for the entry can be obtained, but that is out of scope of reg query command.

### 2020-10-07

* git使用proxy,参考[该页面](https://gist.github.com/laispace/666dd7b27e9116faece6),该命令使用了v2ray软件建立的socket通道。使用时将端口替换成代理服务器相应的端口。v2rayN软件可以导出配置文件，从配置文件中找出相应的端口号。

```git
git config --global http.proxy 'socks5://127.0.0.1:1080'
```

### 2020-09-17 Second

* 在PowerShell播放音乐的命令如下：

``` powershell
Get-ChildItem -Name | Where-object { ffplay $_ -nodisp -autoexit}
```

``` powershell
$arr =@(".\Joel Santos feat Foundeur (BACHATA) - Por Que.mp3", ".\Los ángeles Azules - Acarí?ame feat. Julieta Venegas, Juan Ingaramo, Jay de la Cueva.mp3", ".\Shawn Mendes, Camila Cabello - Se?orita (DJ Tronky Bachata Remix).mp3", ".\Tito el Bambino,Daddy Yankee - Chequea CoI mo Se Siente.mp3")
for ($i=0;$i -lt $arr.Length; $i++) {ffplay $arr[$i] -nodisp -autoexit}
```

### 2020-09-17 First

* 下面这个命令是在Powershell上面打印一个文件，并从中match一个关键词，用了正则表达式。

``` powershell
Get-Content -Path ./autosave.xmi | Where-Object {$_ -match "View"}
```