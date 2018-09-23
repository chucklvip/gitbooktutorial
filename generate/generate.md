# GitBook 生成书籍

&emsp;&emsp;前面章节我们了解到使用 GitBook 可以生成 pdf 等格式的电子书，本章介绍下具体的操作（使用 GitBook 的命令行下工具）。

更加详细的命令可以参阅第二章第 3 节和第 4 节 [《构建图书命令 build 》](/command/build.md) 和 [《其它重要命令》](/command/others.md)

***

### 生成 website（即 html ）

```

gitbook build tbook

```
        上述命令会在项目 tbook 下生成 【_book】文件夹，里面就是 tbook 的 html 格式电子书。


***

### 生成 pdf

```
gitbook pdf tbook tbook.pdf

```
        上述命令会在项目 tbook 下生成 【tbook.pdf】 的 pdf 文档。
        
        如果该命令 gitbook pdf 后的两个参数使用自己的路径，则会在相应路径生成 pdf 文档。

***

### 生成 epub

```
gitbook epub tbook tbook.epub

```

***

### 生成 mobi

```
gitbook mobi tbook tbook.mobi

```