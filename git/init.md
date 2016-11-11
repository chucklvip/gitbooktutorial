# 获取 Git 仓库

***

### 从远程仓库开始之局域网内的 Git 仓库

&emsp;&emsp;如果需要用到远程仓库，即需要共享项目，建议使用这种方式建立远程仓库并用它建立本地仓库。具体步骤如下：

1. 在局域网内的服务器上，建立远程仓库，命令为（记得上一节的简单约定哦）:
```
cd /mnt/nfs/chucklvip
git init --bare mygit.git
```
返回如下提示：
```
初始化空的 Git 仓库于 /mnt/nfs/chucklvip/mygit.git/
```
以上命令建立了一个名为 mygit.git 的 Git 远程仓库，目录的实际路径为 /mnt/nfs/chucklvip/mygit.git 。命令中的仓库目录地址也可以使用绝对路径。

2. 在本地主机上克隆刚才建立的 Git 项目，命令为：
```
cd d:/git
git clone git@192.168.1.200:/mnt/nfs/chucklvip/mygit.git
```
提示输入密码，输入 git账户的密码654321， 返回提示
```
Cloning into 'mygit'...
git@192.168.1.200's password:
warning: You appear to have cloned an empty repository.
Checking connectivity... done.
```
    * 这一步骤可以使用 Git 的GUI工具。如TortoiseGit 是点击右键，选择【 Git Clone 】菜单，填写相关信息即可克隆一个远程仓库到本地。
![](/image/git_clone.jpg)
    * 命令实际还有很多可选参数。如在上述命令后面加上路径，即可指定本地仓库的路径。具体参数可以使用 git clone 的帮助命令查看: ```git clone --help```

&emsp;&emsp;通过以上两步既建立了远程仓库，又从远程仓库建立了本地仓库。**如果使用 Github 作为远程仓库，上面的步骤又该如何呢？**

***
### 从远程仓库开始之 Github 上的 Git 仓库

1. 登录 Github

2. 进入首页 https://github.com ，点击【 Start a project】创建一个 Git 项目

3. 如下图所示，输入仓库名 mygit ，点击下方的【 Create repository 】按钮即可创建一个 mygit 的仓库
![](/image/github_create_repo.jpg)

4. 建完远程仓库后提示如下图所示![](/image/github_create_step2.jpg)

5. 上面第4步可以看到，有几种方法可以和 Github 上的远程仓库建立联系。我们选择最简单的克隆方式，其他几种后面还会讲到。使用命令或者GUI工具进行克隆：
```
cd d:/git
git clone https://github.com/chucklvip/mygit.git
```
返回提示
```
Cloning into 'mygit'...
warning: You appear to have cloned an empty repository.
Checking connectivity... done.
```
上述命令中 Git 项目的地址有两种形式，https 和 ssh ,据说https比较稳定，建议使用https。当然，克隆命令和本节开始克隆局域网的 Git 项目用法一样。

***
### 从本地仓库开始之局域网内的 Git 仓库
&emsp;&emsp;如果一开始没有共享项目的需求，可以考虑只建立本地仓库。具体步骤如下：

1. 在本机上输入建立 Git 仓库的命令：
```
cd D:\git
git init mygit
```
上述命令建立了一个名为 mygit 的本地仓库。如果使用 GUI 工具，可以先建立一个 mygit 的文件夹，进入文件夹后右击【 Git create repository here ... 】，即可将 mygit 文件夹初始化为一个空的本地仓库。如下图所示，空的本地仓库只有一个 .git 文件夹（这个文件夹什么意义呢？上一节讲过）。
![](/image/git_create_gui.jpg)
![](/image/git_create_file.jpg)

2. 上述步骤建立的是本地仓库，如果后期项目想要共享出去，该怎么做呢？很简单：
    * 在远程主机或 Github 上建立一个空的远程仓库，具体做法参照本节开始的【从远程仓库开始之局域网内的 Git 仓库】和【从远程仓库开始之 Github 上的 Git 仓库】相关内容。需要注意的是只建立空仓库就行了，不需要克隆到本地，因为本地已经有一个 Git 仓库了，只需要和远程仓库关联起来。

    * 使用 Git 命令关联两个仓库。和 Github 的远程仓库关联命令时一样的，只是更换下地址。
```
git remote add origin git@192.168.1.200:/mnt/nfs/chucklvip/mygit.git
git push -u origin master
```
    * 上述第一条命令可以将本地仓库和远程仓库关联起来，关联起来之后需要推送一次，将两边仓库的版本历史记录同步起来（第二条就是做了同步的工作，后面章节会具体讲到）。

    * 如果使用 GUI 工具，只需要**进入Git仓库目录**，开启右键菜单并依次点击【Tortoise Git】->【Setting】->【Git】->【Remote】进行设置。填写名称Remote和地址URL，确定即可。当然设置好后最好推送一次，使数据同步。
![](/image/git_add_remote.jpg)
![](/image/git_add_remote2.jpg)

