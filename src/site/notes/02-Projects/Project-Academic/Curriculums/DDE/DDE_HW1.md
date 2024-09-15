---
{"dg-publish":true,"permalink":"/02-Projects/Project-Academic/Curriculums/DDE/DDE_HW1/","title":"HW1","tags":["DDE"],"noteIcon":"1","created":"2024-09-02T07:54:52.000+08:00","updated":"2024-09-15T14:47:32.003+08:00"}
---

# HW1

[Zotero](zotero://select/library/items/GKZ9B65M) [PDF](zotero://open-pdf/library/items/MQY9W2SX)

## ✏️ Notes

(預[[Journal/Daily/Diary-2024-09-02-Mon\|2024-09-02]])
目前不知道是啥毀的：
> [!blue] [Page 1](zotero://open-pdf/library/items/MQY9W2SX?page=1&annotation=ZFVCUWMV)
> 
> the method of steps
> 
> ---
> 答([[Journal/Daily/Diary-2024-09-05-Thu\|2024-09-05]])：[[04-Solidified Extraction/Method_of_Steps\|Method of steps]]
> 
>
{ #ZFVCUWMVaMQY9W2SXp1}


> [!blue] [Page 1](zotero://open-pdf/library/items/MQY9W2SX?page=1&annotation=Z4AW7B8Y)
> 
> prehistory
> 
> ---
> 答([[Journal/Daily/Diary-2024-09-05-Thu\|2024-09-05]])：[[04-Solidified Extraction/前歷史_Prehistory\|前歷史 Prehistory in DDE]]
>
{ #Z4AW7B8YaMQY9W2SXp1}


> [!blue] [Page 2](zotero://open-pdf/library/items/MQY9W2SX?page=2&annotation=2Q6DXNX4)
> 就是把$u(t)=Ce^{\lambda t}$代進去方程裡看看會怎樣。
> 
> ---
> 
> exponential Ansatz
>
{ #2Q6DXNX4aMQY9W2SXp2}


> [!blue] [Page 2](zotero://open-pdf/library/items/MQY9W2SX?page=2&annotation=3WPMX8AF)
> 就是在exp ansatz中代$t=0$進去得到的一個$\lambda$的方程式。
> 
> ---
> 
> characteristic equation
>
{ #3WPMX8AFaMQY9W2SXp2}


---

## Assignments

### $\text{Problem 1}$ 
Consider the shower equation: $\dot{T}(t)=-k\big[T(t-\tau)-T_{d}\big]$ with $\tau >0$ and $k>0$.
1. Find $\alpha, \beta \in \mathbb{R}$ in the rescaling $\tilde{T}(t) := T(\alpha t)-\beta$ that results in the simpler equation
   $$
   \dot{\tilde{T}}(t)=-\tilde{k}\tilde{T}(t-1).
   $$
   What is $\tilde{k}$?
   
   $\textit{Proof}.$ By differentiating both sides of the definition $\tilde{T}(t) := T(\alpha t)-\beta$, we immediately get
   $$
   \dot{\tilde{T}}(t)=\alpha\dot{T}(\alpha t) = \alpha\big[-k(T(\alpha t-\tau)-T_{d})\big], 
   $$
   where the last equation is given by the original shower equation at the very beginning, with $t$ replaced by $\alpha t$. On the other hand, 
   $$
   -\tilde{k}\tilde{T}(t-1) = -\tilde{k}\big[T(\alpha t-\alpha)-\beta\big] = -\tilde{k}T(\alpha t -\alpha) +\tilde{k}\beta.
   $$
   Suppose that $\dot{\tilde{T}}(t)=-\tilde{k}\tilde{T}(t-1)$. Then 
   $$
   \alpha\big[-k(T(\alpha t-\tau)-T_{d})\big] = -\tilde{k}T(\alpha t -\alpha) +\tilde{k}\beta.
   $$
   By comparison of the parameters, we have
   $$
   \alpha = \tau,\; \alpha k=\tilde{k},\; \alpha kT_{d} = \tilde{k}\beta.
   $$
   Therefore, $\alpha = \tau, \beta = T_{d}$, and $k=\tilde{k}/{\alpha}$. $\blacksquare$

2. Consider the rescaled shower equation 
   $$
   \dot{T}(t)=-T(t-1).
   $$
   Use the method of steps. to find $T(1)$ and $T(2)$ with $\phi(t)=1$ on $[-1,0]$.
   
   $\textit{Proof.}$ 
   1.  $\dot{T}(t)=-\phi(t-1)=-1$ when $t\in[0,1]$. Therefore, by the method of steps, 
      $$
      T(t)= T(0)+ ∫_{0}^t \dot{T}(s)ds = -t+1
      $$ 
      on $[0,1]$. Hence $T(1)=0$. $\blacksquare$
    Denote $T_{1}(t)=-t+1$ on $[0,1]$.
   2.  $\dot{T}(t)=-T_{1}(t-1)=-t+1$ when $t\in[1,2]$. Therefore, by the method of steps again,
      $$
      \begin{align}T(t)=T(1)+\int_{1}^t \dot{T}(s)ds &= T(1) - \int_{1}^t T_{1}(s-1)ds  \\ \\
      &= T(1)-∫_{1}^t [-(s-1)+1]ds \\ \\
      &= T(1)+\int_{1}^t (s-2)ds & \\ \\
      &= \hspace{0.4cm} 0 \hspace{0.3cm} + \frac{t^2}{2} -2t+\frac{3}{2}= \frac{t^2}{2} -2t+\frac{3}{2}.
      \end{align}
      $$ 
      Hence, $T(2) = -1 / 2$. $\blacksquare$
### $\text{Problem 2}$ 
(stepwise regularity) Let $u(t)$ be the solution to the DDE
$$
\dot{u}(t) = f (u(t), u(t − 1))
$$
with a continuous prehistory $u(t) = φ(t)$ for $t ∈ [−1, 0]$. Let $f ∈ C^∞(\mathbb{R}^N × \mathbb{R}^N , \mathbb{R}^N )$. Prove $u ∈ C^j([j − 1, T_{max}(φ)), \mathbb{R}^N )$ for $j ∈ \mathbb{N}$, where $T_{max}(φ)$ is the maximal time interval of the existence of the solution.

$\textit{Proof.}$ Note that we can write
$$
u(t)=\int_{0}^t f(u(s),u(s-1))ds + u(0).
$$
Therefore, $u(t)$ is at least $C^0$ on $[-1,T_{max}(φ))$. Now, we prove that $u(t)$ is $C^j$ on $[j-1,T_{max}(φ))$ by induction. Suppose that  $u(t)$ is $C^j$ on $[j-1,T_{max}(φ))$ when $j=k$, i.e., $u(t)$ is $C^k$ on $[k-1,T_{max}(φ))$. Then, when $j=k+1$,

- $u(t)$ is $C^k$ on $[k, T_{max}(\varphi)) \subset [k-1,T_{max}(φ))$ by assumption and
- $u(t-1)$ is $C^k$ on $[k-1, T_{max}(\varphi))$ since $t-1\in[k-1, T_{max}(\varphi))$ for $t\in [k,T_{max}(\varphi))$.
  
Therefore, $\dot{u}(t) = f(u(t),u(t-1))$ is of $C^k$, and hence $u(t)$ is $C^{k+1}$ on $[k,T_{max}(\varphi))$.
By induction, the desired result holds for all $j\in \mathbb{N}$. $\blacksquare$

### $\text{Problem 3}$ 
Consider the shower equation 
$$
\dot{T} (t) = −kT (t − τ )
$$
 with a discrete delay $τ > 0$ and a parameter $k > 0$.
 1. Since the equation is linear, we can substitute the "exponential Ansatz,"
    $$
    T (t) := e^{tλ},
    $$
    into the equation. Derive the characteristic equation for $λ$.
    
    $\textit{Proof.}$ Plug $T(t)=e^{t\lambda}$ into the DDE yields $\lambda e^{t\lambda}=-ke^{\lambda(t-\tau)}$. Since $e^{t\lambda}>0$ for all $t$, we can divide $\lambda e^{t\lambda}=-ke^{\lambda(t-\tau)}$ both sides with $e^\lambda t$ (or set $t=0$) to get 
    $$
    \lambda +ke^{-\lambda \tau}=0,
    $$
    i.e., the characteristic equation for $\lambda$. $\blacksquare$
    
 2. Prove that for each delay $τ > 0$, there exist countably many $k_{j} > 0,\ j ∈ \mathbb{N}$, such that the shower equation with $k = k_{j}$ has a periodic solution in the form
    $$
    T (t) = \mathrm{Re}(e^{itω_{j}} ) = cos(ω_{j}t),\ ω_{j} ∈ \mathbb{R}.
    $$
    Here $\mathrm{Re}(z)$ denotes the real part of $z ∈ \mathbb{C}$. What is $ω_{j}$? Since $T (t) ≡ 0$ is a (trivial) solution, conclude that two different solutions can intersect in $\mathbb{R}$.
    
    $\textit{Proof.}$ Write $\lambda=\lambda_{1}+i\lambda_{2}$, where $\lambda_{1}, \lambda_{2} \in \mathbb{R}$ and $i=\sqrt{ -1 }$. With the fresh characteristic equation of $\lambda$ we derived the above yields
    $$
    (\lambda_{1}+i\lambda_{2})+k^{-(\lambda_{1}+i\lambda_{2})\tau} = 0,
    $$
    which implies that $(\lambda_{1}+i\lambda_{2}) + ke^{-\lambda_{1}\tau}[\cos(\lambda_{2}\tau)-i\sin(\lambda_{2}\tau)] = 0$, and hence
    $$
    \begin{align*}
    \lambda_{1}+ke^{-\lambda_{1}\tau}\cos(\lambda_{2}\tau) &= 0 \\
    \lambda_{2}-ke^{-\lambda_{1}\tau}\sin(\lambda_{2}\tau) &= 0
    \end{align*}
    $$
    because $\left( \lambda_{1}+ke^{-\lambda_{1}\tau}\cos(\lambda_{2}\tau) \right) + i\left( \lambda_{2}-ke^{-\lambda_{1}\tau}\sin(\lambda_{2}\tau) \right) = 0$. Since we wish that our solution has the form $cos(ω_{j}t),\ ω_{j} ∈ \mathbb{R}$, we need $\lambda_{1}$ to be $0$. Hence we get 
    $$
    \begin{align} 
    k\cos(\lambda_{2}\tau) &= 0  \\ 
    \lambda_{2}-k\sin(\lambda_{2}\tau) &= 0 \\
    \end{align}
    $$
    which implies that $\lambda_{2}\tau = (2n+1)({\pi} / {2})$, i.e., $\lambda_{2} = (2n+1)({\pi} / {2\tau})$ for $n \in \mathbb{Z}$, and 
    $$
    k = \lambda_{2 }/ \sin(\lambda_{2}\tau) = \frac{\frac{(2n+1)\pi}{2\tau}}{\sin((2n+1)(\pi / 2))} = 
    \begin{cases}
    \hspace{0.36cm}(2n+1)(\pi / {2\tau}), & \text{if $n$ even}\\
    -(2n+1)(\pi / {2\tau}), & \text{if $n$ odd}.
    \end{cases}
    $$
    
    Since our $k$ are greater than $0$, we must narrow down our candidates of $n$ to be positive even integers, $0$, and negative odd integers. Finally, we can state our result:
    Set 
    $$
    \begin{align}
    V &=\{ v: v=0, \text{or } v \text{ is a positive even integer or a negative odd integer} \} \\
    &= \{ v_{j} \}_{j=1}^\infty.
    \end{align}
    $$ 
    > Let $\text{sign}(x) = 1$ if $x$ is nonnegative and $\text{sign}(x)=-1$ if $x$ is negative. Then, for each delay $τ > 0$, there exist countably many $k_j = \text{sign}(v_{j})(2v_{j}+1)(π / 2\tau) > 0, j ∈ \mathbb{N}$, such that the DDE with $k = k_{j}$ has a periodic solution in the form
    > $$ T(t) = \cos(\omega_{j}t) = \cos\big((2v_{j}+1)({\pi} / {2\tau})t\big).\ \big(\omega_{j}=(2v_{j}+1)({\pi} / {2\tau})\big)$$

    With these periodic solutions and the trivial solution, we see that the solutions of the same equation can intersect with each other. (?!!!!) $\blacksquare$

 3. Why the scalar shower equation has periodic solutions no matter how small the delay $τ > 0$ is? 
    多了一個大於$0$的$\tau$之後，$\lambda$的特徵方程($\lambda +ke^{-\lambda \tau}=0$)因為那個$\tau$的關係導致多出一個$\exp$而具有複數解(在沒有delay的時候，特徵方程為$\lambda + k = 0$)。所以當我們使用exponential ansatz來解DDE的時候，$\lambda$如果有imaginary part，就會跑出$\cos$和$\sin$這兩個週期函數。
    
### $\text{Problem 4}$ 
We know that $x(t) = x_{0} /(1−x_{0}t)$ solves the ODE  $\dot{x}(t) = x^2(t)$ with the initial condition $x(0) = x_0 > 0$, and blows up at a finite time $t = 1 / x_{0}$ , that is, $lim_{t ↗ 1 / x_{0}} x(t) = ∞$.
1. Prove that the DDE  $u(t) = u^2(t − τ )$ does not have finite-time blow-up solutions for any delay $τ > 0$ and prehistory $φ ∈ C^0([−τ, 0], \mathbb{R}$). Hint: Use the method of steps.
   
   $\textit{Proof.}$ $\dot{u}(t)=u^2(t-\tau)=\varphi^2(t-\tau)$ is continuous on $[0,\tau]$, hence
   $$
   u(t)=\int_{0}^t \varphi^2(s-\tau)ds + \varphi(0)
   $$
   is continuous and finite on $[0,\tau]$. Now we prove that $u(t)$ is continuous and finite on $[(j-1)\tau, j\tau]$ for all $j\in \mathbb{N}$. Suppose that the result holds for $j=k$. Then when $j=k+1$, 
	   - $u^2(s-\tau)$ is continuous for all $s \in [(j-1)\tau,t]$ since $(s-\tau) \in [(k-1)\tau, k\tau]$, and 
	   - $u((j-1)\tau)=u(k\tau)$ is finite.
   
   Therefore, $u(t) = ∫_{(j-1)\tau}^t u^2(s-\tau)ds+u((j-1)\tau)$ is continuous and finite on $[(j-1)\tau, j\tau]=[k\tau, (k+1)\tau]$.
   By induction, the result holds for all $j\in \mathbb{N}$. Hence $u(t)$ is finite all the time. $\blacksquare$
   
2. Explain the behavior of solutions of the DDE with $φ(t) ≡ 1$ as $τ ↘ 0$.
   
   $\textit{Proof.}$ The "slope" in the nth step is given by the (n-1)th step, where each step has length $\tau$. When $\tau$ becomes smaller and smaller, each step "shrinks," and the "slope" at each $t$ becomes larger and hence grows faster than before. Therefore, the solution will explode to $\infty$ as $\tau ↘ 0$.
   (For example, assume that the original $\tau$ is $1$, then the "slope" at $3 / 4$ is $1$, which is given by the 0th step. When $\tau$ becomes $1 /2$, the "slope" at $3 / 4$  becomes larger than $1$, which is given by the 1st step.) $\blacksquare$

([[Journal/Daily/Diary-2024-09-11-Wed\|2024-09-11]])

---
## 🤔 Thinking



---
## Links and References



---
