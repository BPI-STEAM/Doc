# 語音辨識

隨著科技的技術日新月異，過去在行動裝置才能使用的語音辨識功能，如今 編輯器也能完整實現，結合 Google 語音辨識的技術，如果電腦有麥克風，就能輕鬆做出「Hey Siri」或「OK Google」的有趣聲控效果。

## 語音辨識積木說明

語音辨識積木可以分別識別中文和英文的語言，無法進行中英文夾雜的混合辨識。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-01.jpg)

語音辨識積木屬於「*執行完成才會繼續執行後方程序*」的類型 ( 點擊前方問號小圖示會提示 )，每段語音辨識時間為兩秒，*辨識後才會繼續執行後方的程序*。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-02.jpg)

## 透過小怪獸顯示語音辨識文字

進行語音辨識之後，就能使用「辨識的文字」積木，下圖的範例會在語音辨識後，讓小怪獸講出辨識的文字。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-03.jpg)

使用語音辨識積木時，如果是「網頁版」的編輯器，在網頁執行後會詢問「是否允許使用麥克風」，勾選允許。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-04.jpg)

網頁允許麥克風後，在瀏覽器頁籤上會出現一個小圓點，提示麥克風正在運作。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-05.jpg)

此時可以對著麥克風講話，語畢就能看見小怪獸講出辨識的文字。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-06.jpg)

## 連續語音辨識

藉由語音辨識積木的特性，搭配重複迴圈，就能不斷進行語音辨識來更新小怪獸講出的文字。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-08.gif)

## 語音辨識控制 開發板

如果將語音辨識結合 開發板，搭配邏輯判斷判斷文字內包含的字詞，就能實現物聯網聲控的應用，下圖的例子便可以很簡單的透過聲控開關燈，或透過聲控改變顏色。

![語音辨識](../images/zh-tw/docs/webbit/sound/speech-recognition-09.gif)
