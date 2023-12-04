---
{"dg-publish":true,"permalink":"/econometrics/","dgPassFrontmatter":true}
---

# Current
Instructor: Prof. Merrick LI Office: ELB 935 Email: merrickli@cuhk.edu.hk 
TA: Wei XU Email: weixu@link.cuhk.edu.hk
1. Class participation: 5%  
2. Midterm Exam: 35% 
3. Final Exam: 60%
```
D:\All Document\Msc\Econometric
```
Mid-term: 27 Oct, venue LSK–LT1(李兆基楼), 13:30—15:30 
Final exam: 11 Dec, venue ELB–LT4, 9:30—12:00
Tutorials Arrangement: Every Wednesday, 14:30 — 16:00, from 13 Sep to 6 Dec, except for 11 Oct
Venue: Science Centre LT 3 (1/F)

|   |   |
|---|---|
|Lecture|Date  <br>Every Wednesday, 2:30 PM - 4:15 PM  <br>Venue: Science Centre SC_L3 (1/F)|
|T1|13 Sep 2023|
|T2|20 Sep 2023|
|T3|27 Sep 2023|
|T4|4 Oct 2023|
|T5|18 Oct 2023|
|T6|25 Oct 2023|
|T7|1 Nov 2023|
|T8|8 Nov 2023|
|T9|15 Nov 2023|
|T10|22 Nov 2023|
|T11|29 Nov 2023|
|T12|6 Dec 2023|

Programming and data
1. Cameron, Colin and Pravin Trivedi. 2009. _Microeconometrics Using Stata_
2. Cunningham, Scott. Causal inference: _The mixtape_. Yale university press, 2021

## Review of Probability, Statistics and Simple Linear Regression
Variance is used to measure the deviation from the mean:
$$\mathbf{Var}(G)=\mathbb{E}((G-\mathbb{E}(G))^2)$$
The probability density function (pdf) will be used to calculate probabilities, expectation, variance, etc., of the continuous random variable

Here is the pdf of a normal random variable $X$ with mean $µ$ and variance $σ^2$
$$f(x)=\frac{1}{\sqrt{2\pi\sigma^2}}exp(-\frac{(x-\mu)^2}{2\sigma^2})$$
$$\mathbb{E}(X)=\int^{\infty}_{-\infty}f(x)xdx=\mu$$
$$\mathbf{Var}(X)=\int^{\infty}_{-\infty}f(x)(x-\mu)^2dx=\sigma^2$$

Let $X$ be a random variable with mean $µ_X$ and variance $σ^2_X$, let a and b be two constants and  $Y=a+bX$, then
$$\mathbb{E}(Y)=a+b\mu_X,Var(Y)=b^2\sigma^2_X$$
as a consequence, a random variable can be transformed into a random variable with mean 0 and variance 1
Let $Y=\frac{X-\mu_X}{\sigma_X}$, then
$$\mathbb{E}(Y)=0,\quad\mathbf{Var}(Y)=1$$

In a discrete setting, we work with the joint pmf(Probability mass function), that is, $P(X=i.Y=j)$
In a continuous setting, we work with the joint pdf(Probability Desnsity Function), that is, $f(x,y)$

$X,Y$ are independent of each other if for any constants $a,b,c,d$
$$\mathbb{P}(a\leq X\leq b,c\leq Y\leq d)=\mathbb{P}(a\leq X\leq b)\mathbb{P}(c\leq Y \leq d)$$
Then,
$$\mathbb{P}(X=i,Y=j)=\mathbb{P}(X=i)\mathbb{P}(Y=j),f(x,y)=f(x)f(y)$$
As a consequence, for any function $f,g$, we have
$$\mathbb{E}(f(X)g(Y))=\mathbb{E}(f(X))\mathbb{E}(g(Y))$$

Let’s consider an example. 
	1. You toss a coin twice 
	2.  Let $X$ be the result of the first flip: $X = 1$ if you get a head and $X = 0$ if you get a tail 
	3.  $Y$ is the result of the second flip and is similarly defined 
	4.  $X$ and $Y$ are independent flips
	5. $Z=X+Y$
We can evaluate the conditional expectation (CE)
$$\begin{align}
\mathbb{E}(Z|X=1)=&0\times\mathbb{P}(Z=0|X=1)+1\times\mathbb{P}(Z=1|X=1)\\
&+2\times \mathbb{P}(Z=2|X=1)\\
&=\frac{3}{2}
\end{align}$$
You can verify that $\mathbb{E}(Z|X=0)=\frac{1}{2}$, and you may note that the CE depends on the conditioned value of $X$
$$\begin{align}\mathbb{E}(Z)&=\mathbb{E}(Z|X=0)\mathbb{P}(X=0)+\mathbb{E}(Z|X=1)\mathbb{P}(X=1)\\
&=\frac{3}{2}\times\frac{1}{2}+\frac{1}{2}\times\frac{1}{2}\\
&=1\\
\mathbb{E}(Z)&=\mathbb{E}(Z|X=0)\mathbb{P}(X=0)+\mathbb{E}(Z|X=1)\mathbb{P}(X=1)
\end{align}$$
### Law of Iterated Expectation


