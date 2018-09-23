GitBook 个性化

&emsp;&emsp;GitBook 会提供用户自定义书籍的设置，那么这个时候就需要我们在书籍的**根目录下创建一个名为 book.json 的文件***，该文件中存放的就是书籍个性化的设置。

***

个性化设置主要包含：

* title : 书名

* description : 简介，一般是一句话简介

* author : 作者

* isbn : isbn号

* language : 语言，如中文是"zh-hans" 

* gitbook : gitbook的版本

* plugins : 插件列表

* pluginsConfig : 插件的配置

* styles : 个性化的样式表配置

下面是本书的 ```book.json``` 个性化配置文件的部分内容

```
{
    "title": "GitBook 实战教程",
    "description": "本书将带您从零学习 GitBook, 让您成为写书高手",
    "author": "Chuck",
    "isbn" : "9787000000001",
    "language" : "zh-hans",
    "gitbook" : ">= 3.2.2",
    "plugins": [
        "mathjax",
        "github"
    ],
    "pluginsConfig": {
        "github": {
            "url": "https://github.com/chucklvip/gitbooktutorial"
        },
    },
    "styles":{
        "website": "styles/website.css"
    }
}


```