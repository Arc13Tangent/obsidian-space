---
{"dg-publish":true,"permalink":"/04-Solidified Extraction/Math/A-More-General-Discrete-Delay/","title":"A More General Discrete Delay","noteIcon":"1","created":"2025-03-03T08:48:31.896+08:00","updated":"2025-03-03T08:48:31.896+08:00"}
---


Time delays are not necessarily constants. They can hide in functions like $g(t)$ that satisfies $g(t)\leq t$ for all admissible $t$. 

In that case, when we want to define the interval where our functions live, we usually take $[t_{0}-\tau, \dots \rangle$ , where we wish $\tau$ satisfies
$$
t-\tau \leq \inf\{ g(t): t \in [t_{0}, \dots\rangle \},
$$
which is equivalent to 
$$
\tau \geq \sup \{ t - g(t) : t \in [t_{0, \dots}\rangle \}.
$$
Or
$$
\tau \geq \sup_{j=1,\dots,m} \{ t - g_{j}(t) : t \in [t_{0, \dots}\rangle \}.
$$
for more general case.

(c.f. NTHU MATH 526500 DDE Note week 3)