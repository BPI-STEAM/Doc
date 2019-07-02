刷入 Webduino 固件
=====================================================

第一次使用，请先烧入 Webduino 固件，如果不烧录就没有 Webduino 硬件运行环境。

.. Hint::

    使用请确认已经安装驱动，且已经得知自己的硬件串口名称，例如：COM5、ttyUSB0。

.. toctree::
    :maxdepth: 2

    ../bpi-steam/driver

在 Windows 下
---------------------------

- 从 `BPI-BIT-Webduino/release <https://github.com/BPI-STEAM/BPI-BIT-Webduino/releases/tag/FlashTool>`_ 中获取烧写工具的链接，附有国内微云网盘分流。

- 下载后打开 `FlashWebduino-*.zip` 压缩包，然后运行里面的 Flashtool.exe 工具即可。

.. image:: flash_web/flash_web.png

- 请先插入硬件后打开软件，这个软件会自动运行烧写。

- 你也可以自己选择串口烧录，升级固件只需要替换压缩包中的 firmware.bin 重新烧入即可。

在 其他系统 下
---------------------------

请参照其他网络教程，如果有特别的需求，可以到 社区 提交问题 或 开 issue 。

.. Hint::

    烧录后显示 x 的问题请看这个 `跳过产测 红 X <https://github.com/BPI-STEAM/BPI-BIT-WebDuino/issues/3>`_，更多问题可以到 `中文社区 <https://forum.banana-pi.org.cn/c/bpi-bit>`_ 反馈。