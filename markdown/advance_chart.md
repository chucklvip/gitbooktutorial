# Markdown 语法 - 进阶功能之图表

&emsp;&emsp;进阶功能主要是指需要通过插件实现的功能。准确来讲这部分不属于 Markdown 语法的内容，但是和Markdown 语法内容比较接近，故而放到这一章节。

&emsp;&emsp;进阶功能主要包含表格、视频、图表、流程图等部分。

&emsp;&emsp;本节是进阶功能的图表部分。

***

* 使用插件：gitbook-plugin-chart

* 图表库：使用 C3.js 或者 Highcharts

* 使用方法：


1. 引入 gitbook-plugin-chart 插件，在后面第六章会讲到

2. 配置图表插件，使用 C3.js 或者 Highcharts (在 book.json 中使用如下配置，具体使用方法参考第六章)
```
{
    "pluginsConfig": {
        "chart": {
            "type": "highcharts"
        }
    },
}
```
```type``` 取值为 ```c3``` 或 ```highcharts```，默认是```c3```

3. 使用。在 Markdown 文件中调用代码（**注意：实际使用时要将代码的 chart 标签中的【@】符号全部替换成【%】**）：
```
{@ chart %}
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 250],
            ["data2", 50, 20, 10, 40, 15, 25]
        ],
        "axes": {
            "data2": "y2"
        }
    },
    "axis": {
        "y2": {
            "show": true
        }
    }
}
{@ endchart %}
```
实际效果如下：
{% chart %}
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 250],
            ["data2", 50, 20, 10, 40, 15, 25]
        ],
        "axes": {
            "data2": "y2"
        }
    },
    "axis": {
        "y2": {
            "show": true
        }
    }
}
{% endchart %}
 
两种图表库的具体使用方法(数据格式)请参照其官网的例子

* https://github.com/csbun/gitbook-plugin-chart

* http://c3js.org/examples.html

* http://www.highcharts.com/demo


