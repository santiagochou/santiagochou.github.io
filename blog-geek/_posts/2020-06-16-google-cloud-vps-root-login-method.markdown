---
layout: post
title:  "Google Cloud VPS Root Login Method"
date:   2020-06-16 19:08:24
category: geek
---

1、进入root账户。然后passwd root设置root密码。
2、修改SSH配置文件/etc/ssh/sshd_config

```Shell
 vim /etc/ssh/sshd_config
```

* 找到PermitRootLogin和PasswordAuthentication

```Shell
# Authentication:
LoginGraceTime 120
PermitRootLogin yes //默认为no，需要开启root用户访问改为yes
StrictModes yes
 
# Change to no to disable tunnelled clear text passwords
PasswordAuthentication yes //默认为no，改为yes开启密码登陆
```

3、重启SSH服务使修改生效

```Shell
/etc/init.d/ssh restart
```