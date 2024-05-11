---
title: 在ubuntu系统中的摸索与重装系统
date: 2024-01-20 19:42:53
tags:
---

抱着去熟悉一下Linux操作系统的念头，我看了网络上很多装双系统的教程，先是虚拟机体验了以下Ubuntu系统，但是总是想自己也尝试用u盘作为启动盘来装双系统。

1. 下载镜像安装包

[ubuntu-20.04.6-desktop-amd64.iso](https://mirrors.tuna.tsinghua.edu.cn/ubuntu-releases/20.04/)

2. 制作启动U盘

我选择下载[rufus](https://rufus.ie/zh/#google_vignette)，启动软件制作启动U盘

之后重启开机时启动电脑Bios，把从U盘启动设置为优先项，然后U盘启动电脑，启动之后根据开机引导安装ubuntu系统到U盘即可

---

但我在安装Ubuntu系统时操作失误把我的固态硬盘格式化了导致我没有了Windows系统，而我的Ubuntu系统也没有成功安装，导致我没有操作系统可以用，我试图在试用的Ubuntu系统中制作Windows的启动U盘，但是很显然是成功不了的，windows的软件很多Ubuntu使用不了，而网络上关于Ubuntu的攻略相比而言少很多，几乎没有在Ubuntu系统中安装windows系统的攻略，我尝试下载wine从而让我安装windows软件，但输入代码安装很慢，甚至失败，我一时无措，将Windows系统映像写入U盘，由于我是试用的Ubuntu系统，而这时Ubuntu系统的启动盘也被破坏，我的电脑因为没有操作系统无法开机

没办法我只能去网吧下载windows系统和rufusU盘制作软件给我的电脑重装系统，重装后顺着引导遇到第一个麻烦，我没有以太网，只能shift+F10输入`OOBE\BYPASSNRO`之后重启则完成了，由于没有网络，不能安装驱动，也就无法连接WiFi，所以我用手机usb网络共享下载[驱动总裁](https://www.sysceo.com/software-softwarei-id-258.html)来自动安装驱动，wifi也就能连接了，之后也就是安装一些应用了，由于我重装的win11家庭版，所以登录之后就自动激活系统，省去一些密钥激活的过程，我一开始听信一些博主的话差点装了专业版，幸好并没有直接使用网络上的一些密钥，不然以后会多很多麻烦。
