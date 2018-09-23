# Markdown 语法 - 公式

当你需要在编辑器中插入数学公式时，可以使用两个美元符 \$\$ 包裹 TeX 或 LaTeX 格式的数学公式来实现。

**注意：GitBook 的公式可能需要插件才能正确显示，推荐的插件有mathjax和katex**
***

下面是一些公式例子(实际使用时要将左右两边加上两个美元符\$\$)

```
x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}
```
$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$


```
\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N
```
$$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N $$


```
f(x) = \sum_{i=0}^{N}\int_{a}^{b} g(t,i) \text{d}t
```
$$f(x) = \sum_{i=0}^{N}\int_{a}^{b} g(t,i) \text{d}t $$


***
### 基本LaTeX 公式命令

#####角标(上下标)

上标命令：^{}

下标命令：_{}

如
```
x^2, x_1^2
```
显示为
$$ x^2, x_1^2 $$

##### 希腊字母
|命令       |显示                |命令            |显示                 |
|-----------|-------------------|----------------|--------------------|
|\alpha     |α                  |\beta           |β                   |
|\gamma     |γ                  |\delta          |δ                   |
|\epsilon   |ϵ                  |\zeta           |ζ                   |
|\eta       |η                  |\theta          |θ                   |
|\iota      |ι                  |\kappa          |κ                   |
|\lambda    |λ                  |\mu             |μ                   |
|\xi        |ξ                  |\nu             |ν                   |
|\pi        |π                  |\rho            |ρ                   |
|\sigma     |σ                  |\tau            |τ                   |
|\upsilon   |υ                  |\phi            |ϕ                   |
|\chi       |χ                  |\psi            |ψ                   |
|\omega     |ω                  |                |                    |

如果使用大写的希腊字母，把命令的首字母变成大写即可，例如 \\Gamma 输出的是$$\Gamma$$

如果使用斜体大写希腊字母，在大写希腊字母的LaTeX命令前加上var即可,例如\\varGamma 生成 $$\varGamma$$

下面是一个较为复杂的公式

```
\varGamma(x) = \frac{\int_{\alpha}^{\beta} g(t)(x-t)^2\text{ d}t }{\phi(x)\sum_{i=0}^{N-1} \omega_i}

```
$$
\varGamma(x) = \frac{\int_{\alpha}^{\beta} g(t)(x-t)^2\text{ d}t }{\phi(x)\sum_{i=0}^{N-1} \omega_i}
$$

##### 和号和积分号

|命令            |显示                |命令            |显示                 |
|---------------|-------------------|----------------|--------------------|
|\sum           |$$\sum$$           |\int            |$$\int$$            |
|\prod          |$$\prod$$          |\iint           |$$\iint$$           |
|\bigcup        |$$\bigcup$$        |\bigcap         |$$\bigcap$$         |


##### 下划线、上划线等

上划线命令：\overline{公式}


下划线命令：\underline{公式}

```
\overline{\overline{a^2}+\underline{ab}+\bar{a}^3}
```

$$\overline{\overline{a^2}+\underline{ab}+\bar{a}^3}$$

上花括弧命令：\overbrace{公式}^{说明}

下花括弧命令：\underbrace{公式}_{说明}

```
 \[ \underbrace{a+\overbrace{b+\dots+b}^{m  个}+c}_{20 个} \] 
```

$$ \underbrace{a+\overbrace{b+\dots+b}^{m  个}+c}_{20 个} $$

##### 其它常用命令
|命令             |显示                 |命令            |显示                 |
|-----------------|--------------------|----------------|--------------------|
|\sqrt{2}         |$$\sqrt{2}$$        |\sqrt[3]{2}     |$$\sqrt[3]{2}$$     |
|x^{3}            |$$x^{3}$$           |x_{3}           |$$x_{3}$$           |
|\lim_{x \to 0}   |$$\lim_{x \to 0}$$  |\frac{1}{2}     |$$\frac{1}{2}$$     |

