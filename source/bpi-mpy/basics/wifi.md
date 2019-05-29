# Document

![](./head.jpg)

## 无线编程模式

### 板子连接 WIFI 热点

- 固件上电后，在面板 LED 灯滚动完毕后，默认就会尝试联网，你可以注意到，如果这时候被工具或人为的 Ctrl + C 停止后，将不会进行联网操作，需要使用以下代码

```python
import wifi # booy.py default enable
wifi.try_connect()
```

- 效果如下图，默认 boot.py 里会默认调用 `import wifi`，所以你也可以直接在 REPL 中调用 `wifi.try_connect()`。

- ![try_connect](how_to_wifi/try_connect.png)

- 在默认的联网模式下，如果从来没有配网过，板子最初会自动连接 WIFI 名称 `webduino.io` 密码 `webduino` 的 WIFI 热点。

- 如果附近没有该热点，将会输出`no AP found`，而我的环境里提前准备了这个热点，因此会得到一个IP地址`192.168.10.185`（如图），否则将会反复输出连接存在的问题（这并不会影响你的输入和输出），如果不希望它继续连接网络，可以手动输入`wifi.close()`停止 WIFI 连接。

- ![got_ip](how_to_wifi/got_ip.png)

#### 1. 手机配网模式

- 当然，你的 WIFI 热点肯定不是这个，所以你现在可以在开机的LED滚动过程中按下 **A键** 并松开，会自动进入配网模式，重新给板子连入其他WIFI，帮助板子连上指定 WIFI，进入`SmartConfig` 的配网模式，LED（18）将会亮起，LED（18）是先前章节点亮过的 LED 灯。

- ![start_config](how_to_wifi/start_config.png)

- 复位后看板子的 LED灯 长亮 即可确认进入了配网模式，如果有必要，你也可以在此时的串口查看输出对应的信息，注意在这个模式将无法正常使用`Mpfshell` 的 open ，这是因为此时板子已经无法响应串口的 REPL 操作了，因此你需要配网完成后再次使用`Mpfshell`。

- ![smartconfig](how_to_wifi/smartconfig.png)

- 如果期间工具运行出错，请使用其他串口工具查看输出信息，例如 [Release](https://github.com/BPI-STEAM/BPI-BIT-MicroPython/releases) 下提供的 `Windows-ComDbg.zip` 。

- ![view_com](how_to_wifi/view_com.png)

- 确认进入了配网模式后，此时你需要使用一台安卓手机来安装 [Tools](https://github.com/BPI-STEAM/BPI-BIT-MicroPython/releases/tag/Tools)  提供的配网软件

- ![view_apk](how_to_wifi/view_apk.png)

- 以 `Android-SmartConfig.apk` 为例，先将手机连入WIFI，然后再将让板子也连入同一个WIFI，再到软件中输入所连WIFI的密码，这将告知板子，如何连接到该WIFI。

- ![open_apk](how_to_wifi/open_apk.png)

- 点击唯一的按钮启动配网，可以看到 REPL 有对应信息输出，同时板子的 LED 灯也会跟着变化。

- ![smc_apk](how_to_wifi/smc_apk.png)

- 等待一会，如果卡在了配网模式没有成功，则会在两分钟内会自动重启。而当配网成功后，LED 灯会变成 **微亮**，此时 REPL 会输出板子连上 WIFI 得到的 IP 地址，如下图为：`192.168.10.185`，并且 值得注意的是 3de1 就对应的是板子的名称，这个名称以后会用到。

- ![smc_finish](how_to_wifi/smc_finish.png)

- 并且在手机上，也会看到板子的 IP 地址，此时板子已经完成了网络配置。

- ![apk_finish](how_to_wifi/apk_finish.png)

- 小提示：如果配网失败，请按以下流程排除问题。

  - 确认进入了 配网模式（SmartConfig）
  - 确认 WIIFI 热点密码无误
  - 确认配网过程中 REPL 输出的信息与图示相近
  - 确认 WIFI 射频 是 2.4Ghz（重要）

#### 2. 手动联网模式

- 当你出现以上配网失败的时候，且找不到任何解决办法，你可以使用直接的联网流程，即手动输入 WIFI 名称和密码。

- （现在固件会在调用 wifi.start() 后自动生成 `wifi_cfg,py`）

- 准备一个 `wifi_cfg,py`, 其中内容为：

  ```python
  WIFI_SSID = '你的WIFI热点名称'
  WIFI_PSWD = '你的WIFI热点密码'
  HOST_NAME = '你板子的网络名称' # 可选
  ```

- （现在已经可以先 `get wifi_cfg.py` 取回配置）与 `mpfshell` 同一个目录中使用 `put wifi_cfg.py`, 将其替换掉现在的 WIFI 连接配置。

- 你也可以直接在 `repl` 中输入 'wifi.smartcoinfig()'， 来手动启动配网模式，而不是使用开机时的按键触发。

### 板子无线使用 REPL

- 注意，使用前确保允许应用通过网络防火墙，且电脑与板子连接处于同一网络下（同一个WIFI下）。

- 在这之前先进入 `repl` 输入`import webrepl_setup`启动网络配置流程。

- 根据步骤依次为（e、1234、y）

  - 启动网络服务配置（启动输入 e，停止输入 d）
  - 设置网络连接密码（不少于4位，需输入两遍，由自己决定，我只是为了省事）
  - 是否需要重启板子（复位输入y，否则输入 n）
  - ![webrepl](how_to_wifi/webrepl.png)

- 此前我已经知道了板子现在的 IP为 `192.168.10.185`，如果不知道可以重新上电查看，接着使用`mpfshell` ，输入`ws:192.168.10.185,1234`， 其中`,1234`是我此前设定的连接密码（前一章），你也可以现在不输入，但待会也一样会提示你输入密码的。（注意是英文输入法的逗号）

- ![into_webrepl](how_to_wifi/into_webrepl.png)

- 可以看到已经连接成功，此时板子也可以透过无线来操作了，你也可以重启复位再试一次。

- 连接失败会有以下两种提示：

  - 连接远端无响应，提示`WebREPL Remote IP Does not respond`，分析的情况是一种可能是与板子不同属一个网络，另一种可能是各种软件或硬件防火墙挡住了。
  - 连接密码错误，提示`WebREPL Password Error`，重新输入密码即可，也许你连到别人的板子去了呢。
  - 出现问题时的操作，假设连不上，先用有线进去按 Ctrl + D 软复位核对连接，接着退出来换成无线连接。
  - ![error_webrepl](how_to_wifi/error_webrepl.png)

- 提示：关于如何使用 Pycharm Mpfshell 插件的无线连接，只需要在设备路径（comx）的地方设置 `ws:192.168.10.185,1234` 即可。

- ![webrepl_pycharm](how_to_wifi/webrepl_pycharm.png)

![logo](./logo.jpg)
