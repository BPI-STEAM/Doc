# 文字

文字积木除了可以显示有意义的词汇，也可以透过相加的方式把文字组合，或是在一段词汇中寻找对应的字词或字母，甚至也可显示语音辨识的内容或物联网串感器的状态。

## 文字积木清单

文字积木分别有指定文字、换行、转换大小写、建立字串、文字工具、文字查找、文字取代、文字转换...等常用的文字功能。

![文字](../images/zh-tw/docs/webbit/basic/text-01.jpg)

## 指定文字

「指定文字」积木可以输入指定的文字，以便其他积木使用。

![文字](../images/zh-tw/docs/webbit/basic/text-02.jpg)

例如在小怪兽讲话积木后方接上指定文字，输入 hello，网页执行后小怪兽就会说出 hello。

![文字](../images/zh-tw/docs/webbit/basic/text-03.jpg)

## 换行

「换行」积木可以将一段文字从指定的位置折行。

![文字](../images/zh-tw/docs/webbit/basic/text-04.jpg)

## 建立字串

「建立字串」积木可以把不同的文字积木组合成一段文字。

![文字](../images/zh-tw/docs/webbit/basic/text-05.jpg)

点击蓝色小齿轮，透过拖拉组合可以增加文字缺口。

![文字](../images/zh-tw/docs/webbit/basic/text-06.gif)

在文字缺口内放入指定的文字积木或是换行积木，就可以认字组合出欲显示的文字，从下图可以看到组合过的文字和单行文字的差异。

![文字](../images/zh-tw/docs/webbit/basic/text-07.jpg)

建立字串也可以用来组合两个变量，例如变量 a 为 hello，变量 b 为 world，透过建立字串就能将两个变量组合为中间换行的 hello world。

![文字](../images/zh-tw/docs/webbit/basic/text-08.jpg)

## 在变量后方加入文字

「在变量后加入文字」能够改变原本变量的内容，使原本变量的内容后方额外增加文字。

![文字](../images/zh-tw/docs/webbit/basic/text-09.jpg)

因为是以「变量」为主，所以如果要让小怪兽讲话，就变成是使用变量的方式呈现。

![文字](../images/zh-tw/docs/webbit/basic/text-10.jpg)


## 取代文字

「取代文字」积木可以快速将一段文字里的某些字，替换为其他的文字，下拉选单可以选择要更换第一个指定的文字，或所有指定的文字。 ( 取代文字不会对变量进行变更，而是产生一段全新的文字 )

![文字](../images/zh-tw/docs/webbit/basic/text-11.jpg)

下图的例子可以只更换第一个「苹果」变成「杨桃」，或是更换所有的「苹果」为「杨桃」。

![文字](../images/zh-tw/docs/webbit/basic/text-12.jpg)

## 寻找字串出现位置

「寻找字串出现位置」会回传指定文字在一段文字中出现的位置，可以选择第一个出现的位置或最后一个出现的位置。

![文字](../images/zh-tw/docs/webbit/basic/text-13.jpg)

文字出现的位置是以「字数」来判断，以下图的例子，橘子的「橘」位在整段文字的第4 个位置，所以出现的数字为4，苹果的苹出现在第10 个位置，如果换成英文，orange 的o 位在第10 个位置，banana 的b 位在第16 个位置。

![文字](../images/zh-tw/docs/webbit/basic/text-14.jpg)

## 取得指定位置的文字

「取得指定位置的文字」积木会取出指定位置的文字，下拉选单共有五种指定位置，分别是第几个、倒数第几个、第一个、最后一个和随机位置。

![文字](../images/zh-tw/docs/webbit/basic/text-15.jpg)

以下图的例子，第 4 个字是橘，第 11 个字是果。

![文字](../images/zh-tw/docs/webbit/basic/text-16.jpg)


## 取得指定区间的文字

「取得指定区间的文字」积木会取出一段指定区间内的文字，需注意的是*第一个空格的数字要比第二个空格内的数字小*。

![文字](../images/zh-tw/docs/webbit/basic/text-17.jpg)

以下图的例子，第 3~8 的文字为「、橘子、西瓜」，而第 8 到最后的文字为「瓜、苹果、香蕉、西瓜」。

![文字](../images/zh-tw/docs/webbit/basic/text-18.jpg)


## 转换大小写

「转换大小写」积木可以针对「英文字」进行大小写转换，包含全部转大写、全部转小写或是首字母大写。

![文字](../images/zh-tw/docs/webbit/basic/text-19.jpg)

以下图的例子，可以全部转换为大写，或是只有第一个 A 是大写。

![文字](../images/zh-tw/docs/webbit/basic/text-20.jpg)


## 消除空格

「消除空格」积木可以消除一段文字中左边、右边或左右两边的空白字元。

![文字](../images/zh-tw/docs/webbit/basic/text-21.jpg)

## 进位转换

「进位转换」积木能把数字转换为二进位、八进位、十进位或十六进位的文字。

![文字](../images/zh-tw/docs/webbit/basic/text-22.jpg)

例如数字 200 转换为二进位就是 11001000，转换为八进位就是 310，转换为十六进位就是 c8。

![文字](../images/zh-tw/docs/webbit/basic/text-23.jpg)

## 文字长度

「文字长度」积木可以取得一串文字的总字数，比较需要注意的是英文字以「字母」为单位，且空白也算是一个字元。

![文字](../images/zh-tw/docs/webbit/basic/text-24.jpg)

以下图为例，「一个苹果」的文字长度为 4，「An apple」因为包含空格，所以文字长度为 8。

![文字](../images/zh-tw/docs/webbit/basic/text-25.jpg)