最简单的开始
=====================================================

.. Hint::

    工欲善其事，必先利其器。

    请确保你已经准备好 BPI-BIT ，且已经 :ref:`flash_mpy`。

    并从这里获取最简单的 MicroPython 编辑器 :download:`mpy-editor <https://github.com/BPI-STEAM/mpy-editor>`.

在 Windows 下连接设备
---------------------------

当你插入设备，打开软件后会提示你选择设备串口，如图点击 COM4 即可，如果断开设备了，你也可以继续点击 Connect（连接设备） 图标重连。

.. image:: simple_use/ready.png

确认连接后，运行代码
---------------------------

复制粘贴到编辑框中，点击 Run（运行），即可让板子显示笑脸::

    from microbit import *
    display.show(Image.HAPPY)

如你所见，板子显示了一个笑脸，我们已经成功了运行 MicroPython 代码。

.. image:: simple_use/display.png

.. Hint::

    固件已经兼容了 microbit 的 Python 代码，所以你可以直接调用大部分 microbit 功能。

本文展示了你如何使用工具进行编程，但还仅仅只是刚刚开始，还有很多基础要学，例如：学习使用更多的案例，或是改善所用的编程工具。
