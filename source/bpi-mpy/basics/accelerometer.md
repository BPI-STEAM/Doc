
# Document

![](./head.jpg)

## 板子姿态检测

- 这个模块可以让你获得板子当前的九轴姿态，分别是加速度、重力、磁感应的(X\Y\Z)方向状态值。
  
- 最基本的功能是获取它们当前的 X、Y、Z 三轴的值来判断板子此时的运动状态，比如说，加速度 Z 值由小增大，表示 Z 轴方向上有在移动（有了加速度），所以可以判断出板子在移动，移动的方向在 Z 轴之上。 
  
### 基础运用

- 经过了简单的介绍，我们可以设计一个简单的判断，例如 获取板子的平衡情况，以 accelerometer 加速度模块为例，获取它的 X 轴的值，即可得到一个基本的数值，如果数值大于 20 说明它向右偏了，如果小于 - 20 则说明它向左偏了，如果在 这两者之间，则说明它是平衡的，所以有如下的代码，显示 L 表示向左偏，而显示 R 表示板子向右偏了，试试吧！

```python
from microbit import *

while True:
    reading = accelerometer.get_x()
    if reading > 20:
        display.show("R")
    elif reading < -20:
        display.show("L")
    else:
        display.show("-")
```

### 实测效果

- ![base](how_to_accelerometer/base.gif)

### 进阶运用

- 姿态检测，例如上下左右左右，前进后退摇晃自由落地等，如下代码就是，当板子面向上的时候显示笑脸，面向下的则是显示生气的表情。

```python
from microbit import *

while True:
    gesture = accelerometer.current_gesture()
    if gesture == "face up":
        display.show(Image.HAPPY)
    else:
        display.show(Image.ANGRY)

```

### 实测效果

- 当前固件还未更新该功能。

### 趣味游戏

- 基于先前的基础运用，我们可以做出一个趣味游戏，代码在下方连接，底下也有对应的实测动图，可能要加载一会，有些庞大。

- [平衡球代码（适用于 1.4 版）](https://github.com/BPI-STEAM/BPI-BIT-MicroPython/blob/master/11.app/balance_ball.py)

- ![balance_ball](how_to_accelerometer/balance_ball.gif)

- ![logo](./logo.jpg)
