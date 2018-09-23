# Markdown 语法 - 进阶功能之视频

&emsp;&emsp;进阶功能主要是指需要通过插件实现的功能。准确来讲这部分不属于 Markdown 语法的内容，但是和Markdown 语法内容比较接近，故而放到这一章节。

&emsp;&emsp;进阶功能主要包含表格、视频、图表、流程图等部分。

&emsp;&emsp;本节是进阶功能的视频部分。

***

##### GitBook 嵌入视频1 - H5视频

* 使用插件：gitbook-plugin-local-video

* 视频类型：HTML5 video 标签支持的视频格式，最终与浏览器等有关

* 使用方法（**注意：实际使用时要将代码的raw标签中的【@】符号全部替换成【%】**）：
```
{@% raw %}
<video id="video-demo" class="video-js" controls preload="auto" width="100%" poster="/image/vodeo.jpg" data-setup="{'aspectRatio':'16:9'}">
    <source src="http://www.runoob.com/try/demo_source/mov_bbb.mp4" type="video/mp4">
    <source src="http://www.runoob.com/try/demo_source/mov_bbb.ogg" type="video/ogg">
    <p class="vjs-no-js">您的浏览器不支持 HTML5 video 标签。</p>
</video>
{@% endraw %}
```

* 插件效果：

{% raw %}

<video id="video-demo" class="video-js" controls preload="auto" width="100%" 
poster="/image/vodeo.jpg" data-setup='{"aspectRatio":"16:9"}'>

    <source src="http://www.runoob.com/try/demo_source/mov_bbb.mp4" type="video/mp4">

    <source src="http://www.runoob.com/try/demo_source/mov_bbb.ogg" type="video/ogg">

    <p class="vjs-no-js">您的浏览器不支持 HTML5 video 标签。</p>

</video>

{% endraw %}


##### GitBook 嵌入视频2 - Youtube视频

* 使用插件：gitbook-plugin-youtubex

* 视频类型：Youtube上的视频

* 使用方法（**注意：实际使用时要将代码的raw标签中的【@】符号全部替换成【%】**）：
```
{@youtube%}视频ID{@endyoutube%}
```

* 插件效果：

视频地址：https://www.youtube.com/watch?v=JxerE4Bysts

{%youtube%}JxerE4Bysts{%endyoutube%}








