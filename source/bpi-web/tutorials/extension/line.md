# LINE 聊天操控

編輯器預設 LINE 即時通訊相關功能，除了支援 LINE Notify 的推播，更可以接收 LINE 的聊天訊息，透過聊天的方式操控 開發板或和小怪獸進行互動。

## LINE 聊天操控積木清單

LINE 聊天操控的積木包含發送推播專用的 LINE Notify 積木、聊天專用 LINE Chat 積木，以及接收訊息、回傳訊息、表情符號三種積木。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-01.jpg)

## LINE Notify

LINE Notify 是 LINE 所提供的一項非常方便的推播服務，每個人的 LINE 帳號都可以使用，使用之前，必須先前往 LINE Notify 的網站 ( [https://notify-bot.line.me/zh_TW/](https://notify-bot.line.me/zh_TW/#_blank) )，使用自己的 LINE 帳號登入，申請 LINE Notify 權杖。

> 更多詳細資訊可參考：[自建 LINE Notify 訊息通知](https://www.oxxostudio.tw/articles/201806/line-notify.html#_blank)

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-02.jpg)

登入後，滑鼠移至上方個人帳號，選擇「個人頁面」。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-03.jpg)

在個人頁面可以發行「權杖」，權杖的作用在於讓「連動的服務」可以透過 LINE Notify 發送訊息通知，發行後的權杖與其名稱會出現在上方的清單中，如果之前有申請過像是 IFTTT 的連動通知，就會發現上方出現 IFTTT 的服務。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-04.jpg)

點選「發行權杖」，指定權杖名稱 ( 傳送通知訊息時所顯示的名稱 )，以及選擇是要一對一接收，或是讓群組也可以接收通知。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-05.jpg)

點選「發行」，會出現一段權杖代碼，由於這段代碼「**只會出現一次**」，請先複製這段代碼，找個筆記本或文件儲存這段代碼，就可以點選下方按鈕「關閉」。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-06.jpg)

完成後在連動的服務裡，就會出現了自訂的服務。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-07.jpg)

同時，LINE 訊息裡也會收到 LINE Notify 發出「已發行個人存取權杖」的訊息，到這一步 LINE Notify 已經設定完成，已經可以開始從 發送訊息。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-08.jpg)

回到 編輯器，使用 LINE Notify 積木，在 Token 的位置填入剛剛產生的權杖代碼，在發送訊息的位置填入欲發送的訊息，執行後，自己的 LINE 就會收到 LINE Notify 的訊息。

> 「LINE Notify」積木屬於「*發送訊息後才會繼續執行後方程序*」的類型 ( 點擊前方問號小圖示會提示 )，當編輯畫面中有這塊積木，*執行時當程序遇到這塊積木會暫停，直到發送訊息後後才會再繼續*。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-10.jpg)

搭配 開發板，也可以做到按下 A 開關就發送 A，按下開關 B 就發送 B 的效果。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-11.jpg)

如果要發送圖片，只要填入圖片網址即可發送，搭配 開發板，也可以做到按下 A 開關就發送一張皮卡丘的圖片。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-13.jpg)

如果要傳送表情貼圖，可使用「表情貼圖」積木，表情貼圖有三種 ( 初次安裝 LINE 時預設的三種 )，每種貼圖分成表情代號 ( STKID ) 和 表情主題 ( STKPKGID )，可以透過 [表情清單](https://devdocs.line.me/files/sticker_list.pdf#_blank)查詢對應的號碼，輸入指定的號碼，執行後就可以發送表情貼圖，舉例來說，搭配 開發板，按下 A 開關就發送生氣圖案，按下 B 開關就發送開心圖案。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-12.jpg)

## LINE Chat 聊天操控

「LINE Chat」積木能讓我們透過「聊天」的方式，接收從 LINE 發送過來的訊息，透過訊息和 編輯器或 開發板互動。

> LINE Chat 積木是屬於「一來一往」的積木，，接收一則訊息才能回應一則訊息，無法像 LINE Notify 積木可以主動發送訊息，或接收一則訊息而回傳多則訊息。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-14.jpg)

要使用 LINE Chat 功能，必須先加入 Webduino Bot 為 LINE 的好友，*使用 LINE 掃描下方 QRCode 加入好友*。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-15.jpg)

加入好友後，會收到一則歡迎訊息，歡迎訊息包含了三個提示：

> - 輸入「id」兩個英文字母，取得頻道名稱 ( 不是你的 id )。
> - 輸入「newid」產生新的頻道名稱。
> - 輸入「id:名稱」自訂頻道名稱 ( 可能會重複 )。

按照指示，輸入 i 和 d 兩個英文字母，就會收到系統配發的聊天頻道名稱，如果是系統配發的頻道名稱，每個人的聊天頻道都不相同，如果是自訂頻道名稱，則可能會和別人的名稱重複，也就可能會收到別人的訊息。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-16.jpg)

在 編輯畫面放入 LINE Chat 的積木，接收到訊息時讓小怪獸說出 LINE 的訊息，執行後，就可用 LINE 傳送訊息給 Webduino Bot，訊息收到的當下，小怪獸就會說出訊息。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-17.jpg)

如果要回傳訊息，只需要放入回傳訊息的積木，寫入回傳的內容 ( 支援文字、表情貼圖和圖片，使用方式請參考上方 LINE Notify 教學 )，執行後，就會在收到訊息後回傳對應的訊息，下圖的範例會在收到訊息後，回傳一模一樣的訊息。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-18.jpg)

除了單純的接收訊息，也可以使用 LINE Chat 來控制 開發板，透過邏輯判斷，就能收到「開燈」的文字就點亮 LED，收到「紅色」的指令就發出紅光，實現真正物聯網的應用情境。

![LINE 聊天操控](../images/zh-tw/docs/webbit/extension/line-19.jpg)


