# Google 试算表

透过 编辑器的 Google 试算表功能，只需要简单几个步骤，就能将 Google 试算表当作资料库，储存传感器所接收到的讯号数值，或透过开发板显示试算表读取的资料。

## 建立并设定试算表权限

使用 编辑器操作 Google 试算表之前，*必须先建立试算表，并设定试算表的权限*，所以请先用 Google 帐号登入 Google 云端硬碟，在云端硬碟里建立一份全新的空白试算表。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-01.jpg)

开启试算表后，在左上方输入试算表名称，就能完成建立Google 试算表的动作，*「试算表」表示整份试算表，每份试算表内可以包含许多「工作表」*，两者可分别给予不同名称。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-02.jpg)

点选试算表右上角的「共用」，设定试算表的权限。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-03.jpg)

开启共用设定视窗，点选「进阶」。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-04.jpg)

每份新建立的试算表权限都是「私人 - 只有您能存取」，点选后方的「变更」就可进行设定。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-05.jpg)

将试算表的权限，设定为*「任何知道连结的使用者」，都可以「编辑」*，按下储存，试算表的权限就设定完成。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-06.jpg)

## Google 试算表积木清单

Google 试算表积木包含试算表初始化、读取资料、写入资料、删除列或栏、增加列或栏...等功能。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-07.jpg)

## 试算表初始化

「试算表初始化」积木可以设定试算表的网址和工作表名称，在操作试算表的任何功能之前，都需要先使用试算表初始化的积木。

> 注意，请勿将「试算表」名称填入「工作表」名称的位置。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-08.jpg)

## 写入资料

「写入资料」积木能够将资料写入试算表，并能指定从上方第一列写入或将资料放在最后一列。

> 写入资料积木属于「*写入资料后才会继续执行后方程序*」的类型，当编辑画面中有这块积木，*执行时当程序遇到这块积木会暂停，直到资料写入后才会再继续*。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-09.jpg)

点选积木前方的蓝色小齿轮，可以增加写入资料的栏位数量。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-10.gif)

先使用初始化试算表积木，填入自己的试算表网址，再放上写入资料的积木，执行后就会看见试算表内出现时间和文字。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-11.jpg)

搭配重复回圈，就能不断写入资料到试算表内。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-12.jpg)

## 指定储存格写入资料

「指定储存格写入资料」可以将资料写入指定的储存格，格式除了单一数值，也支援二维阵列格式的资料。

> 指定储存格写入资料积木属于「*写入资料后才会继续执行后方程序*」的类型，当编辑画面中有这块积木，*执行时当程序遇到这块积木会暂停，直到资料写入后才会再继续*。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-13.jpg)

以下图的例子，执行后会在 b2 储存格，写入「写入资料」四个字。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-14.jpg)

除了可以指定单一储存格，这块积木也*支援「范围」储存格和「二维阵列」的资料格式*，例如要将资料写入`a1:b3` 的储存格范围，就需要使用`[ [a,b],[c,d],[e,f]]` 二维阵列资料，*二维阵列的第一层为纵列( 1、2、3... )，第二层为横栏( A、B、C... )*。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-15.jpg)

以下图的例子，执行后会在 A1 写入 a，B1 写入 b，A2 写入 c，B2 写入 d...依此类推。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-16.jpg)


## 读取资料

「读取资料」积木可以读取单一储存格、整份工作表或最后一列、最后一栏的号码。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-17.jpg)

「读取资料」积木属于「*读取完成才会继续执行后方程序*」的类型( 点击前方问号小图示会提示)，当编辑画面中有这块积木，*执行时当程序遇到这块积木会暂停，直到取得资料后才会再继续*。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-18.jpg)

首先准备一份有资料的试算表，下图范例使用复仇者联盟的成员称号和姓名。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-19.jpg)

若使用「读取单一储存格」的积木，就能在读取到资料后，让小怪兽分别讲出对应储存格的内容。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-20.jpg)

若需要读取的资料量比较多，建议使用「读取所有资料」的积木，该积木读取到的资料，*会以「二维阵列」的方式呈现*，故而可以使用阵列积木进行操作，以下方的例子，搭配重复回圈，就能在读取资料后，让小怪兽依序念出复仇者联盟成员的称号和姓名。

> 取得资料的二维阵列的*第一层为纵列 ( 1、2、3... )，第二层为横栏 ( A、B、C... )*。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-21.gif)

取得的资料除了资料内容，也包含了资料所在的最后一列和最后一栏，可以透过相关积木取得对应的编号( 横向栏位使用数字表现，a 对应1，b 对应2，依此类推)，以复仇者联盟成员试算表的内容为例，取得的最后一列为7，最后一栏为2。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-22.jpg)


## 删除列或栏

「删除列或栏」积木可以删除一个区间的列或栏，列号以数字表现，栏号使用英文表示。

> 删除列或栏的积木属于「*删除后才会继续执行后方程序*」的类型，当编辑画面中有这块积木，*执行时当程序遇到这块积木会暂停，直到删除了列或栏之后才会再继续*。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-23.jpg)

## 增加列或栏

「增加列或栏」积木可以增加一个区间的列或栏，列可以选择增加在上方或下方，栏可以选择增加在左方还是右方。

> 增加列或栏的积木属于「*增加后才会继续执行后方程序*」的类型，当编辑画面中有这块积木，*执行时当程序遇到这块积木会暂停，直到增加了列或栏之后才会再继续*。

![Google 试算表](../images/zh-tw/docs/webbit/extension/google-spreadsheet-24.jpg)