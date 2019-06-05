# 矩陣 LED

開發板的正中央內嵌了 25 顆全彩 LED 所組成的的矩陣，每個 LED 都可透過紅、綠、藍三種顏色進行混合產生各種不同顏色，透過不同位置的燈號與顏色搭配顯示，就能呈現各種圖案造型。

## 矩陣 LED 積木清單

矩陣 LED 積木清單包含顯示顏色、關燈、繪製圖案、預設圖案、指定第幾顆燈的顏色、跑馬燈和亮度等積木。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-01.jpg)

> *使用矩陣 LED 積木必須搭配「開發板」積木*，選擇模擬器，執行後會控制右側模擬器燈號，選擇 USB，執行後會透過 USB 連線方式控制實體開發板，選擇 Wi-Fi 則可透過 Wi-Fi 指定 Device ID 操控。
> - USB 控制模式為「安裝版編輯器」限定，請參考 [編輯器](../index.html#software)
> - Wi-Fi 模式需要開發板連接 Wi-Fi，請參考 [硬體開發板 ( 初始化設定 )](../info/setup.html)

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-02.jpg)

## 顯示顏色

「顯示顏色」積木可以讓 25 顆燈同時亮起指定的顏色。( 若選擇黑色，效果等同不亮燈 )

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-04.jpg)

開發板選擇模擬器，顯示顏色積木選擇紅色，執行後，虛擬的開發板 25 顆燈都變成紅色。( 若手邊有 開發板，可以使用 USB 或 Wi-Fi 連線控制 )

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-03.jpg)

## 繪製圖案

「繪製圖案」積木能夠自定義每顆燈不同的顏色，繪製一個 5x5 的圖案。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-05.jpg)

點選積木上方的顏色區塊就能選擇不同顏色，如果是同顏色，重複點擊就可以還原為黑色 ( 直接使用黑色也是同樣的效果 )。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-07.gif)

例如繪製一朵花，讓花瓣為紅色，花梗和葉子為綠色，執行後，虛擬的開發板就會呈現一朵彩色的花。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-06.jpg)

## 預設圖案

「預設圖案」積木提供 56 種預設圖案，以及一個隨機圖案選項 ( 60 種圖案隨機取出一種 )。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-08.gif)

選擇圖案和顏色，執行後，虛擬的開發板就會出現對應的圖案和顏色。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-09.jpg)


## 顯示一個字

「顯示一個字」積木可以顯示*單一個*大小寫英文字母、數字或標點符號，並指定顯示的顏色。( 不支援中文字 )

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-10.jpg)

在文字積木輸入字母或數字並指定顏色，執行後就會看到指定顏色的字母或數字出現。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-11.jpg)

## 跑馬燈

「跑馬燈」積木可以透過跑馬燈的方式，以指定的顏色顯示一串文字，跑馬燈可以只進行一次或無限次重複播放，並能設定文字移動的速度。( 不支援中文字 )

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-12.jpg)

如果設定跑馬燈次數為「一次」，跑馬燈積木會是「*執行完成才會繼續執行後方程序*」的類型 ( 點擊前方問號小圖示會提示 )，*跑馬燈結束後才會接著執行其他程序*，若設定為「無限次」，*後方程序會繼續執行，但和 LED 矩陣有關的行為會被跑馬燈所取代*，使用上要特別注意。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-13.jpg)

下圖的例子，執行後會先出現紅色 Hello 文字的跑馬燈，結束後緊接著出現綠色笑臉。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-14.gif)

## 陣列控制燈號

「陣列控制燈號」積木可以使用陣列的方式控制矩陣 LED 燈號的運作。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-15.jpg)

陣列的順序對應到 開發板的燈號順序，開發板燈號 1~25 的順序為從左到右、從上到下。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-16.jpg)

舉例來說，若設定陣列的三個值為紅色、綠色和藍色，開發板的第 1~3 個燈就會呈現對應的顏色。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-17.jpg)

如果是多維陣列，會按照陣列元素的順序進行顯示，若元素內容留空，該顆 LED 會呈現熄燈狀態。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-18.jpg)

## 第幾顆燈

「第幾顆燈」積木可以指定第幾顆燈的顏色。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-19.jpg)

第幾顆燈的順序對應到 開發板的燈號順序，開發板燈號 1~25 的順序為從左到右、從上到下。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-16.jpg)

分別指定不同位置的燈號顏色，執行後就會看見指定位置的燈號亮起。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-20.jpg)

## X、Y 座標控制燈號

「X、Y 座標控制燈號」積木可以透過 X 和 Y 的座標值指定燈號的顏色顯示。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-21.jpg)

開發板的 X、Y 座標以左上角為 ( 1, 1 )，往右 X 加 1，往下 Y 加 1，依此類推。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-22.jpg)

分別指定不同 X、Y 的燈號顏色，執行後就會看見指定位置的燈號亮起。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-23.jpg)

## 亮度

「亮度」積木可以控制「*全部 LED 燈*」的亮度，該積木無法指定單一顆燈的亮度，亮度最暗到最亮的數值為 0 ~20，預設值 10。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-24.jpg)

## 關燈

「關燈」積木可以關閉「*全部 LED 燈*」，效果等同於把 25 顆燈的顏色同時設定為黑色。

![矩陣 LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-25.jpg)



