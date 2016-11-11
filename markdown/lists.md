# Markdown 语法 - 列表

Markdown 支持有序列表和无序列表。 

***

##### 无序列表

无序列表使用星号、加号或是减号作为列表标记：
```
*   Red
*   Green
*   Blue
```

等同于：
```
+   Red
+   Green
+   Blue
```

也等同于：
```
-   Red
-   Green
-   Blue
```

也可以混合着来
```
*   Red
+   Green
-   Blue
```
效果都是下面这样

*   Red
+   Green
-   Blue

##### 有序列表

有序列表则使用数字接着一个英文句点：

```
1.  Red
2.  Green
3.  Blue
```

很重要的一点是，你在列表标记上使用的数字并不会影响输出的 HTML 结果，上面的列表所产生的 HTML 标记为：

```
<ol>
<li>Red</li>
<li>Green</li>
<li>Blue</li>
</ol>
```
如果你的列表标记写成：
```
1.  Red
1.  Green
1.  Blue
```

或甚至是：
```
3. Red
1. Green
8. Blue
```
其效果都是下面这样

3. Red
1. Green
8. Blue


列表项目标记通常是放在最左边，但是其实也可以缩进，最多 3 个空格，项目标记后面则一定要接着至少一个空格或制表符。列表可以嵌套

```
1.  Red
    * Apple
        * 红富士
            1. 长富1
            2. 长富2
            3. 长富6
            4. 秋富1
            5. 岩富10
        * 黄元帅
        * 红星
    * Sun      
1.  Green
1.  Blue
```

嵌套列表效果如下

1.  Red
    * Apple
        * 红富士
            1. 长富1
            2. 长富2
            3. 长富6
            4. 秋富1
            5. 岩富10
        * 黄元帅
        * 红星
    * Sun      
1.  Green
1.  Blue

如果要在列表项目内放进引用，那 > 就需要缩进： 

```
* A list item with a blockquote:

    > This is a blockquote
    > inside a list item
```

效果如下
* A list item with a blockquote:

    > This is a blockquote
    > inside a list item

当然，项目列表很可能会不小心产生，像是下面这样的写法： 
```
1986. What a great season.
```
1986. What a great season.

换句话说，也就是在行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠。
```
1986\. What a great season.
```
1986\. What a great season.

