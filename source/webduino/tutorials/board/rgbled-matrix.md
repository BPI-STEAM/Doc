## 矩阵 LED 

开发板的正中央内嵌了一个由 25 颗矩阵 LED  组成的的 LED 矩阵 ，每个 LED 都可通过红、绿、蓝三种颜色进行混合产生各种不同颜色，让指定位置的 LED 显示指定的颜色并组合，就能显示各种图案。

### 矩阵 LED 积木清单

矩阵 LED 积木清单包含显示颜色、关灯、绘制图案、预设图案、指定第几颗灯的颜色、跑马灯和亮度等积木。

![](rgbled-matrix/upload_f63f939496f887fe4786365a69edc0fc.png)

> *使用矩阵 LED 积木必须搭配「开发板」积木*，选择模拟器，执行后可以控制右侧模拟器的 LED 矩阵，选择 USB，执行后会通过 USB 连接方式控制实体开发板，选择 Wi-Fi 则可通过 Wi-Fi 指定 Device ID 操控开发板。

![](rgbled-matrix/upload_a405d0e0455fd644717101c3751df0a6.png)

### 显示颜色

「显示颜色」积木可以让 25 颗灯同时亮起指定的颜色。 ( 若选择黑色，效果等同不亮灯 )

![](rgbled-matrix/upload_e2315998a8cfe9acedd68bec5112c70c.png)

开发板选择模拟器，显示颜色积木选择红色，执行后，虚拟的开发板 25 颗灯都变成红色。 ( 若手边有开发板，可以使用 USB 或 Wi-Fi 连接控制 )

![](rgbled-matrix/upload_081903273b3fd8d4f529c88856192fe4.png)

### 绘制图案

「绘制图案」积木能够自定义每颗灯不同的颜色，绘制一个 5x5 的图案。

![](rgbled-matrix/upload_c852f4d68838e6c5d0016e01560b9f9e.png)

点击积木上方的颜色区块就能选择不同颜色，如果是同颜色，重复点击就可以还原为黑色 ( 直接使用黑色也是同样的效果 )。

![](rgbled-matrix/upload_0b38e47c44fb3a3d7755e7908cea45e5.gif)

例如绘制一朵花，让花瓣为红色，花梗和叶子为绿色，执行后，虚拟的开发板就会呈现一朵彩色的花。

![](rgbled-matrix/upload_32a049fb957b51d0cc47af0c38baf1d1.png)

### 预设图案

「预设图案」积木提供 60 种预设图案，以及一个随机图案选项 ( 60 种图案随机取出一种 )。

![](rgbled-matrix/upload_9b89853f2ac3a318d844980d02b42f0e.gif)

选择图案和颜色，执行后，虚拟开发板就会出现对应的图案和颜色。

![](rgbled-matrix/upload_5a1b8919a68c65b2b25529c2278016ea.png)

### 显示一个字

「显示一个字」积木可以显示*单个*大小写英文字母、数字或标点符号 ，并指定显示的颜色。 ( 不支持显示中文 )

![](rgbled-matrix/upload_d8c17706d60bfdaddf9a1997ad2ebd62.png)

在文字积木输入字母或数字并指定颜色，执行后就会看到指定颜色的字母或数字出现。

![](rgbled-matrix/upload_2810b8f54fbf9129c79c93a919bfa638.png)

### 跑马灯

「跑马灯」积木可以通过跑马灯的方式，以指定的颜色显示一串文字，跑马灯可以只进行一次或无限次重复播放，并能设定文字移动的速度。 ( 不支持显示中文 )

![](rgbled-matrix/upload_879d253f34acc1b464e08ef98965e7f9.jpg)

如果设定跑马灯次数为「一次」，跑马灯积木会是「*执行完成才会继续执行后面积木程序*」的类型( 点击前方问号会提示)，*跑马灯结束后才会接着执行其他程序*，若设定为「无限次」，*后台程序会继续执行，但和LED 矩阵有关的行为会被跑马灯所取代*，使用上要特别注意。

![](rgbled-matrix/upload_7b9090bfacbbbdf3801cf8f77112c4bc.png)

下图的例子，执行后会先出现红色 Hello 文字的跑马灯，结束后紧接着出现绿色笑脸。

![](rgbled-matrix/upload_6fbc7a9ca95c10b182cce3a2b44b1952.gif)

### 矩阵 LED 控制灯号

「矩阵 LED 控制灯号」积木可以控制矩阵 LED 指定灯号的运行。

![](rgbled-matrix/upload_a360aaa10807f6cb8c8e2facc7445288.png)

矩阵 LED 的顺序对应到 开发板的灯号顺序，开发板灯号 1~25 的顺序为从左到右、从上到下。

![](rgbled-matrix/rgbled-matrix-16.jpg)

举例来说，若设定矩阵 LED 的三个值为红色、绿色和蓝色，开发板的第 1~3 个灯就会呈现对应的颜色。

![](rgbled-matrix/upload_392fba6ea5f3fbbc97935255cdfe03de.png)

如果是多维矩阵 LED ，会按照矩阵 LED 元素的顺序进行显示，若元素内容留空，该颗 LED 会呈现熄灯状态。

![](rgbled-matrix/upload_249539e18180c1815e49ef8dd3e51120.png)

### 第几颗灯

「第几颗灯」积木可以指定第几颗灯的颜色。

![](rgbled-matrix/upload_2f91b361f5363749fb2de4332e041c7b.png)

第几颗灯的顺序对应到开发板的灯号顺序，开发板灯号 1~25 的顺序为从左到右、从上到下。

![](rgbled-matrix/rgbled-matrix-16.jpg)

分别指定不同位置的灯号颜色，执行后就会看见指定位置的灯号亮起。

![](rgbled-matrix/upload_670bd7d51c9f594273b0a4329f5a7511.png)

### X、Y 座标控制灯号

「X、Y 座标控制灯号」积木可以通过 X 和 Y 的座标值指定灯号的颜色显示。

![](rgbled-matrix/upload_f467507ed38a3018e166a1a4d806ef7b.png)

开发板的 X、Y 座标以左上角为 ( 1, 1 )，往右 X 加 1，往下 Y 加 1，依此类推。

![](rgbled-matrix/rgbled-matrix-22.jpg)

分别指定不同 X、Y 的灯号颜色，执行后就会看见指定位置的灯号亮起。

![](rgbled-matrix/upload_6e19592bbea111a87ba2441f6b44f05c.png)

### 亮度

「亮度」积木可以控制「*全部 LED 灯*」的亮度，该积木无法指定单一颗灯的亮度，亮度最暗到最亮的数值为 0 ~20，预设值 10。

![](rgbled-matrix/upload_e531c3542454cd50f41475c8f89ae4f9.png)

### 关灯

「关灯」积木可以关闭「*全部 LED 灯*」，效果等同于把 25 颗灯的颜色同时设定为黑色。

![](rgbled-matrix/upload_d8f9d8823ceebcb3763d556a5b0bb4a8.png)
