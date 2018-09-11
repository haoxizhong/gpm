# 习题

## 2.1

1. $\because\varnothing\cap\Omega=\varnothing$

   $\therefore \Pr[\Omega]=\Pr[\varnothing\cup\Omega]=\Pr[\varnothing]+\Pr[\Omega]=1$

   $\therefore\Pr[\varnothing]=0$

2. 设$\gamma=\beta-\alpha$

   则$\gamma\cap\alpha=\varnothing$

   $\therefore\Pr[\beta]=\Pr[\alpha\cup\gamma]=\Pr[\alpha]+\Pr[\gamma]\geq\Pr[\alpha]$

3. $\Pr[\alpha\cup\beta]=\Pr[\alpha]+\Pr[\beta-(\alpha\cap\beta)]$

   $\because\Pr[\beta]=\Pr[\alpha\cap\beta]+\Pr[\beta-(\alpha\cap\beta)]$

   $\therefore\Pr[\alpha\cup\beta]=\Pr[\alpha]+\Pr[\beta]-\Pr[\alpha\cap\beta]$

## 2.2

1. $x^0\perp y^0\Rightarrow\Pr[x^0\cap y^0]=\Pr[x^0]\Pr[y^0]$

   则

   $\Pr[X=x^0,Y=y^0]=\Pr[X=x^0]\Pr[Y=y^0]$

   $$\begin{aligned}\Pr[X=x^1,Y=y^0]&=\Pr[X=x^1|Y=y^0]\Pr[Y=y^0]\\&=(1-\Pr[X=x^0|Y=y^0])\Pr[Y=y^0]\\&=(1-\Pr[X=x^0])\Pr[Y=y^0]\\&=\Pr[X=x^1]\Pr[Y=y^0]\end{aligned}$$

   同理可证其他情况。

2. 比如考虑$\Pr[X=x^i]=\frac{1}{3},\Pr[Y=y^i]=\frac{1}{3}(\forall0\leq i\leq2)$

   其中有 $x^0\perp y^0$。

   但是

   |         | $X=x^0$       | $X=x^1$       | $X=x^2$       |
   | ------- | ------------- | ------------- | ------------- |
   | $Y=y^0$ | $\frac{1}{9}$ | $\frac{1}{6}$ | $0$           |
   | $Y=y^1$ | $0$           | $\frac{1}{9}$ | $\frac{1}{6}$ |
   | $Y=y^2$ | $\frac{1}{6}$ | $0$           | $\frac{1}{9}$ |

   则$X\perp Y$不成立。

3. 否，假设$X,Y,Z$均为二值变量，且每个取值的概率均为$\frac{1}{2}$，那么可以构造如下数据

   |       | $XY=00$       | $XY=01$       | $XY=10$       | $XY=11$       |
   | ----- | ------------- | ------------- | ------------- | ------------- |
   | $Z=0$ | $\frac{1}{8}$ | $\frac{1}{8}$ | $\frac{1}{8}$ | $\frac{1}{8}$ |
   | $Z=1$ | $\frac{1}{4}$ | $0$           | $0$           | $\frac{1}{4}$ |

   则此时并不满足$X\perp Y|z^1$，所以没有$X\perp Y|Z$。

## 2.3

1. $\Pr[\alpha\cap\beta]_{\min}=0\Rightarrow\alpha\cap\beta=\varnothing$。
2. $\Pr[\alpha\cap\beta]_{\max}=\min(\Pr[\alpha],\Pr[\beta])\Rightarrow\alpha\subseteq\beta\text{ or }\beta\subseteq\alpha$。
3. $\Pr[\alpha\cup\beta]_{\min}=\max(\Pr[\alpha],\Pr[\beta])\Rightarrow\alpha\subseteq\beta\text{ or }\beta\subseteq\alpha$。
4. $\Pr[\alpha\cup\beta]_{\max}=\min(\Pr[\alpha]+\Pr[\beta],1)\Rightarrow\alpha$和$\beta$的交尽量小。

## 2.4

1. $\Pr[a|\alpha]=\frac{\Pr[a,\alpha]}{\Pr[\alpha]}\geq0$。
2. $\Pr[\Omega|\alpha]=\frac{\Pr[\Omega,\alpha]}{\Pr[\alpha]}=\frac{\Pr[\alpha]}{\Pr[\alpha]}=1$
3. $\Pr[a\cup b|\alpha]=\frac{\Pr[a\cup b,\alpha]}{\Pr[\alpha]}=\frac{\Pr[a,\alpha]+\Pr[b,\alpha]}{\Pr[\alpha]}=\Pr[a|\alpha]+\Pr[b|\alpha]$

## 2.5

TODO

## 2.6

1. 链式法则：

   $\sum_z\Pr(X,z|Y)=\sum_z\Pr(X|Y)\Pr[z|X,Y]=\Pr[X|Y]\sum_z\Pr[z|X,Y]=\Pr[X|Y]$

