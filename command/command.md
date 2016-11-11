# 第二章 GitBook 命令解析

&emsp;&emsp;GitBook 提供了众多命令行的命令, 方便用户通过命令行操作GitBook。

&emsp;&emsp;GitBook 常用命令有以下几个: init(初始化书籍), install(安装插件), serve(本地服务), build(生成书籍) 等各种命令。本章将详细解析这几个常用命令。

***
#### 获取 GitBook 系统命令
在命令行下键入如下命令可以获取到GitBook的所有**系统命令**
```
gitbook --help
```

返回以下信息
```
Usage: gitbook [options] [command]

Commands:

ls                        List versions installed locally
current                   Display currently activated version
ls-remote                 List remote versions available for install
fetch [version]           Download and install a <version>
alias [folder] [version]  Set an alias named <version> pointing to <folder>
uninstall [version]       Uninstall a version
update [tag]              Update to the latest version of GitBook
help                      List commands for GitBook
*                         run a command with a specific gitbook version

Options:

-h, --help               output usage information
-v, --gitbook [version]  specify GitBook version to use
-d, --debug              enable verbose error
-V, --version            Display running versions of gitbook and gitbook-cli


```

系统命令不常用，功能也简单，这里不做翻译了。

***
#### 获取 GitBook 命令
在命令行下键入如下命令可以获取到GitBook的所有**GitBook 命令**
```
gitbook help
```
将返回以下信息
```
build [book] [output]       生成一本书
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)
    --format                生成图书格式 (默认生成网站;可生成网站,JSON,电子书)
    --[no-]timing           打印定时调试信息 (默认不打印)

serve [book] [output]       生成在线图书预览服务
    --port                  图书预览服务的端口号 (默认是 4000)
    --lrport                对于livereload服务器监听端口 (默认为35729)
    --[no-]watch            启用/禁用文件监控和自动加载 (默认为启用)
    --[no-]live             启用/禁用自动加载 (默认为启用)
    --[no-]open             启用/禁用在浏览器打开书籍 (默认为禁用)
    --browser               指定打开书的浏览器 (默认为未指定)
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)
    --format                生成图书格式 (默认生成网站;可生成网站,JSON,电子书)

install [book]              安装所有的插件依赖包
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)

parse [book]                解析和打印关于书的调试信息
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)

init [book]                 创建一个图书样板 (创建SUMMARY.md和README.md文件)
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)

pdf [book] [output]         生成 pdf 图书
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)

epub [book] [output]        生成 epub 图书
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)

mobi [book] [output]        生成 mobi 图书
    --log                   显示调试日志级别 (默认为info;可用debug, info, warn, error, disabled)
```

