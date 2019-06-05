.. _display.py:

.. module:: display

display 模块
==============

要使用display模块，你需要::

    import display
    display= display.Display()


或者::
     
    from microbit import display

函数
+++++++

.. function::  display.scroll(val, color=Red, delay=150)

    - ``val`` 要显示的字符比如'hello world!'或数字如 12345。

    - ``color`` 
        内部预置的颜色有
        * ``black`` = [0, 0, 0]
        * ``Red`` = [2, 0, 0]
        * ``Orange`` = [2, 1, 0]
        * ``Yellow`` = [2, 2, 0]
        * ``Green`` = [0, 2, 0]
        * ``Blue`` = [0, 0, 2]
        * ``Indigo`` = [0, 2, 2]
        * ``Purple`` = [2, 0, 2]
        用户也可以使用自定义的颜色比如color=[7,8,9],列表中的值分别对应红色，绿色，蓝色的颜色值，取值范围都是0-255。
        同时color也可以包含多个颜色比如[[0,1,5],[2,2,8],[3,2,1],[4,5,6]]，每个字符的颜色就会按照color的颜色显示。
    - ``delay`` 字符滚动的速度。



