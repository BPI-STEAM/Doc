# 小怪獸基本操作

編輯器設計了四隻可愛的小怪獸，透過程序積木編排邏輯順序，就能控制每隻小怪獸的說話、聲音、互動與行為...等動作，甚至能進一步與實際 開發板互動，做出更多好玩的有趣應用。

## 小怪獸積木清單 ( 基本操作 )

基本操作小怪獸的積木分別有講話、展示圖片、情緒、改變位置、改變角度、改變大小、顯示隱藏和階層...等，可以透過這些積木控制小怪獸的外在表現。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-01.jpg)

## 講話＆不講話

「講話」和「不講話」積木可以讓小怪獸講出指定的文字，或不要講出文字，透過下拉選單也可以選擇哪一隻小怪獸講話，或所有小怪獸一起講話。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-02.jpg)

只要在講話的積木後方，連接指定的文字，網頁執行後小怪獸就會說出指定的文字。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-03.jpg)

只要把文字留空，或者使用不說話的積木，就能夠讓小怪獸不說話。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-04.jpg)

## 展示圖片

「展示圖片」積木可以讓小怪後展示一張「網路圖片」。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-05.jpg)

舉例來說，從維基百科上搜尋[蒙娜麗莎](https://zh.wikipedia.org/wiki/%E8%92%99%E5%A8%9C%E4%B8%BD%E8%8E%8E#_blank)，可以得到這張圖片的「[網址](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Mona_Lisa%2C_by_Leonardo_da_Vinci%2C_from_C2RMF_retouched.jpg/460px-Mona_Lisa%2C_by_Leonardo_da_Vinci%2C_from_C2RMF_retouched.jpg#_blank)」，複製圖片網址，貼到小怪獸展示圖片的文字空格內，網頁執行後，就會看見小怪獸展示這張圖片。

> 目前圖片格式僅支援 jpg、jpeg、png、gif

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-06.jpg)

## 情緒

「情緒」積木可以改變小怪獸的情緒，包含開心、驚訝、生氣、難過和隨機。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-07.jpg)

選擇對應的小怪獸 ( 也可以四隻同時 )，選擇對應的情緒，網頁執行後就會看見小怪獸的情緒變化。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-08.jpg)

## 改變位置

「改變位置」積木可以指定小怪獸改變*目前的位置*，選項有往上、往下、往左、往右、隨機或朝向滑鼠方向。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-09.jpg)

搭配重複十次和等待 0.1 秒的積木，就能夠讓小怪獸往右上方移動。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-10.gif)

如果使用無線重複的積木，搭配「朝著滑鼠位置」的設定，就能夠讓小怪獸追著滑鼠移動。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-11.gif)

## 定位

「定位」積木能夠把小怪獸擺放到指定的坐標位置。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-12.jpg)

怪獸的座標系統採用*笛卡兒座標系統* ( 直角座標系統 )，往上 y 為正，往右 x 為正，而 (0,0) *原點位在怪獸互動舞台的左下角*，指定小怪獸 xy 坐標，網頁執行後小怪獸就會出現在指定的位置。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-13.jpg)

## 旋轉角度

「旋轉角度」可以指定小怪獸改變*目前的角度*，選項有往左或往右。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-14.jpg)

搭配重複無限次的積木，就能讓小怪獸不斷的每隔 0.1 秒旋轉 10 度。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-15.gif)


## 面朝方向

「面朝方向」角度可以指定小怪獸旋轉的角度，順時針為正，逆時針為負。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-16.jpg)

因為「面朝方向」是指定一個角度，如果要做到和前一個積木「旋轉角度」一樣的效果，可以使用变量搭配無限重複的積木，在每一次執行時修改变量數值即可。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-17.gif)

## 自動面朝滑鼠方向

「自動面朝滑鼠方向」積木能讓小怪獸轉到滑鼠所在的方向，有自動和停止兩個選項，預設並不會面朝滑鼠。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-18.jpg)

因為「自動面朝滑鼠方向」只會執行一次，所以如果要讓小怪獸不斷的面向滑鼠，就必須搭配無限重複的積木，如下圖，網頁執行後小怪獸就會自動面向滑鼠旋轉。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-19.gif)

## 取得座標和角度

「取得座標和角度」積木能夠讀取小怪獸當前的 X 座標、Y 座標和旋轉角度。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-20.jpg)

下圖的例子，就能讓小怪獸自己講出自己的 X 座標、Y 座標和旋轉角度。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-21.jpg)

## 尺寸放大縮小

「尺寸放大縮小」積木可以指定小怪獸改變*目前的大小*，選項有放大或縮小。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-22.jpg)

搭配重複十次和等待 0.1 秒的積木，網頁執行後，就能夠讓小怪獸逐漸變大。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-23.gif)

## 尺寸百分比

「尺寸百分比」積木可以指定小怪獸放大縮小的百分比。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-24.jpg)

由於 100% 表示原本怪獸大小，所以 200% 就會是一倍大，50% 則是會縮成 1/2 大小，下圖透過尺寸百分比，分別讓四隻小怪獸呈現不同尺寸大小。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-25.jpg)

## 顯示/不顯示

「顯示/不顯示」積木可以指定小怪獸是否顯示在互動舞台區。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-26.jpg)

## 階層

「階層」積木可以指定小怪獸排列的階層，最上層在最前面，最下層在最後面。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-28.jpg)

透過重複迴圈以及等待的積木，能夠讓小怪獸的階層依序顯示在最前面。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-29.gif)

## 回到原始狀態

「回到原始狀態」積木可以讓小怪獸回到初始狀態，初始狀態包含不說話、預設座標、預設旋轉角度和預設尺寸大小。

![小怪獸基本操作](../images/zh-tw/docs/webbit/monster/basic-27.jpg)





