---
{"dg-publish":true,"permalink":"/04-Solidified Extraction/Math/Locally-Lipschitz/","title":"Locally Lipschitz","tags":["Math","DDE"],"noteIcon":"1","created":"2024-09-20T23:36:38.318+08:00","updated":"2024-09-21T03:44:00.315+08:00"}
---


## Definition

$F(t, \psi): \mathbb{R} \times X →  \mathbb{R}^N$ is locally Lipschitz in $\psi$ if for each $(t_{0}, \psi_{0}) \in \mathbb{R} \times X$, there exists an $\varepsilon_{0}>0$ and $L>0$ s.t.
$$
|F(t_{0},\psi)-F(t_{0},\psi_{0})|<L|\psi-\psi_{0}|_{X} \; \text{ for }\; |\psi-\psi_{0}|_{X}<\varepsilon_{0}.
$$

> [!human]- 人話
> $F$ loc. Lip. in $\psi$ 的意思就是隨便給一個 $F$ domain 中的<font color="#92d050">點</font>，都可以找到一個大於 $0$ 的常數 $L$ ，使得只要其它跟<font color="#92d050">它</font>一樣的$t$的點離<font color="#92d050">它</font>夠近，函數值的差就能被<font color="#92d050">它們</font>距離的$L$倍bound住。

## Examples

### DDE 
Consider $\dot{u}(t) = f\big(t, u(g_{1}(t)), u(g_{2}(t)), \dots, u(g_{m}(t))\big)$ with $g_{j}(t)\leq t$ for $t\geq t_{0}$, which can be written as
$$
\begin{cases}
\dot{u}(t) = F(t, u_{t})\\
u_{t_{0}} = \varphi \in X
\end{cases}
$$
with $F(t,\varphi) = f\big(t, \varphi(g_{1}(t)-t), \dots, \varphi(g_{m}(t)-t)\big)$ and the phase space $X = C^0([-\tau, 0], \mathbb{R}^N)$. (c.f. [[04-Solidified Extraction/Math/A-More-General-Discrete-Delay\|A More General Discrete Delay]])
Suppose that $f(t, \xi)$ is loc. Lip in $\xi$. Then $F$ is loc. Lip. in $\psi$. (c.f. [Note](zotero://open-pdf/library/items/8UBJF793?page=1&annotation=ABBCUUWL))

(c.f. NTHU MATH 526500 DDE Note week 3)