# Git SSH 认证

&emsp;&emsp;Git SSH 认证包含局域网的 SSH 认证和 GitHub 的 SSH 认证两种类型，操作方法大同小异。

&emsp;&emsp;GitHub 的 SSH 认证已经包含权限控制，可以放心使用；局域网的 SSH 认证不具备权限控制，Do not be evil !

&emsp;&emsp;如果您不太了解SSH登录的原理，请先百度或谷歌“ssh密钥认证原理”

&emsp;&emsp;**特别提醒：保护好您的私钥！！！**

&emsp;&emsp;**特别提醒：保护好您的私钥！！！**

&emsp;&emsp;**特别提醒：保护好您的私钥！！！**

***

下面介绍如何使用 Git 的 SSH 认证，总共只需三步：

### 一  、生成密钥

1. 首先需要进入 bash 环境（命令解析器，Windows下为 ```cmd``` ）
    
    * 在 Windows 操作系统上，进入 Git 安装目录，默认是 ```C:\Program Files\Git``` 。运行```git-bash.exe```会进入一个 Git 的 ```bash```环境 。

    * Mac 和 Linux 直接打开终端即可。

2. 输入下面的命令，其中的 E-Mail 地址使用您自己的邮箱地址
```
cd ~/.ssh
rm * -rf
ssh-keygen -t rsa -C "youremail@youremail.com"
```
命令需要3个确认，直接回车即可。其中第2和第3次是设定密钥的加密密码，一般不需要设置。返回的信息大概是：
``` 
Generating public/private rsa key pair.
Enter file in which to save the key (/home/sog/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/sog/.ssh/id_rsa.
Your public key has been saved in /home/sog/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:WpCaiWXDNV3CW+u0vZz8oXbGbyLA+kH85kkX5XemasE youremail@youremail.com
The key's randomart image is:
+---[RSA 2048]----+
|      oo...      |
|   . . oo..      |
|    = o  o .    .|
|   + = ...o    o |
|  . +   S+o+  . =|
|       o .=.E  +o|
|      .  ..++=+  |
|        .  =O==..|
|         ..o==.+.|
+----[SHA256]-----+
```

3. 好了，您已经创建了一对```rsa```密钥。其中包含两个文件：

    * id_rsa.pub ： 公钥文件
    
    * id_rsa ： 私钥文件，一定要保护好，打死都不要告诉别人

4. 由于上面的```rsa```密钥是建立在当前账户下的，某些操作如重装系统或者删除当前账户会让这对密钥丢失，所以还是吧这两个文件复制一份到别的地方。


### 二、远程服务器和 GitHub 上配置公钥

为了让远程服务器或者 GitHub 通过 SSH 密钥识别您，需要在远程服务器上和 GitHub 上添加您的公钥。

1. 局域网的远程服务器上配置公钥（请将您的公钥发送给远程主机的管理员即可）

    在远程服务器相应账户主目录下的 ```.ssh``` 文件夹下建立```authorized_keys```文件

    ```
    touch ~/.ssh/authorized_keys
    ```

    然后**将用户的公钥**添加至这个文件里，一行一个。

2. GitHub 上配置公钥

    登录 GitHub 后，右上角点击进入【Settings】->【SSH and GPG keys】，或者直接进入 https://github.com/settings/keys 。点击【New SSH key】,在下面的框内输入 Title (意义不大，用于区分Key) 和 Key (**第二步中生成的公钥文件的内容**)，点击【Add SSH Key】即可
![GitHub 上配置公钥](/image/github_ssh_rsa.jpg)

### 三、使用SSH 认证

前两个步骤已经生成了```rsa```密钥，并将其中的公钥存储在了局域网的远程服务器上或 GitHub 上。下面介绍下如何使用。

首先，验证 SSH 。

在```bash```环境中输入以下测试命令测试局域网内的远程服务器
```
ssh -T git@192.168.1.200
```
大概返回如下信息：
    
```
The authenticity of host '192.168.1.200 (192.168.1.200)' can't be established.
ECDSA key fingerprint is SHA256:aYWwCcueF8LxdJwyL1PPTSQduoY5nV2kbVqN4+o0WJ0.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '192.168.1.200' (ECDSA) to the list of known hosts.
Welcome to Ubuntu 16.04.1 LTS (GNU/Linux 4.4.0-47-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

9 个可升级软件包。
0 个安全更新。

fatal: Interactive git shell is not enabled.
hint: ~/git-shell-commands should exist and have read and execute access.

```

如果配置不正确会要求您输入密码：

```
git@192.168.1.200's password:
```

在```bash```环境中输入以下测试命令测试连接 GitHub 

```
ssh -T git@github.com
```

大概返回如下信息：
```
The authenticity of host 'github.com (192.30.253.113)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
Hi chucklvip! You've successfully authenticated, but GitHub does not provide shell access.

```

如果配置不正确此处会弹出帐号密码输入窗口或者提示
```
Permission denied (publickey).
```

测试成功后，正常使用 Git 即可，使用方法和原先一样，只是少了输入账号密码的操作。

再次提醒：**保护好您的私钥！！！**


### 补充说明

GUI工具可以不识别 Git 创建的密钥，需要根据实际情况处理。比如默认情况下TortoiseGit使用putty作为远程连接的工具，只识别ppk格式的私钥（SSH认证会用到私钥）。

请按下面的方式设置TortoiseGit，让其识别 Git 创建的密钥。

单机右键菜单，点击【TortoiseGit】->【Settings】->【Network】，在Network设置界面将SSH客户端更改为“ssh.exe”，如下图所示：
![TortoiseGit的SSH客户端](/image/TortoiseGit_ssh.jpg)




