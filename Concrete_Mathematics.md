# 第五章	二项式系数

**加法公式**：
$$
{r\choose k}={r-1\choose k}+{r-1\choose k-1}
$$

> $$
> \sum_{k\leq n}{r+k\choose k}=\sum_{k\leq n}\left({r+k+1\choose k}-{r+k\choose k-1}\right)={r+n+1\choose n}
> $$
>
> $$
> \sum_{k\leq n}{k\choose m}=\sum_{k\leq n}\left({k+1\choose m+1}-{k\choose m+1}\right)={n+1\choose m+1}
> $$

拓展的二项式系数：
$$
{r\choose k}=(-1)^k{k-r-1\choose k}
$$

>$$
>(-1)^n{-n-1\choose m}=(-1)^m{-m-1\choose n}={m+n\choose n},m,n\geq 0
>$$
>
>$$
>\sum_{k\leq m}(-1)^k{r\choose k}=(-1)^m{r-1\choose m}
>$$

$$
\sum_{k\leq m}{r\choose k}(\frac{r}{2}-k)=\frac{m+1}{2}{r\choose m+1}
$$

> $$
> 用数学归纳法证明：\frac{m+1}{2}{r\choose m+1}+{r\choose m+1}(\frac{r}{2}-m-1)=\frac{r-m-1}{2}{r\choose m+1}=\frac{m+2}{2}{r\choose m+2}
> $$

$$
\sum_{k\leq m}{m+r\choose k}x^k y^{m-k}=\sum_{k\leq m}{-r\choose k}(-x)^k (x+y)^{m-k}
$$

> $$
> 数学归纳法证明：当m<0时，两边都为零。\\
> 当m=0时，两边都是1。\\
> 如果用S_m表示左边的和式，容易证明：\\
> S_m=\sum_{k\leq m}{m+r-1\choose k}x^ky^{m-k}+\sum_{k\leq m}{m+r-1\choose k-1}x^k y^{m-k}\\
> =yS_{m-1}+{m+r-1\choose m}x^m+xS_{m-1}\\
> =(x+y)S_{m-1}+{-r\choose m}(-x)^m\\
> 右式也满足这个递推式。根据归纳法，两边必定相等。\\
> 另一个更加简洁的证明。当\ r\ 是0\geq r\geq-m中的一个整数时，两边都是(x+y)^{m+r}y^{-r}，\\
> 又由于两边都是关于\ r\ 的\ m\ 次或者更低次的多项式，在\ m+1\ 个不同的值取值相等可以说明一般情形下相等。
> $$

对于上述的式子，如果取 $x=y=1$ 以及 $r=m+1$ ，可以得到
$$
\sum_{k\leq m}{2m+1\choose k}=\sum_{k\leq m}{m+k\choose k}2^{m-k}
$$


而左边正好对上指标为 $2m+1$ 的二项式系数的一半进行了求和，正好等于 $2^{2m}$，所以
$$
\sum_{k\leq m}{m+k\choose k}2^{-k}=2^m
$$

> ​	有组合解释，两个队伍公平比赛，一共进行 $2m+1$ 局比赛，先获得 $m+1$ 场胜利的队伍获得胜利。用 $p(m+1,k)$ 表示队伍A赢下第 $m+k+1$ 场比赛的胜利后成为赢家的概率。
> $$
> \sum_{k=0}^m p(m+1,k)=\sum_{k=0}^m\frac{1}{2}{m+k\choose k}2^{-(m+k)}=\frac{1}{2}\\
> $$
> 所以
> $$
> \sum_{k\leq m}{m+k\choose k}2^{-k}=2^m
> $$

二项式系数的乘积公式总结：
$$
\sum_{k}{r\choose m+k}{s\choose n-k}={r+s\choose m+n}\\
\sum_{k}{l\choose m+k}{s\choose n+k}={l+s\choose l-m+n}\\
\sum_{k}{l\choose m+k}{s+k\choose n}(-1)^k=(-1)^{l+m}{s-m\choose n-l}\\
\sum_{k\leq l}{l-k\choose m}{s\choose k-n}(-1)^k=(-1)^{l+m}{s-m-1\choose l-m-n}\\
\sum_{-q\leq k\leq l}{l-k\choose m}{q+k\choose n}={l+q+1\choose m+n+1}
$$


下面是一些练习：
$$
\begin{aligned}
\sum_{k=0}^m{m\choose k}\left/{n\choose k}\right.&=\sum_{k=0}^m {n-k\choose m-k}\left/{n\choose m}\right.\\
&=\sum_{k=0}^m{n-(m-k)\choose m-(m-k)}\left/{n\choose m}\right.\\
&=\sum_{k=0}^m {n-m+k\choose k}\left/{n\choose m}\right.={n+1\choose m}\left/{n\choose m}\right.\\
&=\frac{n+1}{n+1-m}
\end{aligned}
$$

$$
\begin{aligned}
\sum_{k=0}^n k{m-k-1\choose m-n-1}&=\sum_{k=0}^n (m-(m-k)){m-k-1\choose m-n-1}\\
&=\sum_{k=0}^n m{m-k-1\choose m-n-1}-\sum_{k=0}^n (m-k){m-k-1\choose m-n-1}\\
&=m\sum_{k=0}^n {m-k-1\choose m-n-1}-(m-n)\sum_{k=0}^n {m-k\choose m-n}\\
&=m{m\choose m-n}-(m-n){m+1\choose m-n+1}\\
&=\frac{n}{m-n+1}{m\choose m-n}
\end{aligned}
$$

$$
\begin{aligned}
R_m=\sum_{k\leq m}{m-k\choose k}(-1)^k&=\sum_{k\leq m}{m-1-k\choose k}(-1)^k + \sum_{k\leq m}{m-1-k\choose k-1}(-1)^k\\
&=\sum_{k\leq m} {m-1-k\choose k}(-1)^k + \sum_{k+1\leq m}{m-2-k\choose k}(-1)^{k+1}\\
&=R_{m-1}+(-1)^{2m}-R_{m-2}-(-1)^{2(m-1)}=R_{m-1}-R_{m-2}
\end{aligned}
$$

