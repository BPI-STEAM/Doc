# 顏色

透過改變網頁中元素的顏色，或指定實際 開發板全彩 LED 矩陣的燈光顏色，藉由五顏六色的趣味變化，就能做出許多絢麗奪目的效果。

## 顏色積木清單

陣列積木包含指定顏色、隨機顏色、RGB 三原色、混合顏色...等四種常用顏色積木。

![顏色](../images/zh-tw/docs/webbit/basic/color-01.jpg)

## 指定顏色

「指定顏色」積木可以讓我們透過色彩選取面板，選擇對應的顏色。

![顏色](../images/zh-tw/docs/webbit/basic/color-02.jpg)

如果我們指定小怪獸互動舞台的背景為紅色，網頁執行後舞台背景就會變成紅色。

![顏色](../images/zh-tw/docs/webbit/basic/color-03.jpg)

## 隨機顏色

「隨機顏色」會在每次網頁執行時，隨機從各種顏色中取出一種顏色顯示。

![顏色](../images/zh-tw/docs/webbit/basic/color-04.jpg)

如果搭配重複迴圈，網頁執行後，就能看到小怪獸舞台背景的顏色不斷隨機變化。

![顏色](../images/zh-tw/docs/webbit/basic/color-05.gif)

## RGB 三原色

「RGB 三原色」積木能夠指定網頁中三原色的數值，直接透過數值來呈現不同的顏色。

> 三原色表示 *R 紅色、G 綠色、B 藍色*，三種顏色分別有 256 種從暗到亮的變化，透過三種顏色的混合，就能產生一千六百多萬種的顏色。( 但人的眼睛無法分辨這麼多種顏色 )

![顏色](../images/zh-tw/docs/webbit/basic/color-06.jpg)

因為顏色有 256 種，對應的數值就是 0 ~ 255，0 是最暗，255 是最亮，輸入對應的數值就能產生對應的顏色，舉例來說紅色 255 搭配綠色 255 就會是黃色。

> 網頁的三原色為「*色光*」，*紅色 + 綠色 = 黃色*，*綠色 + 藍色 = 青色*，*紅色 + 藍色 = 紫色*。

![顏色](../images/zh-tw/docs/webbit/basic/color-07.jpg)

搭配重複迴圈，就能夠做出紅色到黃色的顏色轉換效果。

![顏色](../images/zh-tw/docs/webbit/basic/color-08.gif)


## 混合顏色

「混合顏色」積木是指兩種顏色積木按照比例混合產生新的顏色，比例為 0~1 之間的數值，數字越小顏色越接近顏色 1，數字越大顏色越接近顏色 2。

![顏色](../images/zh-tw/docs/webbit/basic/color-09.jpg)

如果把顏色 1 設定為紅色，顏色 2 設定為藍色，比例 0.2 的混合顏色就是偏紅色的紫色。

![顏色](../images/zh-tw/docs/webbit/basic/color-10.jpg)

搭配重複迴圈，就能夠做出從紅色到藍色的顏色轉換效果

![顏色](../images/zh-tw/docs/webbit/basic/color-11.gif)

