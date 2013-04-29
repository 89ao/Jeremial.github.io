--- 
layout: post
title: helloworld
wordpress_id: 1
wordpress_url: http://ISayMe.com/?p=1
date: 2011-03-24 11:57:09 +08:00
tags: [Linux]
---
[![null](http://i.imgur.com/4aOcS.png "Hosted by imgur.com")](http://i.imgur.com/4aOcS.png)

grub2是ubuntu的默认引导工具,但是却不是最漂亮的引导工具.我们知道ubuntu是可以高度自定义化的,这次我们就要教你怎么让你的引导工具更漂亮.

我们需要利用一个叫做[BURG](http://www.burgloader.com/)的附加工具,它是一款由Bean制作的基于grub的创新性的通用型引导工具.它有很多漂亮但GUI,支持主题还有自定义.

**安装BURG**

首先添加PPA源.打开终端,输入如下命令

    sudo add-apt-repository ppa:bean123ch/burg && sudo apt-get update
    
[![](http://i.imgur.com/Ey9UG.png)](http://i.imgur.com/Ey9UG.png)

完成以后,打开新立德软件包管理器,搜索 burg,然后标记,以便安装.

[![](http://i.imgur.com/WQ0yP.png)](http://i.imgur.com/WQ0yP.png)

**注意,建议使用新立德安装burg,以免使用终端安装时出现错误**

在安装的过程中,你会遇到设置窗口.出现第一个窗口时,什么都不要做,直接下一步.

[![](http://i.imgur.com/ldBt8.png)](http://i.imgur.com/ldBt8.png)

第二个窗口时你需要告诉burg安装在什么地方.选择你的ubuntu的根驱动器,如果你有/boot目录的话,就选择/boot目录.

[![](http://i.imgur.com/HCf2T.png)](http://i.imgur.com/HCf2T.png)

最后一件事就是确保burg能够正常启动,打开终端输入如下命令.

    sudo update-burg

这样安装和设置就结束了.重启机器后 引导工具就会被burg替代.在引导菜单画面时,按下F1获得帮助和其他菜单,按下F2查看主题列表,按下F3更改屏幕分辨率.

[![](http://i.imgur.com/7Kl5E.png)](http://i.imgur.com/7Kl5E.png)

**安装 主题**

这是burg的最好的一个特点.你可以在任何时间安装主题.仅仅需要下载一个文件,然后复制到/boot/burg/themes.首先,从<http://gnome-look.org/>下载主题.但是很遗憾的是,在gnome-look.org侧栏上并没有burg的标签,所以你需要使用搜索栏寻找主题.当然你也可以使用google来寻找主题.下载之后,复制到 /boot/burg/themes
    
    sudo cp *PathToFile*/Fortune-BURG-v03.tar.gz /boot/burg/themes

[![](http://i.imgur.com/vJrd3.png)](http://i.imgur.com/vJrd3.png)

根据你的安装位置和下载文件进行命令调整即可.完成之后执行一下命令.

    sudo update-burg

新主题已经安装完毕,你可以重启之后按F2进行选择.

现在你的引导菜单已经有了漂亮的主题啦~~

参考文章[来源](http://www.howtogeek.com/howto/45164/how-to-customize-the-ubuntu-bootloader-screen/)