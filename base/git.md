# Git 和 相关 GUI 安装

&emsp;&emsp;Git是一款免费、开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。[^注1]

### 不同平台的Git及其GUI（图形界面）安装如下：
***
#### Windows系统

1. 前往Git官网下载。地址为 [https://git-scm.com/download/win][1]。浏览器会自动下载相应的版本，如未自动下载，请手动下载32位或64位的 Git 。笔者这里下载的是【Git-2.10.1-64-bit.exe】。
2. 安装Git。安装下载的Git，如Git-2.10.1-64-bit.exe。一路【Next】就行，如果知道相关的安装选项有什么用可以自行设定。
3. 下载TortoiseGit 。TortoiseGit是Git的Windows版GUI客户端，初学者可以很方便的通过它使用Git。同样的，请根据自己的操作系统版本下载32位或64位的安装包。下载地址是[https://tortoisegit.org/download][2]。笔者下载的是【TortoiseGit-2.3.0.0-64bit.msi】
4. 安装TortoiseGit。安装下载的TortoiseGit，如TortoiseGit-2.3.0.0-64bit.msi。安装也是一路【Next】就行，如果知道相关的安装选项有什么用可以自行设定。

***
#### Mac OS 系统

1. 前往Git官网下载。地址为 [https://git-scm.com/download/mac][3]。浏览器会自动下载相应的版本，如未自动下载，请手动下载Git 。笔者这里下载的是【git-2.10.1-intel-universal-mavericks.dmg】。

2. 安装Git。安装刚才下载的Git，如git-2.10.1-intel-universal-mavericks.dmg。可能需要到【系统偏好设置】的【安全与隐私】里面对Git的安装柏解除锁定才能安装。

3. 下载SourceTree。SourceTree是OS X下免费的Git客户端。官网是[https://www.sourcetreeapp.com][4]。官网首页就有下载链接，请下载安装包。笔者下载到的是【SourceTree_2.3.1.zip】。

4. 安装SourceTree。安装下载的SourceTree，如SourceTree_2.3.1.zip。

#### Linux 系统
***
1. 安装Git。从软件仓库安装即可。具体可以参考[https://git-scm.com/download/linux][5]
```bash
sudo apt-get install git -y
```
2. 使用Linux的用户不推荐使用GUI的客户端了。高手都是用命令行的！如果有需要，可以在[ Git 官网 ][6]查看到相关的 GUI 推荐。




[1]:https://git-scm.com/download/win
[2]:https://tortoisegit.org/download
[3]:https://git-scm.com/download/mac
[4]:https://www.sourcetreeapp.com
[5]:https://git-scm.com/download/linux
[6]:https://git-scm.com/downloads/guis


***

[^注1]:Git（官方网站）