The right hand side is in fact the probability weighting of CE, thus equal to $\mathbb{E}(\mathbb{E}(Z|X))$; this the **Law of iterated expectation**:
$$\mathbb{E}(\mathbb{E}(Z|X))=\mathbb{E}(Z)$$
$$\mathbb{E}\{\mathbb{E}(Z|X,Y)|X\}=\mathbb{E}(Z|X)$$
$$\mathbb{E}\{\mathbb{E}(Z|X,Y)|Y\}=\mathbb{E}(Z|Y)$$
{ #LawIteratedExp}


$$\begin{align}&min\ \mathbb{E}((Y-m(X))^2)\\
&=\mathbb{E}[Y-\mathbb{E}(Y|X)+\mathbb{E}(Y|X)-m(X)]^2\\
&=\mathbb{E}\big[(Y-\mathbb{E}(Y|X))^2+(\mathbb{E}(Y|X)-m(X))^2+\cancel{2(Y-\mathbb{E}(Y|X))(\mathbb{E}(Y|X)-m(X))}\big]
\end{align}$$

The covariance of two random variables $X, Y$ is given by
$$\mathbf{Cov}(X,Y)=\mathbb{E}\Big((X-\mathbb{E}(X))(Y-\mathbb{E}(Y))\Big)$$
The correlation of two random variables $X, Y$ is given by
$$\mathbf{corr}(X,Y)=\frac{\mathbf{Cov}(X,Y)}{\sqrt{\mathbf{Var}(X)\mathbf{Var}(Y)}}$$
We always have $-1\leq \mathbf{corr}(X,Y)\leq 1$

$X,Y$ are uncorrelated if $\mathbf{Cov}(X,Y)=0$
If $X,Y$ are independent, then
$$\begin{array}
\mathbf{Cov}(X,Y)&=&\mathbb{E}((X-\mathbb{E}(X))(Y-\mathbb{E}(Y)))\\
&=&\mathbb{E}(X-\mathbb{E}(X))\mathbb{E}(Y-\mathbb{E}(Y))=0
\end{array}$$

For constants $a, b$ and random variables $X, Y, Z$ we have
$$\mathbf{Cov}(aX+bY,Z)=a\mathbf{Cov}(X,Z)+b\mathbf{Cov}(Y,Z)$$
For two random variables $X, Y$ , we have
$$\mathbf{Var}(X+Y)=\mathbf{Var}(X)+\mathbf{Var}(Y)+2\mathbf{Cov}(X,Y)$$
So if $X, Y$ are uncorrelated or independent, we have
$$\mathbf{Var}(X+Y)=\mathbf{Var}(Y)+\mathbf{Var}(Y)$$


## Experiments and Casual Effects
let the health status of individual $i$ be $H(T_i,X_i)$, a function of
- $T_i$: Hospital treatment, where $T=0$ represents no treatment and $T=1$ indicates treatment received
- $X_i$: Other determinants of health, excluding hospital treatment

For any individual $i$, we define the potential outcome by $H_{1i}=H(1,X_i),H_{0i}=H(0,X_i)$

In a compact expression: $H_i=H_{0i}+(H_{1i}-H_{0i})T_i$

We have a bias equal to $\mathbb{E}(H_{0i}|T_i=1)-\mathbb{E}(H_{0i}|T_i=0)$, which is called the selection bias
Selection bias often appears in nonexperimental data

Random assignment (RA) of the treatment $T_i$ solves the selection bias issue, because under random assignment, $T_i\perp H_{0i}$

### Regression Analysis
#### Properties of the Conditional Expectation Function
The following theorem says that given a (group of) variable(s) $x$, any random variable $y$ can be decomposed into two parts: a part that can be “explained” by $x$ and a part that is “orthogonal” to (any function of) $x$:
**Theorem**
The CEF-Decomposition Property
We have $y=\mathbb{E}(y|\mathbf{x})+\varepsilon$, where $(i)\ \mathbb{E}(\varepsilon|\mathbf{x})=0$; $(ii)\ \mathbb{E}(\varepsilon g(\mathbf{x}))=0$ for any function $g$ of $\mathbf{x}$
	Proof $(i)\ \varepsilon=y-E(y|x)=E(y|x)-E[E(y|x)|x]=E(y|x)-E(y|x)=0$ [[Econometrics#Law of Iterated Expectation\|Law of iterated expectation]]
		In addition, this means $\varepsilon_i$ is uncorrelated with any function of $X_i$
		Let $h(X_i)$ be any function of $X_i$. By the law of iterated expectations, $E[h(X_i)\varepsilon_i]=E\{h(X_i)E[\varepsilon_i|X_i]\}$ and by mean-independence, $E\{\varepsilon_i|X_i\}$
	$(ii)\ \mathbb{E}(\varepsilon g(x))\mathop{\Rightarrow}\limits^{Law\ of\ itereated\ expectation} \mathbb{E}\{\mathbb{E}[\varepsilon g(x)|x]\}\mathop{\Rightarrow}\limits^{E[E[xy|x]]=E[xE[y|x]]} \mathbb{E}\{g(x)\mathbb{E}(\varepsilon|x)\}\mathop{=}\limits^{\mathbb{E(\varepsilon|x)}=0}0$ 
		$E[E[xy|x]]=E[xE[y|x]]$ can be [proved](https://stats.stackexchange.com/questions/530324/conditional-expectation-how-is-eexyx-exeyx), but I don't understand right now 

The CEF-Prediction Property
Let $p(x)=\mathbb{E}(y|x)$, and $g$ is any function of $x$, then
$$\mathbb{E}((y-p(x))^2)\leq \mathbb{E}((y-g(x))^2)$$
That is, $p(x)$ solves the minimization problem
$$\mathop{min}\limits_g\ \mathbb{E}((y-g(x))^2)$$
	Proof:
$$\begin{align}
(Y_i-g(X_i))^2=&\big((Y_i-E[Y_i|X_i])+(E[Y_i|X_i]-g(X_i))\big)^2\\
=&(Y_i-E[Y_i|X_i])^2+2(E[Y_i|X_i]-g(X_i))(Y_i-E[Y_i|X_i])\\
&+(E[Y_i|X_i]-g(X_i))^2
\end{align}$$
	The first term doesn't matter because it doesn't involve $g(X_i)$. The second term can be written $h(X_i)\varepsilon$, where $h(X_i)\equiv 2(E[Y_i|X_i]-g(X_i))$, and therefore has expectation zero by the CEF-decomposition property($\mathbb{E}(\varepsilon g(\mathbf{x}))=0$). The last term is minimized at zero when $g(X_i)$ is CEF

#### Uncorrelated
If $E(X|Y)$ is 0 then $X,Y$ are uncorrelated  
	Proof: $E[E(X|Y)]=E(X)=E(0)=0$
	$E[XY]=E[E[XY|Y]]=E[Y\cdot E[X|Y]]$ according to 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/econometrics/#an-important-property" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

$<div class="markdown-embed-title">

# this property

</div>


#### An important property
$E[E[xy|x]]=E[xE[y|x]]$ can be [proved](https://stats.stackexchange.com/questions/530324/conditional-expectation-how-is-eexyx-exeyx), but I don't understand right now  


</div></div>

	$E[Y\cdot E[X|Y]]=E[Y\cdot 0]=E[0]=0$
	$Cov(X,Y)=E[XY]-E[X]E[Y]$ according to [[Econometrics#Analysis of variance (ANOVA)\|#Analysis of variance (ANOVA)]] 
	$E[X]=0$ and $E[XY]=0$
	Thus, $Cov(X,Y)=0$
{ #Uncorrelation}


#### An important property
$E[E[xy|x]]=E[xE[y|x]]$ can be [proved](https://stats.stackexchange.com/questions/530324/conditional-expectation-how-is-eexyx-exeyx), but I don't understand right now 
{ #ImportantP}



#### Analysis of variance (ANOVA)
$\mathbf{Var}(y)=\mathbf{Var}(\mathbb{E}(y|x))+\mathbb{E}(\mathbf{Var}(y|x))$
	Theorem: $Cov(X,Y)=E(XY)-E(X)E(Y)$ [Proof](https://www2.econ.osaka-u.ac.jp/~tanizaki/class/2012/econome1/05.pdf#:~:text=Theorem%3A%20Cov%28Y%29%20E%28XY%29%20E%28X%29E%28Y%29.%20X%2C%20%3D%20%E2%88%92%20Proof%3A,E%28%3D%20XY%20%E2%88%92%20%CE%BCxY%20%E2%88%92%20%CE%BCyX%20%2B%20%CE%BCx%CE%BCy%29)
	Proof $y=E(y|x)+\varepsilon\Rightarrow Var(y)=Var(E(y|x)+\varepsilon)=Var(E(y|x))+Var(\varepsilon)+2Cov(E(y|x),\varepsilon)$
	$Cov(E(y|x),\varepsilon)=E(\varepsilon\cdot E(y|x))-E(E(y|x))E(\varepsilon)=0$
	Since $\mathbb{E}(\varepsilon g(x))=0$ and $E(\varepsilon)=0$
	$Var(\varepsilon)=Var(y-E(y|x))=\mathbb{E}\{[y-\mathbb{E}(y|x)]^2\}\mathop{=}\limits^{Law\ of\ iterated\ expectation}\mathbb{E}\{\mathbb{E}[(y-\mathbb{E}(y|x))^2|x]\}$
		$Var(Y|X)=E((Y-E(Y|X))^2|X)$ [Definition of Conditional variance](https://en.wikipedia.org/wiki/Conditional_variance)
	Therefore, $Var(y)=\mathbf{Var}(\mathbb{E}(y|x))+\mathbb{E}(\mathbf{Var}(y|x))$
{ #ANOVA}


10.26 [Definition of Variance](https://www.kellogg.northwestern.edu/faculty/weber/decs-433/Notes_4_Random_variability.pdf) $Var[X]=E\Big[\big(X-E(X)\big)^2\Big]=E[X^2]-(E[X])^2$

Now suppose $\mathbf{x}$ is a $K$ vector
We would like to investigate the minimization problem in $(1):\ \mathop{min}\limits_g\ \mathbb{E}((Y_i-g(x))^2)$
But we only consider linear functions
$g(\mathbf{x})=\mathbf{x}^T\beta$, $\beta$ is a $K\times 1$ vector
$$\mathop{min}\limits_\beta\ \mathbb{E}\big((Y_i-\mathbf{x}_i^T\beta)^2\big)$$
First order condition yields: 
$$E[\mathbf{X}_i(Y_i-\mathbf{X}_i^T\beta)]=0$$
Suppose $\mathbb{E}(\mathbf{x_i x^T_i})$ is invertible, we have
$$\beta=\mathbb{E}[\mathbf{x_i x_i^T}]^{-1}\mathbb{E}[\mathbf{x}_iy_i]$$
#### BetaOneEstimation
Exercise 
Let $\mathbf{x}=[1,x]^T,\beta=[\beta_0,\beta_1]$. Use $(3)$ to show $\beta_0,\beta_1$ satisfy $\beta_0+\beta_1\mathbb{E}(x)=\mathbb{E}(y);\beta_1=\mathbf{Cov}(y,x)/\mathbf{Var}(x)$ 
	$\mathbf{x}=[1,x]^T$ 有个1是因为有常数项
	$\begin{align}Var(x)&=E[(x-E(x))^2]\\ &=E[x^2-2xE(x)+E^2(x)]\\ &=E(x^2)-2E(x)\cdot E[E(x)]+E[E^2(x)]\\ &=E(x^2)-2E^2(x)+E^2(x)\\ &=E(x^2)-E^2(x)\end{align}$
	$\begin{align}\mathbf{Cov}(y,x)&=E(xy)-E(x)E(y)\\ &=E(x(\beta_1 x+\beta_0))-E(x)E(\beta_1 x+\beta_0)\\ &=E(\beta_1 x^2+\beta_0 x)-E(x)[E(\beta_1 x)+E(\beta_0)] \\&=\beta_1E(x^2)+\beta_0E(x)-\beta_1E^2(x)-\beta_0E(x)\\ &=\beta_1[E(x^2)-E^2(x)] \end{align}$
	$\therefore \beta_1=\mathbf{Cov}(y,x)/\mathbf{Var}(x)$
	----
	$\begin{align}\beta &=\mathbb{E}\left[\begin{array}{11} 1&x\\ x&x^2 \end{array}\right]^{-1} \mathbb{E}\left[\begin{array}{11} y\\ xy \end{array}\right]\\ &=\left[\begin{array}{11} 1&E(x)\\ E(x)&E(x^2) \end{array}\right]^{-1}\left[\begin{array}{11} E(y)\\ E(xy) \end{array}\right]\\ &=\frac{1}{E(x^2)-E^2(x)}\left[\begin{array}{11} E(x^2)&-E(x)\\ -E(x)&1 \end{array}\right]\left[\begin{array}{11} E(y)\\ E(xy) \end{array}\right]\\ &=\frac{1}{E(x^2)-E^2(x)}\left[\begin{array}{11} E(x^2)E(y)-E(x)E(xy)\\-E(x)E(y)+E(xy)  \end{array}\right]  \end{align}$
	$\beta_0=\frac{E(x^2)E(y)-E(x)E(xy)}{E(x^2)-E^2(x)}\ \beta_1=\frac{-E(x)E(y)+E(xy)}{E(x^2)-E^2(x)}$
	$\therefore \beta_0+\beta_1\mathbb{E}(x)=\mathbb{E}(y)$ 
{ #Beta1Estimation}


In the simple bivariate case where the regression vector includes only the single regressor, $x_i$ , and a constant, the slope coefficient is $\beta_1=\frac{Cov(Y_i,x_i)}{V(x_i)}$


Regression Anatomy
$$\beta_k=\frac{\mathbf{Cov}(y,\tilde{x}_{ki})}{\mathbf{Var}(\tilde{x}_{ki})}$$
where $\tilde{x}_{ki}$ is the residual from a regression of $x_{ki}$ on all the other covariates.
$$x_{ki}=\alpha+\beta_1x_{1i}+\dots+\beta_{k-1}x_{(k-1)i}+\beta_{k+1}x_{(k+1)i}+\cdots+\beta_Kx_{Ki}+\tilde{x}_{ki}$$

Note that all the above analysis is based on the population properties of some random variable $(y)$ and random vectors $(\mathbf{x})$
$\beta=\mathbb{E}[\mathbf{x_i x_i^T}]^{-1}\mathbb{E}[\mathbf{x}_iy_i]\Leftrightarrow \hat{\beta}=(\frac{1}{n}\sum\limits^n_{i=1}\mathbf{x}_i\mathbf{x}_i^T)^{-1}\frac{1}{n}\sum\limits^n_{i=1}\mathbf{x}_iy_i$
We use the method of moments: replacing $\mathbb{E}(\cdot)$ by sample average $\frac{1}{n}\sum\limits^n_{i=1}\mathbf{x}_i y_i$
The estimator of $\beta$ is
$$\hat{\beta}=(\sum\limits^n_{i=1}\mathbf{x}_i\mathbf{x}_i^T)^{-1}\sum\limits^n_{i=1}\mathbf{x}_iy_i$$

**SLUTSKY‘S THEOREM** 
1. Consider the sum of two random variables, one of which converges in distribution and the other converges in probability to a constant: the asymptotic distribution of this sum is unaffected by replacing the one that converges to a constant by this constant. Formally, let $a_N$ be a statistic with a limiting distribution and let $b_N$ be a statistic with probability limit $b$. Then $a_N +b_N$ and $a_N +b$ have the same limiting distribution. 
2. Consider the product of two random variables, one of which converges in distribution and the other converges in probability to a constant: the asymptotic distribution of this product is unaffected by replacing the one that converges to a constant by this constant. This allows us to replaces some sample moments by population moments (i.e., by their probability limits) when deriving distributions. Formally, let $a_N$ be a statistic with a limiting distribution and let $b_N$ be a statistic with probability limit $b$. Then $a_Nb_N$ and $a_N b$ have the same asymptotic distribution.

**The Continuous Mapping Theorem**
Probability limits pass through continuous functions. For example, the probability limit of any continuous function of a sample moment is the function evaluated at the corresponding population moment. Formally, the probability limit of $h(b_N)$ is $h(b)$ where $plim$ $b_N = b$ and $h(\cdot)$ is continuous at b.

$plim$ -- 依概率收敛于

Note that $\hat{β}$ can also be obtained via the least square approach
$$\hat{\beta}=\beta+[\sum\mathbf{x_i}\mathbf{x_i}^T]^{-1}\sum\limits x_i e_i$$
	Proof:
	$\hat{\beta}=(\sum\limits^n_{i=1}\mathbf{x}_i\mathbf{x}_i^T)^{-1}\sum\limits^n_{i=1}\mathbf{x}_i(\mathbf{x}_i\beta+\varepsilon)=(\sum\mathbf{x}_i\mathbf{x}'_i)^{-1}(\sum\mathbf{x}_i\mathbf{x}'_i)\beta+(\sum\mathbf{x}_i\mathbf{x}'_i)^{-1}\sum \mathbf{x}_i\varepsilon_i=\beta+[\sum\mathbf{x_i}\mathbf{x_i}^T]^{-1}\sum\limits x_i \varepsilon_i$

The asymptotic distribution of $\sqrt{n}(\hat{\beta}-\beta)$ is of interest:
$$\sqrt{n}(\hat{\beta}-\beta)=n(\sum^n_{i=1}\mathbf{x}_i\mathbf{x}_i)^{-1}\frac{1}{\sqrt{n}}\sum\limits^n_{i=1}\mathbf{x}_i\varepsilon_i$$
By the Slutsky theorem, this has the same asymptotic distribution as $E[X_iX'_i]^{-1}\frac{1}{\sqrt{N}}\sum X_ie_i$. Since $E[X_i e_i]=0,\frac{1}{\sqrt{n}}\sum X_i e_i$ is a root-N-normalized and centered sample moment. By the central limit theorem, this is asymptotically Normally distributed with mean zero and covariance matrix $E[X_iX'_i e^2_i]$, since this fourth moment is the covariance matrix of $X_ie_i$.
Therefore, $\hat{\beta}$ has an asymptotic Normal distribution, with probability limit $\beta$, and covariance matrix
$$E[X_iX'_i]^{-1}E[X_iX'_ie^2_i]E[X_iX'_i]^{-1}$$
==这部分没懂==

The standard errors used to construct t-statistics are the square roots of the diagonal elements of this matrix. In practice these standard errors are estimated by substituting sums for expectations, and using the estimated residuals $\hat{e}_i=Y_i-X_i\hat{\beta}$ to form the empirical fourth moment, $\sum[X_iX_i\hat{e}^2_i]/N$  

Asymptotic standard errors computed in this way are known as **heteroskedasticity-consistent standard errors**, White (1980a) standard errors, or Eicker-White standard errors in recognition of Eickerís (1967) derivation.
These standard errors are said to be robust because, in large enough samples, they provide accurate hypothesis tests and confidence intervals given minimal assumptions about the data and model.
Default standard errors are derived under a homoskedasticity assumption, specifically, that $E[e^2_1|X_i]=\sigma^2$, a constant. Given this assumption, we have
$$E[X_iX'_ie^2_i]=E(X_iX'_iE[e^2_i|X_i])=\sigma^2 E[X_iX'_i]$$
by iterating expectations. The asymptotic covariance matrix of $\hat{\beta}$ then simplifies to
$$\begin{align}
E[X_iX'_i]^{-1}E[X_iX'_ie^2_i]E[X_iX'_i]^{-1}&=E[X_iX'_i]^{-1}\sigma^2 E[X_iX'_i]E[X_iX'_i]^{-1}\\&=E[X_iX'_i]^{-1}\sigma^2
\end{align}$$
#### Residual Variance
Even if you are prepared to assumed that the conditional variance of $y_i$ given $X_i$ is constant, the fact that the CEF is nonlinear means that $E[(y_i-X'_i\beta)^2|X_i]$ will vary with $X_i$.
$$\begin{align}
E[(y_i-X'_i\beta)^2|X_i]&=E\Big\{\big[(y_i-E[y_i|X_i])+(E[y_i|X_i]-X'_i\beta)\big]^2|X_i\Big\}
\\
&=V[y_i|X_i]+(E[y_i|X_i]-X'_i\beta)^2
\end{align}$$
	9/10/2023 note: 这个$i$ 代表有$i$ 组数据构成一个sample, 所以有$i$个$y$和$i$个Independent variable组合，$X$ 中具体有几个independent variable是不知道的。
Therefore, even if $V[y_i|X_i]$ is constant, the residual variance increases with the square of the gap between the regression line and the CEF, a fact noted in White (1980b).
{ #ResidualVariance}


In additon [Conditional variance](https://en.wikipedia.org/wiki/Conditional_variance) 
	The conditional variance of a random variable _Y_ given another random variable _X_ is
	$Var(Y|X)=E\Big(\big(Y-E(Y|X)\big)^2|X\Big)$
#### Saturated Models, Main Effects, and Other Regression Talk
Saturated regression models are regression models with discrete explanatory variables, where the model includes a separate parameter for all possible values taken on by the explanatory variables.
For example, when working with a single explanatory variable indicating whether a worker is a college graduate, the model is saturated by including a single dummy for college graduates and a constant. We can also saturate when the regressor takes on many values. Suppose, for example, that $s_i = 0, 1, 2,\dots,\tau$ . A saturated regression model for $s_i$ is
$$y_i=\beta_0+\beta_1 d_{1i}+\beta_2 d_{2i}+\dots+\beta_{\tau}d_{\tau i}+\varepsilon_i$$

If there are two explanatory variables, say one dummy indicating college graduates and one dummy indicating sex, the model is saturated by including these two dummies, their product, and a constant.
The coefficients on the dummies are known as **main effects**, while the product is called an **interaction term**.
An alternative saturated model includes dummies for male college graduates, male dropouts, female college graduates, and female dropouts, but no intercept.

Note that there is a natural hierarchy of modeling strategies with saturated models at the top. It's natural to start with a saturated model because this fits the CEF. 
On the other hand, saturated models generate a lot of interaction terms, many of which may be uninteresting or imprecise. 
You might therefore sensibly choose to omit some or all of these. 

Exercise
Show that $\mathbb{E}(\varepsilon^2|\mathbf{x})=\mathbf{Var}(y|\mathbf{x})+(\mathbb{E}(y|\mathbf{x})-\mathbf{x}'\beta)^2$
[[Econometrics#Residual Variance\|Solution]]

### Regression and Causality
When can we think of a regression coefficient as approximating the causal effect that might be revealed in an experiment?

#### The Conditional Independence Assumption
##### From textbook
This leads to the conditional independence assumption (CIA), a core assumption that provides the (sometimes implicit) justification for the causal interpretation of regression.

The CIA asserts that conditional on observed characteristics, $X_i$ , selection bias disappears. In this example, the CIA says,==下面这个式子啥意思== ppt上是正交，书上打错了
$$ \{\mathrm{Y}_{0i},\mathrm{Y}_{1i}\}\perp\mathrm{C}_i|\mathrm{X}_i. $$
Given the CIA, conditional-on-$X_i$ comparisons of average earnings across schooling levels have a causal interpretation. In other words,
$$E[Y_i|X_i,C_i=1]-E[Y_i|X_i,C_i=0]=E[Y_{1i}-Y_{0i}|X_i]$$

Regression provides an easy-to-use empirical strategy that automatically turns the CIA into causal effects.
In fact, regression can be seen as a particular sort of matching estimator, capturing an average causal effect much like 3.2.3 or 3.2.5. ==这个结论不是很懂==

Because mean-independence implies orthogonality, the residual in the linear causal model
$$y_i=\alpha+\rho s_i+X'_i\gamma+v_i$$
is uncorrelated with the regressors, $s_i$ and $X_i$ , and the regression coefficient $\rho$ is the causal effect of interest.
==这一张还要重看==

##### From PPT
$y_{1i}-y_{0i}$ is not observable;  only one of $y_{0i}$ and $y_{1i}$ can be observed
What we can observe is $\mathbb{E}(y_i|c_i=1)-\mathbb{E}(y_i|c_i=0)$, which is equal to $\mathbb{E}(y_{1i}|c_i=1)-\mathbb{E}(y_{0i}|c_i=1)$
A further decomposition yields:
- The treatment on the treated: $\mathbb{E}(y_{1i}-y_{0i}|c_i=1)$
- The selection bias: $\mathbb{E}(y_{0i}|c_i=1)-\mathbb{E}(y_{0i}|c_i=0)$

Similar to the hospital treatment analysis, we let $y_{0i}=S(0,\mathbf{X}_i),y_{1i}=S(1,\mathbf{X}_i)$
$\mathbf{X}_i$ are all the factors that may affect earnings except college degree $c_i$
$\{y_{0i},y_{1i}\}\perp c_i$ implies $c_i \perp \mathbf{X}_i$, too strong
Some part of $\mathbf{X}_i$, say $\mathbf{x}_i$ is dependent with $c_i$, e.g., ability, parents education levels
Divide $\mathbf{X}_i=\mathbf{x}_i \cup \varepsilon_i$, we hope $c_i\perp \varepsilon_i$

If we are happy with the assumption that $\{y_{0i},y_{1i}\}\perp c_i$ the bias disappears
A more reasonable assumption than $\{y_{0i} , y_{1i}\} \perp c_i$ is the conditional independence assumption (CIA):
$$\{y_{0i},y_{1i}\}\perp c_i|x_i$$
where $x_i$ represents such characteristics
	Explanation by CJT:
	$y_{0i}\perp c_i\Rightarrow E(y_{0i}|c_i=1)=E(y_{0i}|c_i=0)$
	$y_{1i}\perp c_i\Rightarrow E(y_{1i}|x_i=1)=E(y_{1i}|x_i=0)$ (这个还没有完全看懂)
Under CIA, the observed difference is
$$\mathbb{E}(y_i|\mathbf{x}_i,c_i=1)-\mathbb{E}(y_i|\mathbf{x}_i,c_i=0)=\mathbb{E}(y_{1i}-y_{0i}|\mathbf{x}_i)$$
Selection bias is eliminated

Let’s consider some “continuous” schooling effect
Let $Y_{si}=S(s,\mathbf{x}_i,\varepsilon_i)$ be the potential earnings if individual $i$ receives $s$ years of education
In real data, we only observe $Y_i := Y_{s_i i}$

Thus, conditional on $\mathbf{x}_i$, the average casual effect of one-year increase in education (from $s-1$ to $s$) is 
The CIA for this general setup is
$$Y_{si}\perp s_i| \mathbf{x}_i, \forall s$$
After controlling for $x_i$ , the assignment rule $s_i$ will be independent of all potential outcomes

Given the CIA assumption, how can we recover $\mathbb{E}(Y_{si}-Y_{(s-1)i}|\mathbf{x}_i)$ using observed data $(Y_i,\mathbf{x}_i,s_i)_i$ for a school level $s$?


==这一部分其实也没怎么懂==

$$\begin{align}
\delta_{tot}&=E(Y_i|X_i,D_i=1)-E(Y_i|X_i,D_i=0)\\
&=E(Y_{1i}|X_i,D_i=1)-E(Y_{0i}|X_i,D_i=0)\\
&=E(Y_{1i}-Y_{0i}|X_i,D_i=1)
\end{align}$$
Let $δ_{tot}$ be the treatment effect on treated:
$$\delta_{tot}=\mathbb{E}(Y_{1i}-Y_{0i}|D_i=1)$$
Let $\delta_{x_i}:=\mathbb{E}(Y_i|x_i,D_i=1)-\mathbb{E}(Y_i|x_i,D_i=0)$ be the differences in average earnings brought by the veteran status given the characteristics $x_i$ (e.g., year of birth, education, application year to the military, etc.)

Exercise
show that $\delta_{tot}=\mathbb{E}(\delta_{x_i}|D_i=1)$ under CIA
- Solution:
- $\delta_{tot}=\mathbb{E}(Y_{1i}-Y_{0i}|D_i=1)$
- $\delta_{x_i}:=\mathbb{E}(Y_i|x_i,D_i=1)-\mathbb{E}(Y_i|x_i,D_i=0)$
- According to CIA,
- $\mathbb{E}(Y_i|x_i,D_i=0)=\mathbb{E}(Y_i|x_i,D_i=1)$
- Therefore, $\delta_{x_i}:=\mathbb{E}(Y_i|x_i,D_i=1)-\mathbb{E}(Y_i|x_i,D_i=1)=\mathbb{E}(Y_{1i}-Y_{0i}|x_i,D_i=1)$
- According to [[Econometrics#Law of Iterated Expectation\|Law of Iterated Expectation]]
- $\delta_{tot}=\mathbb{E}\Big(\mathbb{E}(Y_{1i}-Y_{0i}|x_i,D_i=1)|D_i=1\Big)=\mathbb{E}(\delta_{x_i}|D_i=1)$

#### The Omitted Variables Bias Formula
Now consider the previous regression model but with $x_i$ being a scale variable $x_i : Y_i=\alpha+\rho s_i+\beta x_i+\varepsilon_i$
Suppose we do not include $x_i$ in the regression model (either because xi is not available or we are not aware of it) 
We proceed with $Y_i=\alpha'+\rho' s_i+\varepsilon'_i$

Then, we have
$\mathbf{Cov}(Y_i,s_i)=\rho' \mathbf{Var}(s_i)=\rho \mathbf{Var}(s_i)+\mathbf{Cov}(\beta x_i,s_i)$That is,
$$\rho'=\rho+\frac{\beta \mathbf{Cov}(x_i,s_i)}{\mathbf{Var}(s_i)}$$
$\frac{\beta Cov(x_i,s_i)}{Var(s_i)}$ is the omitted variable bias (OVB)
10.27 midterm Can be proved by FOC of OLS

Consider the general regression model: 
$Yi =α+ρs_i+\mathbf{x}'_iβ+ε_i$ 
If there are some omitted variables, they are hiding in $ε_i$ , making εi correlated with $s_i$
If we can include the omitted variables or their proxies, the correlation will disappear 
The regression model then has a causal effect

Exercise
Use the regression anatomy principle to explain that if $\mathbf{Cov}(x_i,s_i)=0$, we have $\rho=\rho'$
	Solution:
	Regression anatomy implies $\rho=\frac{\mathbf{Cov}(Y_i,e_i)}{\mathbf{Var}(e_i)}$, where $e_i$ is the residual in the regression $s_i=a+bx_i+e_i$. Since $\mathbf{Cov}(s_i,x_i)=0$, we have $b=0$; thus the regression reduces to $s_i=a+e_i$, which yields $\frac{\mathbf{Cov}(Y_i,e_i)}{\mathbf{Var}(e_i)}=\frac{\mathbf{Cov}(Y_i,s_i)}{\mathbf{Var}(s_i)}$; the RHS is exactly $\rho'$ in the regression $Y_i=\alpha'+\rho' s_i+\varepsilon_i'$ 
		1. Covariance Property
		$\displaystyle\text{Cov}[cX, Y] = c \cdot \text{Cov}[X, Y]$$\displaystyle\text{Cov}[cX, Y] = c \cdot \text{Cov}[X, Y]$
		2. Pulling out Constants 
		$Cov[cX,Y]=c\cdot Cov[X,Y]\quad Cov[X,cY]=c\cdot Cov[X,Y]$ 
	    3. Distributive Property:
	    $\displaystyle\text{Cov}[X + Y, Z] = \text{Cov}[X, Z] + \text{Cov}[Y, Z]$$\displaystyle\text{Cov}[X + Y, Z] = \text{Cov}[X, Z] + \text{Cov}[Y, Z]$
	    4. Symmetry: $\displaystyle\text{Cov}[X, Y] = \text{Cov}[Y, X]$$\displaystyle\text{Cov}[X, Y] = \text{Cov}[Y, X]$
		5. Constants cannot covary: $\displaystyle\text{Cov}[X, c] = 0$$\displaystyle\text{Cov}[X, c] = 0$
		Thus, $\mathbf{Cov}(Y_i,e_i)=\mathbf{Cov}(Y_i,s_i-a)=\mathbf{Cov}(Y_i,s_i)-\mathbf{Cov}(Y_i,a)\text{(Distributive Property)}$
		$\mathbf{Cov}(Y_i,a)=0\text{(Constans cannot convary)}$
		Therefore, $\mathbf{Cov}(Y_i,e_i)=\mathbf{Cov}(Y_i,s_i)$

#### Bad Control


Exercise
Show that $\mathbf{Cov}(Y_i,\tilde{D}_i)=\mathbb{E}(\tilde{D}_iY_i)$
	Solution:
	$\tilde{D}_i=D_i-\mathbb{E}(D_i|x_i)$
	$\Rightarrow \mathbb{E}[\tilde{D}_i]=\mathbb{E}[D_i-\mathbb{E}(D_i|x_i)]=0$
	$\mathbf{Cov}(Y_i,\tilde{D}_i)=\mathbb{E}(\tilde{D}_iY_i)-\mathbb{E}(\tilde{D}_i)\mathbb{E}(Y_i)=\mathbb{E}(\tilde{D}_iY_i)$
Therefore, we have
$$\delta_R=\frac{\mathbb{E}\Big(Y_i\big(D_i-\mathbb{E}(D_i|x_i)\big)\Big)}{\mathbb{E}\Big(\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\Big)}$$
Exercise
show that $\mathbb{E}[Y_i\big(D_i-\mathbb{E}(D_i|x_i)\big)]=\mathbb{E}\big[\big(D_i-\mathbf{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i,x_i)\big]$
- Solution:
- According to [[Econometrics#Law of Iterated Expectation\|Law of Iterated Expectation]]
- $\mathbb{E}[Y_i\big(D_i-\mathbb{E}(D_i|x_i)\big)]=\mathbb{E}\Big[\mathbb{E}[Y_i\big(D_i-\mathbb{E}(D_i|x_i)\big)|D_i,x_i]\Big]$
- $D_i-E(D_i|x_i)$ is a function of $D_i,x_i$
- According to [[Econometrics#An important property\|An important property]], $D_i-E(D_i|x_i)$  can be taken out of the brackets
- $\mathbb{E}[Y_i\big(D_i-\mathbb{E}(D_i|x_i)\big)]=\mathbb{E}\big[\big(D_i-\mathbf{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i,x_i)\big]$

Exercise==还没看懂==
$\mathbb{E}(Y_i|D_i,x_i)=\mathbb{E}(Y_i|D_i=0,x_i)+\delta_{x_i}D_i$
	Solution:
	$=E(Y_i|D_i=0,x_i)+D_i\Big(E(Y_i|x_i,D_i=1)-E(Y_i|x_i,D_i=0)\Big)$
	这么拆分的情况下
	When $D_i=0$
	$=E(Y_i|x_i,D_i=0)$
	When $D_i=1$
	$E(Y_i|x_i,D_i=1)$
	Therefore, we can assume $E(Y_i|x_i,D_i=1)-E(Y_i|x_i,D_i=0)=\delta_{xi}$
$\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i,x_i)\Big]=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)D_i\delta_{x_i}\Big]$
	Solution:
	According to previous excercise, $\mathbb{E}(Y_i|D_i,x_i)=\mathbb{E}(Y_i|D_i=0,x_i)+\delta_{x_i}D_i$
	$\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i,x_i)\Big]=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)[\mathbb{E}(Y_i|D_i=0,x_i)+\delta_{x_i}D_i]\Big]$
	$=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i=0,x_i)\Big]+\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\delta_{x_i}D_i\Big]$
	Therefore, what we need to do is
	Prove $\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i=0,x_i)\Big]=0$
	According to [[Econometrics#Law of Iterated Expectation\|Law of Iterated Expectation]]
	$\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i=0,x_i)\Big]=E\Bigg[\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i=0,x_i)|x_i\Big]\Bigg]$
	$\because \mathbb{E}(Y_i|D_i=0,x_i)$ is a function of $x_i$ i.e. $f(x_i)$
	According to 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/econometrics/#an-important-property" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### An important property
$E[E[xy|x]]=E[xE[y|x]]$ can be [proved](https://stats.stackexchange.com/questions/530324/conditional-expectation-how-is-eexyx-exeyx), but I don't understand right now  


</div></div>

	$\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(Y_i|D_i=0,x_i)\Big]=E\Bigg[\mathbb{E}(Y_i|D_i=0,x_i)\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)|x_i\Big]\Bigg]$
	In this equation,
	$\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)|x_i\Big]=0$ because
	$\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)|x_i\Big]=\mathbb{E}(D_i|x_i)-\mathbb{E}\Big[\mathbb{E}(D_i|x_i)|x_i\Big]$
	According to [[Econometrics#Law of Iterated Expectation\|Law of Iterated Expectation]]
	$\mathbb{E}\Big[\mathbb{E}(D_i|x_i)|x_i\Big]=\mathbb{E}(D_i|x_i)$
$\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)D_i\delta_{x_i}\Big]=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\delta_{x_i}\Big]$
	Solution:
	To prove $\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)D_i\delta_{x_i}\Big]=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\delta_{x_i}\Big]$
	We should prove $\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)D_i\delta_{x_i}\Big]-\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\delta_{x_i}\Big]=0$
	Since $E[X]+E[Y]=E[X+Y]$
	$\therefore \mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)D_i\delta_{x_i}\Big]-\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\delta_{x_i}\Big]=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)D_i\delta_{x_i}-\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\delta_{x_i}\Big]$
	$=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)[D_i\delta_{x_i}-\big(D_i-\mathbb{E}(D_i|x_i)\big)\delta_{x_i}]\Big]$
	$=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(D_i|x_i)\delta_{x_i}\Big]$
	According to [[Econometrics#Law of Iterated Expectation\|Law of Iterated Expectation]]
	$=\mathbb{E}\Bigg[\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)\mathbb{E}(D_i|x_i)\delta_{x_i}|x_i\Big]\Bigg]$
	$=\mathbb{E}\Bigg[\mathbb{E}(D_i|x_i)\delta_{x_i}\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)|x_i\Big]\Bigg]$
	Same as the precious exercise $\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)|x_i\Big]=0$ 
	$\therefore \mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)D_i\delta_{x_i}\Big]=\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\delta_{x_i}\Big]$
