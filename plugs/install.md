# GitBook 插件

&emsp;&emsp;当我们在书籍中使用到一些第三方的内容或服务时，这时我们把这些东西称之为插件。

&emsp;&emsp;我们想要使用某种插件时，不仅需要在个性化文件 ```book.json``` 中配置插件，还需要安装插件。

***

##### 插件的配置

本书的个性化文件 ```book.json``` 中插件相关的配置如下：

```
"plugins": [
    "mathjax@1.1.2",
    "js-sequence-diagram",
    "mermaid",
    "github@1.0.2", 
    "splitter",
    "toggle-chapters",
    "sectionx",
    "donate",
    "image-captions",
    "chart",
    "github-buttons",
    "local-video",
    "youtubex"
],
"pluginsConfig": {
    "github": {
        "url": "https://github.com/chucklvip/gitbooktutorial"
    },
    "tbfed-pagefooter": {
        "copyright":"&copy chucklvip",
        "modify_label": "该文件修订时间：",
        "modify_format": "YYYY-MM-DD HH:mm:ss"
    },
    "donate": {
        "wechat": "https://www.chuckl.vip/images/wechat.png",
        "alipay": "https://www.chuckl.vip/images/alipay.png",
        "title": "",
        "button": "赏",
        "alipayText": "支付宝打赏",
        "wechatText": "微信打赏"
    },
    "image-captions": {
        "caption": "图 _PAGE_LEVEL_._PAGE_IMAGE_NUMBER_ - _CAPTION_"
    },
}
```

##### 插件的安装

官方推荐使用 ```gitbook install``` 自动安装相关的插件，但是这种方式安装的插件只对当前的项目有效。

下面介绍行之有效的插件安装方式 (命令行或终端下操作)，假设 GitBook 的版本是 3.2.2 ：

1. 进入到 GitBook 的安装目录的【node_modules】下

    * Windows 下使用下面的命令
    ```
    cd %UserProfile%/.gitbook/versions/3.2.2/node_modules
    ```

    * Mac 和Linux 系统使用下面的命令
    ```
    cd  ~/.gitbook/versions/`gitbook ls | grep \* | awk '{print $2}'`/node_modules
    ```

2. 使用 ```npm install gitbook-plugin-PLUGIN_NAME``` 安装插件，例如本书的这些插件可以使用下面的命令安装：

```
npm install gitbook-plugin-adbutler

npm install gitbook-plugin-algolia

npm install gitbook-plugin-chart

npm install gitbook-plugin-codesnippet

npm install gitbook-plugin-comment

npm install react react-dom gitbook-plugin-disqus

npm install gitbook-plugin-donate

npm install gitbook-plugin-emphasize

npm install gitbook-plugin-es6tabs

npm install gitbook-plugin-exercises

npm install gitbook-plugin-ga

npm install gitbook-plugin-gist

npm install gitbook-plugin-gistrun

npm install gitbook-plugin-github

npm install gitbook-plugin-github-buttons

npm install gitbook-plugin-hints

npm install gitbook-plugin-image-captions

npm install gitbook-plugin-infinitescroll

npm install gitbook-plugin-js-sequence-diagram

npm install gitbook-plugin-katex

npm install gitbook-plugin-latex-codecogs

npm install gitbook-plugin-local-video

npm install gitbook-plugin-mathjax

npm install gitbook-plugin-mermaid

npm install gitbook-plugin-mixpanel

npm install gitbook-plugin-puml

npm install gitbook-plugin-quizzes

npm install gitbook-plugin-scripts

npm install gitbook-plugin-sectionx

npm install gitbook-plugin-sitemap

npm install gitbook-plugin-splitter

npm install gitbook-plugin-styles-less

npm install gitbook-plugin-styles-sass

npm install gitbook-plugin-superscript

npm install gitbook-plugin-toggle-chapters

npm install gitbook-plugin-tonic

npm install gitbook-plugin-versions

npm install gitbook-plugin-youtube

npm install gitbook-plugin-youtubex

```

##### 插件列表

上面是一些比较常用和实用的插件，GitBook官方收录了400多个插件，可以在 GitBook 插件的官网找到。

https://plugins.gitbook.com

每一个插件都有相应的使用说明，按照相应的使用说明安装配置即可。

