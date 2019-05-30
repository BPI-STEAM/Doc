随机生成器
===============

随机性
--------------------

什么是随机性呢？

随机性意味着无法预测，真正的随机性只存在于自然世界中。什么地方有闪电是随机的；如果有个地方正在酝酿风暴，可以相当确定那里会有闪电，但无法精确预测具体位置一所以不要站在树下。又比如老师想让同学起来回答问题，但是没有一个同学举手起来回答问题，这时候老师就随便喊了一个座位号，这个座位号也具有随机性。

MicroPython 附带了一个随机数模块，可以很容易地在代码中引入随机数。例如，下面是如何在屏幕上滚动一个随机名称的例子:

.. code:: python

   from microbit import *
   import random

   names = ["Mary", "Yolanda", "Damien", "Alia", "Kushal", "Mei Xiu","Zoltan" ]

   display.scroll(random.choice(names))

列表(names)包含7个不同的名字的字符串。使用 random.choice 方法将列表(names)作为参数，并返回随机选择的项。这个项(随机选择的名称)作为 display.scroll 的参数。效果就是你可以在led显示面板上面看到被随机选中的名字

随机数
--------------------

随机数非常有用。它们在游戏中很常见，比如说骰子。 MicroPython 提供了一些有用的随机数方法。那就让我们来制作一个简单的骰子吧，示例代码：

.. code:: python

   from microbit import *
   import random

   display.show(str(random.randint(1, 6)))

板子每次执行这段函数，它都会显示 1 到 6 之间的数字。 random.randint() 在两个参数1和6之间返回一个整数(包括6)。注意因为 show 函数显示时需要一个字符，所以这里使用 str 函数将数值转换为字符(例如，我们将 6 通过 str(6) 转换为“6”)。
如果你想要一个介于 0 和 N 之间的数字，那么就用 random.randrange() 函数。如果你给它一个参数，它会返回随机整数，但不包括参数 N 的值(这与 random.randint() 不同)。有时你需要有小数点的数字。这些被称为浮点数，那怎么产生随机的浮点数呢？这时候就要使用random.random(),这个函数只会返回0.0到1.0之间的浮点数。那么如何产生大一些的浮点数呢，聪明的你心中应该有答案了吧。那就是同时使用 random.randrange 和 random.random

.. code:: python


   from microbit import *
   import random

   answer = random.randrange(100) + random.random()
   display.scroll(str(answer))

种子随机数
--------------------

计算机使用的随机数生成器并不是真正的随机数生成器。它们只是通过随机种子生成的一个数。那这个种子数是怎么来的呢？通常来自时间或传感器读数，如内置在芯片中的定时器和温度计。

有时你想要具有可重复的随机行为:一种可重复的随机来源。比如说每次掷骰子都需要相同的随机值。通过设置种子值很容易做到这一点。给定一个已知的种子，随机数生成器将创建相同的随机数集。种子是人为设置的，这个版本的骰子程序总是产生相同的结果。

.. code:: python

   from microbit import *
   import random

   random.seed(1337)
   while True:
       if button_a.was_pressed():
           display.show(str(random.randint(1, 6)))

运行上面的程序我们总是得到相同的结果，在led面板上显示’5’,因为在这里我们给定的种子是一个固定的值所以这个程序总是产生一个固定的数
