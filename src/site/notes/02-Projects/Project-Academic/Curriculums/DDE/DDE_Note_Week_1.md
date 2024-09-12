---
{"dg-publish":true,"permalink":"/02-Projects/Project-Academic/Curriculums/DDE/DDE_Note_Week_1/","title":"DDE Note Week 1","tags":["DDE"],"noteIcon":"1","created":"2024-09-05T18:22:07.000+08:00","updated":"2024-09-12T14:37:22.000+08:00"}
---

# 第一週：什麼是DDE？

## 例子：洗澡水溫度

### <u>Notations</u>: 

mixer：就當作水龍頭，冷熱水交互的地方
$T(t)$：mixer在時間$t$的溫度
$\tau$：水從mixer流到蓮篷頭的時間(time delay)
$T_{d}$ ：你想要的溫度
$\phi(t)$：前歷史(prehistory)
所以你感覺到的水溫應該是$T(t-\tau)$。
{ #82331a}


### <u>前提</u>：

水溫變化的幅度和你轉水龍頭的角度成正比，係數$k$(想成你轉水龍頭的速度)

### <u>建模</u>：
$$
 \frac{d}{dt} T(t) := \dot{T}(t) = -k(T(t-\tau)-T_{d})
$$
$k$前面的負號是負回饋的意思ie 水溫比預期大應該是往下調

## DDE的特殊性質


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">

# 前歷史 Prehistory in DDE

</div>



舉例來說，DDE洗澡方程只能apply到$t\geq0$的時候，想知道時間$=s <\tau$的時候的溫度變化，就需要有$T(s-\tau)$這個初值。
以此類推，會需要某一整段時間的初值，
所以這邊DDE要求的「初值」不再是一個單一的值，而是一個函數定義在$[-\tau, 0]$

前歷史簡單起見目前先假設連續

</div></div>



<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">

# Method of steps

</div>



在discrete delay的DDE中，可以拿第0步([[04-Solidified Extraction/前歷史_Prehistory\|前歷史]])代入DDE解出第1步在$[0, \tau]$上
拿第1步再代回去解出第2步在$[\tau, 2\tau]$上
以此類推

</div></div>



<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">

# Stepwise Regularity

</div>



在discrete delay DDE中，用[[04-Solidified Extraction/Method_of_Steps\|Method of steps]]解出來的解，會因為當下這一段是用前一段積出來的，會比前一段多一層可微性
然後在時間段的端點處微分也得拆成左微和右微

</div></div>


(更[[Journal/Daily/Diary-2024-09-11-Wed\|2024-09-11]]) From 作業：


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">

# DDE的解可能會相交

</div>



不太確定有沒有理解錯，我記得在ODE中，不同的解是不可能相交的(by存在唯一？)
但在作業中就直接給了一個很簡單的例子說明DDE不同的解是可以相交的。
這會不會代表過往的一些存在唯一的東西在DDE已經不適用了？

</div></div>

### 問題
雖然這個方法就已經告訴你解了，但寫出來很醜，然後你看不出他的行為，例如時間跑到無窮大會發生什麼事
如果你的delay也和時間有關(distributed delay $\leftrightarrow$ discrete delay)，這個方法也沒辦法解(why?)

([[Journal/Daily/Diary-2024-09-05-Thu\|2024-09-05]])

---

# 當天的筆記

[[IMG-20240911224943441.pdf]]

---
# 作業

[[02-Projects/Project-Academic/Curriculums/DDE/DDE_HW1\|HW1]]