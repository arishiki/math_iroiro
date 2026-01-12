# 記法

$`J_g`$ で関数 $`g`$ のヤコビアンを表す。  
測度・積分は，断りのない限り Lebesgue 積分とする。

# 命題

$`A, B \subset \mathbb{R}^n`$ を開集合とする。  
$`g : A \to B`$ は $`C^1`$ 級写像とし，$`K \subset A`$ はコンパクト集合とする。  
$`g`$ は $`K`$ 上で a.e. 単射であり，かつ a.e. $`J_g \neq 0`$ と仮定する。

$`f : B \to \mathbb{R}`$ を連続関数とすると，次が成り立つ：

$$
\int_K (f \circ g)\ |J_g| = \
\int_{g(K)} f.
$$ 
$`hoge`$ 