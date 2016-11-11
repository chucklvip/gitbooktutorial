# 安装 GitBook

&emsp;&emsp;GitBook 已经在前面介绍过了，这里只讲它的安装。

&emsp;&emsp;安装 GitBook 很简单，需要在命令行下完成。三个平台打开命令行的方式不太一样，但是都很简单，这里不再赘述，如有不懂命令行/终端的请自行百度或Google一下。

***

&emsp;&emsp;下面是具体的安装命令，三个平台都是一样的。

1. 确保已经安装 Node.js，并且有相应的 npm 包管理工具 （参见[本章 1.1 节][1]内容）

2. 在命令行/终端键入如下命令安装 GitBook
```
npm install gitbook-cli -g
```
```
gitbook -V
```
或者(因为Linux 及Mac可能需要管理员权限)
```
sudo npm install gitbook-cli -g
```
```
gitbook -V
```
      上述命令中第一条是预安装，第二条通过查看 GitBook 版本才开始真正的安装。执行完后就可以看到安装的 GitBook版本

3. 安装“ebook-convert”插件。Git在生成 pdf 和 epub 格式的电子书时需要用到一款 “ebook-convert” 的插件，所以这款插件是必装的插件。安装“ebook-convert”插件到官网[https://calibre-ebook.com/download][2]下载安装即可（所有的下载及安装在下载页面有详细说明）。具体为：
    * Windows 版请下载相应的安装包安装。如笔者是下载64位的calibre-64bit-2.70.0.msi安装的。
    * Mac OS 用户同样是下载安装即可。如笔者是下载calibre-2.70.0.dmg安装的。
    * Liunx 用户使用下面的命令行安装（下载页面有详细说明）：
            sudo -v && wget -nv -O- https://raw.githubusercontent.com/kovidgoyal/calibre/master/setup/linux-installer.py | sudo python -c "import sys; main=lambda:sys.stderr.write('Download failed\n'); exec(sys.stdin.read()); main()"

***
至此，GitBook也安装完毕。下一章节介绍安装 **GitBook Editor**。

[1]:nodejs.md
[2]:https://calibre-ebook.com/download