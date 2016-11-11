# Markdown 语法 - 段落与换行
***
&emsp;&emsp;一个 Markdown 段落是由一个或多个连续的文本行组成，它的前后要有一个以上的空行（空行的定义是显示上看起来像是空的，便会被视为空行。比方说，若某一行只包含空格和制表符，则该行也会被视为空行）。

&emsp;&emsp;普通段落不该用空格或制表符来缩进。如果需要段落首行缩写两个中文字符，需要使用代码：

&emsp;&emsp;```&emsp;&emsp;```

&emsp;&emsp;Markdown 中, 多个空行只显示一个空行。

***

空格的表示符号(注：em是字体排印学的计量单位，1em 等于当前的字体尺寸)：

* ```&nbsp;``` 半角的不断行的空格,全称No-Break Space,是按下space键产生的空格

* ```&ensp;``` 半角的空格,全称是En Space,等同于字体度的一半,1/2个中文字宽度

* ```&emsp;``` 全角的空格,全称是Em Space,1个中文字宽度

* ```&thinsp;``` 它叫窄空格，全称是Thin Space,em之六分之一宽

* ```&zwnj;``` 零宽不连字，全称是Zero Width Non Joiner，简称“ZWNJ”，是一个不打印字符，放在电子文本的两个字符之间，抑制本来会发生的连字，而是以这两个字符原本的字形来绘制。

* ```&zwj;``` 零宽连字，全称是Zero Width Joiner，简称“ZWJ”，是一个不打印字符，放在某些需要复杂排版语言（如阿拉伯语、印地语）的两个字符之间，使得这两个本不会发生连字的字符产生了连字效果。


***


参考[www.markdowntutorial.com/lesson/1][1]

[1]: http://www.markdowntutorial.com/lesson/1


