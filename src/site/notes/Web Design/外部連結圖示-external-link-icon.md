---
{"dg-publish":true,"permalink":"/Web Design/外部連結圖示-external-link-icon/","title":"Append icons to external links 外部連結圖示","noteIcon":"1","created":"2024-09-14T18:39:24.263+08:00","updated":"2024-09-16T03:20:43.888+08:00"}
---


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
<font size=2>
The code block style in my local vault, which is created using the <a href="https://github.com/mayurankv/Obsidian-Code-Styler">Code Styler plugin</a>  includes a colorful language icon and a copy code button.
</font>
</center>

---
# References

1. _CSS { In Real Life } | Styling External Links with Attribute Selectors_. (2023, October 11). CSS { In Real Life } | Styling External Links with Attribute Selectors. [https://css-irl.info/styling-external-links-with-attribute-selectors/](https://css-irl.info/styling-external-links-with-attribute-selectors/)

2. Visakan, M. (2024). _mayurankv/Obsidian-Code-Styler_ [JavaScript]. [https://github.com/mayurankv/Obsidian-Code-Styler](https://github.com/mayurankv/Obsidian-Code-Styler) (Original work published 2023)

3. _background-position - CSS: Cascading Style Sheets | MDN_. (2024, February 26). [https://developer.mozilla.org/en-US/docs/Web/CSS/background-position](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position)
