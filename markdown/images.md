# Markdown 语法 - 图片

***

很明显地，要在纯文字应用中设计一个「自然」的语法来插入图片是有一定难度的。

Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。 

##### 行内式的图片

```
![显示百度首页Logo](https://www.baidu.com/img/bd_logo1.png)

![显示百度首页](https://www.baidu.com/img/bd_logo1.png "百度Logo") 

```

详细叙述如下：
*    一个惊叹号 !
*    接着一个方括号，里面放上图片的替代文字
*    接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。


![显示百度首页Logo](https://www.baidu.com/img/bd_logo1.png)

![显示百度首页Logo](https://www.baidu.com/img/bd_logo1.png "百度Logo")


##### 参考式的图片

参考式的图片语法则长得像这样：
```
![Alt text][id]
```

\[id\] 是图片参考的名称，图片参考的定义方式则和链接参考一样：
```
[id]: url/to/image  "Optional title attribute"
```
具体实例如下：
![显示百度首页Logo][1]


[1]:https://www.baidu.com/img/bd_logo1.png "百度Logo"
