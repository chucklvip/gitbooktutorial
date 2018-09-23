# GitBook 个性化及插件
&emsp;&emsp;个性化主要是对书籍的一些设置，比如设置书籍的标题，作者等等。插件是对 GitBook 功能的扩展。

***
&emsp;&emsp;个性化和插件都是在 ```book.json``` 文件中配置的，其中插件不仅需要配置还需要安装。下面分别介绍。

&emsp;&emsp;以下是本书的个性化和插件实际内容：
```
{
    "title": "GitBook 实战教程",
    "description": "本书将带您从零学习 GitBook, 让您成为写书高手",
    "author": "Chuck",
    "isbn": "9787000000001",
    "language": "zh-hans",
    "gitbook": ">= 3.2.2",
    "plugins": [
        "mathjax",
        "js-sequence-diagram",
        "mermaid",
        "github",
        "splitter",
        "toggle-chapters",
        "sectionx",
        "donate",
        "image-captions",
        "chart",
        "github-buttons",
        "local-video",
        "youtubex",
        "disqus",
        "katex",
        "exercises",
        "youtube"
    ],
    "styles": {
        "website": "styles/website.css"
    },
    "pluginsConfig": {
        "github": {
            "url": "https://github.com/chucklvip/gitbooktutorial"
        },
        "tbfed-pagefooter": {
            "copyright": "&copy chucklvip",
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
        }
    }
}
```
