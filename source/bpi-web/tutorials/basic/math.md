# 數學

數學積木包含了許多數學運算，從基本的加減乘除，到四捨五入、平均值、中位數...等應有盡有，不論是簡單的程序或複雜應用，都能透過各式各樣的數學運算實現。

## 數學積木清單

數學的積木分別有數字、運算式、基礎函式、總和、隨機數和尺度轉換...等常用的數學運算式。

![數學](../images/zh-tw/docs/webbit/basic/math-01.jpg)

## 指定數字

「指定數字」積木用來讓我們輸入數字，可輸入整數或是帶有小數點的浮點數，很常用於運算式或判斷式。

![數學](../images/zh-tw/docs/webbit/basic/math-02.jpg)

## 取得範圍內隨機整數

「取得範圍內隨機整數」積木會指定一個數字範圍，在每次執行這塊積木時，就會從這個數字範圍內取出隨機的整數。

![數學](../images/zh-tw/docs/webbit/basic/math-03.jpg)

搭配重複無限次和等待積木，可以讓小怪獸每隔一秒說出一個隨機整數。

![數學](../images/zh-tw/docs/webbit/basic/math-05.gif)

## 取得隨機分數

「取得隨機分數」積木會在每次執行時，隨機取得一個 0 到 1 之間的浮點數。

![數學](../images/zh-tw/docs/webbit/basic/math-04.jpg)

搭配重複無限次和等待積木，可以讓小怪獸每隔一秒說出一個隨機浮點數。

![數學](../images/zh-tw/docs/webbit/basic/math-06.gif)

## 數學運算

「數學運算」積木可以針對數字進行加、剪、乘、除和次方五種運算。

![數學](../images/zh-tw/docs/webbit/basic/math-07.jpg)

如果使用多個數學運算的積木，需要注意是*每個運算積木在計算上都會使用括號，類似的運算式有可能得到不同的結果*，例如下圖積木看起來都是 5 + 2 x 2，但因為括號位置的不同，得到的結果也不相同。

![數學](../images/zh-tw/docs/webbit/basic/math-08.jpg)

數學運算除了可以放入數字，也可以用於变量的相加，例如指定变量 a 為 5，变量 b 為 3，透過數學運算就能算出 a + b 等於 8。

![數學](../images/zh-tw/docs/webbit/basic/math-23.jpg)

## 取得餘數

「數學運算」積木可以取得兩個數字相除的餘數。

![數學](../images/zh-tw/docs/webbit/basic/math-09.jpg)

## 限制數字範圍

「限制數字範圍」積木可以將設定最大值與最小值，並將數字限制在這個指定的範圍內。

![數學](../images/zh-tw/docs/webbit/basic/math-12.jpg)

## 四捨五入

「四捨五入」積木可以對帶有浮點數的數字進行四捨五入、無條件捨去或無條件進位三種運算，同時亦可選擇捨去或進位到第幾位小數點。

![數學](../images/zh-tw/docs/webbit/basic/math-10.jpg)

將需要四捨五入的數字，放在四捨五入的積木後方，就可以得到四捨五入之後的結果。

![數學](../images/zh-tw/docs/webbit/basic/math-11.jpg)

## 尺度轉換

「尺度轉換」積木可以將某個尺度區間內的數值，轉換為另外一個區間尺度對應數值。

![數學](../images/zh-tw/docs/webbit/basic/math-13.jpg)

例如 0.5 為 0~1 尺度區間的數值，轉換為 0~100 尺度區間得到的結果就是 50。

![數學](../images/zh-tw/docs/webbit/basic/math-14.jpg)

尺度轉換積木可以幫助我們完成許多較為複雜的尺度轉換，例如 0.5 位於 -5~5 之間，轉換到 250~400 之間的數值就是 332.5。

![數學](../images/zh-tw/docs/webbit/basic/math-15.jpg)

尺度轉換積木常常會和四捨五入積木搭配使用，*建議將四捨五入積木放在尺度轉換積木前方*，因為尺度轉換後的數值有可能會帶有小數點，轉換後再四捨五入能得到較精確的答案。

![數學](../images/zh-tw/docs/webbit/basic/math-16.jpg)

## 陣列運算

「陣列運算」積木能針對以數字組成的陣列，進行加總、取出最小值、取出最大值、計算平均值、取得中位數、取得比較眾數、計算標準差和隨機抽取的計算。

![數學](../images/zh-tw/docs/webbit/basic/math-17.jpg)

在陣列運算後方接上陣列積木，就可以開始行取值或運算。

![數學](../images/zh-tw/docs/webbit/basic/math-18.jpg)

## 常用數學函數

「常用數學函數」提供常用的數學計算積木，常用數學函數包含以下幾種：開根號、絕對值、負數 (-)、對數函數 (ln)、log10 函數 (log10)、指数函数 (e^) 和 10 的幾次方 (10^)。

![數學](../images/zh-tw/docs/webbit/basic/math-19.jpg)

## 三角函數

「三角函數」積木裡頭提供了兩種三角函數用法，分別是角度 ( sin、cos、tan ) 以及徑度 ( asin、acos、atan )，三角函數可以從下拉選單選擇切換。

![數學](../images/zh-tw/docs/webbit/basic/math-20.jpg)

注意，因為 JavaScript 網頁語言特性，有些情況使用三角函數時，小數點後方會變成無限循環 9999，例如 sin(30) 應該等於 0.5，出來卻變成 0.49999...，當遇到這種情況，需使用四捨五入的方式才能呈現預期的結果。

![數學](../images/zh-tw/docs/webbit/basic/math-21.jpg)


## 常數

「常數」積木會表現是一個不會變動的常數數值，常數包含了以下幾種：圓周率 (π)、指數 (e)、黄金分割率 (φ)、sqrt(2)、sqrt(½) 和無限大 (∞)。

![數學](../images/zh-tw/docs/webbit/basic/math-22.jpg)