2. 条件概率：

   $\Pr[X|Y]=\frac{\Pr[X,Y]}{\Pr[Y]}=\frac{\sum_z\Pr[X,Y,z]}{\Pr[Y]}=\sum_z\frac{\Pr[X,Y,z]}{\Pr[Y]}=\sum_z\Pr[X,z|Y]$

## 2.7

1. 弱联合性：

   $(X\perp Y,W|Z)$

   $\Rightarrow \Pr[X,Y,W|Z]=\Pr[X|Z]\Pr[W,Y|Z]$

   $\Rightarrow\frac{\Pr[X,Y,W|Z]}{\Pr[W]}=\Pr[X|Z]\frac{\Pr[W,Y|Z]}{\Pr[W]}$

   $\Rightarrow\Pr[X,Y|W,Z]=\Pr[X|Z]\Pr[Y|W,Z]$

   由分解性可知，$(X\perp Y,W\mid Z)\Rightarrow(X\perp W\mid Z)$

   $\therefore  \Pr[X|Z]=\Pr[X|W,Z]$

   $\therefore \Pr[X,Y|W,Z]=\Pr[X|W,Z]\Pr[Y|W,Z]$

   $\therefore (X\perp Y\mid W,Z)$

   收缩性：

   $(X\perp Y\mid Z)\Rightarrow \Pr[X,Y\mid Z]=\Pr[X\mid Z]\Pr[Y\mid Z]$

   $(X\perp W\mid Z,Y)\Rightarrow\Pr[X,W\mid Z,Y]=\Pr[X\mid Z,Y]\Pr[W\mid Z,Y]=\Pr[X\mid Z]\Pr[W\mid Z,Y]$

   $\therefore \Pr[X,Y,W\mid Z]$

   $=\Pr[X,W\mid Z,Y]\Pr[Y\mid Z]$

   $=\Pr[X\mid Z]\Pr[W\mid Z,Y]\Pr[Y\mid Z]$

   $=\Pr[X|Z]\Pr[W,Y|Z]$

   $\Rightarrow(X\perp Y,W\mid Z)$

2. 相交性：

   $(X\perp Y\mid Z,W)\Rightarrow\Pr[X,Y|Z,W]=\Pr[X|Z,W]\Pr[Y|Z,W]\Rightarrow \Pr[X|W,Y,Z]=\Pr[X|Z,W]$

   $(X\perp W|Z,Y)\Rightarrow\Pr[X,W|Z,Y]=\Pr[X|Z,Y]\Pr[W|Z,Y]\Rightarrow \Pr[X|W,Y,Z]=\Pr[X|Z,Y]$

   $\therefore \Pr[X|Z,W]=\Pr[X|Z,Y]$

   $\Rightarrow \Pr[X|Z,W]\Pr[Y|Z]\Pr[W|Z]=\Pr[X|Z,Y]\Pr[Y|Z]\Pr[W|Z]$

   $\Rightarrow \Pr[X,W|Z]\Pr[Y|Z]=\Pr[X,Y|Z]\Pr[W|Z]$

   $\Rightarrow \sum_y\Pr[X,W|Z]\Pr[y|Z]=\sum_y\Pr[X,y|Z]\Pr[W|Z]$

   $\Rightarrow \Pr[X,W|Z]=\Pr[X|Z]\Pr[W|Z]$

   $\Rightarrow (X\perp W|Z)$

   同理 $(X\perp Y|Z)$

   $\Pr[X,Y,W|Z]$

   $=\Pr[X|Y,W,Z]\Pr[Y,W|Z]$

   $=\Pr[X|Z]\Pr[Y,W|Z]$

   $\Rightarrow(X\perp Y,W|Z)$

3. TODO

## 2.8

和2.2一模一样

## 2.9

1. $(X\perp Y,W|Z)\Rightarrow\Pr[X,Y,W|Z]=\Pr[X|Z]\Pr[Y,W|Z]$

   $\therefore \sum_w\Pr[X,Y,w|Z]=\Pr[X|Z]\Pr[Y,w|Z]$

   $\therefore\Pr[X,Y|Z]=\Pr[X|Z]\Pr[Y|Z]$

   $\therefore (X\perp Y|Z)$

2. TODO 错的，如下：

   |                   | $(W,Z)=(w_0,z_0)$ | $(W,Z)=(w_1,z_0)$ | $(W,Z)=(w_0,z_1)$ | $(W,Z)=(w_1,z_1)$ |
   | ----------------- | ----------------- | ----------------- | ----------------- | ----------------- |
   | $(X,Y)=(x_0,y_0)$ | $\frac{1}{8}$     | $0$               |                   |                   |
   | $(X,Y)=(x_1,y_0)$ |                   | $0$               |                   |                   |
   | $(X,Y)=(x_0,y_1)$ | $\frac{1}{8}$     | $0$               |                   |                   |
   | $(X,Y)=(x_1,y_1)$ |                   | $0$               |                   |                   |

3. TODO

4. TODO

## 2.10

