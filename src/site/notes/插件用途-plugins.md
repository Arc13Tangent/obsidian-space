---
{"dg-publish":true,"permalink":"/插件用途-plugins/","tags":["Obsidian"],"created":"2024-09-02T10:15:36.000+08:00","updated":"2024-09-04T23:12:54.740+08:00"}
---

# 插件用途

Obsidian的靈魂應該就是上千個自由安裝的open source的插件了
好像沒有什麼功能是一個插件無法解決的 ~~如果有 就裝兩個~~
開啟方式：Preference(或按`cammand/ctrl` + `,`) $\to$  Community Plugins
把Restricted mode關掉就可以載插件


這個列表也是記錄一下各個插件是做什麼的，有時自己裝一裝也忘記這個到底還用不用得到

## 插件列表
只列出自己有裝的，***這樣***代表非常非常推薦裝，**這樣**代表很推薦裝

1. Attachment Management: 把文件的附件整理好。喜歡在檔案裡面放圖片，或是用[[插件用途-plugins#^1dfb2a\|ZotLit]]把註記抓到檔案裡面時，有這個就很方便查看到底有哪些圖片
2. Better Search View: 在搜尋時可以顯示詳細內容，更精確判斷是要開哪個檔案
3. Better Word Count: 就是下面多了一個算反白的範圍有幾個字XD
4. BRAT: 裝beta版插件
{ #009081}

    - jupyter: 其實應該是沒什麼用obsidian開ipynb的理由，但覺得很酷就裝了
5. **Calendar**:  寫日記用。表面上是這樣，但因為很多和時間相關的插件也仰賴日記系統，所以莫名變得很重要XDD
   (比如[[插件用途-plugins#^5a5fff\|Day Planner]]或是其它time sensitive的功能，例如時間到就提醒要做什麼tasks之類的)
6. **Callout Manager**: 設定callout用，例如文獻筆記中，可以自訂一個叫做yellow的callout(同時[[插件用途-plugins#^1dfb2a\|ZotLit]]也設定好格式後)，把註記拉到文件裡面就真的會變黃色的，舒服。
7. **Commander**: 可以在一些地方新增或隱藏按鈕，尤其是裝了插件後一定會有不想看到的東西想隱藏
   例如最左邊的Ribbon區，我設定從上到下是[[插件用途-plugins#^2f66c3\|Project]], Google Calendar([[插件用途-plugins#^e23c88\|Custom Frame]]), Overleaf([[插件用途-plugins#^e23c88\|Custom Frame]]), ChatGPT([[插件用途-plugins#^e23c88\|Custom Frame]]), [[插件用途-plugins#^009081\|Jupyter]]：
   ![Imgur](https://imgur.com/tAJMQkI.jpeg)
   如果沒有這個插件，這邊會被一堆東西塞爆XD
8. **Custom Frame**: 如果有什麼網頁想用ob開就是這個了，好用，工作流不會斷掉，我弄了：
{ #e23c88}

	- Overleaf 
	  ![Imgur](https://imgur.com/1giNqWZ.jpeg)
	  
	- Google Calendar 
	  ![Imgur](https://imgur.com/mex8v9Q.jpeg)
	  
	- ChatGPT 
	  ![Imgur](https://imgur.com/eaozwiD.jpeg)
	  
9. Contribution Graph: 我是拿來記錄習慣的，雖然本來好像不是這樣用的。然後有別的替代品，只是這個比較符合我的審美。
10. **Day Planner**: 可以開時間軸出來排行程，在上面登錄的行程會自動在當天日記新增tasks。反過來，日記上面的tasks也會出現在上面，如果寫tasks時沒有指定時間，還可以在時間軸的地方把它抓下來擺到想要的時間位置上。然後更神的是他還可以和其它日曆同步，例如我就同步了google calendar。老師的meeting通知、學校行事曆、筆記上的tasks全都可以整合在一起。而且目前沒有發生沒更新到的情況，幾乎是改完過3秒內就更新了。
    可以設定時間到就跳提醒，可惜的是沒辦法設個開始前幾分鐘提醒之類的。
    圖中的紅色事項就是我設定Google Calendar上的「重要事項」為這個顏色，它就會同步顯示過來，搭配[[插件用途-plugins#^e23c88\|Custom Frame]]做一個Google Calendar就可以實現在ob上和網路日曆交互：
    ![Imgur](https://imgur.com/JMLh74p.jpeg)
    唯一的小缺點是如果有設定「自動捲動到現在時間」，電腦版很正常，但手機版操作就有點87，然後沒辦法直接在那邊改網路日曆的東西。
    如果想要用一個插件就做到和Google Calendar交互，建議裝名字就叫做Google Calendar的那個插件(但我覺得Day Planner的時間軸好看太多，所以就這樣了XD)
{ #5a5fff}

11. ***Dataview***: 神器，本身就很好用，然後一堆插件也沒他不行，就算不想打指令也要裝。透過設定條件自動收集指定資料，我拿來用在某個文件裡面顯示所有筆記中未完成的tasks。好像還有人用這個做了一個圖書館…。下面是一個例子，還可以設定哪些資料夾的tasks不要看，這邊是不要包含"Markdown"資料夾：
    ![Imgur](https://imgur.com/qzgRlY2.jpeg)
    
12. Excel to Markdown Table: 幫我們自動把從excel或google sheet上複製的東西貼過來變成markdown表格。有點猛，但其實沒怎麼在用，不太常開excel之類的
13. Execute Code: 讓code blocks可以執行，不太確定同一個檔案有沒有共用環境
14. Extended MathJax: 其實ob不是用$LaTeX$而是mathjax，有一些東西沒有，所以網路上有人說裝這個基本上就不會缺東西了。目前除了enumerate等列點的東西出不來，好像也沒看過缺什麼(更別說要列點就直接用markdown就好了還比較快)
15. File Color: 可以幫folders和files設定顏色方便馬上locate
16. File Hider: 把不想看到的資料夾隱藏
17. **Floating search**: 讓內文搜尋可以自己跳出一個視窗，不然預設只能在左上角很小一個到底要看什麼…
18. **Front Matter Title**: 讓顯示的名字和檔名可以不一樣。對於有檔名命名潔癖的人來說不可或缺
19. Git: 其中一個功能是每N分鐘自動備份到GitHub上，多一個保障這樣。當然對版本控制狂來說很爽但我還好。然後因為手機沒有git所以也一直跳錯誤訊息，很87。
20. ***Hover Editor***: 神器+1。有了他可以快速看一個被連結的文件，還可以直接拉出來放旁邊當小小的memo。跨文件編輯有了它變得非常方便。按著`command/ctrl` 然後滑鼠移到想看的檔案或連結上就可以了。
    ![Imgur](https://imgur.com/M6ugzZy.jpeg)
20. ***LaTeX Suite***: 神器再+1，數學系狂喜。我真的不想在overleaf上寫文件了，以後都在ob寫好再貼上去。如同插件一開始就講的一句話：
    
<center>make typesetting LaTeX math as fast as handwriting</center>
<center>它真的做到了</center>

21. **Natural Language Dates**: 可以打today就跳今天日期之類的，之前還試過7days after today之類的，也行，有點神。不過我不知道到底哪些它看得懂哪些看不懂XD
22. Obsidian Columns: 可以把一些元件並排。我也只有在記錄習慣那個文件用到就是了。
23. **Pandoc Reference List**: 就算不跟其它插件搭配也很不錯，可以按一下就複製文獻列表，按指定的格式貼上。引用文獻狂人大喜。
24. Periodic Notes: 寫週記月記之類用的，好像有插件會用到，但我忘了
25. ***Projects***: 神器++，除了不能協作外，根本把trello搬進來了!!!一開始很喜歡trello用了一段時間，想說可以管控自己的專案。然而實際情況是，平常app那麼多誰會記得去開一個純粹管專案的app…久了就直接廢掉了。現在整合就算了，還多了更多功能，例如我除了用他管理專案任務和待辦，還可以用他整理出文獻列表、上課筆記。我想這是因為每一個事件都會是一個md檔所以可操作空間極大
	![Imgur](https://imgur.com/VD45IAH.jpeg)
	Board view，就很像Trello
	
	![Imgur](https://imgur.com/Brq7LCV.jpeg)
	Table view
{ #2f66c3}

26. Pseudocode: 一個專門渲染虛擬程式碼或類似algo的東西
27. **Style Setting**: 很多themes和插件都會用到它，有了它就能自定一堆外觀相關的東西，心情好很多。至少我不想看預設主題寫筆記啊…一點fu都沒有，還長得很像什麼主題都沒有的vscode。
>[!attention]- Spoilor
>其實ob和vs兩個都是基於網頁技術Electron做出來的東西，這也是為什麼不管用電腦開手機開平板開看起來都非常nice的原因)
    
28. Tag Wrangler: 編輯tag用
29. **Templater**: 這個神奇東西可以在md檔上執行js和一些程式碼，做到自動化某些事情。雖然因為我不會語法，所以都是抓別人的拿來改，暫時感受不到他多神，不過沒他一些自動化插件也不能運行，所以就算不會用還是得裝XD
30. VSCode Editor: 讓我們可以在ob裡面打開文字檔，主題只有深淺色有點可惜
31. ***ZotLit***: 究極神器。沒有它我都不想唸論文了🥹老實說我一開始還覺得他的設定好煩好奇怪怎麼都不會動，後來終於摸熟了之後把一切都設定好後，boom。
    沒有這些自動同步註記和連結pdf的功能到底要怎麼整理文獻QQQQQ
    是它讓我決定把ob改造成全能工作軟體的。
    唯一的缺點就是一開始真的看不懂怎麼設定模板，會搞很久，但絕對值得
    ![Imgur](https://imgur.com/ETDB7n6.jpeg)
    實在是沒想到居然可以在一個免費軟體裡面做到像是專門設計成文獻回顧的app的體驗
    
{ #1dfb2a}
