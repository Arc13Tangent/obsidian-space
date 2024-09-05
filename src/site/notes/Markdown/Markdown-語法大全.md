---
{"dg-publish":true,"permalink":"/Markdown/Markdown-語法大全/","title":"Markdown 語法大全","created":"2024-08-24T23:00:12.607+08:00","updated":"2024-09-05T03:28:30.572+08:00"}
---

- [[Markdown/Markdown-語法大全#副標\|副標]]
- [[Markdown/Markdown-語法大全#字體大小\|字體大小]]
- [[Markdown/Markdown-語法大全#字體效果\|字體效果]]
- [[Markdown/Markdown-語法大全#引文\|引文]]
- [[Markdown/Markdown-語法大全#標號\|標號]]
- [[Markdown/Markdown-語法大全#縮排+換行\|縮排+換行]]
- [[Markdown/Markdown-語法大全#巢狀標號\|巢狀標號]]
- [[Markdown/Markdown-語法大全#定義清單\|定義清單]]
- [[Markdown/Markdown-語法大全#連結\|連結]]
- [[Markdown/Markdown-語法大全#簡易超連結\|簡易超連結]]
- [[Markdown/Markdown-語法大全#分隔線\|分隔線]]
- [[Markdown/Markdown-語法大全#程式碼\|程式碼]]
- [[Markdown/Markdown-語法大全#標籤連結\|標籤連結]]
- [[Markdown/Markdown-語法大全#圖片\|圖片]]
- [[Markdown/Markdown-語法大全#圖片連結\|圖片連結]]
- [[Markdown/Markdown-語法大全#表格\|表格]]
- [[Markdown/Markdown-語法大全#短區塊\|短區塊]]
- [[Markdown/Markdown-語法大全#CheckBox\|CheckBox]]
- [[Markdown/Markdown-語法大全#跳脫字元\|跳脫字元]]

@copyright MRcoding筆記

---

主標題
===
>標題的語法

```
標題
===
```

---

副標
---
>副標的語法

```
副標
---
```

---

字體大小
---
>字體大小的示範
># H1
>## H2
>### H3
>#### H4
>##### H5


```
# H1
## H2
### H3
#### H4
##### H5
```

---

字體效果
---
*斜體字*
**粗體字**
***斜粗體***
~~刪除線~~
_斜體2_
__斜粗2__
正常^上標^
正常~下標~
++底線++
==螢光標記==

```
*斜體字*
**粗體字**
***斜體兼粗體***
~~刪除線~~
_斜體2_
__斜粗2__
正常^上標^
正常~下標~
++底線++
==螢光標記==
```

---

引文
---
>縮排語法
>第一層
>>第二層
>>>第三層

```
>縮排語法
>第一層
>>第二層
>>>第三層
```

---

標號
---
1. 數字標號
2. 數字標號
3. 數字標號
- 其他標號
+ 其他標號
* 其他標號

```
1. 數字標號
2. 數字標號
3. 數字標號
- 其他標號
+ 其他標號
* 其他標號
```

---

縮排+換行
---

    
    縮排
換行  

```MD
[Tab]縮排
行末按兩個空格  産生斷行 (．↲)。
```

---

巢狀標號
---

- 無序清單
- 無序清單
    - 無序清單子清單
        - 無序清單子子清單

1. 有序清單
2. 有序清單
    1. 有序清單子清單
        1. 有序清單子子清單

```MD
- 無序清單
- 無序清單
    - 無序清單子清單
        - 無序清單子子清單

1. 有序清單
2. 有序清單
    1. 有序清單子清單
        1. 有序清單子子清單
```

---

定義清單
---

名詞1
: 解釋1

名字2
: 解釋2

名詞 3
~ 定義 3
~ 定義 3

```
名詞1
: 解釋1

名字2
: 解釋2

名詞 3
~ 定義 3
~ 定義 3
```

連結
---
>[連結名稱](https://google.com "游標顯示")

```
[連結名稱](https://google.com "游標顯示")
```

---

簡易超連結
---
><https://google.com>
><text@email.com>

```md
<網址或mail>
```

---

分隔線
---
1.

---
2.
***
3.
- - -
4.
* * *

```
1.
空行
---
2.
***
3.
- - -
4.
* * *
---
```

程式碼
---
```cpp
#include <stdio.h>

int main(){

    printf("Hello World");

    return 0;
}
```
```cpp=
#include <stdio.h>

int main(){

    printf("Hello World");

    return 0;
}
```


\```程式類型
程式碼
\```

\```程式類型=
行號+程式碼
\```

---

標籤連結
---
[Google][1]
[Yahoo][2]
[MSN][3].

  [1]: http://google.com/        "游標顯示"
  [2]: http://search.yahoo.com/  "游標顯示"
  [3]: http://search.msn.com/    "游標顯示"
```
[Google][1]
[Yahoo][2]
[MSN][3]

  [1]: http://google.com/        "游標顯示"
  [2]: http://search.yahoo.com/  "游標顯示"
  [3]: http://search.msn.com/    "游標顯示"
```

---

圖片
---
![圖片](https://i1.wp.com/mrcodingroom.freesite.host/wp-content/uploads/2019/01/Drawing.png "哈")

```md
![圖片名稱](連結 "游標顯示")
```

---

圖片連結
---
[![圖片](https://i1.wp.com/mrcodingroom.freesite.host/wp-content/uploads/2019/01/Drawing.png)](https://mrcodingroom.freesite.host/)

```md
[![圖片](圖片網址)](連結網址)
```

---

表格
---
| 欄位1 | 欄位2 | 欄位3 |
| :-- | --: |:--:|
| 置左  | 置右 | 置中 |
| $100 | $100 | $100 |
| $10 | $10  | $10 |
| $1  | $1  | $1 |

```
| 欄位1 | 欄位2 | 欄位3 |
| :-- | --: |:--:|
| 置左  | 置右 | 置中 |
```

---

短區塊
---
>`內容`

\`內容`

---

CheckBox
---
> - [ ] uncheck
> - [x] check

```md
 - [ ] uncheck
 - [x] check
```



---

跳脫字元
---
\##
\```

```md
\+任意符號
```

###### tags: `MarkDown教學` `HackMD新手教學`


