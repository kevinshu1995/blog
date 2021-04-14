---
title: 消滅 Teachable 的 Sidebar 的時候到了 | Tampermonkey Userscript
categories: 程式筆記
tags:
  - Tampermonkey
  - 程式筆記
keyword:
  - Tampermonkey
  - Teachable
thumbnailImagePosition: left
thumbnailImage: cover_codingNote.svg
abbrlink: 2978793186
date: 2021-04-14 22:39:41
---

那個 Sidebar 甚麼的給我立刻消失 !!!

<!-- excerpt -->

近日又回到 Teachable 上面繼續上之前買的課程，這個平台的版面上的 Sidebar 真的很惱人，因為我習慣把瀏覽器縮小，此時的 Sidebar 跟影片就同時卡在同一個頁面上

![Teachable 原畫面展示](https://cf.jare.io/?u=https://kevinshu1995.github.io/blog/codingnotes/Tampermonkey-SideBarToggleButtonOnTeachable/teachableDemo.jpg)

> 直接氣爆 XD，還是...其實只有我覺得很煩??

![喔!氣氣氣氣氣!](https://media.giphy.com/media/LrXRnC08IEzZ8LfE7w/giphy.gif)


## Tampermonkey

剛好這幾天看到 [保哥](https://www.facebook.com/will.fans) 的粉專貼出了關於 Tampermonkey 的 [貼文](https://www.facebook.com/will.fans/posts/4492143630814746)，用來協助翻譯 Microsoft Doc 的小工具，於是我查了一下發現，好像可以拿來使用在 Teachable 上面。

腳本是用 Javascript 下去寫的，其實應該是可以理解成把腳本丟到到開發人員工具的 console 裡面執行，

不過這東西出很久了，我太菜了今天才知道，哈哈。

> TaDA !!!

![Teachable 新增按紐展示](https://cf.jare.io/?u=https://kevinshu1995.github.io/blog/codingnotes/Tampermonkey-SideBarToggleButtonOnTeachable/teachableDemo_2.jpg)

只要安裝好套件，打開課程影片之後，Tampermonkey 會開始跑腳本，腳本會在右上角新增一個按鈕，只要按下按鈕或是按下快捷鍵 `Ctrl-shift-Z` 就可以把 Sidebar 隱藏起來，在按一次按鈕或快捷鍵就可以復原，是不是超棒的 XDD

*對了我完全沒有在管相容性甚麼的，在我的chrome上面看起來沒問題，那就是沒問題XDD*

## 直接使用在 Teachable 吧!

1. 首先先安裝 [ Tampermonkey Chrome 擴充插建 ](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)

2. 點 [腳本連結](https://github.com/kevinshu1995/SideBarToggleButtonOnTeachable/raw/main/SideBarToggleButtonOnTeachable.user.js) 來安裝腳本


### 調整腳本啟用的網站

1. 目前只有在 courses.hexschool.com 上面才會跑這個腳本，如果有使用 Teachable 其他的課程，要調整 domain，可以打開 Tampermonkey 的主控台之後，會看到目前安裝的腳本，按下要調整的腳本最右側的編輯按鈕(如下圖)

![調整腳本 domain 步驟一](https://cf.jare.io/?u=https://kevinshu1995.github.io/blog/codingnotes/Tampermonkey-SideBarToggleButtonOnTeachable/step_1.jpg)

2. 再按下設定，接著新增 domain 就可以啦! (看是要 include 或是 match )

![調整腳本 domain 步驟一](https://cf.jare.io/?u=https://kevinshu1995.github.io/blog/codingnotes/Tampermonkey-SideBarToggleButtonOnTeachable/step_2.jpg)

附上程式碼

{% gist 9691a0206bc9222b73334b4f3c17b759 SideBarToggleButtonOnTeachable.user.js %}

### 最後

如果你也想寫自己的腳本，發布的時候記得要把檔案名稱取名為 `{你想取的名稱}.user.js`，這樣發佈到 gist (或其他地方)，當打開 Raw 檔時，插件會自己判斷並打開安裝畫面，這樣子別人使用會比較簡單~

當然網路上有蠻多人有寫腳本，要多注意安全性的問題，安裝前要看一下 source code ~ 確保安全


> 參考資源
> [Tampermonkey 載入 jQuery 的簡便方法](https://blog.darkthread.net/blog/greasemonkey-load-jquery)
> [Tampermonkey](https://www.tampermonkey.net/)
> [Tampermonkey documentation](https://www.tampermonkey.net/documentation.php)
> [IT鐵人賽小工具 : Ctrl + V 自動上傳圖片功能](https://ithelp.ithome.com.tw/articles/10211943)
> [保哥的 MSDocsLanguageToggleSwitcher](https://github.com/doggy8088/MSDocsLanguageToggleSwitcher)


## 最後附上連結，如下

- 腳本連結
    - [Github Repository](https://github.com/kevinshu1995/SideBarToggleButtonOnTeachable)
- 個人連結
    - [Github @kevinHWS](https://github.com/kevinshu1995)
    - [JS 地下城網站首頁](https://kevinshu1995.github.io/hex_jsDungeon/)
        - 歡迎來看看JS作品

<br>

_本文章若有任何資訊誤植或侵權，煩請告知，我會立刻處理。_