使用 Pycharm IDE 编程
=====================================================

是时候换一个顶级的 Python 专业 IDE 来编程了，你觉得呢？本文将教你如何在 Pycharm 里写 MicroPython 并运行。

获取 intellij-MicroPython 插件
------------------------------------------------------

在此下载 :download:`intellij-micropython <https://github.com/BPI-STEAM/BPI-BIT-MicroPython/releases/tag/pycharm>` 。

可以在此查看，`项目主页 <https://github.com/junhuanchen/intellij-micropython>`_ 。

安装 pycharm 社区版
---------------------------

获取 `pycharm`_ 使用 windows 系统 `点此下载 2019.1 版本`_ (community 版免费使用)

安装完成打开即可，按 默认 的设置一路进入到以下界面即可。

|image0|

新建一个项目
---------------------------

点击 Create New Project 弹出以下界面。

|image1|

如果没有安装 Python 则是以下界面

|image2|

最后可以看到项目已经建立完成。

|image3|

安装 intellij-MicroPython 插件
---------------------------

|image4|

|image5|

|image6|

提示：该版本已经修改了底层为 mpfshell，并没有完全整合到官方，所以仍和主仓的插件同名，因此 IDE 提示插件需要升级或是其他修复的时候，会被替换回原版，遇到这种情况的时候，忽视了就好。

|image7|

运行一个文件
---------------------------

安装好插件后，在项目中启动它。

|image8|

你可以在设置里搜索 ``MicroPython``\ 得到以上页面。

|image9|

现在启动它，依次点开如图设置，Enable MicroPython support。

|image10|

选择 ESP8266 （ESP32）配置设备类型，再点击 Detect 可以自动判断你连接的板子的路径（或名称），此时的 Detect 一定会失败，因为关键的依赖还没安装。

|image11|

当出现自动识别串口失败，则需要你自己填入自己板子的串口名称（包括路径），或是其他连接参数，比如：ws:192.168.1.1,1234，这和 ``mpfshell`` 的 open 是一样的。

|image12|

此时已经设定好板子的连接参数了，现在可以在 untitled 处右键新建一个
python 文件，第一次使用的时候，务必创建一个文件来触发安装依赖，安装完成后才能使用自动识别串口 和 其他工具（菜单项中的 Tools）。

|image13|

在右侧代码编辑框中写入一句\ ``print(helloworld!)``\ 。

|image14|

第一次使用的时候，会提示你需要安装依赖项，因此点击消息的 Install requirements 即可在后台自动下载安装。

|image15|

耐心等待一会就可以了。

|image16|

安装完成会提示。

|image17|

现在我们可以运行 main.py 文件了，在编辑框的任意地方右键显示菜单选取 Run ‘Flash main.py’，即可自动生成运行文件配置并在板子中运行。

.. Attention::

    如果 Linux 系统出现串口连接不上，须核对串口是否对一般用户有权限，如果不确定，请核对这条指令\ ``usermod -a -G dialout Username && sudo reboot``\ ，Username 是指你的用户名，不是 Username 。

|image18|

可以看到运行结果如下

|image19|

直接使用 Mpfshell
---------------------------

在 MicroPython -> Run Mpfshell Tools 中可以使用 REPL 和 Mpfshell 的快捷功能。

|image20|

.. _pycharm: https://www.jetbrains.com/pycharm/
.. _点此下载 2019.1 版本: https://download-cf.jetbrains.com/python/pycharm-community-2019.1.exe

.. |image0| image:: pycharm/03.png
.. |image1| image:: pycharm/05.png
.. |image2| image:: pycharm/04.png
.. |image3| image:: pycharm/06.png
.. |image4| image:: pycharm/07.png
.. |image5| image:: pycharm/08.png
.. |image6| image:: pycharm/29.jpg
.. |image7| image:: pycharm/09.png
.. |image8| image:: pycharm/10.png
.. |image9| image:: pycharm/11.png
.. |image10| image:: pycharm/12.png
.. |image11| image:: pycharm/13.png
.. |image12| image:: pycharm/14.png
.. |image13| image:: pycharm/15.png
.. |image14| image:: pycharm/16.png
.. |image15| image:: pycharm/17.png
.. |image16| image:: pycharm/18.png
.. |image17| image:: pycharm/19.png
.. |image18| image:: pycharm/20.png
.. |image19| image:: pycharm/21.png
.. |image20| image:: pycharm/22.png