# build

[![Documentation Status](https://readthedocs.org/projects/bpi-steam-docs/badge/?version=latest)](https://bpi-steam-docs.readthedocs.io/zh_CN/latest/?badge=latest)

## how to edit

The document content is in [source](https://github.com/BPI-STEAM/Docs/tree/master/source).

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
