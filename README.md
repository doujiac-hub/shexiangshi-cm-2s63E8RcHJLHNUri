[合集 \- 从零开始的Python世界生活(1\)](https://github.com)1\.从零开始的Python世界生活——内置模块(Math)11\-20收起
# 从零开始的Python世界生活——内置模块(Math)


Python的`math`模块提供了丰富的数学函数和常数，支持基本的数学运算、三角函数、对数、指数等，适用于科学计算和工程应用。


## 数学常量：


注意`math`模块的常量是以双精度浮点数存储的,所以通常只有15到17位有效数字的精度，如果需要更高的精度推荐使用 `decimal` 模块或 `mpmath`  库


### π（圆周率）



```
import math
print(math.pi)
#运行结果:3.141592653589793

```

### τ（2π）


一些数学家提倡使用τ代替π，认为τ更直观，特别是在涉及圆的角度和周期性问题时



```
import math
print(math.tau)
#运行结果:6.283185307179586

```

### e（欧拉数）



```
import math
print(math.e)
#运行结果:2.718281828459045

```

### infinity（无穷大）



```
import math
print(math.inf)
#运行结果:inf

```

### Not a Number(不是一个数字)


未定义或不可表示的值，如0除以0的结果，负数的平方根（在实数范围内），可以在数据分析和科学计算中用来标记缺失或无效的数据点



```
import math
print(math.nan)
#运行结果:nan

```

## 数学函数:


### 1\. 基本数学函数:


`math.fsum(iterable)` 返回可迭代对象的浮点数和，相比`sum(iterable)`具有更高的精度。



```
import math
iterable=[0.1,0.2,0.3]
print(math.fsum(iterable))
#运行结果:0.6

```

### 2\. 幂和对数


#### 幂函数


* `math.pow(x, y)`：返回*x\*\*y*。
* `math.exp(x)`：返回 *e\*\*x*。


#### 对数函数


* `math.log(x[, base])`：返回 log*base*(*x*)，如果未指定基数，则返回自然对数。
* `math.log10(x)`：返回以 10 为底的对数。
* `math.log2(x)`：返回以 2 为底的对数。


### 3\. 三角函数


#### **基本三角函数**


* `math.sin(x)`：返回 sin(*x*)。
* `math.cos(x)`：返回 cos(*x*)。
* `math.tan(x)`：返回 tan(*x*)。


#### **反三角函数**


* `math.asin(x)`：返回 arcsin(*x*)。
* `math.acos(x)`：返回 arccos(*x*)。
* `math.atan(x)`：返回 arctan(*x*)。
* `math.atan2(y, x)`：返回 arctan(*y*/*x*)。


### 4\. 超越函数


#### **双曲函数**


* `math.sinh(x)`：返回双曲正弦。
* `math.cosh(x)`：返回双曲余弦。
* `math.tanh(x)`：返回双曲正切。


#### **反双曲函数**


* `math.asinh(x)`：返回反双曲正弦。
* `math.acosh(x)`：返回反双曲余弦。
* `math.atanh(x)`：返回反双曲正切。


### 5\. 其他函数


#### 阶乘


`math.factorial(x)`：返回x的阶乘



```
import math
x = 3 
print(math.factorial(x))# 运行结果 :6

```

#### 取整和舍入


`math.ceil(x)`：返回大于或等于 x 的最小整数。


`math.floor(x)`：返回小于或等于 x 的最大整数。


`math.trunc(x)`：返回 x 的整数部分。



```
import math
x = 1.5
print(math.ceil(x))#运行结果:2
print(math.floor(x))#运行结果:1
print(math.trunc(x))#运行结果:1

```

#### 平方根和绝对值


`math.sqrt(x)`：返回 x 的平方根。


`math.isqrt(x)`:返回 x 的平方根的整数部分。



```
import math
x = 3
print(math.sqrt(x))#运行结果:1.7320508075688772
print(math.isqrt(x))#运行结果:1

```

`math.fabs(x)`：


返回 x 的绝对值，`注意返回的是浮点数`，故用于获得浮点数的绝对值，获得整数绝对值，使用内置函数`abs(x)`



```
import math
x = -1
print(math.fabs(x)) #运行结果:1.0
print(abs(x))#运行结果:1

```

### 6\. 组合和排列（仅在 Python 3\.8 及以上版本可用）


`math.comb(n, k)`：返回从 n 个元素中选择 k 个元素的组合数。


`math.perm(n, k)`：返回从 n 个元素中选择 k 个元素的排列数。



```
import math
n, k = 5, 3
print(math.comb(n,k))#运行结果:10
print(math.perm(n,k))#运行结果:60

```


> 入门之道，就在其中


  * [从零开始的Python世界生活——内置模块(Math)](#%E4%BB%8E%E9%9B%B6%E5%BC%80%E5%A7%8B%E7%9A%84python%E4%B8%96%E7%95%8C%E7%94%9F%E6%B4%BB%E5%86%85%E7%BD%AE%E6%A8%A1%E5%9D%97math)
* [数学常量：](#%E6%95%B0%E5%AD%A6%E5%B8%B8%E9%87%8F)
* [π（圆周率）](#%CF%80%E5%9C%86%E5%91%A8%E7%8E%87)
* [τ（2π）](#%CF%842%CF%80)
* [e（欧拉数）](#e%E6%AC%A7%E6%8B%89%E6%95%B0)
* [infinity（无穷大）](#infinity%E6%97%A0%E7%A9%B7%E5%A4%A7)
* [Not a Number(不是一个数字)](#not-a-number%E4%B8%8D%E6%98%AF%E4%B8%80%E4%B8%AA%E6%95%B0%E5%AD%97)
* [数学函数:](#%E6%95%B0%E5%AD%A6%E5%87%BD%E6%95%B0)
* [1\. 基本数学函数:](#tid-6aCHmP)
* [2\. 幂和对数](#tid-SYtYsQ)
* [幂函数](#%E5%B9%82%E5%87%BD%E6%95%B0)
* [对数函数](#%E5%AF%B9%E6%95%B0%E5%87%BD%E6%95%B0)
* [3\. 三角函数](#tid-MpfTZd)
* [基本三角函数](#%E5%9F%BA%E6%9C%AC%E4%B8%89%E8%A7%92%E5%87%BD%E6%95%B0):[MeoMiao 萌喵加速](https://biqumo.org)
* [反三角函数](#%E5%8F%8D%E4%B8%89%E8%A7%92%E5%87%BD%E6%95%B0)
* [4\. 超越函数](#tid-e7jsck)
* [双曲函数](#%E5%8F%8C%E6%9B%B2%E5%87%BD%E6%95%B0)
* [反双曲函数](#%E5%8F%8D%E5%8F%8C%E6%9B%B2%E5%87%BD%E6%95%B0)
* [5\. 其他函数](#tid-Ar8zrf)
* [阶乘](#%E9%98%B6%E4%B9%98)
* [取整和舍入](#%E5%8F%96%E6%95%B4%E5%92%8C%E8%88%8D%E5%85%A5)
* [平方根和绝对值](#%E5%B9%B3%E6%96%B9%E6%A0%B9%E5%92%8C%E7%BB%9D%E5%AF%B9%E5%80%BC)
* [6\. 组合和排列（仅在 Python 3\.8 及以上版本可用）](#tid-sXZt8C)

   ![](https://github.com/cnblogs_com/blogs/832194/galleries/2424134/t_241001140621_%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20231111221642.png)    - **本文作者：** [MPyGF](https://github.com)
 - **本文链接：** [https://github.com/666\-777\-eto/p/18558729](https://github.com)
 - **关于博主：** 评论和私信会在第一时间回复。或者[直接私信](https://github.com)我。
 - **版权声明：** 本博客所有文章除特别声明外，均采用 [BY\-NC\-SA](https://github.com "BY-NC-SA") 许可协议。转载请注明出处！
 - **声援博主：** 如果您觉得文章对您有帮助，可以点击文章右下角**【[推荐](javascript:void(0);)】**一下。
     
