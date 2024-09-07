---
{"dg-publish":true,"permalink":"/Plugins/ZotLit/","title":"ZotLit","tags":["Zotero","Obsidian"],"noteIcon":"1","created":"2024-09-07T18:16:11.247+08:00","updated":"2024-09-07T19:43:33.139+08:00"}
---

# ZotZit: Obsidian 與 Zotero 的完美結合

Author: Aiden Liu ([aidenlx](https://github.com/aidenlx))
GitHub repository: https://github.com/PKM-er/obsidian-zotlit 
Best for: 
	在Zotero進行資料收集與標註後，想在Obsidian製作文獻筆記的人 
	For those who like to collect references, annotate PDFs in Zotero, and want to make literature notes in Obsidian.

---

# Introduction

如果是喜歡用Zotero來收集資料並標註，又希望可以利用自己的標註在Obsidian製作文獻筆記的人，一定要試試看這個整合插件。
當所有東西設定好的時候，會有一種這兩個軟體應該是同一個軟體的錯覺，因為一切都同步得太順了！

這邊有官方教學: [Introduction – ZotLit (aidenlx.top)](https://zotlit.aidenlx.top/)  
另一個介紹得很好的網頁: [PKMer_ZotLit：文献引用的流畅体验](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E4%BD%BF%E7%94%A8%E6%8A%80%E5%B7%A7/zotero-obsidian/zotlit%E5%B8%A6%E6%9D%A5%E7%9A%84%E6%96%87%E7%8C%AE%E5%BC%95%E7%94%A8%E6%B5%81%E7%95%85%E4%BD%93%E9%AA%8C/) 

## Features

1. <u>快捷引用</u>：在任一筆記中按下`[@`即會跳出Zotero中的文獻列表，點一下就可以引用。配合插件Pandoc Reference List可以自動將引用的文獻渲染為特定格式，如APA等。
2. <u>導出文獻筆記</u>：在Zotero中對文獻右鍵選擇`Create Literature Note(s)`後，就可以根據設定的模板自動導出含有文獻資訊的md檔，同時右測會同步在Zotero中的annotations。
3. <u>筆記中使用annotations</u>：在Obsidian右側面板可以選擺要跟隨的文獻，選定後即可看到該文獻的annotations，還可以拖進筆記裡面！
4. <u>與文獻連結</u>：如果沒有在模板中刪掉的話，筆記會自動附上「Zotero item」和「PDF」的連結，點一下就可以自動在Zotero中開啟對應檔案。Annotations也有連結可以自動顯示在Zotero中文獻的位置。

## Pros

1. 自動根據模板建立筆記
2. 模板設定很自由，可以控制幾乎所有的參數
3. 有設計一個模板編輯器，可以即時確認模板的輸出內容
4. 同步速度很快，幾乎是即時的
5. 製作筆記過程中使用annatations的方式很直覺

## Cons

1. 可能一開始會不知道要怎麼設定模板，因為真的太多東西可以調了

## Showcases

匯出文獻筆記：
![Imgur](https://imgur.com/B5xa9o2.jpeg)

文獻的matadata和連結也可以自動導出：
![Imgur](https://imgur.com/K2bf05r,jpeg)

同步annotations：
![Imgur](https://imgur.com/Ne9DUNa.jpeg)

---

# References

1. _PKM-er/obsidian-zotlit_. (2024). [TypeScript]. Pkmer. [https://github.com/PKM-er/obsidian-zotlit](https://github.com/PKM-er/obsidian-zotlit) (Original work published 2022)

2. _Introduction – ZotLit_. (2023, September 19). [https://zotlit.aidenlx.top/](https://zotlit.aidenlx.top/)

3. _PKMer_ZotLit：文献引用的流畅体验_. (n.d.). Retrieved September 7, 2024, from [https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E4%BD%BF%E7%94%A8%E6%8A%80%E5%B7%A7/zotero-obsidian/zotlit%E5%B8%A6%E6%9D%A5%E7%9A%84%E6%96%87%E7%8C%AE%E5%BC%95%E7%94%A8%E6%B5%81%E7%95%85%E4%BD%93%E9%AA%8C/](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E4%BD%BF%E7%94%A8%E6%8A%80%E5%B7%A7/zotero-obsidian/zotlit%E5%B8%A6%E6%9D%A5%E7%9A%84%E6%96%87%E7%8C%AE%E5%BC%95%E7%94%A8%E6%B5%81%E7%95%85%E4%BD%93%E9%AA%8C/)