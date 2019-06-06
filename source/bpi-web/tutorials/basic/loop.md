# 重複

在程序領域裡，重複 ( 迴圈 ) 是常常使用的基本功能，重複顧名思義就是重複執行的過程，也可以將需要重複執行的程序碼放在迴圈內，就能指定次數、延遲時間，或是無窮盡的執行。

## 重複積木清單

重複的積木分別有一個「等待」的積木，五種不同重複模式的積木和一個「停止重複」的積木。

![重複](../images/zh-tw/docs/webbit/basic/loop-01.jpg)

## 等待

「等待」積木可以讓我們讓程序暫停一段指定的時間，當程序積木裡遇到等待積木，就會等待指定的時間之後才會進行接續的動作。

![重複](../images/zh-tw/docs/webbit/basic/loop-23.jpg)

以下方的例子來說，如果不加上等待，四隻小怪獸會同時說出 hello，如果加上等待 1 秒，四隻小怪獸就會以每隔一秒的時間依序說出 hello。

> 注意，上述所謂的「同時」，是針對人類肉眼來說的意思，對於程序而言仍然是按照順序進行，只是間隔時間非常短，短到人類的肉眼分辨不出來

沒有加上等待積木

![重複](../images/zh-tw/docs/webbit/basic/loop-02.jpg)

有加上等待積木

![重複](../images/zh-tw/docs/webbit/basic/loop-03.gif)

## 重複執行幾次

「重複執行幾次」積木，可以指定迴圈內的積木程序重複的次數，預設次數為 10 次。

![重複](../images/zh-tw/docs/webbit/basic/loop-06.jpg)

透過重複十次，可以讓小怪獸旋轉 100 度。

![重複](../images/zh-tw/docs/webbit/basic/loop-04.jpg)

延續前面介紹過的等待，如果在重複裡頭不加入等待，就會看見怪獸瞬間旋轉了 100 度，如果我們在加上等待 0.5 秒的積木，就會看到怪獸每隔 0.5 秒旋轉 10 度，旋轉十次。

![重複](../images/zh-tw/docs/webbit/basic/loop-05.gif)

## 計數

「計數」積木有點類似「重複執行幾次」積木的進階版，差別在於計數積木使用了一個变量，透過改變這個变量的數值，來決定重複幾次、如何重複以及重複的間隔。

> 因為內含一個变量，所以當編輯畫面裡有計數的積木，在变量的目錄下也會出現一個對應的变量。

![重複](../images/zh-tw/docs/webbit/basic/loop-07.jpg)

使用「計數積木搭配等待」，可以讓綠色小怪獸每隔 0.5 秒講出变量 i 的數值，這個变量 i 會*根據我們指定的起始數值、最終數值和間隔作數值進行遞增或遞減*，以下圖的例子而言，变量 i 會每隔 1 進行加總，直到變成 10 為止 ( 也就會依序念出 1234...10 )。

> 注意，*如果要「依序」唸出數字，一定要加上等待的積木*，不然就會呈現最後的數字。

![重複](../images/zh-tw/docs/webbit/basic/loop-08.gif)

## 重複無限次

「重複無限次」積木會無止盡的一直執行迴圈內容，除非使用「停止重複」，重複的事件才會停止。

![重複](../images/zh-tw/docs/webbit/basic/loop-09.jpg)

延續前面介紹過的等待，在重複無限次的積木內加入「等待」，搭配小怪獸的旋轉，就可以讓小怪獸不斷地旋轉。

![重複](../images/zh-tw/docs/webbit/basic/loop-10.gif)

## 判斷為真，就重複無限次

「判斷為真，就重複無限次」積木等同於「重複無限次」積木加上「邏輯」判斷，*只要空格內的邏輯判斷為「真」( true )，就會開始進行無限重複*。

![重複](../images/zh-tw/docs/webbit/basic/loop-11.jpg)

舉例來說，我們可以先設定一個变量 a 為 2 到 9 之間的數字，透過判斷如果 a 是偶數，就讓小怪獸開始旋轉，否則就不旋轉。

![重複](../images/zh-tw/docs/webbit/basic/loop-12.gif)

上面的例子也可以使用「邏輯」搭配「重複無限次」來實現同樣的效果。

![重複](../images/zh-tw/docs/webbit/basic/loop-13.jpg)

## 取出陣列元素並執行

有別於上述的重複方式，「取出陣列元素並執行」積木是以陣列長度作為重複次數的依據，因此空格內必須放入陣列積木，網頁執行後就會依序取出陣列內容並執行對應動作。

![重複](../images/zh-tw/docs/webbit/basic/loop-14.jpg)

我們可以設定变量 a 為一個陣列，裡頭放入五種水果名稱，接著設定一個变量 i，依序讓变量 i 等於水果名稱，再讓小怪獸講出水果名稱並進行旋轉的動作。

![重複](../images/zh-tw/docs/webbit/basic/loop-15.gif)

## 背景執行

「背景執行」是所有重複積木裡頭的功能選項，由於程序碼的執行順序緣故，「**前一段程序尚未完成前，無法執行下一段程序**」，也因此*大多數的情況在畫面上只能同時執行一個重複迴圈*，然而背景執行**可以讓重複的動作進入背景執行，就能同時使用多個重複迴圈**。

![重複](../images/zh-tw/docs/webbit/basic/loop-17.jpg)

舉例來說，如果我們使用兩個「重複十次」的積木，都*不勾選背景執行*，第一個放入小怪獸旋轉，第二個放入小怪獸移動，網頁執行後，就會看到小怪獸*先旋轉再移動*。

![重複](../images/zh-tw/docs/webbit/basic/loop-18.gif)

如果我們把上面的例子中的重複，*都勾選背景執行*，網頁執行後就會發現小怪獸*一邊移動一邊旋轉*。

![重複](../images/zh-tw/docs/webbit/basic/loop-19.gif)

是否有背景執行，在「重複無限次」的情況下會更容易發現差異，**如果畫面中有兩個重複無限次的迴圈，如果沒有勾選背景執行，因為行為還停留在前一個重複無限次，在後面的重複無限次就不會執行**。

![重複](../images/zh-tw/docs/webbit/basic/loop-20.gif)

## 停止重複

上述所有的重複行為，都可以透過「停止重複」積木來停止，停止重複又分成「*停止畫面上所有重複*」，或「*放在重複迴圈內，停止所在位置的重複*」。

![重複](../images/zh-tw/docs/webbit/basic/loop-16.jpg)

例如在「重複無限次」積木裡加入「小怪獸旋轉角度大於 90 度就*停止這個重複*」的判斷，就會在小怪獸角度大於 90 度時停止重複，繼續執行下方的講話程序。

![重複](../images/zh-tw/docs/webbit/basic/loop-21.gif)


如果有多個重複，也可以使用「停止所有重複」來停止，例如下方的程序，當小怪獸旋轉角度大於 90 度，就會停止所有重複。( 此處勾選了背景執行，請參閱「[背景執行](loop.html#loop07)」章節 )

![重複](../images/zh-tw/docs/webbit/basic/loop-22.gif)



