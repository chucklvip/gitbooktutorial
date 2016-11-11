# Node.js的安装

简单的说 Node.js 就是运行在服务端的 JavaScript。

Node.js 是一个基于Chrome JavaScript 运行时建立的一个平台。

Node.js是一个事件驱动I\/O服务端JavaScript环境，基于Google的V8引擎，V8引擎执行Javascript的速度非常快，性能非常好。

扯得有点远，总之，GitBook 需要 Node.js 环境。

## 下面开始安装：

---

**Windows平台**

1. 下载安装包。前往 [Node.js 官网下载处](https://nodejs.org/en/download)，根据自己的操作系统版本下载32位或者64位的安装包（msi格式的）。笔者使用的是64位的Windows10，所以下载的是 “64-bit” 的 “
  Windows Installer \(.msi\)” 安装包，具体地址是 [https://nodejs.org/dist/v6.9.1/node-v6.9.1-x64.msi](https://nodejs.org/dist/v6.9.1/node-v6.9.1-x64.msi)

2. 安装 Node.js。安装刚才下载的 “node-v6.9.1-x64.msi”，一路 “Next” 下去就装好了。


---

**Mac平台**

Mac OS 系统自带 node.js ,其中 **El Captain** 的 node.js  版本为V4.4.7

如果想升级的话，可以从node.js官网下载 Mac OS 版本的安装包 \(.pkg文件\) 安装更新。

---

**Linux平台**
虽然Linux下也可以从官网下载安装，但是最简单的还是从软件仓库里安装啦。

终端下运行:

### 代码块

```bash
sudo apt-get update
sudo apt-get install npm -y
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

上面的命令解释下：

第一条更新源；

第二条从软件仓库安装npm，也会安装上Node.js。单独安装node.js可能不会安装npm [^注1]。

第三条让node命令和nodejs命令同时起作用[^注2]

如果想升级的话，可以从node.js官网下载 Linux 版本的二进制包升级安装。

---

## Node.js 安装测试

* 检查 Node.js 是否安装成功

```bash
node -v
```

输出以下内容（不同平台版本号可能不一样，这里用“x”代替）:

```bash
v x.x.x
```

* 新建test.js文件，写入内容【console.log\('Node.js Environment'\);】（大括号中的内容不包含大括号，代码的意思是在控制台打印一句“Node.js Environment”）
* 运行 test.js 文件

```bash
node test.js
```

输出以下内容:

```bash
Node.js Environment
```

---

[^注1]:npm 是随同 Node.js 一起安装的包管理工具，能解决 Node.js 代码部署上的很多问题。 新版的 Node.js 已经集成了npm，但是ubuntu 14.04 的软件仓库中node.js版本较低，没有集成npm，所以需要单独安装。

[^注2]：安装完测试时发现node命令没有，试试nodejs可以，于是有了这个命令

