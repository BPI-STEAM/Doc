# 氣象資訊

氣象資訊積木能夠即時從中央氣象局取得開放資料，包含即時氣象、空氣品質、天氣預報、地震資訊、水庫水情和雷達回波圖...等常用氣象資訊，透過這些氣象資訊搭配物聯網的實作，更能落實氣象資訊的有效應用。

## 氣象資訊積木清單

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-01.jpg)

## 取得氣象資料

氣象資訊有一塊「取得氣象資訊」積木，可以取得六種常用資訊，分別是「空氣品質」、「即時觀測」、「天氣預報」、「地震資訊」、「水庫水情」和「雷達回波圖」。

> 取得氣象資訊的積木屬於「*取得資訊後才會繼續執行後方程序*」的類型，當編輯畫面中有這塊積木，*執行時當程序遇到這塊積木會暫停，直到取得氣象資訊之後才會再繼續*。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-03.jpg)

## 空氣品質

「空氣品質」積木能夠顯示空氣品質的相關資訊，包含 AQI、PM2.5、PM10...等相關數值以及綜合指標的文字描述，偵測的地點為中央氣象局在台灣的觀測站台，可選擇離住家最近的地點作為觀測依據。

> 空氣品質積木需搭配「取得氣象資料」積木取得「空氣品質」資訊。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-02.jpg)

下圖的例子，取得前鎮區空氣品質資料，並透過小怪獸講出空氣品質綜合指標，以及個別的偵測數值。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-04.jpg)

## 即時觀測

「即時觀測」積木能夠顯示目前天氣的相關資訊，包含溫度、濕度、風力、累積雨量...等相關數值，偵測的地點為中央氣象局在台灣的觀測站台，可選擇離住家最近的地點作為觀測依據。

> 即時觀測積木需搭配「取得氣象資料」積木取得「即時觀測」資訊。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-05.jpg)

下圖的例子，分別透過小怪獸講出高雄與台北的即時氣象資訊。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-06.jpg)

## 氣象預報

「氣象預報」積木能夠顯示未來六小時、十八小時和三十六小時的氣象預報，預報地點為台灣的主要縣市，可選住家所在縣市作為觀測依據。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-07.jpg)

下圖的例子，分別透過小怪獸講出高雄八小時的氣象預報，以及新竹十八小時的氣象預報。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-08.jpg)

## 水庫水情

「水庫水情」積木能夠取得全台灣所有水庫的水情資心，包含蓄水百分比、有效蓄水量和降雨量...等。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-09.jpg)

下圖的例子，分別透過小怪獸講出石門水庫和曾文水庫的水情資訊。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-10.jpg)


## 地震資訊

「地震資訊」積木能夠取得最近 1~3 次的地震資訊。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-11.jpg)

下圖的例子，透過小怪獸講出最近一次的地震資訊 ( 範例日期為 5/17 )。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-12.jpg)

## 雷達回波

「雷達回波」積木能夠取得一張雷達回波圖，圖片格式為 jpg。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-13.jpg)

下圖的例子，透過小怪獸展示雷達回波圖。

![氣象資訊](../images/zh-tw/docs/webbit/extension/weather-14.jpg)


