# 图书预览命令serve

&emsp;&emsp;serve 服务是将书籍转换为静态网页，并建立一个简单的http服务器，供用户在线查看预览图书。当用户选择的图书没有生成静态网站时，调用 serve 会自动在该书籍目录下生成 _book 文件夹并生成静态页面。

***

##### 命令格式

```

serve [book] [output] --port --lrport --[no-]watch --[no-]live --[no-]open --browser --log --format

```

##### 使用方法

上面的命令看上去有点复杂，但是可以很简单的使用它：

1. 命令行或终端切换至图书根目录下

```

cd D:\git\tbook

```

2. 使用最简单的serve命令

```

gitbook serve

```

3. 返回以下信息

```

Live reload server started on port: 35729

Press CTRL+C to quit ...

info: 7 plugins are installed

info: loading plugin "livereload"... OK

info: loading plugin "highlight"... OK

info: loading plugin "search"... OK

info: loading plugin "lunr"... OK

info: loading plugin "sharing"... OK

info: loading plugin "fontsettings"... OK

info: loading plugin "theme-default"... OK

info: found 50 pages

info: found 48 asset files

info: >> generation finished with success in 5.9s !

Starting server ...

Serving book on http://localhost:4000

```

然后访问 http://localhost:4000 即可预览这本图书

其他参数也有特定的功能，请读者自行尝试。




