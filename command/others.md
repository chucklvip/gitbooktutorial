# 其它重要命令

***

&emsp;&emsp;上一节介绍了 build 命令，用于生成网页版本的电子书。开篇已经介绍过，GitBook 还可以制作 pdf、epub、mobi 等格式的电子书，下面介绍如何生成这几种电子书。

##### 命令格式
```
gitbook pdf [book] [output] --log
gitbook epub [book] [output] --log
gitbook mobi [book] [output] --log

```
上述3条命令分别可以生成pdf、epub、mobi三种格式的电子书。可以看到这几条命令格式很相近，也和上一节中的 build 命令比较接近。


### 使用方法
**特别提醒：**生成 pdf/epub/mobi 需要用到 **ebook-convert** 插件，请按照【[安装 GitBook ][1]】章节介绍，先安装好  **ebook-convert** 插件。
```
gitbook pdf ./tbook tbook.pdf --log debug
gitbook epub ./tbook tbook.epub --log debug
gitbook mobi ./tbook tbook.mubi --log debug

```
上面3条命令将电子书 tbook 分别转换成了 tbook.pdf 、tbook.epub、tbook.mubi。

这几条命令后面都是3个参数，都是可选参数，其意义分别为：

* 原图书路径[book]：建议使用绝对路径

* 转换后的电子图书路径和名称[output]：同样建议使用绝对路径

* 日志级别 --log ：日志的级别可用debug、info、 warn、error、disabled，这里是debug


[1]:/base/gitbook.md