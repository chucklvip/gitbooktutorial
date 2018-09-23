# Markdown 语法 - 进阶功能之插件

&emsp;&emsp;进阶功能主要是指需要通过插件实现的功能。准确来讲这部分不属于 Markdown 语法的内容，但是和Markdown 语法内容比较接近，故而放到这一章节。

&emsp;&emsp;进阶功能主要包含表格、视频、图表、流程图等部分。

&emsp;&emsp;本节是进阶功能的表格部分，表格不需要插件。

***

表格非常简单，下面是两个示例

注意事项：

* GitBook 对 Markdown 表格的支持目前还不是特别好，一些高级特性如内容的排版(居中、居左等)还没有实现
 
* 代码中的表格排版和实际可以不一样，只需分隔符号符合要求就行。如代码中表格列之间不需要空格，实际效果是列宽度均分 

示例1

```
| Tables        | Are           | Cool  |
| ------------- |---------------| ------|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

```


| Tables        | Are           | Cool  |
| ------------- |---------------| ------|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |


示例2

```
dog | bird | cat
----|------|----
foo | foo  | foo
bar | bar  | bar
baz | baz  | baz
```

dog | bird | cat
----|------|----
foo | foo  | foo
bar | bar  | bar
baz | baz  | baz
