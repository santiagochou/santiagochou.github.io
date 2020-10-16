---
layout: post
title:  "FRP Self-Starting in Windows 10"
date:   2020-10-16 15:02:24
category: geek
---
* Reference:
  * https://blog.csdn.net/leadseczgw01/article/details/103298118
  * https://blog.csdn.net/a873744779/article/details/102933229

#### First step: Create start.bat under the frp directory:

for ubuntu install the shadowsocks on computer by run commands below:

```Shell
@echo off
if "%1" == "h" goto begin
mshta vbscript:createobject("wscript.shell").run("""%~nx0"" h",0)(window.close)&&exit
:begin
D:\frp_0.29.0\frpc.exe -c D:\frp_0.29.0\frpc.ini
```



#### Second step: Move the shortcut of the start.bat to Windows 10 StartUp directory:

Create a shortcut of the `start.bat`, and move it StartUp directory as showing below.

```shell
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp
```

Done!