Now we have
$$\delta_R=\frac{\mathbb{E}\Big[\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\delta_{x_i}\Big]}{\mathbb{E}\Big(\big(D_i-\mathbb{E}(D_i|x_i)\big)^2\Big)}$$
Let $\sigma^2_D(x_i)=\mathbf{E}\Big((D_i-\mathbb{E}(D_i|x_i))^2|x_i\Big)$, the conditional variance of $D_i$ given $x_i$ , hence a function of $x_i$

Exerciese==没看懂求解答== 看上一题 ，把$\sigma^2_D(x_i)=\mathbf{E}\Big((D_i-\mathbb{E}(D_i|x_i))^2|x_i\Big)$带进去就行
Show that
$$\delta_R=\frac{\mathbb{E}\big(\sigma^2_D(x_i)\delta_{x_i}\big)}{\mathbb{E}\big(\sigma^2_D(x_i)\big)}$$

Exercise 
D is a binary variable with $\mathbb{P}(D=1)=p\in(0,1)$. Show that $\mathbf{Var}(D)=(1-p)p$
	Solution:
	To show that $\mathbf{Var}(D) = (1-p)p$, we can start by calculating the variance of a binary random variable.
	The variance of a random variable $X$ is defined as:
	$$\mathbf{Var}(X) = E[(X - E(X))^2]$$
	In this case, $D$ is a binary variable that takes the value 1 with probability $p$ and the value 0 with probability $1-p$. The expected value of $D$ can be calculated as:
$$E(D) = p \cdot 1 + (1-p) \cdot 0 = p$$
	Now, let's calculate the variance of $D$:
$$\mathbf{Var}(D) = E[(D - E(D))^2]$$
	Substituting the value of $E(D)$, we get:
$$\mathbf{Var}(D) = E[(D - p)^2]$$
	Since $D$ can only take the values 0 and 1, we can write:
$$\mathbf{Var}(D) = (0 - p)^2 \cdot \mathbb{P}(D=0) + (1 - p)^2 \cdot \mathbb{P}(D=1)$$
	Since $\mathbb{P}(D=0) = 1 - \mathbb{P}(D=1)$, we can rewrite this as:
$$\mathbf{Var}(D) = p^2 \cdot (1 - p) + (1 - p)^2 \cdot p$$
	Simplifying this expression, we get:
$$\mathbf{Var}(D) = p(1-p)(p + 1 - p)$$
$$\mathbf{Var}(D) = (1-p)p$$
	Therefore, we have shown that $\mathbf{Var}(D) = (1-p)p$.

Exercise==还没看懂==
Show that
$$\mathbb{E}[Y_{1i}-Y_{0i}|D_i=1]=\frac{\sum_s \delta_s \mathbb{P}(D_i=1|x_i=s)\mathbb{P}(x_i=s)}{\sum_s  \mathbb{P}(D_i=1|x_i=s)\mathbb{P}(x_i=s)}$$
Hint: You may apply the Bayes’ rule:
$$\mathbb{P}(x_i=s|D_i=1)=\frac{\mathbb{P}(D_i=1|x_i=s)\cdot\mathbb{P}(s_i=s)}{\mathbb{P}(D_i=1)}$$
	Solution:
	Let $δ_{tot}$ be the treatment effect on treated:
$$\delta_{tot}=\mathbb{E}(Y_{1i}-Y_{0i}|D_i=1)$$
	treatment on all applicants:
