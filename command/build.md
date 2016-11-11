# 构建图书命令 build

构建图书命令 build 可以将图书构造格式化成各种各样的电子书格式，并生成相应的文件及结构目录。

***

&emsp;&emsp;构造的格式有:website(静态网站:默认),json(json 格式图书),ebook(ebook 格式图书)。

##### 命令格式

```

build [book] [output] --log --format --[no-]timing

```

##### 使用方法1

和前面的serve命令相似，首先切换至图书根目录

```

cd tbook

```

使用图书构建命令生成图书

```

gitbook build

```

返回的信息为

```

info: 7 plugins are installed

info: 6 explicitly listed

info: loading plugin "highlight"... OK

info: loading plugin "search"... OK

info: loading plugin "lunr"... OK

info: loading plugin "sharing"... OK

info: loading plugin "fontsettings"... OK

info: loading plugin "theme-default"... OK

info: found 50 pages

info: found 48 asset files

info: >> generation finished with success in 6.0s !

```

##### 使用方法2
这次将可选参数都用上，首先到书籍的上层目录，或者在build命令里面写绝对路径
```
cd ..
```

build命令
```
gitbook build tbook tbook2 --log debug --format json --timing

```
输出非常多，最终和 tbook 同一个目录下生成了 tbook2 的文件夹，里面是构建出来的json格式的图书。上述命令在 build 指令后有 5 个参数，分别表示：

* 原图书路径[ tbook ]，可以是绝对路径

* 转换后的电子书存放路径[ tbook2 ] ，可以是绝对路径，目录下不能有文件或目录，否则会被删除

* 日志级别[ --log debug ]，日志的级别可用debug、info、 warn、error、disabled，这里是debug

* 生成格式[ --format json ]，可生成网站(website),JSON(json),电子书(ebook),这里是JSON

* 是否打印定时调试信息 [ --timing ]，使用 --timing 或 --no-timing

后面四个参数都有默认值，所以可以不加这些参数。读者可根据实际需要调节。


