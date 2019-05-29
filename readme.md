# &emsp;&emsp;&emsp;&emsp; BPI-STEAM/Docs 基础手册（自由编辑）

[![Open Source Love](https://badges.frapsoft.com/os/v3/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badge/)

[![Documentation Status](https://readthedocs.org/projects/bpi-steam-docs/badge/?version=latest)](https://bpi-steam-docs.readthedocs.io/zh_CN/latest/?badge=latest)

## how to edit

The document content is in [source](https://github.com/BPI-STEAM/Docs/tree/master/source).

文档结构如下：（如果你需要操作，请扫一遍关键目录，可以用 markdown 也可以用 rst，看自己喜欢）

- [source](https://github.com/BPI-STEAM/Docs/tree/master/source)
- [source/bpi-dev](https://github.com/BPI-STEAM/Docs/tree/master/source/bpi-dev) 工具类、归档类、目录类相关。
- [source/bpi-mpy](https://github.com/BPI-STEAM/Docs/tree/master/source/bpi-mpy) micropython 教程相关。
- [source/bpi-web](https://github.com/BPI-STEAM/Docs/tree/master/source/bpi-web) webduino 教程相关。
- [source/bpi-steam](https://github.com/BPI-STEAM/Docs/tree/master/source/bpi-steam) bpi-bit 产品、介绍相关。
- mPython/docs 引用掌控板的公共文档。
- micropython/docs 引用官方英文的公共文档。
- conf.py 自动化部署脚本，不需要修改
- contents.rst 和 index.rst 为 根目录（进入网站左边一排），需保持一致。

如果想提交内容，直接提交即可，提交后，项目会自动编译部署到网站，而你只需要在本地 build 核对一下即可，如果出现问题请提交 issue 或直接反馈到群里。

## related and thank them

感谢以下文档提供的公共部分内容，我们将保留引用信息链接。

[esp32 中文](https://docs.singtown.com/micropython/zh/latest/esp32/index.html)

[openmv 中文](https://docs.singtown.com/micropython/zh/latest/openmvcam/index.html)

[microbit 中文](http://www.qingchuangzhiyi.com/doc/tutorials/hello.html)

[micropython 官方](http://docs.micropython.org/en/latest/esp32/quickref.html)

[MicroPython 中文](https://MicroPython.readthedocs.io/zh/master/)

## python

```unix
pip install sphinx, sphinx_rtd_theme, recommonmark
```

## powershell

```bat
.\make.bat html
```

## git (Do not handle)

```unix
git submodule add https://github.com/micropython/micropython
git submodule add https://github.com/labplus-cn/MicroPython

git submodule update --init --recursive
```