$$\delta_{ate}=\mathbb{E}(Y_{1i}-Y_{oi})=\sum\limits_s \delta_s \mathbb{E}(x_i=s)$$
	==上面为什么要引用treatment on all applicants属实没看懂== 可能是为了引出$\delta_s$ ?
	TA's method:
	$\delta_{tot}=\mathbb{E}(Y_{1i}-Y_{0i}|D_i=1)$
	According to [Definition of Conditional expectation](https://en.wikipedia.org/wiki/Conditional_expectation#:~:text=In%20probability%20theory%2C%20the%20conditional%20expectation%2C%20conditional%20expected,certain%20set%20of%20%22conditions%22%20is%20known%20to%20occur.)
	In Discrete random variables
	$E(X|Y=y)=\sum\limits_x xP(X=x|Y=y)=\sum\limits_x x\frac{P(X=x,Y=y)}{P(Y=y)}$
	In addition, accrding to sildes-4, the definition of $\delta_s$
	Note that in $\mathbb{E}(\delta_{x_i}|D_i=1)$, the (conditional) expectation averages out $x_i$
	Suppose $x_i$ takes discrete values, e.g., years of education $\{0,1,\dots,16\}$, we can figure out the condiional probabilities: $\mathbb{P}(x_i=s|D_i=1),s\in\{0,1,\dots,16\}$
	In this case, $\mathbb{E}(\delta_{x_i}|D_i=1)=\sum\limits_s \delta_s\mathbb{P}(x_i=s|D_i=1)$
	Therefore, 
	$\delta_{tot}=\sum_s \delta_s P(x_i=s|D_i=1)$
	According to Bayers' rule
	$\delta_{tot}=\sum_s \delta_s \frac{P(D_i|x_i=s)P(x_i=s)}{P(D_i=1)}$
	According to [Law of total probability](https://en.wikipedia.org/wiki/Law_of_total_probability), $P(A)=\sum\limits_n P(A\cap B_n)$ or alternatively, $P(A)=\sum\limits_n P(A|B_n)P(B_n)$
	$P(D_i=1)=\sum_s P(D_i=1|x_i=s)P(x_i=s)$
	Therefore, $\mathbb{E}[Y_{1i}-Y_{0i}|D_i=1]=\frac{\sum_s \delta_s \mathbb{P}(D_i=1|x_i=s)\mathbb{P}(x_i=s)}{\sum_s  \mathbb{P}(D_i=1|x_i=s)\mathbb{P}(x_i=s)}$


## ECON 5122 Exercise Set 1
```
D:\All Document\Msc\Econometric
```
Exercise 1. 
Suppose that the classical regression model applies but that the true value of the constant $β_0$ is zero. That is , 
$$y_i = β_1x_i + u_i$$ 
We further assume that $\{x_i\}^n_{i=1}$ are non-random. $\{u_i\}^n_{i=1}$ are i.i.d.(independent and identical distribution) with mean zero and variance $σ^2$ . 
1. Suppose you observe $(x_1, y_1), . . . ,(x_n, y_n)$. Derive the OLS estimator of $β_1$, which will be denoted by $\tilde{β}_1$. Show that $\tilde{β}_1$ is unbiased estimator of $β_1$. 
	My Proof:
	According to OLS estimation $\sum\limits_{i=1}^n (y_i-\tilde{\beta_1}x_i)^2$ is the minimum
	The derivation is $\sum\limits^n_{i=1} 2(y_i-\tilde{\beta_1}x_i)x_i=0$ （后来发现这里可以直接得出$\tilde{\beta}_1=\frac{\sum x_i u_i}{\sum x^2_i}$）
	$\Rightarrow \sum\limits_{i=1}^n (\beta_1-\tilde{\beta_1})x^2_i+\sum\limits_{i=1}^n u_i x_i=0$
	$\because u_i$ is uncorrelated with $x_i$ $\Rightarrow Cov(x_i,u_i)=0=E(x_i u_i)=E(x_i)E(u_i)$ See [[Econometrics#Uncorrelated\|Uncorrelation]]
	$\therefore \sum\limits_{i=1}^n u_i x_i=\sum\limits_{i=1}^n u_i \sum\limits_{i=1}^n x_i$
	$\because \{u_i\}^n_{i=1}$ are with mean zero
	$\therefore \therefore \sum\limits_{i=1}^n u_i x_i=\sum\limits_{i=1}^n u_i \sum\limits_{i=1}^n x_i=0$
	$\Rightarrow \sum\limits_{i=1}^n (\beta_1-\tilde{\beta_1})x^2_i=0$
	$\Rightarrow \sum\limits^n_{i=1}\beta_1 x^2_i=\sum\limits^n_{i=1}\tilde{\beta_1} x^2_i \Rightarrow \sum\limits^n_{i=1}\beta_1 =\sum\limits^n_{i=1}\tilde{\beta_1} \Rightarrow n \beta_1=\sum\limits^n_{i=1}\tilde{\beta_1}$
	$\Rightarrow \beta_1=\frac{\sum\limits^n_{i=1}\tilde{\beta_1}}{n} \Rightarrow \beta_1=E(\tilde{\beta_1})$
	$\tilde{\beta_1}$ is unbiased
2. Now suppose you do not know $β_0 = 0$, thus you obtain the OLS estimator of $β_1$ as usual, which will be denoted by $\hat{β}_1$, based on the model $y_i = β_0 + β_1x_i + u_i$ . Is $\hat{β}_1$ an unbiased estimator of $β_1$? Compare the variances of $\tilde{β}_1$ and $\hat{β}_1$.
	$Var(\hat{\beta_1})=Var(\beta_1+\frac{\sum x_i u_i}{\sum x^2_i})=Var(\frac{\sum x_i u_i}{\sum x^2_i})=\frac{1}{[\sum x^2_i]^2}Var(\sum x_i u_i)=\frac{\sum x^2_i}{[\sum x^2_i]^2}Var( u_i)$ ==方差计算中分子是怎么拿出来的？== 虽然没有实际定理，但是董yc教材里面就是这么操作的。所以我们可以得出结论，$x_i$ is uncorrelated with $u_i$, $Var(u_i)$ is known as $\sigma^2$. $Var{\sum x_i u_i}=\sum x^2_i Var(u_i)$ i.e. 在uncorrelated的情况下，sum的variance等于variance的sum $\operatorname{Var}\left(\sum_{i=1}^mX_i\right)=\sum_{i=1}^m\operatorname{Var}(X_i)+2\sum_{i<j}\operatorname{Cov}(X_i,X_j).$ 证明[在此](https://stats.stackexchange.com/questions/31177/does-the-variance-of-a-sum-equal-the-sum-of-the-variances)
		至于提出来为什么是$x_i^2$,TA给出的证明
		以两项为例 $Var(u_1x_1+u_2x_2)=Var(u_1x_1)+Var(u_2x_2)=x_1^2 Var(u_1)+x_2^2Var(u_2)$
	$\sum (x_i-\bar{x})^2\leq \sum x^2_i\Rightarrow Var(\tilde{\beta}_1)\leq Var(\hat{\beta}_1)$
董雨辰の宿題
![276d2f3c42342e733fec1cfadeda383](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031710541.jpg)
==为什么$\rho_0=0$时$\beta_1$的求解公式发生改变？== 将一般的公式代入第一个，得到的结果也是unbiased

$\hat{β}=\frac{∑(x_i−\bar{x})(y_i−\bar{y})}{∑(x_i−\bar{x})^2}=\frac{∑(x_i−\bar{x})y_i}{∑(x_i−\bar{x})}$
[Proof](https://stats.stackexchange.com/questions/343324/expression-for-hat-beta-in-simple-linear-regression)
$$
\begin{align}
\hat{\beta} &=  \frac{\sum(x_i-\bar{x})(y_i-\bar{y})}{\sum(x_i-\bar{x})^2}=\frac{\sum(x_i-\bar{x})y_i-\sum(x_i-\bar{x})\bar{y}}{\sum(x_i-\bar{x})^2}\\
&=\frac{\sum(x_i-\bar{x})y_i-\bar{y}\sum(x_i-\bar{x})}{\sum(x_i-\bar{x})^2}=
\frac{\sum(x_i-\bar{x})y_i-\bar{y}\cdot 0}{\sum(x_i-\bar{x})^2}\\
&=\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}=\sum\frac{(x_i-\bar{x})y_i}{\sum(x_j-\bar{x})^2}
\end{align}
$$

Exercise 2. 
Your would like to study the ice cream sales in Hong Kong. The company makes available to you quarterly ice cream sales $(Y)$ and informs you that the price per gallon has approximately remained constant over the sample period. You gather information on average daily temperatures $(X)$ during these quarters and regress $Y$ on $X$, adding seasonal binary variables for spring, summer, and fall. These variables are constructed as follows: $D_1$ takes on a value of 1 during the spring and is zero otherwise, $D_2$ takes on a value of 1 during the summer, $D_3$ takes on a value of 1 during the fall. Specify three regression models where the following conditions hold:
1. The intercept terms and slopes are forced to be the same for each quarter. 
	1. $Y$ sales $X$ temp $D_1,D_2,D_3$ dummy
	2. $Y_t=\beta_0+\beta_1x_t+u_t$
2. The slopes are forced to be the same for each quarter but we allow for different intercept terms for each season; find the intercept term for each season. 
	1. $Y_t=\beta_0+\beta_1D_1+\beta_2D_2+\beta_3D_3+\beta_4x_t+u_t$
	2. $D_1=1,D_2=0,D_3=0$
	3. $Y_t=\beta_0+\beta_1+\beta_4x_t+u_t$ Intercept $\beta_0+\beta_1$ 
	4. $D_1=0,D_2=1,D_3=0$
	5. $Y_t=\beta_0+\beta_2+\beta_4x_t+u_t$ Intercept $\beta_0+\beta_2$
	6. $D_1=0,D_2=0,D_3=1$
	7. $Y_t=\beta_0+\beta_3+\beta_4x_t+u_t$ Intercept $\beta_0+\beta_3$
	8. $D_1=0,D_2=0,D_3=0$
	9. $Y_t=\beta_0+\beta_4x_t+u_t$ Intercept $\beta_0$
3. We allow for varying slopes and intercept terms for each season; find the intercept term and slope for each season. Which parameters capture the main effects?
	1. $$\begin{align}Y_t=&\beta_0+\beta_1D_1+\beta_2D_2+\beta_3D_3\\&+\beta'_1D_1x_t+\beta'_2D_2x_t+\beta'_3D_3x_t\\&+\beta_4x_t+u_t\end{align}$$
	2. Spring $D_1=1$
	3. $Y_t=\beta_0+\beta_1+(\beta'_1+\beta_4)x_t+u_t$
	4. Summer $D_2=1$
	5. $Y_t=\beta_0+\beta_2+(\beta'_2+\beta_4)x_t+u_t$
	6. Fall $D_3=1$
	7. $Y_t=\beta_0+\beta_3+(\beta'_3+\beta_4)x_t+u_t$
	8. Winter all the dummy are zero
	9. $Y_t=\beta_0+\beta_4x_t+u_t$

Exercise 3. 
Let’s consider that we aim to investigate the causal effect of a college degree on future earnings. 
	What are the potential outcomes in this scenario for an individual $i$? 
		Solution:
		$y_{0i}$ don't go to college $y_{1i}$ go to college
	What is the causal effect of college degree on earnings for individual $i$?
		Solution:
		$y_{1i}-y_{0i}$ casual effect 
We have data on earnings of two distinct groups: individuals who have completed college education and those who have not. 
	Describe how you would proceed with the data. 
		Solution:
		$$y_i(\text{real outcome})=\left\{\begin{array}{**lr**} y_{0i}\quad if\ c_i=0 \\ y_{1i}\quad if\ c_i=1\end{array}   \right.$$
	Could there be any potential problems due to selection bias?
		Solution:
		$$\begin{align}J&=E(y_i|c_i=1)-E(y_i|c_i=0)\\&=E(y_{1i}|c_i=1)-E(y_{0i}|c_i=0)\\&=\underbrace{E(y_{1i}-y_{0i}|c_i=1)}_{casual\ effect}+\underbrace{E(y_{0i}|c_1=1)-E(y_{0i}|c_i=0)}_{selection\ bias}\end{align}$$

## Mid-term
**October 27, 2023**. 
It will take place from **1:30 PM to 3:30 PM** in **LT1** at the **LSK building**. 
This is a closed-book examination, and it will cover all materials up to and including Topic 4: Regression Analysis (II).

Question 1 (40 pts). Consider a simple linear regression model
$$Y_i=\beta_0+\beta_1X_i+u_i,\quad i=1,2,\dots,n$$
(i) (6 pts) State the least square assumptions for the simple linear regression model.
	(1) $E(X_i|u_i)=0$; 
	(2) $(X_i,Y_i),i=1,2,\dots,n$ are i.i.d.; 
	(3) Large outliers are unlikely

(ii) (10 pts) Show that the OLS estimator $\hat{β}_0, \hat{β}_1$ satisfy
$$\hat{\beta}_0+\hat{\beta}_1\bar{X}=\bar{Y},\quad \hat{\beta}_1=\frac{\sum^n_{i=1}(X_i-\bar{X})(Y_i-\bar{Y})}{\sum^n_{i=1}(X_i-\bar{X})^2}$$
where $\bar{X}=\frac{1}{n}\sum^n_{i=1}X_i,\bar{Y}=\frac{1}{n}\sum^n_{i=1}Y_i$
	$\hat{\beta}_0,\hat{\beta}_1$ can be obtained by solving the following least squares problem
$$\min_{b_0,b_1}\sum\limits^n_{i=1}(Y_i-(b_0+b_1X_i))^2$$
	First order conditions lead to
$$\sum\limits^n_{i=1}(Y_i-\hat{\beta}_0-\hat{\beta}_1X_i)=0\tag{4}$$
$$\sum\limits^n_{i=1}X_i(Y_i-\hat{\beta}_0-\hat{\beta}_1X_i)=0\tag{5}$$
	Rearrange terms and divide both sides by $n$, we have $\hat{\beta}_0+\hat{\beta}_1\bar{X}=\bar{Y}$. Next, substitute $\hat{β}_0$ into (5), we have
$$\sum\limits^n_{i=1}X_i(Y_i-\bar{Y}-\hat{\beta}_1(X_i-\bar{X}))=0\Leftrightarrow \sum\limits^n_{i=1}(X_i-\bar{X})(Y_i-\bar{Y}-\hat{\beta}_1(X_i-\bar{X}))=0$$
	Next, rearrange terms, we have $\hat{\beta}_1=\frac{\sum^n_{i=1}(X_i-\overline{X})(Y_i-\overline{Y})}{\sum^n_{i=1}(X_i-\overline{X})^2}$

(iii) (10 pts) Recall that the $R^2$ in the regression of $Y$ on $X$ is given by
$$R^2=\frac{\sum^n_{i=1}(\hat{Y}_i-\overline{Y})^2}{\sum^n_{i=1}(Y_i-\overline{Y})^2}$$
where $\hat{Y}_i=\hat{\beta}_0+\hat{\beta}_1 X_i$ is the fitted value. Show that the regression $R^2$ in the regression of $Y$ on $X$ is the squared value of the sample correlation between X and Y . That is, show that $R^2=r^2_{XY}$. (Recall that $r_{XY}=\frac{s_{XY}}{s_X s_Y}$, where $s_{XY}=\frac{1}{n-1}\sum^n_{i=1}(X_i-\overline{X})(Y_i-\overline{Y}),s^2_X=\frac{1}{n-1}\sum^n_{i=1}(X_i-\overline{X})^2,s^2_Y=\frac{1}{n-1}\sum^n_{i=1}(Y_i-\overline{Y})^2$).
	Since $\hat{\beta}_0+\hat{\beta}_1\overline{X}=\overline{Y}$
$$\hat{Y}_i-\overline{Y}=\hat{\beta}_1(X_i-\overline{X})$$
	Thus,
$$R^2=\hat{\beta}^2_1\frac{\sum^n_{i=1}(X_i-\overline{X})^2}{\sum^n_{i=1}(Y_i-\overline{Y})^2}$$
	Since $\hat{\beta}_1=\frac{\sum^n_{i=1}(X_i-\bar{X})(Y_i-\bar{Y})}{\sum^n_{i=1}(X_i-\bar{X})^2}$ we have
$$R^2=\frac{\Big(\sum^n_{i=1}(X_i-\bar{X})(Y_i-\bar{Y})\Big)^2}{\Big(\sum^n_{i=1}(X_i-\bar{X})^2\Big)^2} \frac{\sum^n_{i=1}(X_i-\overline{X})^2}{\sum^n_{i=1}(Y_i-\overline{Y})^2}=\frac{\Big(\sum^n_{i=1}(X_i-\overline{X})(Y_i-\overline{Y})\Big)^2}{\sum^n_{i=1}(X_i-\overline{X})^2\sum^n_{i=1}(Y_i-\overline{Y})^2}$$
	Rearrange terms, we have $R^2=r^2_{XY}$


(iv) (4pts) Show that the $R^2$ from the regression of $Y$ on $X$ is the same as the $R^2$ from the regression of $X$ on $Y$ .
	Trivial since $r_{XY} =r_{YX}$.

(v) (10 pts) Now suppose $β_0=0$. Derive an OLS estimator of $β_1$.
	$\tilde{β}_1$ can be obtained by solving the following least squares problem
$$\min_{b_0,b_1}\sum\limits^n_{i=1}(Y_i-b_1X_i)^2$$
	First order conditions lead to
$$\sum\limits^n_{i=1}(Y_i-\tilde{\beta}_1X_i)X_i=0$$
	which yields
$$\tilde{\beta}_1=\frac{\sum^n_{i=1}Y_iX_i}{\sum^n_{i=1}X^2_i}$$



Question 2 (40 pts). Consider a simple linear regression model
$$Y_i=\beta_0+\beta_1X_i+u_i,\quad i=1,2,\dots,n$$
(i) (6 pts) Assume that $\mathbb{E}(u_i)=0,\mathbb{E}(X_i u_i)=0$. Show that
$$\beta_1=\frac{\mathbf{Cov}(X_i,Y_i)}{\mathbf{Var}(X_i)}$$
Based on (3), propose an estimator of $β_1$ based on the method of moments
	[[Econometrics#BetaOneEstimation\|Solution]]

(ii) (6 pts) Now suppose $\mathbf{Cov}(u_i,X_i)\neq 0$. We have an endogenous problem. However, we have some variable $Z_i$ satisfying $\mathbf{Cov}(Z_i,u_i)=0$ and $\mathbf{Cov}(Z_i,X_i)\neq 0$. Show that
$$\beta_1=\frac{\mathbf{Cov}(Y_i,Z_i)}{\mathbf{Cov}(X_i,Z_i)}$$
Propose an estimator of $β_1$ given that $\mathbf{Cov}(u_i,X_i)\neq 0$.
	Since $\mathbf{Cov}(Z_i,u_i)=0$
$$\mathbf{Cov}(Y_i,Z_i)=\mathbf{Cov}(\beta_0+\beta_1 X_i+u,Z_i)=\beta_1\mathbf{Cov}(X_i,Z_i)$$
	moreover, $\mathbf{Cov}(X_i,Z_i)\neq 0$
	we have $\beta_1=\frac{\mathbf{Cov}(Y_i,Z_i)}{\mathbf{Cov}(X_i,Z_i)}$
	Thus, an estimator is given by
$$\hat{\beta}_1=\frac{\sum^n_{i=1}(Z_i-\overline{Z})(Y_i-\overline{Y})}{\sum^n_{i=1}(X_i-\overline{X})(Z_i-\overline{Z})}$$

(iii) (10 pts) In class, we have discussed a scenario where we would like to know the effect of skipping classes on exam performance: 
$$score =β_0 + β_1\text{skipped} + u.$$
We realize that the skipped classes skipped may be an endogenous variable. That is, $\mathbf{Cov}(skipped,u)\neq 0$. Suppose we have the data about attendance checks: some professors don’t check attendance at all $(A = 0)$, some check attendance seriously $(A =1)$, and we propose the following measure of the effect of skipping classes
$$\frac{\mathbb{E}(\text{score}|A=0)-\mathbb{E}(\text{score}|A=1)}{\mathbb{E}(\text{skipped}|A=0)-\mathbb{E}(\text{skipped}|A=1)}$$
Show that such a measure is exactly equal to $β_1$. (You may use the result in part (ii).)
	

(iv) (10 pts) Now suppose $u_i=\varepsilon_i+\theta \varepsilon_{i-1}$ , where $ε_i , i= 1, 2, . . . , n$ are i.i.d. variables with mean 0 and variance $σ^2_{\varepsilon}$ . Calculate $\mathbf{Var}(u_i)$ and $\mathbf{Cov}(u_i,u_{i+k})$ for any $k \geq 1$. Let $\mathbf{u}=[u_1,u_2,\dots,u_n]'$. Find an expression for $Ω=\mathbb{E}(\mathbf{uu'})$. Will you proceed with OLS or GLS?
	Note that
	$$$$
	One should proceed with GLS since $u_i$ is not independently distributed.
	In addition,
	[Which is better GLS or OLS?](https://timeseriesreasoning.com/contents/generalized-least-squares/#:~:text=GLS%20is%20especially%20suitable%20for,useful%20alternative%20to%20OLS%20estimation.)
	**GLS is especially suitable for fitting linear models on data sets that exhibit heteroskedasticity (i.e., non-constant variance) and/or auto-correlation**. Real world data sets often exhibit these characteristics making GLS a very useful alternative to OLS estimation.

(v) (8 pts) Now suppose $Y_i$ represents the salary of individual $i$, and $X_i$ is the years of education. 
	(a) (2 pts) State what issue may arise if you apply a simple linear regression model to study the salary-education problem and estimate the model via OLS. 
		$X$ might be an endogenous variable that correlated with some omitted variable included in $u$, e.g., cognitive ability. OLS estimator will be biased and inconsistent.
	(b) (6 pts) Now suppose the issue in part (a) does not exists. You have a gender dummy variable $D_i$ . Propose a regression model that help you to identify the gender inequalities in returns of education. (State clearly which parameter captures the gender inequality.)
		Let $D_i =1$ if $i$ is a female and 0 otherwise. 
		Consider the following regression model
$$Y_i=\beta_0+\beta_1X_i+\beta_2D_iX_i+u_i$$
		On average we have for females
$$Y_i=\beta_0+(\beta_1+\beta_2)X_i;\Rightarrow \Delta Y=(\beta_1+\beta_2)\Delta X\Leftrightarrow \frac{\Delta Y}{\Delta X}=\beta_1+\beta_2$$
		and for males
$$\frac{\Delta Y}{\Delta X}=\beta_1$$
		Thus, one more unit of education brings additional $β_1$ and $β_1+β_2$ units of salary for male and females; respectively. The gender inequality is captured by $β_2$.


Question 3 (20 pts). 
(i) (15 pts) The table below is the Table 2 of Li, H., Liu, P. W., Zhang, J., & Ma, N. (2007). Economic returns to communist party membership: Evidence from urban Chinese twins. The Economic Journal, 117(523), 1504-1520. Based on the first column of the regression outputs: 
	(a) (5 pts) Provide an estimate of the economic returns of being a party member. 
		Note that the coefficient of the party membership is 0.124. Since the dependent variable is log earning, thus, the interpretation is that being party members increases earinings by 12.4%.
	(b) (10 pts) Calculate the age of maximum wages
		Denote $a_i$ be the age of individual $i$, and $y_i$ the log earnings, then, the estimates specify
$$y_i=0.027a_i-0.026\times \frac{a^2_i}{100}+\text{other variables}$$
		First order condition implies
$$\frac{\partial y_i}{\partial a_i}=0.027a_i-2\times0.00026a_i=0$$
		Thus the age of maximum earning is $a^*_i=51.92$.
![202312031710542.png (692×507) (raw.githubusercontent.com)](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031710542.png)
(ii) (5 pts) The Figure below captures a presentation slide of the paper by Fisman, R., Shi, J., Wang, Y., & Xu, R. (2018). Social ties and favoritism in Chinese science. Journal of Political Economy, 126(3), 1134-1171. Comment on the last bullet point.
	(1) The mechanism could be in the opposite direction: more grants attracts more fellows. (2) There may be some factors that attract both grants and fellows, e.g., the overall research capacity of university staff.


### Real Exam
Question 4
Consider a linear regression model $Y=\beta_0+\beta_1X_1+\beta_2X_2+\varepsilon$. Suppose for some reasons, the variable $X_2$ is not included in the model. Thus, we proceed with $Y=\beta'_0+\beta'_1X_1+\varepsilon'$
(i) 有两种做法，一种官方一种是我的OLS一阶条件
Derive the _ommitted variable bias_ in $\beta'_1$ in terns of $\beta_1,\beta_2$ and the variance and covariances of $X_1,X_2$.
1. $\beta'_1=\frac{Cov(Y,x_1)}{Var(x_1)}=\frac{Cov(\beta'_0+\beta'_1X_1+\varepsilon',x_1)}{Var(x_1)}=\frac{Cov(\beta_0+\beta_1X_1+\beta_2 X_2+\varepsilon,x_1)}{Var(x_1)}=\frac{\beta_1 Cov(X_1,X_1)+\beta_2Cov(X_1,X_2)}{Var(x_1)}=\beta_1+\frac{\beta_2Cov(X_1,X_2)}{Var(X_1)}$
2. $Y=\beta'_0+\beta'_1X_1+\varepsilon'$
	According to OLS 
$$\begin{align}\min\ Y-\beta'_0-\beta'_1X_1\\
\left\{\begin{array}{**lr**} \sum X_1(Y-\beta'_0-\beta'_1X_1)=0\quad(1)\\ \sum X_1(Y-\beta'_0-\beta'_1X_1)=0\quad(2)\end{array}   \right.
\end{align}$$
	From $(2)$ we get
$$\overline{Y}=\beta'_1\overline{X}_1+\beta'_0\quad(3)$$
	Substitute $(3)$ into $(1)$
$$\begin{align}\sum X_1(Y-(\overline{Y}-\beta'_1\overline{X}_1)-\beta'_1X_1)=0\\
\Rightarrow \sum X_1[(Y-\overline{Y})-\beta'_1(X_1-\overline{X})]=0\\
\Rightarrow \sum (X_1-\overline{X})[(Y-\overline{Y})-\beta'_1(X_1-\overline{X})]=0\quad(4)
\end{align}$$
$$\begin{align}
Y=\beta_0+\beta_1X_1+\beta_2X_2+\varepsilon\\
\overline{Y}=\beta_0+\beta_1\overline{X}_1+\beta_2\overline{X}_2+\overline{\varepsilon}
\end{align}$$
	$(4)$ will become
$$\begin{align}
\sum (X_1-\overline{X})[\beta_1(X_1-\overline{X}_1)+\beta_2(X_2-\overline{X}_2)+(\varepsilon-\overline{\varepsilon})-\beta'_1(X_1-\overline{X})]=0\\
\Rightarrow \beta'_1=\beta_1+\beta_2\frac{Cov(X_1,X_2)}{Var(X_1)}+\frac{Cov(X_1,\varepsilon)}{Var(X_1)}\\
\text{Since }Cov(X_1,\varepsilon)=0\\
\beta'_1=\beta_1+\beta_2\frac{Cov(X_1,X_2)}{Var(X_1)}
\end{align}$$
(ii) 要考虑$\beta_1>0$
(iii)要考虑$\beta_2<0$

Question 5
We would like to investigate the casual effect of a company's training program on employee productivity:
(i) What are the potential outcomes in this scenario for an individual $i$?
	$Y_{1i}$ and $Y_{0i}$
(ii) What is the casual effect of the training program on productivity for individuals $i$?
	对个人而非对群体($E[Y_{1i}-Y_{0i}|D=1]$是对群体)
	$s=Y_{1i}-Y_{0i}$
## Instrumental Variables
Consider a regression model $Y=\alpha+\rho s+\varepsilon$
The fundamental assumption for consistency of OLS is that the error $ε$ is uncorrelated with the regressor $s$
$$\mathbb{Cov}(s,\varepsilon)=0\text{ or }\mathbb{E}(\varepsilon| s)=0$$
$\mathbb{E}(\varepsilon| s)=0 \Rightarrow \mathbb{E}(\varepsilon)=0$ Therefore, people sometimes utlize $\mathbb{E}(\varepsilon)=0$

Because under the above assumptions, we have
$$\rho=\frac{\mathbf{Cov}(Y,s)}{\mathbf{Var}(s)}$$
$Cov(Y,s)=Cov(\alpha+\rho s+\varepsilon,s)=Cov(\rho s,s)=\rho Var(s)$

The OLS estimator is the sample analogue
$$\hat{\rho}=\frac{\sum\limits^n_{i=1}(Y_i-\overline{Y})(s_i-\bar{s})}{\sum\limits^n_{i=1}(s_i-\bar{s})^2}$$
By LLN,
$$\hat{\rho}\mathop{\longrightarrow}^{\mathbb{P}}\rho$$

However, when $\mathbf{Cov}(\varepsilon,s)\neq 0$, we have trouble with OLS 
There might be some omitted variables $(x)$ like cognitive abilities hidden in $ε$ that directly affect both $s$ and $Y$
$$\varepsilon=\mathbf{x'\beta}+e$$
If the correlation is induced by omitted variables, we could 
1. include the omitted variables or their proxies upon availability Y 
	 $$Y=\alpha+\rho s+\mathbf{x'\beta}+e$$
2. use panel data upon availability (will be introduced later)

We don’t always enjoy the blessings of data availability; need to find information in available data

Consider the following interesting example 
We would like to know the effect of skipping classes on exam performance 
Perhaps the simplest scientific approach is to set the simple linear model:
$$score=\beta_0+\beta_1 skipped+\varepsilon$$
We need more information related 
Suppose we have the data about attendance checks: some professors don’t check attendance at all $(A=0)$, some check attendance seriously $(A=1)$ 
We may expect a difference in
$\mathbb{E}(skipped|A=0)-\mathbb{E}(skipped|A=1)$
We may also expect a difference in
$\mathbb{E}(score|A=0)-\mathbb{E}(score|A=1)$
Then a good measure of $\beta_1$ is given by
$$\frac{\mathbb{E}(score|A=0)-\mathbb{E}(score|A=1)}{\mathbb{E}(skipped|A=0)-\mathbb{E}(skipped|A=1)}$$
In the above example, we can estimate the parameter $β_1$ with the assistance of $A$ 
A will be called the **instrumental variable**, a powerful tool to solve **endogeneity** issue

We have a similar scenario in the simple linear regression model: $Y=\alpha+\rho s+\varepsilon$ where $\mathbf{Cov}(s,\varepsilon)\neq 0$
$s$ is called an endogenous variable

Suppose we have another variable $z$ satisfying 
$$\mathbf{Cov}(s,z)\neq 0,\mathbf{Cov}(\varepsilon,z)=0$$
- $\mathbf{Cov}(s,z)\neq 0$ is the **relevance** condition 
- The condition $\mathbf{Cov}(\varepsilon,z)=0$ 0 is called the **exclusion** restriction, or **exogeneity**

Then, we have
$$\begin{aligned}\mathbf{Cov}(Y,z)&=\mathbf{Cov}(\alpha+\rho s+\varepsilon,z)=\rho\mathbf{Cov}(s,z)\\&\Rightarrow\rho=\frac{\mathbf{Cov}(Y,z)}{\mathbf{Cov}(s,z)}&(1)\end{aligned}$$
This suggests an estimator of $ρ$ that is given by the sample analogue
$$\hat{\rho}=\frac{\sum\limits^n_{i=1}(Y_i-\overline{Y})(z_i-\overline{z})}{\sum\limits^n_{i=1}(s_i-\overline{s})(z_i-\overline{z})}$$
Note if $s=z,\hat{\rho}$ reduces to the OLS estimator of $ρ$

Exercise
An implication of $(1)$ to the attendance check example is that $\beta_1=\frac{\mathbf{Cov}(score,A)}{\mathbf{Cov}(skipped,A)}$. Use this to show that the “good measure” of $β_1$ (RHS below) is indeed equal to $β_1$:
$$\beta_1=\frac{\mathbb{E}(score|A=0)-\mathbb{E}(score|A=1)}{\mathbb{E}(skipped|A=0)-\mathbb{E}(skipped|A=1)}$$
	Solution:
	$s:score\quad sk:skipped$
	$\mathbb{E}(A)=\mathbb{P}(A=1)=\mathbb{P}$
	$\mathbf{Cov}(a,A)=\mathbb{E}((s-\bar{s})(A-P))$
	$\Rightarrow \mathbb{E}(s(A-P))-\mathbb{E}(\bar{s}(A-P))$
	$\mathbb{E}(\bar{s}(A-P))=0$
	Therefore, $\mathbf{Cov}(s,A)=\mathbb{E}(s(A-P))$
	$\mathbf{Cov}(s,A)=\mathbb{E}(s(A-P))=\mathbb{E}(s(1-p)|A=1)\mathbb{P}(A=1)+\mathbb{E}(s(0-p)|A=0)\mathbb{P}(A=0)=(1-p)p[\mathbb{E}(score|A=0)-\mathbb{E}(score|A=1)]$
	Similarly, $Cov(sk,A)=p(1-p)[\mathbb{E}(skipped|A=0)-\mathbb{E}(skipped|A=1)]$
	$\beta_1=\frac{Cov(s,A)}{Cov(sk,A)}$

Recall that 
- Endogeneity: $\mathbf{Cov}(s,\varepsilon)\neq 0$
- Valid IV: $\mathbf{Cov}(z,\varepsilon)=0,\mathbf{Cov}(s,z)\neq 0$
Suppose we can decompose $s$ into two parts, $s=\tilde{s}+\tilde{s}'$ such that  is the “cleaned” part: $\mathbf{Cov}(\tilde{s},\varepsilon)=0$ 
How to find $\tilde{s}$? Regress $s$ on $z$: $s=\theta+\delta z+\eta$, let $\tilde{s}=\theta+\delta z$ 
Now regress $Y$ on $\tilde{s}$ instead: $Y=\tilde{\alpha}+\tilde{\rho}\tilde{ s}+\tilde{\varepsilon}$

Exercise
Show that
1. $\mathbf{Cov}(Y,\tilde{s})=\delta\rho\mathbf{Cov}(s,z)$;
	1. Solution：
	2. $Cov(Y,\tilde{s})=Cov(\alpha+\rho s+\varepsilon,\theta+\delta z)=\delta\rho Cov(s,z)$
2. $\tilde{\rho}=\rho$ (Hint:$\delta=\frac{\mathbf{Cov}(s,z)}{\mathbf{Var}(z)},\tilde{\rho}=\frac{\mathbf{Cov}(Y,\tilde{s})}{\mathbf{Var}(\tilde{s})}$)
	1. Solution:
	2. From (1) we get $\rho=\frac{\mathbf{Cov}(Y,\tilde{s})}{\delta\mathbf{Cov}(s,z)}$
	3. $\mathbf{Cov}(Y,\tilde{s})=\tilde{\rho}\mathbf{Var}(\tilde{s})$
	4. According to $\tilde{s}=\theta+\delta z$, we got $\mathbf{Var}(\tilde{s})=\delta^2\mathbf{Var}(z)$
	5. Therefore, $\mathbf{Cov}(Y,\tilde{s})=\tilde{\rho}\delta^2\mathbf{Var}(z)$
	6. According to $\delta=\frac{\mathbf{Cov}(s,z)}{\mathbf{Var}(z)}$
	7. $\mathbf{Cov}(Y,\tilde{s})=\tilde{\rho}\delta^2 \frac{\mathbf{Cov}(s,z)}{\delta}$
	8. We get $\tilde{\rho}=\frac{\mathbf{Cov}(Y,\tilde{s})}{\delta\mathbf{Cov}(s,z)}$, proved
	9. 结论就是intrument variable的结论和clean part回归的结论一致

This exercise highlights the**two stage least squares** (2SLS) approach to an IV regression model 
	Regress the endogenous variables on the IV, and find the “cleaned” proxy of the endogenous variable 
	Regress the dependent variable on the proxy

We have four types of variables in a general IV regression model 
The dependent variable $Y$ 
The endogenous regressors $x$ 
The exogenous regressors $w$ 
The instrumental variables $z$

We could have a general IV regression model:
$$Y_i=\mathbf{x'}_i\beta+w'_i\gamma+\varepsilon_i$$
where
- $\beta,\gamma$ are unknown coefficients
- $\mathbf{x}_i=(1,x_{1i},\dots,x_{ki})'$ are the $k$ endogenous regressors plus a constant
- $\mathbf{x}_i$ may be correlated with the error term $\varepsilon_i$
- $w_i=(w_{1i},\dots,w_{ri})'$ are $r$ included exogenous regressors, $\mathbb{E}(\varepsilon_i|w_i)=0$
- $z_i=(z_{1i},\dots,z_{mi})'$ are $m$ instrumental variables
- If $m=k$, we have exact identification; if $m > k (m < k)$ we have overidentification (underidentification)
- IV regression requires $m\geq k$

Exercise
$$\hat{\rho}=\rho+\frac{\frac{1}{n}\sum\limits^n_{i=1}(z_i-\overline{z})(\varepsilon_i-\overline{\varepsilon})}{\frac{1}{n}\sum\limits^n_{i=1}(s_i-\overline{s})(z_i-\overline{z})}$$
	Solution:
	$Y_i=\alpha+\rho s_i+\varepsilon_i \Rightarrow \overline{Y}=\alpha+\rho\overline{s}+\overline{\varepsilon}$
	$\hat{\rho}=\frac{\sum (Y_i-\overline{Y})(z_i-\overline{z})}{\sum (s_i-\overline{s})(z_i-\overline{z})}=\frac{\sum [\rho(s_i-\overline{s})+(\varepsilon-\overline{\varepsilon})](z_i-\overline{z})}{\sum (s_i-\overline{s})(z_i-\overline{z})}=\rho+\frac{\frac{1}{n}\sum\limits^n_{i=1}(z_i-\overline{z})(\varepsilon_i-\overline{\varepsilon})}{\frac{1}{n}\sum\limits^n_{i=1}(s_i-\overline{s})(z_i-\overline{z})}$
By LLN, $\frac{1}{n}\sum\limits^n_{i=1}(z_i-\overline{z})(\varepsilon_i-\overline{\varepsilon})\mathop{\longrightarrow}\limits^{\mathbb{P}}\mathbf{Cov}(z,\varepsilon)=0,\frac{1}{n}\sum\limits^n_{i=1}(s_i-\overline{s})(z_i-\overline{z})\mathop{\longrightarrow}\limits^{\mathbb{P}}\mathbf{Cov}(s,z)\neq0$
Thus, the IV estimator is valid: $\hat{\rho}\mathop{\longrightarrow}\limits^{\mathbb{P}}\rho$

However, the OLS estimator, denoted by $\tilde{ρ}$ is not valid in the presence of an endogenous variable:
$$\begin{align}
\tilde{\rho}&=\frac{\sum^n_{i=1}(Y_i-\overline{Y})(s_i-\overline{s})}{\sum^n_{i=1}(s_i-\overline{s})^2}=\rho+\frac{\frac{1}{n}\sum^n_{i=1}(s_i-\overline{s})(\varepsilon_i-\overline{\varepsilon})}{\frac{1}{n}\sum^n_{i=1}(s_i-\overline{s})^2}\\
&\mathop{\rightarrow}\limits^{\mathbb{P}}\rho+\frac{\mathbf{Cov}(s,\varepsilon)}{\mathbf{Var}(s)}\neq \rho\text{ if }\mathbf{Cov}(s,\varepsilon)\neq 0
\end{align}$$

Therefore, IV estimator is valid (consistent) in the presence of an endogenous variable while OLS is not valid (inconsistent) 
However, if there is no endogeneity issue, both estimators are valid 
But can we distinguish the two estimators? 
Let’s consider another measure of the estimator quality, the **variance**

To see this, we note $\hat{\rho}-\rho=\frac{\sum^n_{i=1}(z_i-\overline{z})\varepsilon_i}{\sum^n_{i=1}(s_i-\overline{s})(z_i-\overline{z})}$
The variance of $\hat{ρ}$ is given by $\mathbb{E}\Big((\hat{\rho}-\rho)^2\Big)$
To simplify the analysis, let’s treat $z$ and $s$ nonrandom

Then, since $\varepsilon$ is an i.i.d. sequence, we have given all $s$ and $z$ that ==这里其实没懂==
$$\mathbb{E}\Big((\hat{\rho}-\rho)^2\Big)=\frac{\sigma^2_{\varepsilon}\sum\limits^n_{i=1}(z_i-\overline{z})^2}{\big(\sum\limits^n_{i=1}(s_i-\overline{s})(z_i-\overline{z})\big)^2}$$
Similarly we have $\tilde{\rho}-\rho=\frac{\sum\limits^n_{i=1}(s_i-\overline{s})\varepsilon_i}{\sum\limits^n_{i=1}(s_i-\overline{s})^2}$
We can show $\mathbb{E}\Big((\tilde{\rho}-\rho)^2\Big)=\frac{\sigma^2_{\varepsilon}}{\sum\limits^n_{i=1}(s_i-\overline{s})^2}$

Thus, the ration of the variance of $\tilde{\rho}$ and $\hat{\rho}$ is given by
$$\frac{\big(\sum\limits^n_{i=1}(s_i-\overline{s})(z_i-\overline{z})\big)^2}{\sum\limits^n_{i=1}(s_i-\overline{s})\sum\limits^n_{i=1}(z_i-\overline{z})}=r^2_{sz}<1$$
where $r_{sz}$ is the sample correlation of $s$ and $z$ ==这一部分其实也没懂==
Thus, the IV estimator has large variance, i.e., lower precision

### [STATA Code](https://www.economics.utoronto.ca/blanchenay/stata/Blanchenay_StataHowTo_InstrumentalVariables.pdf)
1. Basic syntax
The command for performing a estimation based on instrumental variables using two-stage least squares is ivregress 2sls.
```
ivregress 2sls y (x = z), robust
```
where 𝑦 is our dependent variable, 𝑥 is our initial explanatory variable, and 𝑧 is the variable we use to instrument for 𝑥. 
If instead of one, we have two instruments 𝑧1 and 𝑧2 for variable 𝑥, we would instead run:
```
ivregress 2sls y (x = z1 z2), robust
```

2. Additional controls
Naturally, we can also include control variables in the IV estimation. If residuals still depend on 𝑥 after controlling for $𝑤_1$ and $𝑤_2$,  we would run:
```
ivregress 2sls y (x = z1 z2) w1 w2, robust
```
As with OLS regressions, we can easily turn a categorical variable into a series of dummies using the i. operator:
```
ivregress 2sls y (x = z1 z2) w1 w2 i.group, robust
```

3. Example
Let’s use the auto. We use it to see how car prices (price) depends on their range, measured in miles-per-gallon (mpg).
```
sysuse auto, clear // Clears memory and loads a default dataset included in Stata
```

```
ivregress 2sls price (mpg=weight), robust
```
And if we still want to control for domestic versus foreign cars:
```
ivregress 2sls price (mpg=weight) i.foreign, robust
```
![Pasted image 20231106164230](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031710543.png)

### Real Data Example and Analysis: How does fertility affect labor supply?
Angrist, J. D., & Evans, W. N. (1998). Children and Their Parents’ Labor Supply: Evidence from Exogenous Variation in Family Size. American Economic Review, 88(3), 450-477.
```
D:\All Document\Msc\Econometric
```

The research question is: how much does a woman’s labor supply fall when she has an additional child
Data: married women from the 1980 U.S. Census, data set contains information on married women aged 21–35 with two or more children

### Using Geographic Variation in College Proximity to Estimate the Return to Schooling
Card, D. (1993). “Using Geographic Variation in College Proximity to Estimate the Return to Schooling.” National Bureau of Economic Research.
```
D:\All Document\Msc\Econometric
```

### The effect of family size and birth order on children’s education
Black, S. E., Devereux, P. J., & Salvanes, K. G. (2005). The more the merrier? The effect of family size and birth order on children’s education. Quarterly Journal of Economics, 120(2), 669-700.
```
D:\All Document\Msc\Econometric
```

## Panel Data Models
Panel data set: we have multiple observations for each individual at different time periods
Instead of $Y_i=\mathbf{x}'_{i}\beta+\varepsilon_i$, we have time indices as well
$$Y_{it}=\mathbf{x}'_{it}\beta+\varepsilon_{it}\tag{1}$$
If we assume $c_i$ is constant cross time periods, e.g., ability is close to a constant at least in a short period of time
$(1)$ becomes
$$Y_{it}=+c_i+\varepsilon_{it}$$
Thus, for any two periods, $t, s$, we have
$$\begin{align}
Y_{it}=\mathbf{x}'_{it}+c_i+\varepsilon_{it}\\
Y_{is}=\mathbf{x}'_{is}+c_i+\varepsilon_{is}
\end{align}$$
If we take a difference,
$$Y_{it}-Y_{is}=(\mathbf{x}_{it}-\mathbf{x}_{is})'\beta+\varepsilon_{it}-\varepsilon_{is}$$
We get rid of $c_i$
Li Zhen 6/11/2023: $\varepsilon_{it}-\varepsilon_{is}$ might not be i.i.d.($\varepsilon_{it}-\varepsilon_{i(t-1)}$ and $\varepsilon_{it-1}-\varepsilon_{it-2}$) Therefore, the standard deviation of $\beta$ will be larger. The $\beta$ itself is accurate. The confidence interval will be larger. 

An Motivating Example: Fataility Rates and Taxes on Alcohol
Studies show that drunk drivers have 13 times higher chances to have a fatal crash 
Basic economic theory says increased taxes will discourage consumption 
So taxes on beers v.s. fatality rates?

A panel data model:
$\text{FatalityRate}_{it}=\beta_0+\beta_1 \text{BeerTax}_{it}+c_i+\varepsilon_{it}$
- $c_i$ is the unobserved effect of state $i$ that affects fatality rate 
- Example of ci is local cultural attitude toward drinking and driving 
- $c_i$ will not change over time 
$c_i$ can be eliminated:
$$\begin{align}
\text{FatalityRate}_{i1988}-&\text{FatalityRate}_{i1982}=\\
&\beta_1(\text{BeerTax}_{i1988}-\text{BeerTax}_{i1982})+\varepsilon_{i1988}-\varepsilon_{i1982}
\end{align}$$
Panel data consist of observations on the same $n$ entities, or individuals, or units at two or more time periods $T$ 
Observations: $(x_{it},Y_{it}),i=1,2,\dots,n;t=1,2,\dots,T$
If we do not miss any value of $(x_{it},Y_{it}),i=1,2,\dots,n;t=1,2,\dots,T$, we have a **balanced panel**

We usually assume $n\rightarrow \infty$ while $T$ is fixed for the asymptotic(渐进的) framework
We assume random sampling for the cross section data, that is, for each fixed $t$, $(x_{it},Y_{it}),i=1,2,\dots,n$  are randomly drawn, $(x_{it},Y_{it})$ is independent of $(x_{jt},Y_{jt})$ for $i\neq j$

The model of unobserved individual effect is:
$$Y_{it}=\mathbf{x}'_{it}\beta+c_i+\varepsilon_{it}$$
where
1. $x_{it}$ is a $K\times1$ vector of observable variables that may change across $t$ or $i$
2. $c_i$ is the unobserved effect, or individual heterogeneity; it’s fixed across $t$
3. $\varepsilon_{it}$ is the idiosyncratic error

The individual effect $c_i$ is fixed for each individual, justifies the fixed effect model 
However, it does not mean $c_i$ is nonrandom or a constant 
In particular, it can be arbitrarily correlated with $x$ 
Another popular model of panel data is the random effect model
$c_i$ is a random variable from a distribution, and $c_i \perp \{\varepsilon_{it},x_{it}\}$

In a random effect model, $Y_{it}=\mathbf{x}'_{it}\beta+\tilde{\varepsilon}_{it}$, where $\tilde{\varepsilon}_{it}=c_i+\varepsilon_{it}$
Exercise
Show that $\mathbf{Cov}(\tilde{\varepsilon}_{it},\tilde{\varepsilon}_{is})\neq0$ for $t\neq s$
	Solution:
	$\tilde{\varepsilon}_{it}=c_i+\varepsilon_{it}$
	$\tilde{\varepsilon}_{is}=c_i+\varepsilon_{is}$
	If $\mathbf{Cov}(\tilde{\varepsilon}_{it},\tilde{\varepsilon}_{is})=0$, then $t\neq s$ and $i\neq j$

In the presence of serial correlation, the OLS is not the “best” one 
One can proceed with the generalized least square (GLS)

The random effects assumption (made in a random effects model) is that the **individual specific effects are uncorrelated with the independent variables**. The fixed effect assumption is that the individual specific effect is correlated with the independent variable

对于面板数据来说，通常使用[[Econometrics#[Hausman Test](https //zhuanlan.zhihu.com/p/457740001)\|hausman检验]]来判断使用固定效应模型或者随机效应模型
	TA: 一般不怎么用random effect
	个人感觉在什么情况下使用random effect还是值得多想想



### Within and First-Difference Estimators
Now we briefly discuss the estimation strategy of panel data models with fixed effects 
The general idea is to take differences to eliminate $c_i$ before using OLS 
The first difference:
	Notation: $\Delta Y_{it}=Y_{it}-Y_{i,t-1}$
	Apply OLS on $\{\Delta Y_{it},\Delta X_{it}\}:\Delta Y_{it}=\Delta \mathbf{x}'_{it}\beta+\Delta \varepsilon_{it}$
	Why does OLS work?
The within estimator:
	Notation: $\tilde{Y}_{it}=Y_{it}-\overline{Y}_i$ where $\overline{Y}_i=\frac{1}{T}\sum\limits^T_{t=1}Y_{it}$
	Apply OLS on $\{\tilde{Y}_{it},\tilde{X}_{it}\}:\tilde{Y}_{it}=\tilde{\mathbf{x}}_{it}\beta+\tilde{\varepsilon}_{it}$
	Why does OLS work?

Exercise Show that the first difference estimator and the within estimator are the same if $T=2$
	Solution:
	We have $Y_{i1},Y_{i2},X_{i1},X_{i2}$
	FD: $\{Y_{i1}-Y_{i2},X_{i1}-X_{i2}\}$
	WE: $\overline{Y}_i=\frac{Y_{i1}+Y_{i2}}{2}$ $\tilde{Y}_{i1}=\frac{Y_{i1}-Y_{i2}}{2}$ $\tilde{Y}_{i2}=\frac{Y_{i2}-Y_{i1}}{2}$
	The data set of WE is just half of FD, so the regression result will be the same

In an panel data model, OVB at the individual levels is captured by $c_i$ 
There are some unobserved effects, or omitted variables that may change over time, but fixed across individuals, e.g., nationwide or state wide change of polices It calls for a **time fixed effect** denoted by, say, $δ_t$

Thus, a complete model with both fixed individual and time effects is
$$Y_{it}=\mathbf{x}'_{it}\beta+c_i+\delta_t+\varepsilon_{it}\tag{3}$$
How to perform estimation? Use the same differencing strategy

Denote $\overline{Y}_t=\frac{1}{n}\sum\limits^n_{i=1} Y_{it}$ similar notations apply to $x, ε$ as well
We have $\overline{Y}_t=\overline{x}'_t+\beta+\overline{c}+\delta_t+\overline{\varepsilon}_t$ where $\overline{c}=\frac{\sum\limits^n_{i=1}c_i}{n}$
Now $\delta_t$ is eliminated by
$$Y_{it}-\overline{Y}_t=(\mathbf{x}_{it}-\overline{\ \mathbf{x}_t})'\beta+c_i-\overline{c}+\varepsilon_{it}-\overline{\varepsilon}_t$$
We can proceed to eliminate the individual effect $c_i$ as we did before

### SHOOTING DOWN THE MORE GUNS, LESS CRIME HYPOTHESIS
```
D:\AllDocument\Msc\Econometric
```

felony convictions 严重犯罪
“Shall-issue” laws exist in certain U.S. states 
They mandate concealed gun carry permits for eligible applicants 
Eligibility typically includes citizenship, mental competence, and no felony convictions 
Some states have additional restrictions

Proponents believe these laws deter crime 
Critics argue they could increase crime due to accidental or spontaneous use 
We will analyze the effect of concealed weapons laws on violent crime

The dataset is a balanced panel data on 50 US states and the District of Columbia, spanning the years 1977 to 1999 
Each observation represents a specific state in a given year, leading to a total of 1173 observations 
The dataset is obtained from a research paper by John Donohue of Stanford University and were used in his research paper with Ian Ayres titled “Shooting Down the ‘More Guns Less Crime’ Hypothesis”

简单回归的结果
Shall-issue law reduces violent crime by 44%!

The “evidence” of more guns, less crime is spurious and most likely is due to omitted variable bias No statistically significant evidence that concealed weapons laws have any effect on crime rates


### Difference-in-Difference Estimator
We have reviewed regression models with dummy variables 
Quite often, the dummy variable represents some treatment effect 
1. $D_i =1$ for college degree holders and 0 for non-holders 
2. $D_i=1$ for if individual i receives job market training 0 otherwise 
The coefficient of the binary variable (or the interaction term of the binary variable with other variables) captures the treatment effect

Now we consider a binary variable in a panel data setting
$$D_{it}=\left\{\begin{array}{**lr**} 1\quad \text{if individual i receives treatment in period }0\\ 0\quad \text{otherwise}\end{array}   \right.$$
Consider a fixed effect model
$$Y_{it}=\phi D_{it}+c_i+\delta_t+\varepsilon_{it}$$

$c_i$ can be eliminated by taking differences:
$$\Delta Y_{it}=\phi \Delta D_{it}+\delta_t-\delta_{t-1}+\Delta \varepsilon_{it}$$
Some individuals are treated in time t and some not

Thus, for the treated group, we have
$$\Delta Y^{tr}_{it}=\phi+\delta^{tr}_{t}-\delta^{tr}_{t-1}+\Delta \varepsilon^{tr}_{it}$$
and for the untreated group
$$\Delta Y^{ut}_{it}=\delta^{ut}_{t}-\delta^{ut}_{t-1}+\Delta \varepsilon^{ut}_{it}$$
If we can assume the common trend:
$\delta^{tr}_{t}-\delta^{tr}_{t-1}=\delta^{ut}_{t}-\delta^{ut}_{t-1}$
$$\Delta Y^{tr}_{it}-\Delta Y^{ut}_{it}=\phi+\Delta \varepsilon^{tr}_{it}-\Delta \varepsilon^{ut}_{it}$$
Of course, we can have a richer model by adding other covariants $x_{it}$

### Minimum Wages and Employment: A Case Study of the Fast-Food Industry in New Jersey and Pennsylvania
```
D:\AllDocument\Msc\Econometric
```
Prof. Li Zhen's favorite paper 

Conclusion:
Contrary to the central prediction of the textbook model of the minimum wage, but consistent with a number of recent studies based on cross-sectional time-series comparisons of affected and unaffected markets or employers, we find no evidence that the rise in New Jersey's minimum wage reduced employment at fast-food restaurants in the state.
Finally, we find that prices of fast-food meals increased in New Jersey relative to Pennsylvania, suggesting that much of the burden of the minimum-wage rise was passed on to consumers. 
### Regression Discontinuity Design
$$Y_i=\beta_0+\beta_1 X_i+\varepsilon_i$$
We assume if $X$ moves continuously, the effect of changes of $X$ on $Y$ is constant (on average), captured by $β_1$:
$$dY=\beta_1 dX$$
E.g., $Y$ is the starting salary and $X$ is the GPA of a fresh graduate 
However, as the GPA moves smoothly, the degree classification jumps 
E.g., at CUHK, if you GPA is 3.50, you get 1st class honors; if your GPA is 3.49, you get 2nd upper 
What is your expected salary increment if you improve your GPA from 3.48 to 3.49? What about from 3.49 to 3.50?

Let $D_i$ be a dummy or binary variable, with $D_i = 1$ or $0$ 
Consider a simple linear regression $Y_i=\beta_0+\rho D_i+\varepsilon_i$
Assume $\mathbb{E}(\varepsilon_i|D_i)=0$, we have
$$\mathbb{E}(Y_i|D_i=1)=\beta_0+\rho$$
and
$$\mathbb{E}(Y_i|D_i=0)=\beta_0$$
Interpretation: If $Y$ is salary and $D_i=1$ for female and $D_i =0$ for male, $β_0 +ρ$ is the average salary for females and $ρ$ is the salary difference of being a female

Let $X_i$ be a regressor, e.g., education,
$$Y_i=\beta_0+\rho D_i+\beta_1X_i+\varepsilon_i$$
We have
$$\mathbb{E}(Y_i|D_i=1,X_i)=\beta_0+\rho+\beta_1 X_i$$
and
$$\mathbb{E}(Y_i|D_i=0,X_i)=\beta_0+\beta_1X_i$$
Interpretation: We have two regression lines for the two groups (e.g., female and male) with different intercept terms 
The two groups have the same slope coefficient — the same effect of education on income

Interpretation: We have two regression lines for the two groups (female and male) with different intercept terms and slopes The effects of education on income may be different for the two groups

Next, we include an interaction term, $D_i$ $X_i$
$$Y_i = β_0 + ρD_i +β_1X_i + β_2D_iX_i + ε_i$$
We have
$$\mathbb{E}(Y_i|D_i=1,X_i)=\beta_0+\rho+(\beta_1+\beta_2)X_i$$
and
$$\mathbb{E}(Y_i|D_i=0,X_i)=\beta_0+\beta_1X_i$$
Interpretation: We have two regression lines for the two groups (female and male) with different intercept terms and slopes 
The effects of education on income may be different for the two groups

Now we consider a dummy variable that is dependent on $X$ 
Let $D_c$ be a function of the regressor $X_i$ , such that
$$D_c(X_i)=\left\{\begin{array}{**lr**} 1\quad \text{if }X_i\geq c\\ 0\quad \text{if }X_i< c\end{array}   \right.$$
Thus, $D_c$ is an indicator of the regressor that exceeds a threshold c

Now consider
$$Y_i=\beta_0+\rho D_c(X_i)+\beta_1X_i+\varepsilon_i$$
We have
$$\begin{align} &\mathbb{E}(Y_i|X_i\geq c)=\beta_0+\rho+ \beta_1X_i\\
&\mathbb{E}(Y_i|X_i\geq c)=\beta_0+ \beta_1X_i
\end{align}$$
We observe a “jump” of size $ρ$ when $X$ moves above $c$
$ρ$ captures the treatment effect we are interested in Such treatment occurs when $X$ moves cross the threshold $c$
![Pasted image 20231120165059](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031710544.png)

We could extend the model further; now consider
$$Y_i=\beta_0+\rho D_c(X_i)+\beta_1 X_i+\beta_2 X^2_i+\varepsilon_i$$
We have
$$\begin{align} &\mathbb{E}(Y_i|X_i\geq c)=\beta_0+\rho+ \beta_1X_i+\beta_2 X^2_i\\
&\mathbb{E}(Y_i|X_i\geq c)=\beta_0+ \beta_1X_i+\beta_2 X^2_i
\end{align}$$
By including a quadratic term, we have a more flexible way to model the relation of $Y$ and $X$ before and after the treatment
![Pasted image 20231120165123](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031710545.png)

We consider another extension of the model: we would like to have different intercept terms and slopes 
This can be achieved by including an interaction term:
$$Y_i=\beta_0+\rho D_c(X_i)+\beta_1X_i+\beta_2D_c(X_i)X_i+\varepsilon_i$$
We have
$$\begin{align} &\mathbb{E}(Y_i|X_i\geq c)=(\beta_0+\rho)+(\beta_1+\beta_2)X_i\\
&\mathbb{E}(Y_i|X_i\geq c)=\beta_0+ \beta_1X_i
\end{align}$$
![Pasted image 20231120165152](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031710546.png)
You may note that the jump size, or the treatment effect in the previous plot is not close to $ρ=1$

Exercise
Let $δ > 0$. Show that
$$\lim_{\delta\downarrow0}\mathbb{E}(X_i=c+\delta)-\mathbb{E}(Y_i|X_i=c-\delta)=\rho+\beta_2c$$
	Solution:
	$\mathbb{E}(X_i=c+\delta)=(\beta_0+\beta_1)(c+\delta)$
	$\mathbb{E}(Y_i|X_i=c-\delta)=\beta_0+\beta_1(c-\delta)$
	$\lim_{\delta\downarrow 0}=\rho+\beta_2 c+2\beta_1 \delta+\beta_2\delta$
	When $\delta\rightarrow 0$, $=\rho+\beta_2 c$

Note that by comparing the differences of the conditional means of Y on X that barely above the threshold $c (X = c +δ)$ and on X that is slightly below $c (X = c ´-δ)$ will not identify the treatment effect $ρ$
...unless the threshold value $c = 0$

Thus, we may consider to regress on $\tilde{X}_i =X_i - c$ instead 
What is the cut-off point for $\tilde{X}$?

We revise the regression model:
$$Y_i=\tilde{\beta}_0+\rho D_0(\tilde{X}_i)+\beta_1 \tilde{X_i}+\beta_2 D_0(\tilde{X_i})\tilde{X}_i+\varepsilon_i$$
Exercise
Show that $\lim\limits_{\delta\downarrow 0}\mathbb{E}(Y_i|\tilde{X_i}=\delta)-\mathbb{E}(Y_i|\tilde{X}_i=-\delta)=\rho$
	Solution:
	$\mathbb{E}(Y_i|\tilde{X}_i=\delta)=(\tilde{\beta}_0+\rho)+(\beta_1+\beta_2)\delta$
	$\mathbb{E}(Y_i|\tilde{X}_i=-\delta)=\tilde{\beta}_0-\beta_1\delta$
	 $\therefore \lim\limits_{\delta\downarrow 0}\mathbb{E}(Y_i|\tilde{X_i}=\delta)-\mathbb{E}(Y_i|\tilde{X}_i=-\delta)=\rho$
	Prof. Li Zhen 要这么减掉threshold 是因为quadratic form的存在，如果是linear function的话则不需要这个操作。还提到这个和Taylor Series有点像，我们去approximate一个函数的时候往往设定$x=0$
	2023/11/20 我的理解是既然原来的effect is $\rho+\beta_2 c$,那剪掉一个$c$ 就好了

The regression we have introduced is the sharp regression discontinuity 
The treatment is a deterministic and discontinuous function of the regressor $X$:
$$D_c(X_i)=\left\{\begin{array}{**lr**} 1\quad \text{if }X_i\geq c\\ 0\quad \text{if }X_i< c\end{array}   \right.$$
Denote the potential outcome
$$Y_i=\left\{\begin{array}{**lr**} Y_{0i}\quad \text{if }D_c(X_i)=0\\ Y_{1i}\quad \text{if }D_c(X_i)=1\end{array}   \right.$$
That is, $Y_i=Y_{0i}+(Y_{1i}-Y_{0i})D_c(X_i)$

The simple way to have different CEFs is to use the interaction terms ==其实这句话没懂,，感觉去掉intersection问题也不大== 
11/27 Pro. Li Zhen 在线性的情况下确实没影响，但是quadratic的情况就必须加intersection
自己感觉是加入intersection可以让两部分人本身的function就不同，这样更加有利于拟合

Exercise 
Verify that for the nonlinear CEF
$$\begin{align}Y_i=\beta_0&+\rho D_0(\tilde{X}_i)+\beta_1 \tilde{X}_i+\beta_2 D_0 (\tilde{X}_i)\tilde{X}_i\\
&+\beta_3\tilde{X}_i^2+\beta_4D_0(\tilde{X}_i)\tilde{X}^2_i+\varepsilon_i
\end{align}$$
we have $\lim_{x\downarrow c}\mathbb{E}(Y_i|X_i=x)-\lim_{x\uparrow c}\mathbb{E}(Y_i|X_i=x)=\rho$
	Solution:
$$Y_i=\left\{\begin{array}{**lr**} \beta_0+\beta_1\tilde{X}_1+\beta_3 \tilde{X}^2_1\quad \text{if }x_i<0\Leftrightarrow \tilde{X}_i<0\\ \beta_0+\rho+(\beta_1+\beta_2)\tilde{X}_1+(\beta_3+\beta_4) \tilde{X}^2_1\quad \text{if }x_i>0\Leftrightarrow \tilde{X}_i>0\end{array}   \right.$$
	When $x\Rightarrow c$
	$x<c:\mathbb{E}(Y_i|X_i=X)=\beta_0$
	$x>c:\mathbb{E}(Y_i|X_i=X)=\beta_0+\rho$

(Optional) Imbens, G. W., & Lemieux, T. (2008). Regression discontinuity designs: A guide to practice. Journal of Econometrics, 142(2), 615-635.
```
D:\AllDocument\Msc\Econometric
```

### Fuzzy Regression Discontinuity Design
Recall the degree classification example 
Let $X=GPA$ and $c=3.50$ 
Let $D_c(X_i)=1$ if $X_i\geq c$ and 0 otherwise 
Thus $D_c(X_i)$ is the indicator of obtaining a first class honors degree 
You will get the 1st class honors for sure if your GPA exceeds the threshold, no uncertainty 
Now we consider a different indicator: $D_i=1$ if $i$ finds a job in the finance industry and 0 otherwise

Would you expect a deterministic relation of $D_i$ and $X_i$? 
Would you get the job for sure if you have a $GPA = 3.51$? 
Would you always get rejected if have a $GPA =3.49$?

A more reasonable way to model the scenario is as follows: For a given GPA $X_i$ , you have a certain chance, or probability $\mathcal(X_i)$ to get the job


A more reasonable way to model the scenario is as follows: For a given GPA $X_i$ , you have a certain chance, or probability $\mathcal{P}(X_i)$ to get the job

$$\mathbb{E}(D_i=1|X_i)=\left\{\begin{array}{**lr**} \mathcal{P}_1(X_i)\quad \text{if }X_i\geq c\\ \mathcal{P}_0(X_i)\quad \text{if }X_i< c\end{array}   \right.$$
with $\mathcal{P}_1(c)>\lim_{x\uparrow c}\mathcal{P}_0(x)$

$ρ_{FRD}$ is defined as follows
$$\rho_{FRD}=\frac{\lim_{x\downarrow c}\mathbb{E}(Y_i|X_i=x)-\lim_{x\uparrow c}\mathbb{E}(Y_i|X_i=x)}{\lim_{x\downarrow c}\mathcal{P}_1(x)-\lim_{x\uparrow c}\mathcal{P}_0(x)}$$
{ #RhoFRD}


In sharp regression discontinuity design, $\lim_{x\downarrow c}\mathcal{P}_{1}(x)=1$ and $\lim_{x\uparrow c}\mathcal{P}_0(x)=0$, $\rho_{FRE}$ reduces to
$$\lim_{x\downarrow c}\mathbb{E}(Y_i|X_i=x)-\lim_{x\uparrow c}\mathbb{E}(Y_i|X_i=x)$$

Recall in the Sharp Regression Discontinuity (SRD) design, we let $\mathbb{E}(Y_{0i}|X_i)=f_0(X_i),\mathbb{E}(Y_{1i}|X_i)=f_1(X_i)$
The treatment effect is given by
$$\rho=\lim_{x\downarrow c}f_1(x)-\lim_{x\uparrow c}f_0(x)$$

#### Estimation: Local Linear Regression(LLR)
What if the patterns before and after the cutoff point are nonlinear? 
The idea: approximate the nonlinear patterns by linear functions 
But we should try to make the approximations in a neighbourhood of the cutoff point 
The method is called Local Linear Regression (LLR)

Given the cutoff point $c$, we select a distance $h$
To get the linear approximation before $c$, we do the following
$$\min_{\delta_0,\theta_0}\sum_{i:c-h<X_i<c}(Y_i-\delta_0-\theta_0(X_i-c))^2$$
To get the linear approximation after $c$, we do the following
$$\min_{\delta_1,\theta_1}\sum_{i:c\leq X_i<c+h}(Y_i-\delta_1-\theta_1(X_i-c))^2$$
The solutions of the above minimization problems are denoted by $\hat{\delta_0},\hat{\delta_1},\hat{\theta_0},\hat{\theta_1}$
An estimator of the treatment effect $\rho$ is given by
$$\hat{\rho}=\hat{\delta}_1-\hat{\delta}_0$$

Note that the estimates depend on the choice of $h$ 
1. There are some trade-off in selecting $h$ 
2. Small $h$ includes too few observations but also smaller approximation errors 
3. Large $h$ includes more observations but with potentially larger approximation errors 
4. There are rules to select the “optimal” $h$, which we don’t discuss here

Recall $$\rho_{FRD}=\frac{\lim_{x\downarrow c}\mathbb{E}(Y_i|X_i=x)-\lim_{x\uparrow c}\mathbb{E}(Y_i|X_i=x)}{\lim_{x\downarrow c}\mathcal{P}_1(x)-\lim_{x\uparrow c}\mathcal{P}_0(x)}$$
We have applied LLR to estimate the numerator
The idea: we can apply LLR to estimate the denominator as well, and $ρ_{FRD}$ can be estimated by the two ratios

#### An IV Interpretation of FRD
Now we will derive an alternative interpretation of FRD 
FRD becomes an IV estimation in a small neighbourhood around the cutoff point, where the treatment $D_i$ is endogenous
We will show the IV estimate is numerically identical to $\rho_{FRD}$

Suppose we would like to know the market value of a finance job We work with the following regression model:
$$Y_i=\beta_0+\rho D_i+\beta_1\tilde{X}_i+\beta_2D_i\tilde{X}_i+\varepsilon_i$$
where
1. $D_i$ is the indicator that individual $i$ works in the finance industry
2. We have a control variable $\tilde{X}_i$ is the excess $GPA$, i.e., real $GPA-c$ where $c=3.5$
3. $Y_i$ is the wage

$D_i$ is likely to be endogenous: individuals with strong monetary incentives may self-select into finance industry, a typically highly paid industry 
In other words, the random error εi contains monetary incentive which is correlated with the choice to get a finance job $(D_i)$

Let’s consider an instrumental variable (IV) of $D_i$ : the 1st Class Honours Degree indicator $D_c(X_i)$ or $D_0(\tilde{X}_i)$
Is $D_c(X_i)$ correlated with $D_i$? (Recall the job AD) 
Is $D_c(X_i)$ correlated with other factors in $ε_i$ , in particular monetary incentives? (Recall $X_i$ is a proxy of individual’s “ability”, already included in the regression)

Let’s consider the two-stage least squares (TSLS) estimation 
First stage: we regress the endogenous variable $D_i$ on the instrumental variable $D_0(\hat{X}_i)$ and the exogenous variable $\hat{X}_i$
$$D_i=\beta'_0+\rho'D_0(\hat{X}_i)+\beta'_1\hat{X}_i+\beta'_2D_0(\hat{X}_i)\hat{X}_i+\varepsilon'_i$$
We get the predicted $D_i$
$$\hat{D}_i\approx \mathbb{E}(D_i|X_i)=\beta'_0+\rho'D_0(\hat{X}_i)+\beta'_1\tilde{X}_i+\beta'_2D_0(\tilde{X}_i)\tilde{X}_i$$
We are more concerned with $X_i$ close to $c$, say
$X_i\in(c-\delta,c+\delta)$, we know $\tilde{X}_i(-\delta,\delta)\approx 0$
Therefore, we have the approximation
$$\hat{D}_i\approx \mathbb{E}(D_i|X_i\in(c-\delta,c+\delta))\approx \beta'_0+\rho'D_0(\tilde{X}_i)$$
In the second stage: we replace $D_i$ by $\hat{D}_i$ in
$$Y_i=\beta_0+\rho D_i+\beta_1 \tilde{X}_i+\beta_2D_i\tilde{X}_i+\varepsilon_i$$

Exercise ==这一张没看懂，晚点看看== 看懂了
Show that
$$Y_i=\lambda_0+\varrho D_0(\tilde{X}_i)+\lambda_1 \tilde{X}_i+\lambda_2 D_0(\tilde{X}_i)\tilde{X}_i+\varepsilon_i$$
where
$$\lambda_0=\beta_0+\rho \beta'_0,\varrho=\rho\rho',\lambda_1=\beta_1+\beta_2\beta'_0,\lambda_2=\beta_2\rho'$$
	Solution:
	$\because \hat{D}_i\approx \mathbb{E}(D_i|X_i\in(c-\delta,c+\delta))\approx \beta'_0+\rho'D_0(\tilde{X}_i)$
	$\therefore Y_i=\beta_0+\rho \big(\beta'_0+\rho'D_0(\tilde{X}_i)\big)+\beta_1 \tilde{X}_i+\beta_2\big(\beta'_0+\rho'D_0(\tilde{X}_i)\big)\tilde{X}_i+\varepsilon_i$
	$\Rightarrow Y_i=\beta_1+\rho\beta'_0+\rho\rho'D_0(\tilde{X}_i)+(\beta_1+\beta_2\beta_0)\tilde{X}_i+\rho'\beta_2\tilde{X}_i+\varepsilon_i$
	Based on $\lambda_0=\beta_0+\rho \beta'_0,\varrho=\rho\rho',\lambda_1=\beta_1+\beta_2\beta'_0,\lambda_2=\beta_2\rho'$
	We got $Y_i=\lambda_0+\varrho D_0(\tilde{X}_i)+\lambda_1 \tilde{X}_i+\lambda_2 D_0(\tilde{X}_i)\tilde{X}_i+\varepsilon_i$

Therefore, to estimate $ρ$, we first get an estimator of $ρ'$ (via LLR), say $\hat{ρ}'$ in the first stage and get an estimator of $\varrho$ (via LLR), say $\hat{\rho}$ in the second stage, an estimator of ρ is given by
$$\hat{\rho}=\frac{\hat{\varrho}}{\hat{\rho}'}$$
Therefore, $\hat{ρ}$ is numerically the same as $\hat{ρ}_{FRD}$

(Optional) Imbens, G. W., & Lemieux, T. (2008). Regression discontinuity designs: A guide to practice. Journal of Econometrics, 142(2), 615-635.
```
D:\AllDocument\Msc\Econometric
```

### Binary Outcome Models
Let’s review some properties of binary variables
Suppse $Y$ satisfies
$$Y=\left\{\begin{array}{**lr**} 1\quad \text{probability }p\\ 0\quad \text{probability }1-p\end{array}   \right.$$
Then $\mathbb{E}(Y)=p=\mathbb{P}(Y=1),\mathbf{Var}(Y)=p(1-p)$

In a Linear Probability Model (LPM) for Binary Variables
$$Y_i=\mathbf{x}'_i\beta+\varepsilon_i$$
where $\mathbf{x}_i=(1,x_{i1},\dots,x_{ik}),\beta=(\beta_0,\beta_1,\dots,\beta_k)'$

这个模型很好，但是对于binary的情况解释性不足，所以要引入nonlinear model
![202312031719519.png (416×267) (raw.githubusercontent.com)](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031719519.png)

(Optional) Bertrand, M., & Mullainathan, S. (2004). Are Emily and Greg more employable than Lakisha and Jamal? A field experiment on labor market discrimination. American Economic Review, 94(4), 991-1013
```
D:\AllDocument\Msc\Econometric
```

### Exercise Set 2
Exercise 1. Let’s consider a straightforward model designed to estimate the impact of owning a personal computer (PC) on the grade point average of graduating seniors at a large public university:
$$GPA=\beta_0+\beta_1 PC+u$$
where PC is a binary variable representing PC ownership. 
(i) What might cause PC ownership to be correlated with $u$? 
(ii) Please elaborate on why PC is likely to be associated with parents’ yearly income. Does this imply that parental income serves as a good instrumental variable (IV) for PC? Please explain your reasoning. 
(iii) Assume that, four years prior, the university provided grants to approximately half the incoming students to purchase computers, with the recipients chosen randomly. Could you provide a detailed explanation of how you might use this information to create an instrumental variable for PC?

Exercise 2. A student of Econ 5122 collects data about the housing prices and floor areas in Jinan in 2016. He aims to replicate the study discussed in class to evaluate the return of an urban hukou in China, using the regression discontinuity design approach. Let $S'_i = S_i-90$, where $S_i$ is the floor area of flat $i$. Let $\mathbf{X}_i$ be all house characteristics except the floor area, and $P_i$ be the housing price.
(i) The student runs two linear regressions:
$$P_i=\alpha_0+\alpha_1S'_i+\mathbf{X}'_i\beta+u_i$$
for $S'_i<0$ and
$$P_i=\gamma_0+\gamma_1S'_i+\mathbf{X}'_i\theta+u_i$$
for $S'_i\geq 0$. Let $\hat{\alpha}_0,\hat{\alpha}_1,\hat{\gamma}_0,\hat{\gamma}_1,\hat{\beta},\hat{\theta}$ be the estimates of the coefficients of the two models. Explain how one could estimate the treatment effect at $S_i = 90$ (or $S'_i = 0$) using these estimates.
(ii) Let
$$D_i=\left\{\begin{array}{**lr**} 1\quad S'_i\geq 0\\ 0\quad S'_i\leq 0\end{array}   \right.$$
Now consider the following model
$$P_i=\alpha+\pi_1D_i+\pi_2S'_i+\pi_3D_i\cdot S'_i+\mathbf{X}'_i+u_i$$
Assume that $\mathbb{E}(u_i|S'_i,\mathbf{X}_i)=0$. Calculate $\mathbb{E}(P_i|S'_i\geq0,\mathbf{X}_i)$ and $\mathbb{E}(P_i|S'_i<0,\mathbf{X}_i)$
![Pasted image 20231129112206](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312031710548.png)
<center>Figure 1: Housing prices v.s. floor area</center>

(iii) Now consider the model
$$P_i=\alpha+\pi_1D_i+\pi_2S'_i+\pi_3D_i\cdot S'_i+\pi_4S'^2_i+\mathbf{X}'_i\beta+u_i$$
Assume that $\mathbb{E}(u_i|S'_i,\mathbf{X}_i)=0$. Calculate $\mathbb{E}(P_i|S'_i\geq 0,\mathbf{X}_i)$ and $\mathbb{E}(P_i|S'_i\leq 0,\mathbf{X}_i)$ . Is the model in (1) sufficient to capture the plots in Figure 1? If not, propose another model and discuss the conditions on the parameters so that the model can capture the patterns plotted in Figure 1.

# [Hausman Test](https://zhuanlan.zhihu.com/p/457740001)
```Stata
**豪斯曼检验
qui xtreg lny lnx1 lnx2 lnx4 lnx20 lnx25,fe //固定效应估计
est store FE //储存结果
qui xtreg lny lnx1 lnx2 lnx4 lnx20 lnx25,re //随机效应估计
est store RE //储存结果
hausman FE RE 
```
![Pasted image 20231113151957.png](/img/user/attachments/Pasted%20image%2020231113151957.png)
其结果如上表：由于p值为0.0000，故强烈拒绝原假设，应使用固定效应模型，而不是随机效应模型。但是很多时候计算出的统计量可能为负，这时候使用sigmamore或者stigmaless选项可以大大减少出现负值的可能性。
```Stata
hausman FE RE,constant sigmamore
```
![v2-a78ac127eee5eacfdefe8dff2e03539d_r.jpg (783×440) (zhimg.com)](https://pic2.zhimg.com/v2-a78ac127eee5eacfdefe8dff2e03539d_r.jpg)
由结果可知加入sigmamore选项的结果与未加入选项的结果是一致的，故强烈拒绝原假设，应使用固定效应模型，而不是随机效应模型。

但是，如果聚类稳健标准误与普通标准误相差较大时，或者说数据存在异方差与自相关时，则传统的豪斯曼检验不适用，此时可以通过xtoverid命令使用稳健的豪斯曼检验，其stata命令如下：
```Stata
**稳健的豪斯曼检验
ssc install xtoverid
ssc install ivreg2
ssc install ranktest //安装相关命令
quietly xtreg lny lnx1 lnx2 lnx4 lnx20 lnx5,re r 
xtoverid
```
![v2-b1a7f8c480db3bffb3323573c1aa4f4c_720w.webp (720×421) (zhimg.com)](https://pic1.zhimg.com/80/v2-b1a7f8c480db3bffb3323573c1aa4f4c_720w.webp)
稳健的hausman检验结果
由图3结果可知，稳健的hausman检验p值为0.0000，故强烈拒绝原假设，使用固定效应模型。

在进行空间面板模型的hausman检验时本文以空间杜宾模型为例，进行相关检验：
```Stata
**Hausman检验
xtset id year //需先设定面板
*方法1
spatwmat using w0.dta,name(w0) standardize
xsmle lny lnx1 lnx2 lnx4 lnx20 lnx23 lnx26,model(sdm) wmat(w0) hausman nolog
*方法2
spatwmat using w0.dta,name(w0) standardize
xtset id year
qui xsmle lny lnx1 lnx2 lnx4 lnx20 lnx23 lnx26,wmat(w0) model(sdm) fe type(ind) nolog effects
est store sdm_fe
qui xsmle lny lnx1 lnx2 lnx4 lnx20 lnx23 lnx26,wmat(w0) model(sdm) re type(ind) nolog effects 
est store sdm_re
hausman sdm_fe sdm_re
```
![v2-98dbc80bdc769d1aba4de8f1c58e2ca4_720w.webp (720×450) (zhimg.com)](https://pic1.zhimg.com/80/v2-98dbc80bdc769d1aba4de8f1c58e2ca4_720w.webp)
如果按照方法二出现负值，而其结果较大，网上的一些意见是拒绝随机效应模型的原假定，使用固定效应模型，也可以更换变量或模型形式。或者通过方法一进行计算，但是这个命令有点奇怪，用同样的变量，p值有时候能出来有时候出不来，建议不经意间多运行几次，实在不行就随缘吧！
![v2-685ba53b1fdded112be8fbb9a07f79d0_r.jpg (791×657) (zhimg.com)](https://pic1.zhimg.com/v2-685ba53b1fdded112be8fbb9a07f79d0_r.jpg)
![v2-63317342d7b438a3501c2e03216b2f9d_720w.webp (720×597) (zhimg.com)](https://pic2.zhimg.com/80/v2-63317342d7b438a3501c2e03216b2f9d_720w.webp)
在我经历了无数次尝试之后终于把方法一的结果导出来了，是不是很奇怪？