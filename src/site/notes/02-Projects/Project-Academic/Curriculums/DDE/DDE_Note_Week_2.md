---
{"dg-publish":true,"permalink":"/02-Projects/Project-Academic/Curriculums/DDE/DDE_Note_Week_2/","title":"DDE Note Week 2","tags":["DDE"],"noteIcon":"1","created":"2024-09-13T04:42:10.000+08:00","updated":"2024-09-17T22:36:07.393+08:00"}
---

# 第二週：DDE的性質──維度、跟ODE和PDE的比較與關係、FDE form


## 和ODE的比較

一個普通的線性ODE:
$$
\begin{cases}
\dot{x}(t) = Ax(t) & \text{for } t \in \mathbb{R}\\
x(0) = x_{0} \in \mathbb{R}^n&
\end{cases}
$$

一個普通的DDE:
$$
\begin{cases}
\dot{T}(t)=-kT(t-\tau) & \text{for } t\geq0 \\
\varphi(t)\in C^0[-\tau,0] &
\end{cases}
$$

### Backward continuation
#### ODE
Unique backward continuation.
#### DDE
Haha, no way!

1. (no backward continuation) Consider $\dot{T}(t)=aT(t)+bT(t-\tau)$ for $t\geq0$ with  $T(t)=c$ on $[-\tau,0]$(prehistory).
   Assume that it can be continued to $[-\tau-\epsilon, -\tau]$. Then for $t \in [-\tau, 0]$:
   $$
   \dot{T}(t)=0=ac+bT(t-\tau) \implies T(t-\tau)=-\frac{ac}{b}\neq c\ \text{ if } -\frac{a}{b}\neq1.
   $$
   That is, $T(t) = -ac / b$ on $[-\tau-\epsilon, -\tau]$, and $T$ has a discontinuity at $t=-\tau$, which contradicts with stepwise continuity.
2. (many backward continuation)


### FDE form of the DDE
Define $X = C^0([-\tau,0],\mathbb{R}^N)$. The the DDE can be written as
$$
\begin{cases}
\dot{u}(t) = F(u_{t}) & \text{for } t\geq0, \\
u_{0} = \varphi \in X,
\end{cases}
$$
where $F:X \to \mathbb{R}^N$ is a linear functional, and $u_{t}(\theta)=u(t+\theta)$ is a function lives on $[-\tau,0]$.


### (semi-)flow 自然律/Dynamical system 動力系統
#### ODE的自然律(flow)
$\Phi:\mathbb{R}\ ×\ \mathbb{R}^n \to \mathbb{R}^n$, defined by
$$
\Phi(t,x_{0})=\Phi^t(x_{0})=e^{tA}x_{0}.
$$

#### DDE的自然律(semiflow)
$\Psi:[0,\infty)\ ×\ X \to X$, defined by
$$
\Psi(t,\varphi)=\Psi^t(\varphi) = u_{t},
$$
where 
$$
u_{t}(\theta) = u(t+\theta) =
\begin{cases}
\varphi(t+\theta) & \text{ if } t+\theta \in [-\tau,0] \\
\varphi(0)+\int_{0}^{t+\theta}F(u_{s})ds & \text{ if } t+\theta > 0.
\end{cases}
$$

##### solution segment/window
就是$u_{t}$們

### 無窮小生成元(infinitesimal generator)

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">

# Infinitesimal generator 無窮小生成元

</div>



Let $X$ be a [[01-Fleeting/Banach_space\|Banach space]]. Let $Φ$ be a flow on $X$. The infinitesimal generator associated with $Φ$ is defined by
$
Gv := ∂_{t}Φ^t(v)|_{t=0}
 = \lim_{t↘0} \frac{Φ^t(v) − v}{t}
$
with the domain 
$
D(G) = \left\{  v ∈ X : \lim_{t↘0} \frac{Φ^t(v) − v}{t} \text{ exists in } X  \right\}
$ 

</div></div>


#### ODE的無窮小生成元
The matrix $A$.

#### DDE的無窮小生成元
$\partial_{\theta}$.
##### Compatibility conditions (相容條件)

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">

# Compatibility conditions 相容條件

</div>



為了確認FDE form of the DDE的無窮小生成元的domain，我們注意到在定義中，當$\theta=0$的時候：
$
 G\varphi(0) = \varphi'(0) = \dot{u}(0) = Fu_{0} = F\varphi.
$
所以$G$的domain有一個限制條件就是$\varphi'(0) = F\varphi$.

</div></div>


##### Transport PDEs on $X$
###### boundary condition


## DDE是無窮維的
這句話是什麼意思？就是像空間(phase space)是有限維還是無窮維的意思

## FDE form 和 ODE form 的優勢


---
# 當天的筆記

<center><iframe src="https://drive.google.com/file/d/1PacJp3YdhrNR9wzc5ylpH6nkcmLvHjVM/preview" 
width="90%" height="480" allow="autoplay" aspect-ratio="4 / 4" overflow="hidden" position="absolute" scrolling="no">
</iframe></center>

[[IMG-20240913045502596.pdf]]

---
# 作業