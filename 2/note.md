# 基础知识

## 概率论

条件概率：

$$\Pr[\alpha\cap\beta]=\Pr[\alpha]\Pr[\beta\mid\alpha]$$

由此有贝叶斯规则：

$$\Pr[\alpha\mid\beta]=\frac{\Pr[\beta\mid\alpha]\Pr[\alpha]}{\Pr[\beta]}$$

以背景事件$\gamma$为条件的贝叶斯规则：

$$\Pr[\alpha\mid\beta\cap\gamma]=\frac{\Pr[\beta\mid\alpha\cap\gamma]\Pr[\alpha\mid\gamma]}{\Pr[\beta\mid\gamma]}$$

最大后验概率：

$\mathrm{MAP}(W\mid e)=\mathrm{argmax}_wP(w,e)$



随机变量

对称性：

$(X\perp Y|Z)\Rightarrow (Y\perp X|Z)$

分解性：

$(X\perp Y,W|Z)\Rightarrow (X\perp Y|Z)$

弱联合：

$(X\perp Y,W|Z)\Rightarrow(X\perp Y|Z,W)$

收缩性：

$(X\perp W|Z,Y),(X\perp Y|Z)\Rightarrow (X\perp Y,W|Z)$



信息熵：

$H(X)=E\left[\log\frac{1}{\Pr[X]}\right]=\sum_x\Pr[x]\log\frac{1}{\Pr[X]}$

互信息：

$I(X:Y)=H(X)-H(X|Y)=E\left[\log\frac{\Pr[X|Y]}{\Pr[X]}\right]$

相对熵：

$D(P,Q)=E_P\left[\log\frac{P}{Q}\right]$

