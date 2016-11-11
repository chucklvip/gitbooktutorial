# 初始化命令 init

&emsp;&emsp; init 命令初始化图书。可以根据配置进行初始化，也可以使用默认方式初始化图书。

***

命令格式为
```
init [book]
```
***
用法1：首先切换至某个目录，不加可选参数，则将这个目录初始化为一本图书的根目录。
```
cd tBook

gitbook init

```

初始化过程提示
```
warn: no summary file in this book
info: create README.md
info: create SUMMARY.md
info: initialization is finished

```
初始化了一本名为 tBook 的图书，目前的图书结构为
```
tBook
    ├── README.md
    └── SUMMARY.md
```

***
用法2：指定图书名称创建图书，也即加上可选参数。
```
gitbook init tbook

```
初始化过程提示
```
warn: no summary file in this book
info: create README.md
info: create SUMMARY.md
info: initialization is finished

```
建立了tBook目录作为图书根目录，初始化了一本名为 tBook 的图书，目前的图书结构为
```
tBook
    ├── README.md
    └── SUMMARY.md
```

***

以上两种方法初始化图书大同小异。关于初始化图书，后面章节会更深入的介绍。