1. 1. $\Pr[H|E_1,E_2]==\frac{\Pr[H,E_1,E_2]}{\Pr[E_1,E_2]}=\frac{\Pr[E_1,E_2|H]\Pr[H]}{\Pr[E_1E_2]}$

      但由于不知道$E_1,E_2$之间的关系，所以无法用$\Pr[E_1|H]$和$\Pr[E_2|H]$得出$\Pr[E_1,E_2|H]$。

      所以不行。

   2. $\Pr[H|E_1,E_2]=\frac{\Pr[H,E_1,E_2]}{\Pr[E_1,E_2]}=\frac{\Pr[E_1,E_2|H]\Pr[H]}{\Pr[E_1,E_2]}$

   3. 在逗我吗，这比第一个的信息还少，显然不行。

2. 如果是独立的，首先第一个和第二个肯定可以。

   第三个的话

   $\Pr[H|E_1,E_2]=\frac{\Pr[H,E_1,E_2]}{\Pr[E_1,E_2]}=\frac{\Pr[E_1,E_2|H]\Pr[H]}{\Pr[E_1,E_2]}$

   由于没有$\Pr[E_1,E_2]$的信息，所以仍然没法算。

## 2.11

$Var[X]=E[(X-E[X])^2]=E[X^2-2XE[X]+E[X]^2]=E[X^2]-2E[XE[X]]+E[E[X]^2]=E[X^2]-E[X]^2$

## 2.12

$E[X]=\sum_{x}\Pr[x]\cdot x=\sum_{x<t}\Pr[x]\cdot x+\sum_{x\geq t}\Pr[x]\cdot x\geq\sum_{x\geq t}\Pr[x]\cdot x\geq t\sum_{x\geq t}\Pr[x]=t\Pr[X\geq t]$

证毕

## 2.13

令 $Y=|X-E[X]|$

则 $\Pr[Y\geq t]=\Pr[Y^2\geq t^2]\leq\frac{E[Y^2]}{t^2}=\frac{Var(X)}{t^2}$

证毕

## 2.14

$E[Y]=E[aX+b]=aE[x]+b=a\mu+b$

$Var[Y]=Var[aX+b]=Var[aX]=a^2Var[x]=a^2\sigma^2$

证毕

## 2.15

1. 设$t=ax+(1-a)y$

   则 $f''(x)\leq 0$

   $\Rightarrow f'(a)<f'(b),\forall a<b$

   $\Rightarrow f(t)=f(x)+\int_x^tf'(a)da\geq f(x)+f'(t)(t-x)$

   $f(t)=f(y)-\int_t^yf'(a)da\geq f(y)-f'(t)(y-t)$

   $\Rightarrow f(t)\geq af(x)+(1-a)f(y)+f'(t)(t-ax-(1-a)y)=af(x)+(1-a)f(y)$

   反之，取$y=x+2\epsilon,t=x+\epsilon$，则

   $f''(x)=\frac{f(y)-2f(t)+f(x)}{\epsilon^2}=\frac{0.5f(x)+0.5f(y)-f(t)}{2\epsilon^2}\leq 0$。

   证毕。

2. $\log''(x)=-\frac{1}{x^2}\leq 0$

## 2.16

1. TODO。

   $H(X)=E\left[\log\frac{1}{\Pr[X]}\right]\leq\log E\left[\frac{1}{\Pr[X]}\right]$

2. $\Pr[x]\leq 1\Rightarrow H(X)=\sum_x\Pr[x]\log\frac{1}{\Pr[x]}\geq 0$。

3. 3

## 2.17

TODO

## 2.18

即要证明$H(X)\geq H(X|Y)$

    $H(X)-H(X|Y)=-E\left[\log\frac{\Pr[X]}{\Pr[X|Y]}\right]$

$\geq-\log E\left[\frac{\Pr[X]}{\Pr[X|Y]}\right]$

$=-\log\sum_{x,y}\Pr[x,y]\frac{\Pr[x]}{\Pr[x|y]}$

$=-\log\sum_{x,y}\Pr[x,y]\frac{\Pr[x]\Pr[y]}{\Pr[x,y]}$

$=0$

证毕  

## 2.19

1. 题目应该是写错了，应该是$H(X|Y,Z)$

   $H(X|Z)-H(X|Y,Z)$

   $=\sum_{x,y,z}\Pr[x,y,z]\left(\log\frac{1}{\Pr[x|z]}-\log\frac{1}{\Pr[x|y,z]}\right)$

   $=\sum{x,y,z}\Pr[x,y,z]\log\frac{\Pr[x|y,z]}{\Pr[x|z]}$

   $=E\left[\log\frac{\Pr[X|Y,Z]}{\Pr[X|Z]}\right]$

2. $I[X;Y]+I[X;Z|Y]=H[X]-H[X|Y]+H[X|Y]-H[X|Y,Z]=H[X]-H[X|Y,Z]=I[X;Y,Z]$

## 2.20

2.19+2.18

## 2.21

不想做，TODO

## 2.22

深度优先搜索的过程中，把当前在栈里面的点标记一下，就行。

## 2.23

题目要求算法构造链分支的话，那其实随便瞎搞就行了。

首先把所有无向边连的点进行合并（并查集）。

新图只有有向边，那直接top排序。

然后按照top序和并查集，再把点全部展开，就是答案了。