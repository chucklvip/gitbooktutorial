# Markdown 语法 - 代码区域

***

和程序相关的写作或是标签语言原始码通常会有已经排版好的代码区块，通常这些区块我们并不希望它以一般段落文件的方式去排版，而是照原来的样子显示。

要在 Markdown 中建立代码区块有几种方式：

1. 简单地缩进 4 个空格或是 1 个制表符
```
这是一个普通段落，下面是代码区块：

    void setup() {
        pinMode(LED_BUILTIN, OUTPUT);
    }
    void loop() {
         digitalWrite(LED_BUILTIN, HIGH);
         delay(1000);
         digitalWrite(LED_BUILTIN, LOW);
         delay(1000);
    }
```
以下是真实效果
    这是一个普通段落，下面是代码区块：

        void setup() {
            pinMode(LED_BUILTIN, OUTPUT);
        }
        void loop() {
            digitalWrite(LED_BUILTIN, HIGH);
            delay(1000);
            digitalWrite(LED_BUILTIN, LOW);
            delay(1000);
        }

2. 上面的方式如果代码很多，每行都要缩进，很费事。可以使用 \`\`\` 代码区 \`\`\`的方式来替代。

```
\`\`\` Arduino
void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
}
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000);
}
\`\`\`

```

上面的代码效果如下(代码里面的\\要去掉, 前面的 \`\`\` 之后尽量加上代码对应的语言)：

``` Arduino
void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
}
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000);
}
```
