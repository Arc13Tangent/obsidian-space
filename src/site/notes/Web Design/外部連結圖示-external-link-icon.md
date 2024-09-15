---
{"dg-publish":true,"permalink":"/Web Design/外部連結圖示-external-link-icon/","title":"外部連結圖示 Append icon to external link","noteIcon":"1","created":"2024-09-14T18:39:24.263+08:00","updated":"2024-09-15T13:50:26.958+08:00"}
---


> [!info]- 為什麼會有這個系列
> 自從使用Digital Garden來佈署個人網頁後，為了實作一些小小的酷東西來~~彰顯自己與模板仔的不同~~讓網頁更有自己的個性，不知不覺就學了一點CSS和網頁設計的code tracing，滿妙的XD
> 
> 然而由於自己完全沒有前端的知識，一開始想實作某個功能，就打開一樣使用DG佈署網頁的人的GitHub Repo，把每個元件的code一個一個複製到自己的code上面看看會發生什麼事，相當的暴力且耗時。所以想記錄一下一些~~小廢物~~小元件怎麼實作。
> 
> (雖然是這麼說，不過我的意思是我沒辦法手刻網頁。歸功於建北電資的學長姐，我至少還看得懂HTML等markup languages，所以可以猜出每一個block在做什麼)

這一次記錄的是如何在網頁中的外部連結後面加上一個小圖示。其實DG本來就有這個設定，但不知道為什麼壞掉了。電腦版上沒有顯示圖示就算了，用手機打開就直接顯示一個broken image在那邊，看得很阿雜。

下面是參考[CSS In Real Life](https://css-irl.info/styling-external-links-with-attribute-selectors)以及 Digital Garden 插件本身的SCSS 檔內容融合而成的最終設定：

scss
a[href^='http']::after {
content: '';
display: inline-block;
width: 1em;
height: 1em;
margin-left: 0em;
padding-left: 0em;
background-size: 70%;
background-image: url(/img/outgoing.svg);
background-repeat: no-repeat;
background-position: center bottom 10%;
}


事實上這組code不一定只能使用在其它網頁上，只要將line1中的`http`換成其它的字串，就可以為其它連結也加上圖示。例如我的閱讀筆記中含有Zotero的連結(zotero://)，就可以將line1的`http`換成`zotero`。
