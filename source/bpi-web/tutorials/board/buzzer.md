# 音樂＆聲音

開發板內建一個微型蜂鳴器，可以發出三個八度音階的單一聲響，藉由不同音符代碼的組合，或者搭配內建的範例音樂，就能讓開發板發出各種美妙的旋律。

## 音樂＆聲音積木清單

音樂＆聲音的積木包含演奏某個音階、休息、預設音樂和停止演奏...等積木。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-01.jpg)

> *音樂＆聲音積木必須搭配「開發板」積木*，選擇模擬器，執行後可以聽見電腦喇叭發出聲音，選擇 USB，執行後會透過 USB 連線方式控制實體開發板，讓開發板的蜂鳴器發出聲音，選擇 Wi-Fi 則可透過 Wi-Fi 指定 Device ID 操控。
> - USB 控制模式為「安裝版編輯器」限定，請參考 [編輯器](../index.html#software)
> - Wi-Fi 模式需要開發板連接 Wi-Fi，請參考 [硬體開發板 ( 初始化設定 )](../info/setup.html)

## 演奏音階

「演奏音階」積木可以演奏三個八度音階，同時亦可指定每個音階的拍子，拍子分為 1/16、1/8、1/4、1/2、1 和 2 拍。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-02.jpg)

點選音階的選項會彈出一個虛擬的鋼琴鍵盤，使用滑鼠移到琴鍵上，電腦的喇叭就會發出對應的聲響。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-03.gif)

在音階的缺口，可以分別放入音階和休止符積木，持續的缺口只能放入拍子積木。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-08.jpg)

放入好幾個音階，執行後可以聽到一個音階接著一個音階播放。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-04.gif)

由於演奏音階積木會是「*演奏完成才會繼續執行後方程序*」的類型，若程序放在音階之後，在所有音階演奏完成後，才會執行後方程序。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-05.gif)

演奏音階積木也可以搭配重複迴圈，做到不斷重複播放一段旋律的效果。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-06.gif)

音階積木支援陣列的使用，藉由陣列的排列組合，就能自行編輯音樂並重複使用，下圖的例子，分別將音階和拍子獨立成兩個陣列。

> 使用陣列的情況下，若音階數量少於拍子，多出來的拍子會採用最後一個音階播放，若拍子數量少於音階，多出來的音階會採用最後一個拍子播放。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-09.jpg)


## 演奏休息

「演奏休息」積木表示該拍子沒有聲音，等同於使用演奏音階積木搭配休止符積木。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-07.jpg)

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-10.gif)

## 演奏音樂

「演奏音樂」積木包含超級瑪琍、超級瑪琍和弦、真善美、哥哥爸爸真偉大和叮叮噹五首音樂，可以獨立使用或和音階積木搭配使用。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-11.jpg)

由於演奏音樂積木會是「*演奏完成才會繼續執行後方程序*」的類型，若有音階或其他程序放在演奏音樂之後，音樂演奏完成後，才會執行後方程序。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-12.gif)


## 停止/暫停/繼續演奏

「停止/暫停/繼續演奏」積木可以控制音樂演奏的行為。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-13.jpg)

下圖的例子透過 開發板的按鈕開關控制音樂播放，A 和 B 同時按下時開始播放，播放進行中按下 A 就會暫停，按下 B 就會繼續播放。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-14.gif)

如果要將音樂、音階拍子積木混合控制，在切換音樂之前加入「停止播放」的積木，就可完全停止現有的音樂並進行切換。

![音樂＆聲音](../images/zh-tw/docs/webbit/board/buzzer-15.jpg)

