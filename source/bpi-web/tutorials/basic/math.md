# 数学

数学积木包含了许多数学运算，从基本的加减乘除，到四舍五入、平均值、中位数...等应有尽有，不论是简单的程序或复杂应用，都能透过各式各样的数学运算实现。

## 数学积木清单

数学的积木分别有数字、运算式、基础函式、总和、随机数和尺度转换...等常用的数学运算式。

![数学](../images/zh-tw/docs/webbit/basic/math-01.jpg)

## 指定数字

「指定数字」积木用来让我们输入数字，可输入整数或是带有小数点的浮点数，很常用于运算式或判断式。

![数学](../images/zh-tw/docs/webbit/basic/math-02.jpg)

## 取得范围内随机整数

「取得范围内随机整数」积木会指定一个数字范围，在每次执行这块积木时，就会从这个数字范围内取出随机的整数。

![数学](../images/zh-tw/docs/webbit/basic/math-03.jpg)

搭配重复无限次和等待积木，可以让小怪兽每隔一秒说出一个随机整数。

![数学](../images/zh-tw/docs/webbit/basic/math-05.gif)

## 取得随机分数

「取得随机分数」积木会在每次执行时，随机取得一个 0 到 1 之间的浮点数。

![数学](../images/zh-tw/docs/webbit/basic/math-04.jpg)

搭配重复无限次和等待积木，可以让小怪兽每隔一秒说出一个随机浮点数。

![数学](../images/zh-tw/docs/webbit/basic/math-06.gif)

## 数学运算

「数学运算」积木可以针对数字进行加、剪、乘、除和次方五种运算。

![数学](../images/zh-tw/docs/webbit/basic/math-07.jpg)

如果使用多个数学运算的积木，需要注意是*每个运算积木在计算上都会使用括号，类似的运算式有可能得到不同的结果*，例如下图积木看起来都是5 + 2 x 2，但因为括号位置的不同，得到的结果也不相同。

![数学](../images/zh-tw/docs/webbit/basic/math-08.jpg)

数学运算除了可以放入数字，也可以用于变量的相加，例如指定变量 a 为 5，变量 b 为 3，透过数学运算就能算出 a + b 等于 8。

![数学](../images/zh-tw/docs/webbit/basic/math-23.jpg)

## 取得余数

「数学运算」积木可以取得两个数字相除的余数。

![数学](../images/zh-tw/docs/webbit/basic/math-09.jpg)

## 限制数字范围

「限制数字范围」积木可以将设定最大值与最小值，并将数字限制在这个指定的范围内。

![数学](../images/zh-tw/docs/webbit/basic/math-12.jpg)

## 四舍五入

「四舍五入」积木可以对带有浮点数的数字进行四舍五入、无条件舍去或无条件进位三种运算，同时亦可选择舍去或进位到第几位小数点。

![数学](../images/zh-tw/docs/webbit/basic/math-10.jpg)

将需要四舍五入的数字，放在四舍五入的积木后方，就可以得到四舍五入之后的结果。

![数学](../images/zh-tw/docs/webbit/basic/math-11.jpg)

## 尺度转换

「尺度转换」积木可以将某个尺度区间内的数值，转换为另外一个区间尺度对应数值。

![数学](../images/zh-tw/docs/webbit/basic/math-13.jpg)

例如 0.5 为 0~1 尺度区间的数值，转换为 0~100 尺度区间得到的结果就是 50。

![数学](../images/zh-tw/docs/webbit/basic/math-14.jpg)

尺度转换积木可以帮助我们完成许多较为复杂的尺度转换，例如 0.5 位于 -5~5 之间，转换到 250~400 之间的数值就是 332.5。

![数学](../images/zh-tw/docs/webbit/basic/math-15.jpg)

尺度转换积木常常会和四舍五入积木搭配使用，*建议将四舍五入积木放在尺度转换积木前方*，因为尺度转换后的数值有可能会带有小数点，转换后再四舍五入能得到较精确的答案。

![数学](../images/zh-tw/docs/webbit/basic/math-16.jpg)

## 阵列运算

「阵列运算」积木能针对以数字组成的阵列，进行加总、取出最小值、取出最大值、计算平均值、取得中位数、取得比较众数、计算标准差和随机抽取的计算。

![数学](../images/zh-tw/docs/webbit/basic/math-17.jpg)

在阵列运算后方接上阵列积木，就可以开始行取值或运算。

![数学](../images/zh-tw/docs/webbit/basic/math-18.jpg)

## 常用数学函数

「常用数学函数」提供常用的数学计算积木，常用数学函数包含以下几种：开根号、绝对值、负数(-)、对数函数(ln)、log10 函数(log10)、指数函数(e^)和10 的几次方(10^)。

![数学](../images/zh-tw/docs/webbit/basic/math-19.jpg)

## 三角函数

「三角函数」积木里头提供了两种三角函数用法，分别是角度 ( sin、cos、tan ) 以及径度 ( asin、acos、atan )，三角函数可以从下拉选单选择切换。

![数学](../images/zh-tw/docs/webbit/basic/math-20.jpg)

注意，因为JavaScript 网页语言特性，有些情况使用三角函数时，小数点后方会变成无限循环9999，例如sin(30) 应该等于0.5，出来却变成0.49999...，当遇到这种情况，需使用四舍五入的方式才能呈现预期的结果。

![数学](../images/zh-tw/docs/webbit/basic/math-21.jpg)


## 常数

「常数」积木会表现是一个不会变动的常数数值，常数包含了以下几种：圆周率(π)、指数(e)、黄金分割率(φ)、sqrt(2)、sqrt(½) 和无限大(∞)。

![数学](../images/zh-tw/docs/webbit/basic/math-22.jpg)