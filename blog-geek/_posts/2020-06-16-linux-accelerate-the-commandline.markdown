---
layout: post
title:  "Linux Accelerate the Command-line"
date:   2020-06-16 19:02:24
category: geek
---
参考1:https://www.sundabao.com/ubuntu%E4%BD%BF%E7%94%A8shadowsocks/

参考2:https://freefq.com/firefox/2018/05/27/switchyomegafirefox.html

参考3:https://blog.fazero.me/2015/08/31/%E5%88%A9%E7%94%A8proxychains%E5%9C%A8%E7%BB%88%E7%AB%AF%E4%BD%BF%E7%94%A8socks5%E4%BB%A3%E7%90%86/

参考4:https://blog.csdn.net/jiezhi2013/article/details/50624561

First step: Install ss.
for ubuntu install the shadowsocks on computer by run commands below.

sudo apt install shadowsocks
then, we test the installation of the shadowsocks by run:

sslocal --help
now, we comfigure the shadowsocks.json like that showing follow.

{
    "server":"11.22.33.44",
    "server_port":50003,
    "local_port":1080,
    "password":"123456",
    "timeout":600,
    "method":"aes-256-cfb"
}

and then you should put the line below to your ~/.bashrc file.

alias runss="sslocal -c your-file-folder/shadowsocks.json"
and source it to enable this line.

Now, the shadowsocks are installed and configured.

Second step: test ss on firefox.
add extension  Proxy SwitchyOmega on your firefox explorer, and comfigure a proxy like that.

SOCKS5 127.0.0.1 1080
and then push the Apply changes, I always forgot it.

Done it !

Third step: install the proxychains on compute.
now,install the proxychains follow commands below, us super user to make and make install will success build the program.

sudo apt install g++ -y
sudo apt install git -y
sudo apt install make -y
git clone https://github.com/rofl0r/proxychains-ng.git
cd proxychains-ng
./configure
sudo su 
make && make install
cp ./src/proxychains.conf /etc/proxychains.conf
then,we configure the proxychains by.

vim /etc/proxychains.conf
and change the last line of 

socks4  127.0.0.1 9050

to

socks5 127.0.0.1 1080
now, change user by su user and then we append the follow line to ~/.bashrc.

alias pc="proxychains4"
don't forget to source it.now, you can accelerate your command by add pc prior on your inputed line ,e.g.

pc wget http://xxx.com/xxx.zip

then, we complete the whole process. Enjoy it !