---
{"dg-publish":true,"permalink":"/04-Solidified Extraction/Math/infinitesimal-generator/","title":"Infinitesimal generator 無窮小生成元","tags":["DDE"],"noteIcon":"1","created":"2025-03-03T08:48:31.910+08:00","updated":"2025-03-03T08:48:31.910+08:00"}
---

Let $X$ be a [[01-Fleeting/Banach_space\|Banach space]]. Let $Φ$ be a flow on $X$. The infinitesimal generator associated with $Φ$ is defined by
$$
Gv := ∂_{t}Φ^t(v)|_{t=0}
 = \lim_{t↘0} \frac{Φ^t(v) − v}{t}
$$
with the domain 
$$
D(G) = \left\{  v ∈ X : \lim_{t↘0} \frac{Φ^t(v) − v}{t} \text{ exists in } X  \right\}.
$$ 
(c.f. NTHU MATH 526500 DDE Note week 2)