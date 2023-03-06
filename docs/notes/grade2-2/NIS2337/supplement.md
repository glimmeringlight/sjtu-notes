## 典型集和典型序列

### AED，渐进均分性

对于一系列的独立的同分布的随机变量$X_i$的取值$x_i$，则有

$$
H(X)-\varepsilon\leqslant -\dfrac{1}{n}\log p(x_1,x_2,\dots ,x_n)\leqslant H(X)+\varepsilon.
$$

给出简单的证明：

$$
\begin{aligned}
\lim_{n\to \infty}-\dfrac{1}{n}\log p(x_1,x_2,\dots ,x_n) &=\lim_{n\to \infty} -\dfrac{1}{n}\sum_{i}^{n}\log p(x_i)\\
&=-E[\log p(x)]=H(X).
\end{aligned}
$$

注意，上述推导过程使用到了大数定理，也就是说，对于上述$n$个取值，对于$\forall i\leqslant n$，都应该有$\dfrac{N(x_i\mid \{x_n\})}{n}\approx p(x_i)$.其中，$N(x_i\mid \{x_n\})$表示序列中$x_i$出现的次数。

一个额外的推论是：

$$
2^{-n(H(X)+\varepsilon)}\leqslant p(x_1,x_2,\dots,x_n)\leqslant 2^{-n(H(X)-\varepsilon)}.
$$

### 典型序列和典型集

根据上述所说的渐进均分性，我们可以用其来定义典型序列：如果序列$\{x_1,x_2,\dots ,x_n\}$满足：

$$
2^{-n(H(X)+\varepsilon)}\leqslant p(x_1,x_2,\dots,x_n)\leqslant 2^{-n(H(X)-\varepsilon)}.
$$

则称其为概率分布$X\sim p(x)$的一个典型序列。

这样的满足要求的序列的集合称为典型集，记作$T(\varepsilon ,n)-p(x)$.

### 典型序列的性质

**性质一**：如果$\{x_n\}$为典型序列，则$p(\{x_n\})=2^{-nH(X)}$.

简短的证明如下：

$$
\begin{aligned}
    p(\{x_n\})&=\prod_{i=1}^{n}p(x_i)\\
    &=\prod _{x\in X}p(x)^{N(x\mid x_n)}\\
    &=2^{\log \prod_{x\in X}p(x)^{N(x\mid x_n)}}\\
    &=2^{\sum_{x\in X}\log p(x)^{N(x\mid x_n)}}\\
    &=2^{\sum_{x\in X}N(x\mid x_n)\log p(x)}\\
    &=2^{\sum_{x\in X}np(x)\log p(x)}=2^{-nH(X)}.
\end{aligned}
$$

**性质二**：$P(T(\varepsilon , n))\geqslant 1-\varepsilon$，也就是说，任一随机序列属于典型集的概率无限趋近于$1$。

简短的证明如下：

由于定义，$-\dfrac{1}{n}\log p(x_1,\dots ,x_n)$依概率收敛于$H(X)$。于是有：

$$
\lim_{n\to \infty}\textrm{Pr}(\left |-\dfrac{1}{n}\log p(x_1,\dots ,x_n)-H(X)\right |< \varepsilon)\geqslant 1-\delta. 
$$

取$\delta = \varepsilon$即得证。

**性质三**：$\left | T(\varepsilon , n)\right |\approx 2^{nH(X)}$.

由于性质一说明了典型序列的出现概率；性质二说明了任一随机序列属于典型集的概率。两者共同考虑，则可以不严格地推出典型集的元素个数为$2^{nH(X)}$.