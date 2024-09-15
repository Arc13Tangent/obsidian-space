---
{"dg-publish":true,"permalink":"/Web Design/外部連結圖示-external-link-icon/","title":"Append icons to external links 外部連結圖示","noteIcon":"1","created":"2024-09-14T18:39:24.263+08:00","updated":"2024-09-16T00:54:31.580+08:00"}
---


> [!info]- Why I Created This Series 為什麼會有這個系列
> After deploying my personal digital garden by the Obsidian Digital Garden plugin, I wanted to put some cool little things on it to make it stand out and feel more "me" instead of just following a template. Along the way, I picked up some CSS and learned a bit about web design and code tracing – it’s been a fun journey!
> 
> Since I had zero front-end experience, my initial approach was pretty chaotic. I'd open up other people's GitHub Repos (also using DG), copy-paste their code piece by piece into mine, and see what happens – not the most efficient, but definitely an adventure! So I decided to document how I built some small, fun components here.
> 
> <font color="#7f7f7f">(Just to be clear, I can’t hand-code a website from scratch, but thanks to the seniors and friends from CKEFGISC, I can at least understand markup languages like HTML and figure out what each block is supposed to do.)</font>
> 
> 自從使用Digital Garden來佈署個人網頁後，為了實作一些小小的酷東西來~~彰顯自己與模板仔的不同~~讓網頁更有自己的個性，不知不覺就學了一點CSS和網頁設計的code tracing，滿妙的XD
> 
> 然而由於自己完全沒有前端的知識，一開始想實作某個功能，就打開一樣使用DG佈署網頁的人的GitHub Repo，把每個元件的code一個一個複製到自己的code上面看看會發生什麼事，相當的暴力且耗時。所以想記錄一下一些~~小廢物~~小元件怎麼實作。
> 
> <font color="#7f7f7f">(雖然是這麼說，不過我的意思是我沒辦法手刻網頁。歸功於建北電資的學長姐和損友朋友們，我至少還看得懂HTML等markup languages，所以可以猜出每一個block在做什麼)</font>

Today I’m trying to add a small icon next to external links on a webpage.
DG originally had this feature, but for some reason, it stopped working. 
While the icon doesn’t show up at all on desktop, it’s even worse on mobile – it displays a broken image with a frustrating question mark in the center, which is super annoying!

The following code snippet is a combination of the example from [CSS In Real Life](https://css-irl.info/styling-external-links-with-attribute-selectors) and the SCSS file from the Digital Garden plugin.

這一次記錄的是如何在網頁中的外部連結後面加上一個小圖示。
其實DG本來就有這個設定，但不知道為什麼壞掉了。
電腦版上沒有顯示圖示就算了，用手機打開就直接顯示一個broken image在那邊，看得很阿雜。

下面是參考[CSS In Real Life](https://css-irl.info/styling-external-links-with-attribute-selectors)以及 Digital Garden 插件本身的SCSS 檔內容融合而成的最終設定：

```scss
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
```

In fact, with a slight modification, the above snippet can be used for other types of links, not just `http`. 
For example, in my literature notes, I have Zotero links (zotero://). By replacing `http` with `zotero` in line 1, an icon will also appear after Zotero links.

事實上這組code不一定只能使用在其它網頁上，只要將line1中的`http`換成其它的字串，就可以為其它連結也加上圖示。
例如我的閱讀筆記中含有Zotero的連結(zotero://)，就可以將line1的`http`換成`zotero`。

---

By the way, I really want beautiful code blocks in my garden! Hopefully, one day I'll find a way to publish the code block styles from my local vault.

<center>
<img width=500 src="https://imgur.com/ZFElAHT.jpeg">
</center>
<center>
The code block style in my local vault, which is created using the Code Styler plugin.
</center>
