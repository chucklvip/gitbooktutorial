# Markdown 语法 - 链接

***

Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。 

不管是哪一种，链接文字都是用 \[方括号\] 来标记。

##### 行内式链接

要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：

```
This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
```

效果如下

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.


如果你是要链接到同样主机的资源，你可以使用相对路径：

See my [README](/README.md "ReadMe Page") page.

##### 参考式链接

参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：

```
This is [an example][1] reference-style link.
```

接着，在文件的任意处，你可以把这个标记的链接内容定义出来： 

```
[1]: http://example.com/  "Optional Title Here"
```
链接内容定义的形式为：
*     方括号（前面可以选择性地加上至多三个空格来缩进），里面输入辨识链接的标记。链接辨别标签可以有字母、数字、空白和标点符号，但是并不区分大小写。
*     接着一个冒号
*     接着一个以上的空格或制表符
*     接着链接的网址，链接网址也可以用方括号包起来
*     选择性地接着 title 内容，可以用单引号、双引号或是括弧包着。可以把 title 属性放到下一行，也可以加一些缩进，若网址太长的话，这样会比较好看


实际效果

This is [an example][1] reference-style link.

隐式链接标记功能让你可以省略指定链接标记，这种情形下，链接标记会视为等同于链接文字，要用隐式链接标记只要在链接文字后面加上一个空的方括号，如果你要让 "Google" 链接到 google.com，你可以简化成：
```
[Google][] 
```
然后定义链接内容：
```
[Google]: http://google.com/
```

效果如下：

[Google][] 


##### 自动链接
Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用方括号包起来， Markdown 就会自动把它转成链接。自动链接可以看作是行内式的简化版本。

一般网址的链接文字就和链接地址一样，例如：
```
<http://example.com/>
```
甚至直接写网址即可
```
<http://example.com/>
```
效果都是下面这样

<http://example.com/>



[1]: http://example.com/ "Optional Title Here"
[Google]: http://google.com/


