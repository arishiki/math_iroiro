
# Lebesgue 積分における変数変換

## 記法

$J_g$ で関数 $g$ のヤコビアンを表す．  
測度・積分は，断りのない限り Lebesgue 積分とする．

## 命題

$A, B \subset \mathbb{R}^n$ を開集合とする．  
$g : A \to B$ は $C^1$ 級写像とする．  
$g$ は $A$ 上で a.e. 単射であり，かつ a.e. $J_g \neq 0$ と仮定する．

$f : B \to \mathbb{R}$ を連続関数とする．

$\int_{A} (f \circ g)\ |J_g|d\mu\cdots(1), \int_{g(A)} fd\mu\cdots(2)$
に対し，$f$ が $g(A)$ 上非負または(1), (2)のいずれかが可積分なら $(1)=(2)$．

## 証明

$N\subset A$ に対し $\mu(N) = 0$ なら $g(N) = 0$ となる．このことは以下のようにしてわかる：
コンパクト集合の列 $\{K_n\}$ が存在して

$$
K_1 \subset K_2 \subset \cdots,\qquad \bigcup_{n=1}^\infty K_n = A
$$

（すなわち $K_n \nearrow A$）となる．


各 $n$ について $N_n := N \cap K_n$ とおくと $\mu(N_n)=0$ である．

また $K_n$ はコンパクトで $g$ は $C^1$ 級だから，ある $C_n \gt 0$ が存在して
$g$ は $K_n$ 上 $C_n$-Lipschitz 連続である（[杉浦II]命題 3.1）．  
よって

$$
\mu(g(N_n)) = 0
$$

である（[杉浦II]命題 3.2）．

ここで $N_n \nearrow N$ なので $g(N_n) \nearrow g(N)$ であり，

$$
g(N) = \bigcup_{n=1}^\infty g(N_n)
$$

が成り立つ．したがって

$$
\mu(g(N)) = 0
$$

を得る．

仮定より，ある可測集合 $N \subset A$ が存在して

- $\mu(N) = 0$，
- $A \setminus N$ 上で $g$ は単射，
- $A \setminus N$ 上で $J_g \neq 0$

が成り立つ．

以下，$A \setminus N$ を $A'$ と書く．

逆関数定理より，$A'$ の各点 $x$ に対して，ある開集合 $U\subset A$ が存在し，
$g(U)$ は開集合であり，$g : U \to g(U)$ は $C^1$ 級同相写像となる．

集合

$$
C := \{ x \in A : J_g(x) = 0 \}
$$

は閉集合であるから，一般性を失うことなく，
$U$ 上で $J_g \neq 0$ と仮定してよい．

いま，ある $\delta \gt 0$ が存在して

$$
U(x, \delta) \subset U
$$

となる．  
このとき，$U(x, \delta/2)$ はある有理点 $q$ を含む．

さらに，

$$
d(x, q) < r < \delta/2
$$

を満たす有理数 $r$ を取ることができる．  
このとき

$$
x \in U(q, r)
$$

であり，かつ

$$
U(q, r) \subset U
$$

が成り立つ．

以上より，$A'$ は開集合の可算族 $\lbrace U _ n \rbrace _ {n\in\mathbb{N}}$ によって被覆され，
$U _ n \subset A$ であり，各 $U _ n$ 上で

- $J_g \neq 0$，
- $g$ は $C^1$ 級同相写像

が成り立つ．

各 $n$ に対して，可算個の有界閉区間 $\lbrace I _ m^n \rbrace _ {n,m\in\mathbb{N}}$ が存在して

$$
\bigcup_{m\in\mathbb{N}} I _ m^n = U _ n
$$

が成り立つ．

いま， $\lbrace I _ m^n \rbrace _  {m, n\in\mathbb{N}}$ を並べ直して $\lbrace J _ n \rbrace _ {n\in\mathbb{N}}$ とし，

$$
B _ n = \bigcup _ {m\leq n}J _ m
$$

$$
C _ {n+1} = B _ {n+1} \setminus (B _ n)^\circ, C _ 0 = B _ 0
$$
とすると，
$$
\begin{eqnarray}
    \bigcup _ {n \in \mathbb{N}} C _ n &= \bigcup _ {n \in \mathbb{N}} B _ n \\
         &= \bigcup _ {n \in \mathbb{N}} J _ n \\
         &= \bigcup _ {n \in \mathbb{N}} J _ n \\
         &= \bigcup _ {m, n \in \mathbb{N}} I _ m^n \\
         &= \bigcup _ {n \in \mathbb{N}} U _ n \supset A'
\end{eqnarray}
$$
であり，
$\lbrace C _ n \rbrace _ {n\in\mathbb{N}}$ はコンパクト集合の族で任意の $m\neq n$ に対し $\mu(C _ m \cap C _n) = 0$ となる．

以下，まず $f$ が $g(A)$ 上非負のケースについて考える．
任意の $n \in \mathbb{N}$ に対し，
$$
\int _ {\bigcup _ {m \leq n} C _ m} f\circ g =
\sum _ {m \leq n} \int _ {C _ m} f\circ g -
\int _ {C _ m \setminus \bigcup _ {l \lt m} C _ l} f\circ g.
$$

一方，$C _ m \setminus \bigcup _ {l \lt m} C _ l  \subset \bigcup _ {l \lt m} C _ l \cap C _ m$ であり，右辺は測度 0 だから，
$$
\int _ {\bigcup _ {m \leq n} C _ m} f\circ g =
\sum _ {m \leq n} \int _ {C _ m} f\circ g.
$$
<!-- $$~$$内の\displaylines{ }内で\\により改行使える-->