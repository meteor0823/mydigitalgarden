---
{"dg-publish":true,"link":"https://www.notion.so/Microeconomics-631f45ab79e341bf918ee69b925da687","notionID":"631f45ab-79e3-41bf-918e-e69b925da687","permalink":"/microeconomics/","dgPassFrontmatter":true}
---


# Current
Instructor: Prof. Shi, Ce Matthew (史 册) shice@cuhk.edu.hk 
Office hours: Tuesday 9 – 10AM Thursday 3:30 – 4:30PM (or by appointment) ELB 910 
TA: Mr. Geng, Hao (耿 浩) isaacgeng@link.cuhk.edu.hk 
Office hours: Wednesday 4 – 5PM UCA 306 Tutorials: 9 – 10:15AM (on selected Tuesday) ELB 401
11.14 Shi Ce 这节课2/3时间在正面为什么自由市场是efficient的

There are many other utility functions besides Cobb-Douglas. For example, some common utility functions are **constant elasticity of substitution (CES)**, **linear**, **Leontief**, and **quasilinear**
## Textbook
```
D:\All Document\Msc\Advanced Microeconomics\Current
```
Microeconomic Analysis, by Hal Varian

## Homework
交纸质版，写下problem以防出现不同version

## Production Function & Profit Maximization
Consider a single output $(y)$ case:
Production possibilities set: $Y$

### Input Requirement Set
Input requirement set: $V(y)=\{\mathbf{x}\ in\ R^n_+:(y,-\mathbf{x})\ is\ in\ Y \}$
{ #InputReqS}


### Isoquant(等产量曲线):
$Q(y)=\{\mathbf{x}\ in\ R^n_+:\mathbf{x}\ is\ in\ V(y),\mathbf{x}\ is\ not\ in\ V(y')\ for\ y'>y\}$

### Production function:
$f(\mathbf{x})=\{y\ in\ R:y\ is\ the\ maximum\ output\ associated\ with\ -\mathbf{x}\ in\ Y \}$

We often assume that we can describe the set of technologically efficient production plans by a transformation function $T : R_n\rightarrow R$ where $T(y) = 0$

E.g., Cobb-Douglas technology
$$\begin{align}
Y&=\{(y,-x_1,-x_2)\ \text{in}\ R^3:y\leq x^\alpha_1x^{1-\alpha}_2\}\\
V(y)&=\{(x_1,x_2)\ \text{in }R^2_+:y\leq x^{a}_1x^{1-a}_2\}\\
Q(y)&=\{(x_1,x_2)\ \text{in }R^2_+:y=x^a_1x^{1-a}_2 \}\\
Y(z)&=\{(y,-x_1,-x_2)\ \text{in}\ R^3:y\leq x^\alpha_1x^{1-\alpha}_2,x_2=z\}\\
T(y,x_1,x_2)&=y-x^a_1x^{1-a}_2\\
f(x_1,x_2)&=x^a_1x^{1-a}_2
\end{align}
$$
![Pasted image 20230919120004](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353588.png)

E.g., Leontief technology
$$\begin{align}
Y&=\{(y,-x_1,-x_2)\ \text{in}\ R^3:y\leq \min (ax_1,bx_2)\}\\
V(y)&=\{(x_1,x_2)\ \text{in }R^2_+:y\leq \min (ax_1,bx_2)\}\\
Q(y)&=\{(x_1,x_2)\ \text{in }R^2_+:y=\min (ax_1,bx_2) \}\\
T(y,x_1,x_2)&=y-\min (ax_1,bx_2)\\
f(x_1,x_2)&=\min (ax_1,bx_2)
\end{align}
$$
![Pasted image 20230919120022](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353589.png)


Some Assumptions
$V(y)$ is a closed, nonempty set for all $y\geq 0$

(Monotonicity) If $\mathbf{x}$ is in $V(y)$ and $\mathbf{x'}\geq \mathbf{x}$, then $\mathbf{x'}$ is in $V(y)$
(if you can use $\mathbf{x}$ to produce $y$, you can use more input to produce $y$)

(Convexity) $V(y)$  is a convex set.
$\mathbf{x,x'}\in V(y)\Rightarrow t\mathbf{x}+(1-t)\mathbf{x'}\in V(y)$
If we can use 1 labour and 100 machine to produce, and 100 labour and 1 machine to produce. Then, we can use 1-100 labour and 1-100 machine to produce.

Convexity of $V(y)$ is implied by convexity of $Y$
Proof: 
	We need to prove $t\mathbf{x}+(1-t)\mathbf{x'}\in V(y)$
	$Y$ is convex $(y,-\mathbf{x}),(y',-\mathbf{x'})\in Y$
	$(ty+(1-t)y',-(t\mathbf{x}+(1-t)\mathbf{x'}))=(y,-(t\mathbf{x}+(1-t)\mathbf{x'}))\in Y$
	Therefore, $t\mathbf{x}+(1-t)\mathbf{x'}\in V(y)$

### Technical Rate of Substitution(TRS)
$$f(x_1,x_2)=y$$
$$dy=\frac{\partial f}{\partial x_1}dx_1+\frac{\partial f}{\partial x_2}dx_2$$
For a constant $y$,
$$0=\frac{\partial f}{\partial x_1}dx_1+\frac{\partial f}{\partial x_2}dx_2$$
So,
$$\frac{dx_2}{dx_1}=-\frac{\partial f /\partial x_1}{\partial f /\partial x_2}$$
Example:
Given that $f(x_1,x_2)=x^a_1x^{1-a}_2$, we can take the derivatives to find
$$\begin{align}
&\frac{\partial f(\mathbf{x})}{x_1}=ax_1^{a-1}x_2^{1-a}=a[\frac{x_2}{x_1}]^{1-a}\\
&\frac{\partial f(\mathbf{x})}{\partial x_2}=(1-a)x_1^ax_2^{-a}=(1-a)[\frac{x_1}{x_2}]^a
\end{align}$$
It follows that
$$\frac{\partial x_2(x_1)}{\partial x_1}=-\frac{\partial f /\partial x_1}{\partial f/ \partial x_2}=-\frac{a}{1-a}\frac{x_2}{x_1}$$

### Elasticity of substitution
The technical rate of substitution measures the slope of an isoquant. The elasticity of substitution measures the curvature of an isoquant.
**Elasticity of substitution**, $\sigma$ , measures the curvature of an isoquant
$$\sigma=\frac{\%d\frac{x_2}{x_1}}{\%d TRS}=\frac{d\ln\frac{x_2}{x_1}}{d\ln |TRS|}$$

Cobb-Douglas
$$f(x_1,x_2)=x_1^\alpha x_2^{1-\alpha}$$
$$TRS=\frac{\partial f/\partial x_1}{\partial f/\partial x_2}=-\frac{a}{1-a}\frac{x_2}{x_1}$$
or
$$\frac{x_2}{x_1}=-\frac{1-a}{a}TRS$$
It follows that
$$\ln \frac{x_2}{x_1}=\ln \frac{1-a}{a}+\ln |TRS|$$
This in turn implies
$$\sigma=\frac{d\ln \frac{x_2}{x_1}}{d\ln|TRS|}=1$$

![Pasted image 20230914142101](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353590.png)

For both homogeneous and homothetic function, TRS is independent of it scale of production

### Elasticity of Scale
The **elasticity of scale** measures the percent increase in output due to a one percent increase in all inputs.
The elasticity of scale is given by
$$e(\mathbf{x})=\frac{\frac{dy(t)}{y(t)}}{\frac{dt}{t}}$$
evaluated at $t=1$. Rearranging this expression, we have
$$e(\mathbf{x})=\frac{dy(t)}{dt}\frac{t}{y}|_{t=1}=\frac{df(t\mathbf{x})}{dt}\frac{t}{f(t\mathbf{x})}|_{t=1}$$
We say that the technology exhibits locally increasing, constant, or decreasing returns to scale as $e(\mathbf{x})$ is greater, equal, or less than 1.

Example: Returns to scale and the Cobb-Douglas technology
  Suppose that $y=x^a_1x^b_2$. Then $f(tx_1,tx_2)=t(x_1)^a(tx_2)^b=t^{a+b}x^a_1x^b_2=t^{a+b}f(x_1,x_2)$. Hence, $f (tx_1, tx_2) = tf(x_1, x_2)$ if and only if $a + b = 1$. Similarly, $a + b > 1$ implies increasing returns to scale, and $a + b < 1$ implies decreasing returns to scale. 
  
  In fact, the elasticity of scale for the Cobb-Douglas technology turns out to be precisely $a + b$. To see this, we apply the definition:
$$\frac{d(tx_1)^a(tx_2)^b}{dt}=\frac{dt^{a+b}x^a_1x^b_2}{dt}=(a+b)t^{a+b-1}x^a_1x^b_2$$
  Evaluating this derivative at $t = 1$ and dividing by $f (x_1, x_2) =x^a_1x^b_2$ gives us the result.

1.4. If $\varepsilon(\mathbf{x})$ is the elasticity of scale and $\varepsilon_i(\mathbf{x})$ is the output elasticity of factor $i$, show that $\varepsilon(\mathbf{x})=\sum\limits^n_{i=1} \varepsilon_i(\mathbf{x})$
	Proof 
	$\varepsilon_i(\mathbf{x})=\frac{\frac{\partial f(\mathbf{x})}{f(\mathbf{x})}}{\frac{\partial x_i}{x_i}}$
	$\varepsilon(\mathbf{x})=\frac{\frac{dy(t)}{y(t)}}{\frac{dt}{t}}=\frac{dy(t)}{dt}\frac{t}{y}|_{t=1}=\frac{df(t\mathbf{x})}{dt}\frac{t}{f(t\mathbf{x})}|_{t=1}$
	$\frac{df(t\mathbf{x})}{dt}=\sum\limits^n_{i=1}\frac{\partial f(t\mathbf{x})}{\partial tx_i}\frac{\partial tx_i}{dt}=\sum\limits^n_{i=1}\frac{\partial f(\mathbf{x})}{\partial x_i}x_i$ (Chain Rule)
	$t=1\Rightarrow \frac{1}{y}\frac{dy}{dt}=\frac{1}{f(\mathbf{x})}\sum\limits^n_{i=1}\frac{\partial f(\mathbf{x})}{\partial x_i}x_i=\sum\limits^n_{i=1} \varepsilon_i(\mathbf{x})$

### Return to Scale
Constant return to scale:
$$f(t\mathbf{x})=tf(\mathbf{x})\text{ for all }t\geq 0$$
Increasing return to scale:
$$f(t\mathbf{x})>tf(\mathbf{x})\text{ for all }t>1$$
Decreasing return to scale:
$$f(t\mathbf{x})<tf(\mathbf{x})\text{ for all }t>1$$

### Homogeneous and homothetic technologies
A function $f(x)$ is homogeneous of degree $k$ if $f(tx)=t^kf(x)$ for all $t>0$
A homothetic function is a monotonic transformation of a function that is homogeneous of degree 1. In other words, $f(x)$ is homothetic if and only if it can be written as $f(x)=g(h(x))$ where $h(\cdot)$ is homogeneous of degree 1 and $g(\cdot)$ is a monotonic function.

![Pasted image 20230920222014](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353591.png)
Panel A depicts a function that is homogeneous of degree 1. If $x$ and $x'$ can both produce $y$ units of output, then $2x$ and $2x'$ can both produce $2y$ units of output. Panel B depicts a homothetic function. If $x$ and $x'$ produce the same level of output, $y$, then $2x$ and $2x'$ can produce the same level of output, but not necessarily $2y$

### Profit Maximization: Single input
$$\pi(x)=pf(x)-wx$$
$p$ and $w$: exogenous variables.
The first-order condition (FOC) for profit maximization is
$$\pi'(x)=pf'(x)-w=0$$
The (sufficient) second-order condition (SOC) for maximization is:
$$\pi''(x)=pf''(x)<0$$
Decreasing return to scale


The optimal choice function is implicitly defined by the FOC with
$$x^*=x^*(p,w)$$
Comparative statics:
$$\begin{align}&pf'(x^*(p,w))-w=0\\
&\Rightarrow pf''(\quad)\frac{dx^*}{dw}-1=0\Rightarrow \frac{dx^*}{dw}=\frac{1}{pf''}<0\quad pf'' \text{ is negative}\\ 
&\text{the factor demand curve slopes downward}\\
&\Rightarrow \frac{dp}{dp}f'+pf''\frac{dx^*}{dp}=0\Rightarrow \frac{dx^*}{dp}=\frac{-f'\text{ (negative)}}{pf''\text{ (negative)}}<0
\end{align}$$


### Profit Maximization: Two Inputs
The profit function is
$$\pi(x_1,x_2)=pf(x_1,x_2)-w_1x_1-w_2x_2$$
FOCs:
$$\begin{align}
&\pi_1=pf_1(x_1,x_2)-w_1=0\\
&\pi_2=pf_2(x_1,x_2)-w_2=0
\end{align}$$
SOC requires the Hessian matrix be negative definite.
$$H=\left|\begin{array}{22}
\pi_{11}&\pi_{12}\\
\pi_{21}&\pi_{22}
\end{array}\right|=\left|\begin{array}{22}
pf_{11}&pf_{12}\\
pf_{21}&pf_{22}
\end{array}\right|$$
Since the Hessian matrix is negative definite, $pf_{11}<0$, $\left|\begin{array}{22}pf_{11}&pf_{12}\\pf_{21}&pf_{22}\end{array}\right|>0$. Thus, $pf_{11}pf_{22}-pf_{12}^2>0$. Since $pf_{12}^2>0, pf_{11}<0$, $pf_{22}<0$ is for sure.
Differentiate FOCs with $w_1,w_2$
$$\begin{align}
pf_{11}\frac{\partial x_1}{\partial w_1}+pf_{12}\frac{\partial x_2}{\partial w_1}-1=0\\
pf_{21}\frac{\partial x_1}{\partial w_1}+pf_{22}\frac{\partial x_2}{\partial w_1}-0=0\\
=[H]\left[\begin{array}{1}\frac{\partial x_1}{\partial w_1}\\\frac{\partial x_2}{\partial w_1}\end{array}\right]=\left[\begin{array}{1}1\\0\end{array}\right]
\end{align}$$
Using [Cramer's Rule](https://www.youtube.com/watch?v=Ot87qLTODdQ), 
$$\frac{\partial x^*_1}{\partial w_1}=\frac{\left|\begin{array}{22}1&pf_{12}\\0&pf_{22}\end{array}\right|}{[H]}=\frac{pf_{22}}{|H|}<0(\text{since }pf_{22}<0, |H|>0)$$
$$\frac{\partial x^*_2}{\partial w_1}=\frac{\left|\begin{array}{22}pf_{11}&1\\pf_{21}&0\end{array}\right|}{[H]}=\frac{-pf_{21}}{|H|}\left\{
\begin{array}{**lr**}<0\quad f_{21}>0\\>0\quad f_{21}<0\end{array}    \right.$$

$$\begin{align}
pf_{11}\frac{\partial x_1}{\partial w_2}+pf_{12}\frac{\partial x_2}{\partial w_2}-0=0\\
pf_{21}\frac{\partial x_1}{\partial w_2}+pf_{22}\frac{\partial x_2}{\partial w_2}-1=0\\
=[H]\left[\begin{array}{1}\frac{\partial x_1}{\partial w_2}\\\frac{\partial x_2}{\partial w_2}\end{array}\right]=\left[\begin{array}{1}1\\0\end{array}\right]
\end{align}$$
Using [Cramer's Rule](https://www.youtube.com/watch?v=Ot87qLTODdQ), 
$$\frac{\partial x^*_1}{\partial w_2}=\frac{\left|\begin{array}{22}0&pf_{12}\\1&pf_{22}\end{array}\right|}{[H]}=\frac{-pf_{12}}{|H|}\left\{\begin{array}{**lr**}<0\quad f_{21}>0\\>0\quad f_{21}<0\end{array}    \right.$$
$$\frac{\partial x^*_2}{\partial w_2}=\frac{\left|\begin{array}{22}pf_{11}&0\\pf_{21}&1\end{array}\right|}{[H]}=\frac{pf_{11}}{|H|}<0(\text{since }pf_{11}<0, |H|>0)$$


Differentiate FOCs with $p$ (with chain rule)
$$\begin{align}
f_1+pf_{11}\frac{\partial x_1}{\partial p}+pf_{12}\frac{\partial x_2}{\partial p}=0\\
f_2+pf_{21}\frac{\partial x_1}{\partial p}+pf_{22}\frac{\partial x_2}{\partial p}=0\\
H\cdot\left[\begin{array}{1} \frac{\partial x_1}{\partial p}\\ \frac{\partial x_2}{\partial p}\end{array}\right]=\left[\begin{array}{1} -f_1\\ -f_2\end{array}\right]
\end{align}$$
Using [Cramer's Rule](https://www.youtube.com/watch?v=Ot87qLTODdQ), 
$\frac{dy^*}{dp}=\frac{\left|\begin{array}{11} -f_1&pf_{12}\\ -f_2&pf_{22} \end{array}\right|}{|H|}=\frac{-f_1pf_{22}+f_2pf_{12}}{|H|}$
$f_1=\frac{w_1}{p}>0,pf_{22}<0,f_2>0$
If $f_{12}>0$, $\frac{dy^*}{dp}>0$ 
	$f_{12}>0$  means two products are complement
	$f_{12}<0$ means two products are substitute

$f_{21}$ if I have more input 1, what will the marginal product of input 2

Next we need to prove $\frac{\partial x^*_1}{\partial w_2}=\frac{\partial x^*_2}{\partial w_1}$ 

$\begin{align}\frac{\partial y}{\partial w_1}&=f_1\frac{\partial x^*_1}{\partial w_1}+f_2\frac{\partial w^*_2}{\partial w_1}\\ &=\frac{f_1pf_{22}}{|H|}+\frac{f_2(-pf_{21})}{|x|}\\ &=\frac{(f_1pf_{22}-f_2pf_{21})}{|x|} \end{align}$
will discuss it next week

$\begin{align}\frac{\partial y^*}{\partial p}&=f_1\frac{\partial x^*}{\partial p}+f_2\frac{\partial x^*_2}{\partial p}\\ &=\frac{f_1(-pf_1f_{22}+pf_2f_{12})}{|H|}+\frac{f_2(-pf_2f_{11}+pf_1f_{21})}{|H|}\\&=-p[-f_2\ f_1]\left[\begin{array}{1} f_{11}&f_{12}\\ f_{12}&f_{22} \end{array}\right]\left[\begin{array}{1} -f_2\\ f_1 \end{array}\right]/|H|\ (z=\left[\begin{array}{1} -f_2\\ f_1 \end{array}\right])\\ &=\frac{-z'Hz}{|H|}>0\ (|H|>0)\end{align}$

### Profit Maximization: Short Run
In short-run, suppose there is a constraint $\bar{x}_2$
The profit function is
$$\pi(x_1,\bar{x}_2)=pf(x_1,\bar{x}_2)-w_1x_1-w_2\bar{x}_2$$
FOC:
$$pf_1(x_1,\bar{x}_2)-w_1=0$$
SOC:
$$pf_{11}(x_1,\bar{x}_2)<0$$
The solution $x^s_1(p,w_1,\bar{x}_2)$ equals $x^*_1(p,w_1,w_2)$ when $\bar{x}_2=x^*_2(p,w_1,w_2)$
Differentiating 
$$\begin{align}
x^s_1\big(p,w_1,x^*_2(p,w_1,w_2)\big)=x^*_1(p,w_1,w_2)\\
\frac{\partial x^s_1}{\partial w_1}+\frac{\partial x^s_1}{\partial x_2}\frac{\partial x^*_2}{\partial w_1}=\frac{\partial x^*_1}{\partial w_1}
\end{align}$$
==没搞明白==
$\frac{\partial x^s_1}{\partial w_1}-\frac{\partial x^*_1}{\partial w_1}>0$

**LeChatelier Principle**
In other words, the short-run demand function is less sensitive to a change in than the long-run demand function.

#### Difficulties
For each vector of prices $(p, w)$ there will in general be some optimal choice of factors $x^*$. The function that gives us the optimal choice of inputs as a function of the prices is called **the factor demand function** of the firm. This function is denoted by $x(p,w)$. 
Similarly, the function $y(p,w)=f(\mathbf{x}(p,w))$ is called **the supply function** of the firm.
==factor demand function和supply function的定义很重要==

Example: The profit function for Cobb-Douglas technology
Consider the problem of maximizing profits for the production function of the form $f(x)=x^a$ where $a>0$. The first order condition is 
$$pax^{a-1}=w$$
and the second-order condition reduces to
$$pa(a-1)x^{a-2}\leq 0$$

The second-order condition can only be satisfied when $a\leq 1$, which means that the production function must have constant or decreasing returns to scale for competitive profit maximization to be meaningful.
{ #Meaningful}


If $a=1$, the first-order condition reduces to $p=w$. Hence, when $w=p$ any value of $x$ is a profit-maximizing choice. 
When $a<1$, we use the first-order condition to solve for the factor demand function
$$x(p,w)=(\frac{w}{ap})^{\frac{1}{a-1}}$$
The supply function is given by
$$y(p,w)=f(x(p,w))=(\frac{w}{ap})^{\frac{a}{a-1}}$$
and the profit function is given by
$$\pi(p,w)=py(p,w)-wx(p,w)=w(\frac{1-a}{a})(\frac{w}{ap})^{\frac{1}{a-1}}$$

#### Properties of demand and supply functions
the factor demand functions must be homogeneous of degree zero
$$x_i(tp,tw)=x_i(p,w)$$


### Problem Set 1
Chapter 1 Problems: 1.1, 1.2, 1.3, [[Microeconomics#Elasticity of Scale\|1.4*]], 1.5, 1.7, 1.8, 1.9*, 1.11 
Chapter 2 Problems: 2.1, 2.2, 2.3*, 2.4*, 2.5, 2.7 
Chapter 3 Problems: 3.1, 3.2, 3.3, 3.4*, 3.5

#### Chapter 1
1.1 True or false? If $V(y)$ is a convex set, then the associated production set $Y$ must be convex
	False. There are many counterexamples. Consider the technology generated by a production function $f(x)=x^2$. The production set is $Y=\{(y,-x):y\leq x^2\}$ which is certainly not convex, but the input requirement set is $V(y)=\{x:x\geq \sqrt{y}\}$ which is a convex set. 
	==不是很懂==

1.2. What is the elasticity of substitution for the general $CES$ technology $y =(a_1x_1^\rho+a_2x_2^\rho)^{1/\rho}$  when $a1\neq a_2$?
	$TRS=\frac{\text{MP}_1}{\text{MP}_2}=\frac{\frac{1}{\rho}(a_1x^\rho_1+a_2x^\rho_2)^{1/\rho-1} a_1 x^{\rho -1}_1}{\frac{1}{\rho}(a_1x^\rho_1+a_2x^\rho_2)^{1/\rho-1} a_2 x^{\rho- 1}_2}=\frac{ a_1 x^{\rho -1}_1 }{ a_2 x^{\rho- 1}_2 }$
	$\ln (TRS)=\ln(\frac{a_1}{a_2})+(\rho-1)\ln(\frac{x_1}{x_2})\Rightarrow \sigma=\frac{1}{1-\rho}$
{ #Problem1-2}


1.3 Define the output elasticity of a factor $i$ to be
$$\varepsilon_i(\mathbf{x})=\frac{\partial f(\mathbf{x})}{\partial x_i}\frac{x_i}{f(\mathbf{x})}$$
If $f(x)=x^a_1x^b_2$ , what is the output elasticity of each factor?
	$\varepsilon_1(\mathbf{x})=\frac{\partial f(\mathbf{x})}{\partial x_1}\frac{x_1}{f(\mathbf{x})}=ax^{a-1}_1x^b_2 \frac{x_1}{x^a_1x^b_2}=a$
	In similar, $\varepsilon_2(\mathbf{x})=b$

[[Microeconomics#Elasticity of Scale\|1.4*]]

1.5 What is the elasticity of scale of the CES technology, $f (x_1, x_2)=(x^{\rho}_1+ x^{\rho}_2)^{\frac{1}{\rho}}$?
	Key point is to understand the definition of the **the elasticity of scale**
$$f (tx_1,tx_2)=[(tx_1)^{\rho}+ (tx_2)^{\rho}]^{\frac{1}{\rho}}=t[x^{\rho}_1+x^{\rho}_2]^{\frac{1}{\rho}}=tf(x_1,x_2)$$
	Substitute $tx_i$ for $i = 1, 2$ to get
	This implies that the CES function exhibits constant returns to scale and hence has an elasticity of scale of 1.

1.9 Consider the CES technology $f(x_1,x_2)=[a_1x^\rho_1+a_2x^\rho_2]^{\frac{1}{\rho}}$. Show that we can always write this in the form $f(x_1,x_2)=A(\rho)[bx^{\rho}_1+(1-b)x^{\rho}_2]^{\frac{1}{\rho}}$
	$b=\frac{a_1}{A(\rho)^\rho},1-b=\frac{a_2}{A(\rho)^{\rho}}$
	$\therefore \frac{a_1}{A(\rho)^\rho}+\frac{a_2}{A(\rho)^{\rho}}=1$
	$\therefore a_1+a_2=A(\rho)^{\rho}$
	Let $A(\rho)=(a_1+a_2)^{\frac{1}{\rho}},b=\frac{a_1}{a_1+a_2},1-b=\frac{a_2}{a_1+a_2}$
	then $\begin{align}f(x_1,x_2)&=A(\rho)[bx_1^{\rho}+(1-b)x_2^\rho]^{\frac{1}{\rho}}\\ &=(a_1+a_2)^{\frac{1}{\rho}}[\frac{a_1}{a_1+a_2}x^\rho_1+\frac{a_2}{a_1+a_2}x^\rho_2]^{\frac{1}{\rho}}\\ &=(a_1x_1^\rho+a_2x_2^\rho)^{\frac{1}{\rho}}   \end{align}$
 

2.3 Calculate explicitly the profit function for the technology $y = x^a$, for $0 < a < 1$ and verify that it is homogeneous and convex in $(p, w)$.
	In the text the supply function and the factor demands were computed for this technology. Using those results, the profit function is given by
$$\pi(p,w)=p(\frac{w}{ap})^{\frac{a}{a-1}}-w(\frac{w}{ap})^{\frac{1}{a-1}}$$
	To prove homogeneity, note that
$$\pi(tp,tw)=tp(\frac{w}{ap})^{\frac{a}{a-1}}-tw(\frac{w}{ap})^{\frac{1}{a-1}}=t\pi(p,w)$$
	which implies that π(p, w) is a homogeneous function of degree 1. 
	Before computing the Hessian matrix, factor the profit function in the following way:
$$\pi(p,w)=p^{\frac{1}{1-a}}w^{\frac{a}{a-1}}(a^{\frac{a}{1-a}}-a^{\frac{1}{1-a}})=p^{\frac{1}{1-a}}w^{\frac{a}{a-1}}\phi(a)$$
	where $\phi(a)$ is strictly positive for $0<a<1$
	The Hessian matrix can now be written as
$$\begin{aligned}
D^{2}\pi(p,\omega)& =\begin{pmatrix}\frac{\partial^2\pi(p,w)}{\partial p^2}&\frac{\partial^2\pi(p,w)}{\partial p\partial w}\\\frac{\partial^2\pi(p,w)}{\partial w\partial p}&\frac{\partial^2\pi(p,w)}{\partial w^2}\end{pmatrix}  \\
&=\begin{pmatrix}\frac a{(1-a)^2}p^{\frac{2a-1}{1-a}}w^{\frac a{a-1}}&-\frac a{(1-a)^2}p^{\frac a{1-a}}w^{\frac1{a-1}}\\\\-\frac a{(1-a)^2}p^{\frac a{1-a}}w^{\frac1{a-1}}&\frac a{(1-a)^2}p^{\frac1{1-a}}w^{\frac{2-a}{a-1}}\end{pmatrix}\phi(a).
\end{aligned}$$
	The principal minors of this matrix are
$$\frac{a}{(1-a)^2}p^{\frac{2a-1}{1-a}}w^{\frac{a}{a-1}}\phi(a)>0$$
	and 0. Therefore, the Hessian is a positive semidefinite matrix, which implies that $π(p, w)$ is convex in $(p, w)$.
==暂时没懂== 懂了


2.4 Let $f (x_1, x_2)$ be a production function with two factors and let $w_1$and $w_2$ be their respective prices. Show that the elasticity of the factor share $(w_2x_2/w_1x_1)$ with respect to $(x_1/x_2)$ is given by $1/\sigma - 1$.
	$TRS=\frac{\frac{\partial f(x_1,x_2)}{\partial x_1}}{\frac{\partial f(x_1,x_2)}{\partial x_2}}=\frac{w_1}{w_2}$
	$\sigma=\frac{d(\ln \frac{x_2}{x_1})}{d (\ln TRS)}=\frac{d(\ln \frac{x_2}{x_1})}{d(\ln \frac{w_1}{w_2})}$
	$\begin{align}\text{elasticity}&=\frac{d [\ln (w_2x_2/w_1x_1)]}{d[\ln(x_1/x_2)]}\\ &=\frac{d(\ln \frac{w_2}{w_1}+\ln \frac{x_2}{x_1})}{d (\ln \frac{x_2}{x_1})}\\ &=\frac{d(-\ln \frac{w_1}{w_2})}{d(-\ln \frac{x_2}{x_1})}+\frac{d(-\ln \frac{x_1}{x_2})}{d(\ln \frac{x_1}{x_2})}\\ &=\frac{1}{\sigma}-1 \end{align}$
注意分子是$\frac{x_2}{x_1}$ ，其余一切都好

3.4 Given the production function $f(x_1,x_2)=x^{a_1}_1x^{a_2}_2$ calculate the profit-maximizing demand and supply functions, and the profit function. Assume $a_i > 0$. What restrictions must $a_1$ and $a_2$ satisfy?
	$\pi(x_1,x_2)=px^{a_1}_1x^{a_2}_2-w_1x_1-w_2x_2$
	First of condition, $\left\{\begin{array}{**lr**} pa_1x_1^{a_1-1}x_2^{a_2}-w_1=0\\ pa_2x_2^{a_2-1}x_1^{a_1}-w_2=0\end{array}   \right.\Rightarrow \left\{\begin{array}{**lr**} x^*_1=[(\frac{a_1}{w_1})^{a_2-1}(\frac{w_2}{a_2})^{a_2}\frac{1}{p}]^{\frac{1}{a_1+a_2-1}}\\ x^*_2=[(\frac{a_2}{w_2})^{a_1-1}(\frac{w_1}{a_1})^{a_1}\frac{1}{p}]^{\frac{1}{a_1+a_2-1}}\end{array}   \right.$
	$\pi(x^*_1,x^*_2)=[(\frac{w_1}{a_1})^{a_1}(\frac{w_2}{a_2})^{a_2}\frac{1-a_1^{a_1+a_2-1}-a_2^{a_1+a_2-1}}{p}]^{\frac{1}{a_1+a_2-1}}$
	In order for this to be meaningful, the technology must exhibit decreasing returns to scale, so $a_1+a_2<1$

Answer
```
D:\All Document\Msc\Advanced Microeconomics\Current
```

#### Quiz 2
In the case of 2 factors, show that the factor demand functions are homogeneous of degree zero.
	Proof
	We want to prove $x_i(tp,tw_1,tw_2)=x_i(p,w_1,w_2)$
	$\max\ \pi=pf(x)-w_1x_1-w_2x_2$
	$F.O.C\ pf_1(x)-w_1=0$
	$\quad\quad\quad\ pf_2(x)-w_2=0$
	we can prove the first order condition is the same
	$\max\ \pi=tpf(x)-tw_1x_1-tw_2x_2$
	$F.O.C\ tpf_1(x)-tw_1=0\Rightarrow pf_1(x)-w_1=0$
	$\quad\quad\quad\ tpf_2(x)-tw_2=0\Rightarrow pf_2(x)-w_2=0$
	^quiz2

## Profit Function

$$\begin{align}
\pi(\mathbf{p})=\max \mathbf{py}\\
\text{such that } y\text{ is in } Y
\end{align}$$
问了一下TA
$$\mathbf{p}=[p,w_1,w_2]$$
$$\mathbf{y}=[f(x_1,x_2),-x_1,-x_2]$$
这样就可以用$\pi(\mathbf{p})=\mathbf{py}$ 表示$\pi(\mathbf{p})=pf(x_1,x_2)-w_1x_1-w_2x_2$
而且这也解释了[[Microeconomics#Input Requirement Set\|Input requirement set]]中为什么x是负的
### Properties of the profit function
1. Nondecreasing in output prices, nonincreasing in input prices
2. Homogeneous of degree 1 in $p$.
	1. Proof: Let $y$ be a profit-maximizing net output vector at $p$, so that $py\geq py'$ for all $\mathbf{y'}$ in Y. It follows that for $t\geq 0$, $tpy\geq tpy'$ for all $\mathbf{y'}$ in Y. Hence $y$ also maximizes profits at price $tp$. Thus $\pi(t\mathbf{p})=t\mathbf{py}=t\pi(\mathbf{p})$
3. Convex in $p$.
	1. Let $y$ maximize profits at $p$. $\mathbf{y}'$ maximize profits at $\mathbf{p}'$, and $\mathbf{y}"$ maximize profits at $\mathbf{p}"$. Then we have
	2. $\pi(\mathbf{p}'')=\mathbf{p}''\mathbf{y}''=(t\mathbf{p}+(1-t)\mathbf{p}')\mathbf{y}''=t\mathbf{p}\mathbf{y}''+(1-t)\mathbf{p}'\mathbf{y}''\tag{3.1}$
	3. By the definition of profit maximization, we know that
	4. $\begin{align} t\mathbf{p}\mathbf{y}''\leq t\mathbf{py}=t\pi(\mathbf{p})\\(1-t)\mathbf{p}'\mathbf{y}'' \leq (1-t)\mathbf{p}'\mathbf{y}'=(1-t)\pi(\mathbf{p}')\end{align}$
	5. Adding these two inequalities and using (3.1), we have
	6. $\pi(\mathbf{p}'')\leq t\pi(\mathbf{p})+(1+t)\pi(\mathbf{p}')$
4. Continuous in $p$. 
==Don't understand proof so far==

The properties of the profit function have several uses.
For example, suppose that we have access to accounting data for some firm and observe that when all prices are scaled up by some factor $t > 0$ profits do not scale up proportionally. If there were no other apparent changes in the environment, we might suspect that the firm in question is not maximizing profits

Example: The effects of price stabilization
$$q\pi(p_1)+(1-a)\pi(p_2)\geq \pi(qp_1+(1-q)p_2)=\pi(\bar{p})$$
Thus average profits with a fluctuating price are at least as large as with a stabilized price.

Suppose that instead we are given the profit function and are asked to find the net supply functions. How can that be done?

#### **Hotelling's Lemma**
Let $y_i(p)$ be the firm's net supply function for good $i$. Then
$$y_i(p)=\frac{\partial \pi(\mathbf{p})}{\partial p_i}\text{ for }i=1,\dots,n$$
	[Proof](https://www.youtube.com/watch?v=V6Rziu74uhA): 
$$\begin{align}
\max \pi(y,x_1,x_2)=py-w_1x_1-w_2x_2\\
s.t.\ f(x_1,x_2)\geq q\\
\text{Define }G(q,x_1,x_2)=q-f(x_1,x_2)\leq 0\\
G\text{ has no parameter such as }p,w_1,w_2\\
V(p,w_1,w_2)\text{ is profit}\\
\frac{\partial V}{\partial p}=\frac{\partial \pi}{\partial p}-\lambda \frac{\partial G}{\partial p}=y-\lambda(0)=\hat{y}(p,w_1,w_2)\\
\frac{\partial V}{\partial w_i}=\frac{\partial \pi}{\partial w_i}-\lambda\frac{\partial G}{\partial w_i}=-\hat{x}_i(p,w_1,w_2)\quad (\text{Factor Demand Function})
\end{align}$$
{ #HotellingLemma}


#### Exercise
When the price of an output increases by a small amount there will be two effects. 
First, there is a direct effect: because of the price increase the firm will make more profits, even if it continues to produce the same level of output. 
But secondly, there will be an indirect effect: the increase in the output price will induce the firm to change its level of output by a small amount. However, the change in profits resulting from any infinitesimal change in output must be zero since we are already at the profit-maximizing production plan. Hence, the impact of the indirect effect is zero, and we are left only with the direct effect.

3.1 . A competitive profit-maximizing firm has a profit function $\pi=(w_1,w_2)=\phi(w_1)+\phi(w_2)$. The price of output is normalized to be 1.
	1. What do we know about the first and second derivatives of the functions $\phi(w_i)$?
		Solution:
		Since the profit function is convex and a decreasing function of the factor prices, we know that $\phi_i'(w_i)\leq 0$ and $\phi_i''(w_i)\geq 0$
	2. If $x_i(w_1, w_2)$ is the factor demand function for factor $i$, what is the sign of $\partial x_i/\partial w_j$?
		Solution:
		It is zero. ==这个也没太懂== 
	3. Let $f (x_1, x_2)$ be the production function that generated the profit function of this form. What can we say about the form of this production function? (Hint: look at the first-order conditions.)
		Solution:
		The demand for factor $i$ is only a function of the $i^{th}$  price. Therefore the marginal product of factor $i$ can only depend on the amount of factor $i$. It follows that $f(x_1, x_2) = g_1(x_1) + g_2(x_2)$.

3.2. Consider the technology described by $y = 0$ for $x\leq 1$ and $y = \ln x$ for $x > 1$. Calculate the profit function for this technology.
	Solution:
	The firm can always choose $x=0$ and make zero profits
	When $y=\ln x$
	$\pi=p\ln x-wx$
	The first order condition are $\frac{p}{x}=w$, which gives us the demand function $x=\frac{p}{w}$ and the supply function $y=\ln (\frac{p}{w})$. The profits from operating at this pint are $p\ln (\frac{p}{w})-p$.
	In summary, $\pi(p,w)=\max \{p\ln(\frac{p}{w}-p,0)\}$

3.3 Given the production function $f (x_1, x_2) = a_1 \ln x_1 + a_2 \ln x_2$, calculate the profit-maximizing demand and supply functions, and the profit function, For simplicity assume an interior solution. Assume that $a_i> 0$. 
	Solution:
	The first-order conditions are
$$\begin{align}
a_1\frac{p}{x_1}-w_1=0\\
a_2\frac{p}{x_2}-w_2=0
\end{align}$$
	which can easily be solved for the factor demand functions. Substituting into the objective function gives us the profit function 

3.5. Given the production function $f (x_1, x_2) = \min\{x_1, x_2\}^a$, calculate the profit-maximizing demand and supply functions, and the profit function. What restriction must a satisfy?
	Solution:
	If $w_i$ is strictly positive, the firm will never use more of factor $i$ than it needs to, which implies $x_1 = x_2$. Hence the profit maximization problem can be written as 
$$\max\ px^a_1-w_1x_1-w_2x_2$$
	The first-order condition is
$$pax^{a-1}_1-(w_1+w_2)=0$$
	Demand function: $x_1=(\frac{w_1+w_2}{pa})^{\frac{1}{a-1}}$
	Supply function: $y=p(\frac{w_1+w_2}{pa})^{\frac{a}{a-1}}=p^{\frac{1}{1-a}}(\frac{w_1+w_2}{a})^{\frac{a}{a-1}}$
	In order for a maximum to exist, $a<1$ ==最后一个怎么证明的没搞懂==
		用second order condition证明是$0<a<1$ [[Microeconomics#Difficulties\|Difficulties]]
		10.19问JZH：$a$默认大于0,不需要深究

## Cost Minimization
$$\begin{align}\min_x \mathbf{wx}\\
\text{such that }f(\mathbf{x})=y
\end{align}$$
We analyze this constrained minimization problem using the method of Lagrange multipliers.
$$\mathcal{L}(\lambda,\mathbf{x})=\mathbf{wx}-\lambda(f(\mathbf{x})-y)$$
The first-order conditions characterizing an interior solution $\mathbf{x}^*$ are
$$\begin{align}w_i-\lambda\frac{\partial (\mathbf{x}^*)}{\partial x_i}=0\\
f(\mathbf{x}^*)=y
\end{align}$$
These conditions can also be written in vector notation.
Letting $Df(\mathbf{x})$ be the gradient vector, the vector of partial derivatives of $f(\mathbf{x})$, we can write the derivative conditions as
$$\mathbf{w}=ADf(\mathbf{x}^*)$$
We can interpret these first-order conditions by dividing the $i^{th}$ condition by the $j^{th}$ condition to get
$$\frac{w_i}{w_j}=\frac{\frac{\partial f(\mathbf{x^*})}{\partial x_i}}{\frac{\partial f(\mathbf{x^*})}{\partial x_j}}\quad i,j=1,\dots,n.$$
isoquant 等产量曲线 isocost 等支出曲线



**Conditional factor demand**
In economics, a **conditional factor demand** is the cost-minimizing level of an input (factor of production) such as labor or capital, required to produce a given level of output, for given unit input costs (wage rate "Wage rate") and cost of capital) of the input factors.

$$\mathbf{D}^2\mathcal{L}(\lambda^*,x_1^*,x_2^*)=\begin{pmatrix}\frac{\partial^2\mathcal{L}}{\partial\lambda^2}&\frac{\partial^2\mathcal{L}}{\partial\lambda\partial x_1}&\frac{\partial^2\mathcal{L}}{\partial\lambda\partial x_2}\\\frac{\partial^2\mathcal{L}}{\partial x_1\partial\lambda}&\frac{\partial^2\mathcal{L}}{\partial x_1^2}&\frac{\partial^2\mathcal{L}}{\partial x_1\partial x_2}\\\frac{\partial^2\mathcal{L}}{\partial x_2\partial\lambda}&\frac{\partial^2\mathcal{L}}{\partial x_2\partial x_1}&\frac{\partial^2\mathcal{L}}{\partial x_2^2}\end{pmatrix}.$$
It is convenient to use $f_{ij}$ to denote $\partial^2 f/\partial x_i \partial_j$. Calculating the various second derivatives and using this notation gives us
$$\mathbf{D}^2\mathcal{L}(\lambda^*,x_1^*,x_2^*)=\begin{pmatrix}0&-f_1&-f_2\\-f_1&-\lambda f_{11}&-\lambda f_{12}\\-f_2&-\lambda f_{21}&-\lambda f_{22}\end{pmatrix}.$$




$\frac{\partial x^{\#}_2}{\partial w_1}=\frac{\left|\begin{array}{111}0&-f_1&0\\-f_1 &-\lambda f_{11}&-1\\-f_2&-\lambda f_{21}&0 \end{array}\right|}{|\bar{H}|}=\frac{\overbrace{-(-f_1)(-f_2)}^{negative}}{\underbrace{|\bar{H}|}_{negative}}>0$


$\frac{dx_i^{\#}}{dy}$


Linking cost minimization and profit maximization, we have
$$\frac{\partial x^*}{\partial w_1}=\frac{\partial x^*_1}{\partial w_1}+\frac{\partial x^{\#}_1}{\partial y}\frac{\partial y^*}{\partial w_1}$$



Envelope Theorem 
$$\frac{df^*(a)}{da}=\frac{\partial f(x^*(a),a)}{\partial a}$$
	Proof:
$$\frac{df^*(a)}{d a}=\overbrace{\underbrace{\frac{\partial f^*}{\partial x}}_{\text{FOC}=0}\underbrace{\frac{\partial x^*}{\partial a}}_{\frac{dx}{da}}}^{0}+\frac{\partial f^*}{\partial a}$$




only direct effect matters


The Sherphard’s Lemma
$$\begin{align}\partial C^*(w_1,w_2,y)/\partial w_1=x_1^{\#}(y,w_1,w_2)\\
\partial C^*(w_1,w_2,y)/\partial w_2=x_2^{\#}(y,w_1,w_2)
\end{align}$$

$C=\frac{y}{25}(w_1 w_2)^{\frac{1}{2}}$ Find the production function
	The Sherphard's Lemma
	$x_1^{\#}=\frac{dc}{dw_1}=\frac{1}{2}\frac{y}{25}w^{-\frac{1}{2}}_1 w_2^{\frac{1}{2}}\Rightarrow (\frac{w_1}{w_2})^{\frac{1}{2}}=\frac{y}{50x_1^{\#}}\ (1)$
	$x_2^{\#}=\frac{dc}{dw_2}=\frac{1}{2}\frac{y}{25}w^{\frac{1}{2}}_1 w_2^{-\frac{1}{2}}\ (2)$
	Combine $(1)$ and $(2)$
	$x_1x_2=\frac{y}{50}\cdot\frac{y}{50}$
	$\Rightarrow y=50x^{\frac{1}{2}}_1x^{\frac{1}{2}}_2$

EXAMPLE: Cost function for the Cobb-Douglas technology
Consider the cost minimization problem
$$\begin{align}
c(\mathbf{w},y)=\min_{x_1,x_2} w_1x_1+w_2x_2\\
\text{such that }Ax^a_1x^b_2=y
\end{align}$$
Solving the constraint for $x_2$, we see that this problem is equivalent to
$$\min_{x_1} w_1x_1+w_2A^{-\frac{1}{b}}y^{\frac{1}{b}}x^{-\frac{a}{b}}_1$$
The first-order condition is
$$w_1-\frac{a}{b}w_2A^{-\frac{1}{b}}y^{\frac{1}{b}}x^{-\frac{a+b}{b}}_1=0$$
which gives us the conditional demand function for factor 1:
$$x_1(w_1,w_2,y)=A^{-\frac{1}{a+b}}[\frac{aw_2}{bw_1}]^{\frac{b}{a+b}}y^{\frac{1}{a+b}}$$
for factor 2:
$$x_2(w_1,w_2,y)=A^{-\frac{1}{a+b}}[\frac{aw_2}{bw_1}]^{-\frac{a}{a+b}}y^{\frac{1}{a+b}}$$
The cost function is
$$\begin{align}
c(w_1,w_2,y)&=w_1x_1(w_1,w_2,y)+w_2x_2(w_1,w_2,y)\\
&=A^{\frac{-1}{a+b}}\Big[(\frac{a}{b})^{\frac{b}{a+b}}+(\frac{a}{v})^{\frac{-a}{a+b}}\Big]w^{\frac{a}{a+b}}_1w^{\frac{b}{a+b}}_2y^{\frac{1}{a+b}}
\end{align}$$
When we use the Cobb-Douglas technology for examples, we will usually measure units so that $A = 1$ and use the constant-returns-to-scale assumption that $a + b = 1$. In this case the cost function reduces to
$$c(w_1,w_2,y)=Kw^a_1w^{1-a}_2y$$
where $K=a^{-a}(1-a)^{a-1}$

EXAMPLE: The cost function for the CES technology
Suppose that $f(x_1,x_2)=(x^{\rho}_1+x^{\rho}_2)^{\frac{1}{\rho}}$.What is the associated cost function? The cost minimization problem is
$$\begin{align}
\min\ w_1x_1+w_2x_2\\
\text{such that }x^{\rho}_1+x^{\rho}_2=y^{\rho}
\end{align}$$
The first-order condition are
$$\begin{align}
w_1-\lambda \rho x^{\rho-1}_1=0\\
w_2-\lambda \rho x^{\rho-1}_2=0\\
x^{\rho}_1+x^{\rho}_2=y^{\rho}
\end{align}$$
Solving the first two equations for $x^{\rho}_1$ and $x^{\rho}_2$, we have
$$\begin{align}
x^{\rho}_1=w^{\frac{\rho}{\rho-1}}_1(\lambda \rho)^{\frac{-\rho}{\rho-1}}\\
x^{\rho}_2=w^{\frac{\rho}{\rho-1}}_2(\lambda \rho)^{\frac{-\rho}{\rho-1}}  \tag{4.5}
\end{align}$$
```
用tag{}实现公式标号
```
Substitute this into the production function to find
$$(\lambda\rho)^{\frac{-\rho}{\rho-1}}[x^{\frac{\rho}{\rho-1}}_1+w^{\frac{\rho}{\rho-1}}_2]=y^{\rho}$$
Solve this for $(\lambda \rho)^{\frac{-\rho}{\rho-1}}$ and substitute into the system (4.5). This gives us the conditional factor demand functions
$$\begin{align}
x_1(w_1,w_2,y)=w^{\frac{1}{\rho-1}}_1[w^{\frac{\rho}{\rho-1}}_1+w^{\frac{\rho}{\rho-1}}_2]y\\
x_2(w_1,w_2,y)=w^{\frac{1}{\rho-1}}_2[w^{\frac{\rho}{\rho-1}}_1+w^{\frac{\rho}{\rho-1}}_2]y
\end{align}$$
Substituting these functions into the definition of the cost function yields
$$\begin{align}
c(w_1,w_2,y)&=w_1x_1(w_1,w_2,y)+w_2x_2(w_1,w_2,y)\\
&=y[w^{\frac{\rho}{\rho-1}}_1+w^{\frac{\rho}{\rho-1}}_2][w^{\frac{\rho}{\rho-1}}_1+w^{\frac{\rho}{\rho-1}}_2]^{-\frac{1}{\rho}}\\
&=y[w^{\frac{\rho}{\rho-1}}_1+w^{\frac{\rho}{\rho-1}}_2]^{\frac{\rho-1}{\rho}}
\end{align}
$$
This expression looks a bit nicer if we set $r = \rho/(\rho- 1)$ and write
$$c(w_1,w_2,y)=y[w^r_1+w^r_2]^{\frac{1}{r}}$$
Note that this cost function has the same form as the original CES production function with $r$ replacing $p$. In the general case where
$$f(x_1,x_2)=[(a_1x_1)^{\rho}+(a_1x_1)^{\rho}]^{\frac{1}{\rho}}$$
similar computations can be done to show that
$$c(w_1,w_2,y)=y[(w_1/a_1)^r+(w_2/a_2)^r]^{\frac{1}{r}}$$

EXAMPLE: The cost function for the Leontief technology
he firm must operate at a point where $y = ax_1 = bx_2$. Hence, if the firm wants to produce y units of output, it must use $y/a$ units of good 1 and $y/b$ units of good 2 no matter what the input prices are. Hence, the cost function is given by
$$c(w_1,w_2,y)=\frac{w_1y}{a}+\frac{w_2y}{b}=y(\frac{w_1}{a}+\frac{w_2}{b})$$

EXAMPLE: The cost function for the linear technology
$$\begin{align}
\min\ w_1x_1+w_2x_2\\
\text{s.t. }x_1+x_2=y\\
x_1\geq 0\\
x_2 \geq 0
\end{align}
$$
The Lagrangian for this problem can be written as
$$\mathcal{L}(\lambda,\mu_1,\mu_2,x_1,x_2)=w_1x_1+w_2x_2-\lambda(x_1+x_2-y)-\mu_1 x_1-\mu_2x_2$$
The Kuhn-Tucker first-order conditions are
$$\begin{align}
w_1-\lambda-\mu_1=0\\
w_2-\lambda-\mu_2=0\\
x_1+x_2=y\\
x_1\geq 0\\
x_2\geq 0
\end{align}$$
and the complementary slackness conditions are
p71后面看教材吧


**Conditional factor demand function**
Applying the usual arguments, the conditional factor demand functions $\mathbf{x}(\mathbf{w}, y)$ must satisfy the first-order conditions
$$\begin{align}
f(\mathbf{x}(\mathbf{w},y))\equiv y\\
\mathbf{w}-\lambda Df(\mathbf{w},y)\equiv0
\end{align}$$
It is easy to get lost in matrix algebra in the following calculations, so we will consider a simple two-good example. In this case the first-order conditions look like
$$\begin{align}
f(x_1(w_1,w_2,y),x_2(w_1,w_2,y))\equiv y\\
w_1-\lambda\frac{\partial f(x_1(w_1,w_2,y),x_2(w_1,w_2,y))}{\partial x_1} \equiv 0\\
w_2-\lambda\frac{\partial f(x_1(w_1,w_2,y),x_2(w_1,w_2,y))}{\partial x_2} \equiv 0
\end{align}$$
Therefore, we can differentiate these identities with respect to $w_1$, say.
$$\begin{align}
\frac{\partial f}{\partial x_1}\frac{\partial x_1}{\partial w_1}+\frac{\partial f}{\partial x_2}\frac{\partial x_2}{\partial w_1}& \boldsymbol{=0}  \\
1-\lambda\left[\frac{\partial^2f}{\partial x_1^2}\frac{\partial x_1}{\partial w_1}+\frac{\partial^2f}{\partial x_1\partial x_2}\frac{\partial x_2}{\partial w_1}\right]-\frac{\partial f}{\partial x_1}\frac{\partial\lambda}{\partial w_1}& \equiv0  \\
0-\lambda\left[\frac{\partial^2f}{\partial x_2\partial x_1}\frac{\partial x_1}{\partial w_1}+\frac{\partial^2f}{\partial x_2^2}\frac{\partial x_2}{\partial w_1}\right]-\frac{\partial f}{\partial x_2}\frac{\partial\lambda}{\partial w_1}& \equiv0. 
\end{align}$$
These equations can be written in matrix form as
$$\begin{pmatrix}0&-f_1&-f_2\\-f_1&-\lambda f_{11}&-\lambda f_{21}\\-f_2&-\lambda f_{12}&-\lambda f_{22}\end{pmatrix}\begin{pmatrix}\frac{\partial\lambda}{\partial w_1}\\\frac{\partial x_1}{\partial w_1}\\\frac{\partial x_2}{\partial w_1}\end{pmatrix}\equiv\begin{pmatrix}0\\-1\\0\end{pmatrix}.$$
We can use a standard technique from matrix algebra, Cramer's rule
$$\frac{\partial x_1}{\partial w_1}=\frac{\begin{vmatrix}0&0&-f_2\\-f_1&-1&-\lambda f_{21}\\-f_2&0&-\lambda f_{22}\end{vmatrix}}{\begin{vmatrix}0&-f_1&-f_2\\-f_1&-\lambda f_{11}&-\lambda f_{21}\\-f_2&-\lambda f_{12}&-\lambda f_{22}\end{vmatrix}}.$$
Let $H$ be the determinant of the matrix in the denominator of this fraction. We know that this is a negative number by the second-order conditions for minimization. Carrying out the calculation in the numerator, we have
$$\frac{\partial x_1}{\partial w_1}=\frac{f^2_2}{H}<0$$
Hence, the conditional factor demand curve slopes downward.

Similarly, we can derive the expression for $\frac{\partial x_2}{\partial w_1}$.
$$\frac{\partial x_2}{\partial w_1}=\frac{\begin{vmatrix}0&-f_1&0\\-f_1&-\lambda f_{11}&-1\\-f_2&-\lambda f_{12}&0\end{vmatrix}}{\begin{vmatrix}0&-f_1&-f_2\\-f_1&-\lambda f_{11}&-\lambda f_{21}\\-f_2&-\lambda f_{12}&-\lambda f_{22}\end{vmatrix}}.$$
Carrying out the indicated calculations,
$$\frac{\partial x_2}{\partial w_1}=-\frac{f_2f_1}{H}>0\tag{4.6}$$
Repeating the same sorts of calculations for $\frac{\partial x_1}{\partial w_2}$, we find
$$\frac{\partial x_1}{\partial w_2}=\frac{\begin{vmatrix}0&0&-f_2\\-f_1&0&-\lambda f_{12}\\-f_2&-1&-\lambda f_{22}\end{vmatrix}}{\begin{vmatrix}0&-f_1&-f_2\\-f_1&-\lambda f_{11}&-\lambda f_{21}\\-f_2&-\lambda f_{12}&-\lambda f_{22}\end{vmatrix}}.$$
which implies
$$\frac{\partial x_1}{\partial w_2}=-\frac{f_1f_2}{H}>0\tag{4.7}$$
Comparing expressions (4.6) and (4.7), we see that they are identical. Thus $\frac{\partial x_1}{\partial w_2}$ equals $\frac{\partial x_2}{\partial w_1}$. Just as in the case of profit maximization, we find a symmetry condition: as a consequence of the model of cost minimization the "cross-price effects must be equal."
In the two-input case under examination here, the sign of the cross-price effect must be positive. That is, the two factors must be **substitutes**. This is special to the two-input case; 
if there are more factors of production, the cross-price effect between any two of them can go either direction.

We now proceed to rephrase the above calculations in terms of matrix algebra.
The first-order conditions for cost minimization are
$$\begin{aligned}f(\mathbf{x}(\mathbf{w}))&\equiv y\\\mathbf{w}-\lambda\mathbf{D}f(\mathbf{x}(\mathbf{w}))&\equiv\mathbf{0}.\end{aligned}$$
Differentiating these identities with respect to w we find:
$$\begin{aligned}\mathbf{D}f(\mathbf{x}(\mathbf{w}))\mathbf{D}\mathbf{x}(\mathbf{w})&=\mathbf{0}\\\mathbf{I}-\lambda\mathbf{D}^2f(\mathbf{x}(\mathbf{w}))\mathbf{D}\mathbf{x}(\mathbf{w})-\mathbf{D}f(\mathbf{x}(\mathbf{w}))\mathbf{D}\lambda(\mathbf{w})&=\mathbf{0}.\end{aligned}$$
Rearranging slightly gives us
$$\begin{pmatrix}0&-\mathbf{D}f(\mathbf{x})\\-\mathbf{D}f(\mathbf{x})^t&-\lambda\mathbf{D}^2f(\mathbf{x})\end{pmatrix}\begin{pmatrix}\mathbf{D}\lambda(\mathbf{w})\\\mathbf{D}\mathbf{x}(\mathbf{w})\end{pmatrix}=-\begin{pmatrix}0\\\mathbf{I}\end{pmatrix}$$
$$\begin{pmatrix}\mathbf{D}\lambda(\mathbf{w})\\\mathbf{D}\mathbf{x}(\mathbf{w})\end{pmatrix}=\begin{pmatrix}0&\mathbf{D}f(\mathbf{x})\\\mathbf{D}f(\mathbf{x})^t&\lambda\mathbf{D}^2f(\mathbf{x})\end{pmatrix}^{-1}\begin{pmatrix}0\\\mathbf{I}\end{pmatrix}.$$

### Algebraic approach to cost minimization
An obvious necessary condition is that the cost of the observed choice of inputs is no greater than the cost of any other level of inputs that would produce at least as much output. Translated into symbols, this says
$$\mathbf{w}^t\mathbf{x}^t\leq \mathbf{w}^t\mathbf{x}^s\text{ for all }s\text{ and }t\text{ such that }t^s\geq y^t $$
We will refer to this condition as the Weak Axiom of Cost Minimization (WACM).
==暂时没有看懂 P75==

## Cost Function
In general, the cost function can always be expressed simply as the value of the conditional factor demands.
$$c(\mathbf{w},y)=\mathbf{wx}(\mathbf{w},y)$$

short-run total cost = STC = $\mathbf{w}_v\mathbf{x}_v(\mathbf{w},y,\mathbf{x}_f)+\mathbf{w}_f\mathbf{x}_f$ 
short-run average cost = SAC = $\frac{c(\mathbf{w},y,\mathbf{x}_f)}{Y}$
short-run average variable cost = SAVC = $\frac{\mathbf{w}_v\mathbf{x}_v(\mathbf{w},y,\mathbf{x}_f)}{Y}$ 
short-run average fixed cost = SAFC = $\frac{\mathbf{w}_f\mathbf{x}_f}{Y}$ 
short-run marginal cost = SMC = $\frac{\partial c(\mathbf{w},y,\mathbf{x}_f)}{\partial y}$

long-run average cost=LAC=$\frac{c(\mathbf{w},y)}{Y}$
long-run marginal cost=LMC=$\frac{\partial c(\mathbf{w},y)}{\partial y}$

EXAMPLE: 
The short-run Cobb-Douglas cost functions Suppose the second factor in a Cobb-Douglas technology is restricted to operate at a level $k$. Then the cost-minimizing problem is
$$\begin{align}
\min\ w_1x_1+w_2k\\
\text{such that }y=x^a_1k^{1-a}
\end{align}$$
Solving the constraint for $x_1$ as a function of $y$ and $k$ gives
$$x_1=(yk^{a-1})^{\frac{1}{a}}$$
Thus
$$c(w_1,w_2,y,k)=w_1(yk^{a-1})^{\frac{1}{a}}+w_2k$$
The following variations can also be calculated:
$$\text{short-run average cost =}w_1(\frac{y}{k})^{\frac{1-a}{a}}+\frac{w_2 k}{y}$$
$$\text{short-run average variable cost=}w_1(\frac{y}{k})^{\frac{1-a}{a}}$$
$$\text{short-run average fixed cost =}\frac{w_2 k}{y}$$
$$\text{short-run marginal cost=}\frac{w_1}{a}(\frac{y}{k})^{\frac{1-a}{a}}$$

**Properties of the cost function**
1. Nondecreasing in $w$. If $\mathbf{w'}\geq \mathbf{w}$, then $c(\mathbf{w'},y)\geq c(\mathbf{w},y)$
2. Homogeneous of degree 1 in $w$. $c(t\mathbf{w},y)=tc(\mathbf{w},y)$ for $t>0$
3. Concave in $w$. $c(t\mathbf{w}+(1-t)\mathbf{w'},y)\geq tx(\mathbf{w},y)+(1-t)c(\mathbf{w'},y)$ for $0\leq t \leq 1$
	1. Let $(\mathbf{w}, x)$ and $(\mathbf{w}', x')$ be two cost-minimizing price-factor combinations and let $\mathbf{w}" = t\mathbf{w} + (1-t)\mathbf{w}'$ for any $0 \leq t\leq 1$. Now,
	2. $c(\mathbf{w}'',y)=\mathbf{w}''\mathbf{x}''=t\mathbf{w}\mathbf{x}''+(1+t)\mathbf{w}'\mathbf{x}''$
	3. Since $\mathbf{x}''$ is not necessarily the cheapest way to produce y at prices $\mathbf{w}'$ or $\mathbf{w}$, we have $\mathbf{wx}" \geq c(\mathbf{w}, y)$ and $\mathbf{w}'\mathbf{x}" \geq c(\mathbf{w}', y)$. Thus,
	4. $c(\mathbf{w}'',y)\geq tx(\mathbf{w},y)+(1+t)c(\mathbf{w}',y)$
4. Continuous in $w$. $c(\mathbf{w},y)$ is continuous as a function of $w$, for $w>0$
Proof is on P86

**Shephard's lemma**. (The derivative property.) 
Let $x_i(w, y)$ be the firm's conditional factor demand for input $i$. Then if the cost function is differentiable at $(w, y)$, and $w_i > 0$ for $i = 1,. . . , n$ then
$$x_i(\mathbf{w},y)=\frac{\partial c(\mathbf{w},y)}{\partial w_i}\quad i=1,\dots,n$$ 
### Comparative statics using the cost function
1. The cross-price effects are symmetric. That is
$$\frac{\partial x_i(\mathbf{w},y)}{\partial w_j}=\frac{\partial^2 c(\mathbf{w},y)}{\partial w_j \partial w_i}=\frac{\partial^2 c(\mathbf{x},y)}{\partial w_i \partial w_j}=\frac{\partial x_j(\mathbf{x},y)}{\partial w_i}$$
2. The own-price effects are nonpositive. Roughly speaking, the conditional factor demand curves are downward sloping. This follows since $\partial x_i(\mathbf{w}, y)/\partial w_i, = \partial^2 c(\mathbf{w}, y)/\partial w^2_i\leq0$ where the last inequality comes from the fact that the diagonal terms of a negative semidefinite matrix must be nonpositive.
3. The vector of changes in factor demands moves "opposite" the vector of changes in factor prices. That is, $\frac{dw}{dx}\leq0$.

## Duality
the cost function contains essentially the same information that the production function contains. Any concept defined in terms of the properties of the production function has a "dual" definition in terms of the properties of the cost function and vice versa. This general observation is known as the principle of **duality**.
## Choice
If we let $p_1$ vary and hold $p_2$ and m fixed, our budget line will tilt, and the locus(轨迹) of tangencies will sweep out a curve known as the **price offer curve**.
a decrease in the price of good 1 brings about a decreased demand for good 1. Such a good is called a **Giffen good**.

![Pasted image 20231102094529](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353592.png)
Excise tax and income tax. A consumer is always worse off facing an excise tax than an income tax that generates the same revenue.

## Demand Functions and Revealed Preference
1. $e\big(\mathbf{p},v(\mathbf{p},m)\big)\equiv m$. The minimum expenditure necessary to reach utility $v(\mathbf{p}, m)$ is $m$.
2. $v\big(\mathbf{p},e(\mathbf{p},u)\big)\equiv u$. The maximum utility from income $e(\mathbf{p}, u)$ is $u$. 
3. $x_i(\mathbf{p},m)\equiv h_i \big(\mathbf{p},v(\mathbf{p},m)\big)$. The Marshallian demand at income m is the same as the Hicksian demand at utility $v(\mathbf{p}, m)$.
4. $h_i(\mathbf{p},u)\equiv x_i\big(\mathbf{p},e(\mathbf{p},u)\big)$. The Hicksian demand at utility $u$ is the same as the Marshallian demand at income $e(\mathbf{p}, u)$.

The function $v(\mathbf{p}, m)$ that gives us the maximum utility achievable at given prices and income is called the **indirect utility function**. The value of x that solves this problem is the consumer's **demanded bundle**
Properties of the indirect utility function
1. $v(\mathbf{p}, m)$ is nonincreasing in $\mathbf{p}$
2. $v(\mathbf{p}, m)$ is homogeneous of degree 0 in $(p, m)$.
3. $v(\mathbf{p}, m)$ is quasiconvex in $p$; that is, $\{p : v(\mathbf{p},m) \leq k\}$ is a convex set for all $k$.
4. $v(\mathbf{p}, m)$ is continuous at all $p > 0, m > 0$.

An equivalent definition of the expenditure function is given by the following problem:
$$\begin{align}
e(\mathbf{p},u)=\min \mathbf{px}\\
\text{such that }u(\mathbf{x})\geq u
\end{align}$$
The expenditure function gives the minimum cost of achieving a fixed level of utility.
#### Properties of the expenditure function
1. $e(\mathbf{p},u)$ is nondecreasing in $p$
2. $e(\mathbf{p},u)$ is homogeneous of degree 1 in $p$
3. $e(\mathbf{p},u)$ is concave in $p$
{ #ExpenditureConcave}


[Proof](https://www.youtube.com/watch?v=HCANzswyhis)
	Assume $p''=\alpha p+(1-\alpha) p'$
	We need to prove $e(p'',\overline{u})\geq \alpha e(p,\overline{u})+(1-\alpha)e(p',\overline{u})$
	$e(p'',\overline{u})=p''\cdot x(p'',\overline{u})=p''\cdot h(p'',\overline{u})=\alpha p h(p'',\overline{u})+(1-\alpha)p'h(p'',\overline{u})$
	since $ph(p'',\overline{u})\geq e(p,\overline{u})$ and $p'h(p'',\overline{u})\geq e(p',\overline{u})$ ($e(p,\overline{u})$ is chpeast boundle under $p$, $e(p',\overline{u})$ is chpeast boundle under $p'$)
	Therefore, $e(p'',\overline{u})\geq \alpha e(p,\overline{u})+(1-\alpha)e(p',\overline{u})$

4. $e(\mathbf{p},u)$ is continuous in $p$, for $p>0$
5. If $h(\mathbf{p},u)$ is the expenditure-minimizing bundle necessary to achieve utility level u at prices p, then $h_i(\mathbf{p},u)=\frac{\partial e(\mathbf{p},u)}{\partial p_i}$
{ #HicksianAndExpenditure}


The function $h(\mathbf{p}, u)$ is called the **Hicksian** demand function.
Hicksian demand function is sometimes called **a compensated demand function**.(Hicksian=compensated demand function) This terminology comes from viewing the demand function as being constructed by varying prices and income so as to keep the consumer at a fixed level of utility. Thus, the income changes are arranged to 'compemate" for the price changes.
we want to emphasize the difference between the Hicksian demand function and the usual demand function, we will refer to the latter as the **Marshallian** demand function, $x(p,m)$

#### **Roy's identity**.
If $\mathbf{x}(\mathbf{p}, m)$ is the Marshallian demand function, then
$$x_i(\mathbf{p},m)=-\frac{\frac{\partial v(\mathbf{p},m)}{\partial p_i}}{\frac{\partial v(\mathbf{p},m)}{\partial m}}\text{ for }i=1,\cdots,k$$
$$\begin{aligned}\mathsf{Proof}{:}\\&u^*\equiv\nu(\boldsymbol{p},\boldsymbol{e}(\boldsymbol{p},u^*))\\\\&0=\frac{\partial v(\boldsymbol{p}^*,\boldsymbol{m}^*)}{\partial p_i}+\frac{\partial\nu(\boldsymbol{p}^*,\boldsymbol{m}^*)}{\partial m}\frac{\partial e(\boldsymbol{p},\boldsymbol{m}^*)}{\partial p_i}\\\\&x_i(\boldsymbol{p}^*,\boldsymbol{m}^*)\equiv h_i(\boldsymbol{p}^*,\boldsymbol{u}^*)=\frac{\partial e(\boldsymbol{p},\boldsymbol{m}^*)}{\partial p_i}=-\frac{\frac{\partial v(\boldsymbol{p},\boldsymbol{m})}{\partial p_i}}{\frac{\partial v(\boldsymbol{p},\boldsymbol{m})}{\partial\boldsymbol{m}_°}}\end{aligned}$$
在知道indirect utility function的情况下用来计算demnand function
{ #RoyIdentity}

### Law of Demand
$\frac{\partial x_i(\mathbf{p},m)}{\partial p_i}=\frac{\partial h(\mathbf{p},u)}{\partial p_i}-x^*_i \frac{\partial x_i(\mathbf{p},m)}{\partial m}$
The first thing is negative, the second thing is always positive, therefore the slope is always downward(这个存在记错的可能性，没有证明过)
10/20 研究了一边感觉是没有记错的
$$\begin{aligned}\mathsf{Proof}{:}&\quad h_i(\boldsymbol{p},u)\equiv x_i(\boldsymbol{p},e(\boldsymbol{p},u))\\\frac{\partial h(\boldsymbol{p},u)}{\partial p_i}&=\frac{\partial x_i(\boldsymbol{p},m)}{\partial p_i}+\frac{\partial x_i(\boldsymbol{p},m)}{\partial m}\frac{\partial e(\boldsymbol{p},u)}{\partial p_i}\end{aligned}$$

### Revealed Preference
Definition: Suppose $\mathbf{x^t}$ is chosen when prices are $\mathbf{p^t}$, and is chosen when prices are $\mathbf{p}$. If $\mathbf{p^t x^t}\geq \mathbf{p^t x}$, then $\mathbf{x^t}$ is directly revealed preferred to $\mathbf{x}$, or $\mathbf{x^r}\ R^D\ \mathbf{x}$
As a consequence of this definition and the assumption that the data were generated by utility maximization, we can conclude that "$\mathbf{x}^tR^D\mathbf{x}$ implies $u(\mathbf{x}^t) \geq u(\mathbf{x})$."

If $\mathbf{p}^t\mathbf{x}^t > \mathbf{p}^t \mathbf{x}$, we will say that $\mathbf{x}^t$ is strictly directly revealed preferred to $\mathbf{x}$ and write $\mathbf{x}^t P^D \mathbf{x}$.

[Zhiguo He | The University of Chicago Booth School of Business](https://www.chicagobooth.edu/faculty/directory/h/zhiguo-he)
Shi Ce mentioned him

**GARP**
$\mathbf{x}^t R\ \mathbf{x}^s$ implies not $\mathbf{x}^S P^D \mathbf{x}^t$. In other words, $\mathbf{x}^t R \mathbf{x}^S$ implies $\mathbf{p}^s\mathbf{x}^s \leq \mathbf{p}^s\mathbf{x}^t$.0
### Slutsky equation $w/\Delta$
the derivative of the Marshallian demand with respect to price and income. This relationship is known as the Slutsky equation.
$$\frac{\partial x_j(\mathbf{p},m)}{\partial \mathbf{p}_i}=\frac{\partial h_j(\mathbf{p},v(\mathbf{p},m))}{\partial p_i}-\frac{\partial x_j(\mathbf{p},m)}{\partial m}x_i(\mathbf{p},m)$$
	Proof:
	It is identically true that
$$h_j(\mathbf{p},u^*)\equiv x_j(\mathbf{p},e(\mathbf{p},u^*))$$
	We can differentiate this with respect to $p_i$ and evaluate the derivative at $\mathbf{p}^*$ to get
$$\frac{\partial h_j(\mathbf{p}^*,u^*)}{\partial p_i}=\frac{\partial x_j(\mathbf{p}^*,m^*)}{\partial p_i}+\frac{\partial x_j(p^*,m^*)}{d m}\frac{\partial e(\mathbf{p}^*,u^*)}{\partial p_i}$$
	According to ShepherdLemma
$$\frac{\partial x_j(\mathbf{p}^*,m^*)}{\partial \mathbf{p}_i}=\frac{\partial h_j(\mathbf{p}^*,u^*)}{\partial p_i}-\frac{\partial x_j(\mathbf{p}^*,m^*)}{\partial m}x^*_i(\mathbf{p},m)$$

Divide both sides by $\Delta p_i$:
$$\frac{x_i(\mathbf{p}+\Delta\mathbf{p},m)-x_i(\mathbf{p},m)}{\Delta p_i}=\frac{\Delta x_i}{\Delta p_i}-x_i\frac{\Delta x_i}{\Delta m}$$
第一项是对price研究，第二项是对budget的里面

The Slutsky equation decomposes the demand change induced by a price change $\Delta p_i$ into two separate effects: the substitution effect and the income effect

In the two-good case the Slutsky equation looks like this:
$$\begin{aligned}
\mathbf{D}_{p}\mathbf{x}(\mathbf{p},m)& =\mathbf{D}_{p}\mathbf{h}(\mathbf{p},u)-\mathbf{D}_{m}\mathbf{x}(\mathbf{p},m)\mathbf{x}  \\
\begin{bmatrix}\frac{\partial x_1(\mathbf{p},m)}{\partial p_1}&\frac{\partial x_1(\mathbf{p},m)}{\partial p_2}\\\frac{\partial x_2(\mathbf{p},m)}{\partial p_1}&\frac{\partial x_2(\mathbf{p},m)}{\partial p_2}\end{bmatrix}& =\begin{bmatrix}\frac{\partial h_{1}(\mathbf{p},u)}{\partial p_{1}}&\frac{\partial h_{1}(\mathbf{p},u)}{\partial p_{2}}\\\frac{\partial h_{2}(\mathbf{p},u)}{\partial p_{1}}&\frac{\partial h_{2}(\mathbf{p},u)}{\partial p_{2}}\end{bmatrix}  \\
&-\begin{bmatrix}\frac{\partial x_1(\mathbf{p},m)}{\partial m}\\\frac{\partial x_2(\mathbf{p},m)}{\partial m}\end{bmatrix}[x_1,x_2]
\end{aligned}$$
where $u=v(\mathbf{p},m)$
Expanding the last term gives
$$\begin{bmatrix}\frac{\partial x_1(\mathbf{p},m)}{\partial m}\\\frac{\partial x_2(\mathbf{p},m)}{\partial m}\end{bmatrix}[x_1,x_2]=\begin{bmatrix}\frac{\partial x_1(\mathbf{p},m)}{\partial m}x_1&\frac{\partial x_1(\mathbf{p},m)}{\partial m}x_2\\\frac{\partial x_2(\mathbf{p},m)}{\partial m}x_1&\frac{\partial x_2(\mathbf{p},m)}{\partial m}x_2\end{bmatrix}$$
Suppose we consider a price change $\Delta \mathbf{p} = (\Delta p_1, \Delta p_2)$ and we are interested in the approximate change in demand $\Delta x = (\Delta x_1, \Delta x_2)$.
$$\begin{gathered}
\left.\left[\begin{smallmatrix}\Delta x_1\\\Delta x_2\end{smallmatrix}\right.\right] \left.\approx\left[\begin{array}{ll}{\frac{\partial h_{1}}{\partial p_{1}}}&{\frac{\partial h_{1}}{\partial p_{2}}}\\{\frac{\partial h_{2}}{\partial p_{1}}}&{\frac{\partial h_{2}}{\partial p_{2}}}\\\end{array}\right.\right]\left[\begin{array}{l}{\Delta p_{1}}\\{\Delta p_{2}}\\\end{array}\right]-\left[\begin{array}{ll}{\frac{\partial x_{1}}{\partial m}x_{1}}&{\frac{\partial x_{1}}{\partial m}x_{2}}\\{\frac{\partial x_{2}}{\partial m}x_{1}}&{\frac{\partial x_{2}}{\partial m}x_{2}}\\\end{array}\right]\left[\begin{array}{l}{\Delta p_{1}}\\{\Delta p_{2}}\\\end{array}\right] \\
\left.=\quad\left[\begin{matrix}{\Delta x_{1}^{s}}\\{\Delta x_{2}^{s}}\\\end{matrix}\right.\right]\quad-\quad\left[\begin{matrix}{\Delta x_{1}^{m}}\\{\Delta x_{2}^{m}}\\\end{matrix}\right] 
\end{gathered}$$
The first vector is the substitution effect. It indicates how the Hicksian demands change. Since changes in Hicksian demands keep utility constant, $(\Delta x^s_1, \Delta x^s_2)$ will be tangent to the indifference curve. The second vector is the income effect. The price change has caused "purchasing power" to change by $x_1\Delta p_1+x_2\Delta p_2$ and the vector ($\Delta x^m_1,\Delta x^m_2$) measures the impact of this change on demand, with prices held constant at the initial level. This vector therefore lies along the income expansion path.
![1699356953140](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353593.png)


#### The Hicks decomposition of a demand change: 
Example: 
$U=x_1x_2,m=72,p_1=9,p_2=1$
If $p_1=9\rightarrow p_1=4$, what is the substitution effect and the income effect?
	Solution:
	When $p_1=4,U=(72-4x_2)x_2$ 
	$\max U=324$
	$\frac{MU_1}{MU_2}=\frac{x_2}{x_1}=\frac{P_2}{P_1}=9$
	$U'=9\cdot 36=324$
	$\Rightarrow x_1=6\ x_2=54$
	$4\rightarrow 6$ is the income effect, $6\rightarrow 9$ is the substituion effect.
![5ee8a52a5b4f587ffadd0be7ad01341](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353594.jpg){ #HicksDecomposition}


EXAMPLE: The Cobb-Douglas Slutsky equation
Let us check the Slutsky equation in the CobbDouglas case. As we've seen, in this case we have (accordint to [[Microeconomics#Related Curve of Cobb-Douglas\|Indirect Utility of Cobb-Douglas]])
$$\begin{aligned}
&v(p_{1},p_{2},m)=mp_{1}^{-a}p_{2}^{a-1}  \\
&e(p_{1},p_{2},u)=up_{1}^{a}p_{2}^{1-a}  \\
&x_{1}(p_{1},p_{2},m)=\frac{am}{p_{1}}  \\
&h_{1}(p_{1},p_{2},u)=ap_{1}^{a-1}p_{2}^{1-a}u. 
\end{aligned}$$
Thus,
$$\begin{aligned}
\frac{\partial x_{1}(\mathbf{p},m)}{\partial p_{1}}& =-\frac{am}{p_{1}^{2}}  \\
\frac{\partial x_{1}(\mathbf{p},m)}{\partial m}& =\frac{a}{p_{1}}  \\
\frac{\partial h_{1}(\mathbf{p},u)}{\partial p_{1}}& =a(a-1)p_{1}^{a-2}p_{2}^{1-a}u  \\
\frac{\partial h_{1}(\mathbf{p},v(\mathbf{p},m))}{\partial p_{1}}& =a(a-1)p_{1}^{a-2}p_{2}^{1-a}mp_{1}^{-a}p_{2}^{a-1}  \\
&=a(a-1)p_{1}^{-2}m.
\end{aligned}$$
Now plug into the Slutsky equation to find
$$\begin{aligned}
{\frac{\partial h_{1}}{\partial p_{1}}}-{\frac{\partial x_{1}}{\partial m}}x_{1}& =\frac{a(a-1)m}{p_{1}^{2}}-\frac{a}{p_{1}}\frac{am}{p_{1}}  \\
&=\frac{[a(a-1)-a^{2}]m}{p_{1}^{2}} \\
&=\frac{-am}{p_{1}^{2}}=\frac{\partial x_{1}}{\partial p_{1}}.
\end{aligned}$$
### Properties of demand functions
1. The matrix of substitution terms $\frac{\partial h_j(\mathbf{p},u)}{\partial p_i}$ is negative semidefinite. This follows because(according to [[Microeconomics#The Hicks decomposition of a demand change\|The Hicks decomposition of a demand change]])
$$\frac{\partial h_j(\mathbf{p},u)}{\partial p_i}=\frac{\partial^2 e(\mathbf{p},u)}{\partial p_i \partial p_j}$$
which is negative semidefinite because the [[Microeconomics#Properties of the expenditure function\|expenditure function is concave]].

2. The matrix of substitution terms is symmetric——since
$$\frac{\partial h_j(\mathbf{p},u)}{\partial p_i}=\frac{\partial^2 e(\mathbf{p},u)}{\partial p_j \partial p_i}=\frac{\partial^2 e(\mathbf{p},u)}{\partial p_i \partial p_j}=\frac{\partial h_i(\mathbf{p},u)}{\partial p_j}$$

3. In particular, "the compensated own-price effect is nonpositive"; that is, the Hicksian demand curves slope downward:
$$\frac{\partial h_i(\mathbf{p},u)}{\partial p_i}=\frac{\partial^2 e(\mathbf{p},u)}{\partial p^2_i} \leq 0$$
since the substitution matrix is negative semidefinite and thus has non-positive diagonal terms.
==这个看不懂== 11.14 这是二阶导的意思，应该可证明

4. The substitution matrix $(\frac{\partial x_j(\mathbf{p},m)}{\partial p_i}+\frac{\partial x_j(\mathbf{p},m)}{\partial m}x_i)$ is a symmetric, negative semidefinite matrix

==后面看不懂了==

## Preference and Utility
Our ultimate goal is to get demand curve

Consumption set: $X$
Consumption bundles: $x,y$
Preference relations: 
	''$R$'': weak preference $\succcurlyeq$
	"$P$": strict preference $\succ$
	"$I$": Indifference

1. Completerness
For all $x,y$ in $X$, there is (i) $x\ R\ y$, or (ii) $y\ R\ x$, or (iii) both
2. Reflexivity
For all $x$ in $X$, $x\ R\ x$.
3. Transitivity
For all $x,y,z$ in $X$, if $x\ R\ y$, and $y\ R\ z$, then $x\ R\ z$
No cyclical preference
4. Continuity
If $\{x_i\}$ is a sequence of bundles that converges to bundle $x$, and if $x_i\ R\ y$ for all $i$, then $x\ R\ y$
No "lexicographic preferences"
==这个有点不懂== lexicographic means dictionary
现实生活中有一种常见的偏好会违背连续性，那就是 Lexicographic preference。假设超市促销，将苹果和香蕉捆绑售卖，但提供不同的组合套餐。你超级喜欢苹果，因此你对这些套餐的偏好是：首先看苹果的数量，选苹果数量最多的；如果两个套餐中苹果的数量一样，再选香蕉更多的。

If Axioms 1-4 hold, then we can use a continuous utility function to represent the underlying preferences with $x\ P\ y$ if and only if $u(x)>u(y)$.

5. (Weak) Monotonicity
If $x\geq y$, then $x\ R\ y$ (You will not be worse off if you consume more)
![Pasted image 20231005131604](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353595.png)
6. Non-satiation
For any $x$ in $X$ and $\varepsilon >0$, then there exists some bundle $y$ in $X$ with $|x-y|<\varepsilon$, $y\ R\ x$  
Monotonicity implies non-satiation. (Monotonicity gives a direction"more is better")

If Axioms 1 - 4 + 5 hold, show there exists a continuous utility function that represents the underlying preferences with $\mathbf{x\ P\ y}$ if and only if $u(x)>u(y)$.

### Utility Function
- $u(x)$ is ordinal (e.g., movie rating) not cardinal (e.g., test scores) 
- Given a (positive) monotonic function $f$ ,$u(x)$ and $f(u(x))$ represent the same underlying preferences. 
- No interpersonal comparison of utilities.

Indiffernece Curve的三维示意图
![Pasted image 20231005134055](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353596.png)
**Marginal Rate of Substitution**
For $$U(x_1,x_2)=u$$
$$du=\frac{\partial U}{\partial x_1}dx_1+\frac{\partial U}{\partial x_2}dx_2$$
For a constant $u$
$$0=\frac{\partial U}{\partial x_1}dx_1+\frac{\partial U}{\partial x_2}dx_2$$
So,
$$\frac{dx_2}{dx_1}=-\frac{\partial U/\partial x_1}{\partial U/\partial x_2}$$


### Utility Maximization: Two Goods
Consumers' problem is to
$$\begin{align}
\max U(x_1,x_2)\\
\text{subject to }p_1x_1+p_2x_2\leq m
\end{align}$$
From the Lagrangian:
$$L=U(x_1,x_2)+\lambda(m-p_1x_1-p_2x_2)$$
FOCs (for an interior optimum):
$$\begin{align}
\frac{\partial L}{\partial x_1}=U_1-\lambda p_1=0\\
\frac{\partial L}{\partial x_2}=U_2-\lambda p_2=0\\
\frac{\partial L}{\partial \lambda}=m-p_1x_1-p_2x_2=0
\end{align}$$
FOCs imply:
$$\begin{align}
p_1x_1+p_2x_2=m\\
p_1/U_1=p_2/U_2
\end{align}$$
The maximum should touch the budget line and the solpe is the matginal substitution.
SOC requires s the border-preserving principle minor determinants of the bordered Hessian matrix alternate in sign. $|\bar{H}|>0$ ==为什么最大值要Hessian大于0== 根据教材P499:It turns out that in the case of a regular maximum with $b\neq0$, the second-order conditions given above imply that the bordered Hessian has a positive determinant.
![Pasted image 20231005143341](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353597.png)

![Pasted image 20231005144050](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353598.png)
$\frac{\partial x_1}{\partial p_1}$ is also demand curve
$\frac{\partial x_1}{\partial m}$ incmome effect and  $p_2$ substitution effect
只有当第一项是inferior good而且足够大，demand curve才会向上

$v(\mathbf{p},m)=u(x(\mathbf{p},m))$: indirect utility function


### Expenditure Minimization: 2-goods
$$\begin{align}
\max p_1x_1+p_2x_2\\
\text{subject to }U(x_1,x_2)=u_0
\end{align}$$
From the Lagrangian:
$$L=p_1x_1+p_2x_2+\lambda(u_0-U(x_1,x_2))$$
#### Kink Effect
![Pasted image 20231005150920](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353599.png)

![Pasted image 20231005151004](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353600.png)
给food stamp带来的效用不如现金，但是食物消费会更多
{ #kinkEffect}

### Problem Set 2
Chapter 4 Problems: 4.1, 4.2, 4.3, 4.5, 4.6, 4.8* 
Chapter 5 Problems: 5.1, 5.2, 5.4, 5.5, 5.6, 5.7 (=4.8!), 5.8, 5.9*, 5.11*, 5.13, 5.16, 5.17 
Chapter 7 Problems: 7.2*, 7.3, 7.4, 7.5*, 7.6 
Chapter 8 Problems: 8.2, 8.5, 8.6*, 8.8, 8.11, 8.12, 8.14, 8.16

4.1 Prove rigorously that profit maximization implies cost minimization
	Let $\mathbf{x}^∗$ be a profit-maximizing input vector for prices $(p,\mathbf{w})$. This means that $\mathbf{x}^∗$ must satisfy $pf(\mathbf{x}^∗) − w\mathbf{x}^∗ ≥ pf(\mathbf{x}) − w\mathbf{x}$ for all permissible $\mathbf{x}$. 
	Assume that $\mathbf{x}^∗$ does not minimize cost for the output $f(\mathbf{x}^∗)$; i.e., there exists a vector $\mathbf{x}^{∗∗}$ such that $f(\mathbf{x}^{∗∗}) ≥ f(\mathbf{x}^∗)$ and $\mathbf{w}(\mathbf{x}^{∗∗}− \mathbf{x}^∗ ) < 0$. But then the profits achieved with $\mathbf{x}^{∗∗}$ must be greater than those achieved with $\mathbf{x}^∗$ :
$$pf(\mathbf{x}^{**})-\mathbf{wx}^{**}\geq pf(\mathbf{x}^{*})-\mathbf{wx}^{**}\geq pf(\mathbf{x}^{*})-\mathbf{wx}^{*}$$
	which contradicts the assumption that $\mathbf{x}^∗$ was profit-maximizing.

4.8 A firm has a production function $y = x_1x_2$. If the minimum cost of production at $w_1= w_2 = 1$ is equal to 4, what is $y$ equal to?
	Solution
$$\begin{align}
\min x_1+x_2\\
x_1x_2=y
\end{align}$$
	Substitute to get the unconstrained minimization problem
$$\min x_1+\frac{y}{x_1}$$
	The first order condition is
$$1-\frac{y}{x^2_1}$$
	which implies $x_1=\sqrt{y}$. By symmetry, $x_2=\sqrt{y}$. We are given that $2\sqrt{y}=4$, so $\sqrt{y}=2$, from which it follows that $y=4$

5.9. A typical Silicon Valley firm produces output of chips $y$ using a cost function $c(y)$, which exhibits increasing marginal costs. Of the chips it produces, a fraction $1 - a$ are defective and cannot be sold. Working chips can be sold at a price $p$ and the chip market is highly competitive. 
(a) Calculate the derivative of profits with respect to $a$ and its sign. 
	Solution:
	$\pi=p(ay)-c(y)$
	$\frac{\partial \pi}{\partial a}=py>0$
(b) Calculate the derivative of output with respect to a and its sign. 
	Solution:
	$\frac{dy}{d a}=-\frac{d\pi/d a}{d\pi/ dy}=-\frac{yp}{ap-c'(y)}$
	$\frac{d\pi}{dy}=ap-c'(y)=f(a,y)$
	$\frac{dy}{da}=-\frac{df(a,y)/da}{df(a,y)/da}=\frac{p}{c''(y)}>0$
	10.19Shi Ce:使用$\pi$ 或其一阶条件等价
(c) Suppose that there are n identical chip producers, let $D(p)$ be the demand function, and let $p(a)$ be the competitive equilibrium price. Calculate ($dp/da$) and its sign.
	Solution:
	$D(p^*)=\underbrace{a\cdot n\cdot y^*}_{supply} \quad (Q)$
	$\frac{d P}{d a}=-\frac{dQ/ da}{dQ/dp^*}$
	==这题还是不太清楚==
	AI's answer:
	To calculate $\frac{dp}{da}$ and determine its sign, we need to analyze the effects of a change in the fraction of defective chips $(a)$ on the competitive equilibrium price $(p)$.
	In a competitive market, the equilibrium price is determined by the intersection of the market demand $(D(p))$ and market supply. Given that there are $n$ identical chip producers, each with cost function $c(y)$, the market supply is the sum of the individual firm's supply, which can be expressed as $n \cdot y(a)$, where $y(a)$ is the quantity of working chips produced by each firm.
	To determine the equilibrium price, we equate the market demand and market supply:
	
$$D(p) = n \cdot y(a)$$
	Now, let's differentiate both sides of the equation with respect to $a$:
	
$$\frac{d}{da} D(p) = \frac{d}{da} (n \cdot y(a))$$
	Using the chain rule, we have:
	
$$\frac{dD}{dp} \cdot \frac{dp}{da} = n \cdot \frac{dy}{da}$$
	Rearranging the equation, we can solve for $\frac{dp}{da}$:
	
$$\frac{dp}{da} = \frac{n}{\frac{dD}{dp}} \cdot \frac{dy}{da}$$
	To determine the sign of $\frac{dp}{da}$, we need to consider the signs of $\frac{dD}{dp}$ and $\frac{dy}{da}$.
	Since the cost function $c(y)$ exhibits increasing marginal costs, the marginal cost of production is positive. As a result, the supply curve of each individual firm slopes upward, indicating that $\frac{dy}{da}$ is positive.
	The sign of $\frac{dD}{dp}$ depends on the demand function $D(p)$. Without specific information about the form of the demand function, we cannot determine its sign.
	Therefore, the sign of $\frac{dp}{da}$ will depend on the relative magnitudes and signs of $\frac{dy}{da}$ and $\frac{dD}{dp}$. If $\frac{dy}{da}$ is larger than zero and $\frac{dD}{dp}$ is positive, then $\frac{dp}{da}$ will also be positive. Conversely, if $\frac{dy}{da}$ is larger than zero and $\frac{dD}{dp}$ is negative, then $\frac{dp}{da}$ will be negative.
	In summary, without specific information about the demand function $D(p)$, we cannot determine the sign of $\frac{dp}{da}$ definitively. It will depend on the specific characteristics of the market demand and the magnitude of the change in the fraction of defective chips $(a)$

5.11 A firm uses 4 inputs to produce 1 output. The production function is $(x_1,x_2,x_3,x_4) = \min\{x_1,x_2\} +\min\{x_3,x_4\}$. 
(a) What is the vector of conditional factor demands to produce 1 unit of output when the factor price vector is $w = (1,2,3,4)$?
	$\mathbf{x}=(1,1,0,0)$
	Review 3.5, $\min\{x_1,x_2\}$ means $x_1=x_2$. $\min\{x_3,x_4\}$ means $x_3=x_4$.
	We assume $x_1=x_2=a,x_3=x_4=b$
$$\begin{align}\min 3a+7b\\
a+b=1\\
a\geq 0\\
b\geq0\end{align}$$
	We got $a=1,b=0$. Therefore, $\mathbf{x}=(1,1,0,0)$
(b) What is the cost function? 
	$c(w_1,w_2,w_3,w_4)=\min\{w_1+w_2,w_3+w_4\}y$
(c) What kind of returns to scale does this technology exhibit? 
	Constant return to scale
(d) Another firm has a production function $f (x_1, x_2,x_3,x_4) = \min\{x_1 + x_2, x_3 + x_4\}$. What is the vector of conditional factor demands to produce 1 unit of output when prices are $w = (1,2,3,4)$? 
	$\min\{x_1 + x_2, x_3 + x_4\}$ means $x_1+x_2=x_3+x_4=1$.
$$\begin{align}
\min\ x_1+2x_2+3x_3+4x_4\\
x_1+x_2=x_3+x_4=1\\
x_1\geq 0,x_2\geq0,x_3\geq 0,x_4\geq 0
\end{align}$$
	$x_1+2x_2+3x_3+4x_4=x_2+1+3+x_4$
	To make it minimum, $x_2=x_4=0$. Therefore, $x_1=x_3=1$
	the vector of conditional factor demands=$(1,0,1,0)$
(e) What is the cost function for this frim? 
	$c=[\min\{w_1,w_2\}+\min\{w_3.w_4\}]y$ ==能看懂，但是具体怎么得出的不知道== 目前还是只能靠理解，而不能靠数学推导得出结论
(f) What kind of returns to scale does this technology represent?
	Constant return to scale
{ #5-11}


7.2 A consumer has a utility function $u(x_1, x_2) = \max\{x_1, x_2\}$. What is the consumer's demand function for good 1? What is his indirect utility function? What is his expenditure function?
	Solution:
	The demand function is
$$x_1=\left\{\begin{array}{**lr**} m/p_1\quad \text{if }p_1<p_2\\ \text{any } x_1\text{ and }x_2 \text{ such that }p_1x_1+p_2x_2=m\quad \text{if }p_1=p_2\\ 0\quad \text{if }p_1>p_2\end{array}   \right.$$
	The indirect utility function is $v(p_1, p_2, m) = \max\{m/p_1, m/p_2\}$, and the expenditure function is $e(p_1, p_2, u) = u\min\{p_1, p_2\}$.

7.5 A consumer has a direct utility function of the form 
$$U(x_1,x_2)=u(x_1)+x_2$$
Good 1 is a discrete good; the only possible levels of consumption of good 1 are $x_1 = 0$ and $x_1 = 1$. For convenience, assume that $u(0) = 0$ and $p_2 = 1$. 
(a) What kind of preferences does this consumer have? 
	Quasilinear preference
(b) The consumer will definitely choose $x_1 = 1$ if $p_1$ is strictly less than what? 
	When $x_1=1,\max\ U(x_1,x_2)=u(1)+x_2=u(1)+(m-p_1)$
	When $x_1=0,\max\ U(x_1,x_2)=u(0)+x_2=m$
	The consumer will choose $x_1=1$ if $p_1$ is strictly less than $u(1)$ 
(c) What is the algebraic form of the indirect utility function associated with this direct utility function?
	$v(p_1,p_2,m)=\max\{u(1)+m-p_1,m\}$

8.2 Calculate the substitution matrix for the Cobb-Douglas demand system with two goods. Verify that the diagonal terms are negative and the cross-price effects are symmetric
==没懂==

8.5. Find the demanded bundle for a consumer whose utility function is  $u(x_1, x_2) = x^{\frac{3}{2}}_1x_2$ and her budget constraint is $3x_1 + 4x_2 = 100$.
	The definition of demanded bundle: textbook P113
	The value of x that solves this problem is the consumer's **demanded bundle**: it expresses how much of each good the consumer desires at a given level of prices and income. We assume that there is a unique demanded bundle at each budget
	Cobb-Douglas utility可以加个$\ln$ 来计算，比较方便

8.6 Use the utility function $u(x_1, x_2) = x^{\frac{1}{2}}_1x^{\frac{1}{3}}_2$; and the budget constraint $m = p_1x_1 +p_2x_2$ to calculate $x(\mathbf{p},m), v(\mathbf{p},m), h(\mathbf{p},u)$ and $e(\mathbf{p},u)$.
	Solution
$$\mathcal{L}(\mathbf{x},\lambda)=x^{\frac{1}{2}}_1x^{\frac{1}{3}}_2-\lambda(p_1x_1+p_2x_2-m)$$
	Derivatives,
$$\begin{align}
\frac{1}{2}x^{-\frac{1}{2}}_1x^{\frac{1}{3}}_2=\lambda p_1\\
\frac{1}{3}x^{\frac{1}{2}}_1x^{-\frac{2}{3}}_2=\lambda p_2\\
p_1x_1+p_2x_2=m
\end{align}$$
	Solving, we get
$$x_1(\mathbf{p},m)=\frac{3m}{5p_1},x_2(\mathbf{p},m)=\frac{2m}{5p_2}$$
	Plugging these demands into the utility function, we get the indirect utility function
$$v(\mathbf{p},m)=U\big(\mathbf{x}(\mathbf{p},m)\big)=(\frac{3m}{5p_1})^{\frac{1}{2}}(\frac{2m}{5p_2})^{\frac{1}{3}}=(\frac{m}{5})^{\frac{5}{6}}(\frac{3}{p_1})^{\frac{1}{2}}(\frac{2}{p_2})^{\frac{1}{3}}$$
	Rewrite the above expression replacing $v(\mathbf{p}, m)$ by $u$ and $m$ by $e(\mathbf{p}, u)$. Then solve it for $e(·)$ to get (the function that relates income and utility in this way-the inverse of the indirect utility function-is known as the expenditure function and is denoted by $e(\mathbf{p}, u)$.) 
	==这一步推导没懂== 懂了，把$u=(\frac{m}{5})^{\frac{5}{6}}(\frac{3}{p_1})^{\frac{1}{2}}(\frac{2}{p_2})^{\frac{1}{3}}$ 反过来， 根据教材P103 
$$e(\mathbf{p},u)=5(\frac{p_1}{3})^{\frac{3}{5}}(\frac{p_2}{2})^{\frac{2}{5}}u^{\frac{6}{5}}$$
	Finally, since $hi = ∂e/∂p_i$, the Hicksian demands are
$$h_1(\mathbf{p},u)=(\frac{p_1}{3})^{-\frac{2}{5}}(\frac{p_2}{2})^{\frac{2}{5}}u^{\frac{6}{5}}$$
	and
$$h_2(\mathbf{p},u)=(\frac{p_1}{3})^{\frac{3}{5}}(\frac{p_2}{2})^{-\frac{3}{5}}u^{\frac{6}{5}}$$


### Quiz 2
Consider the CES technology $y=(\alpha x^{\rho}_1+\beta x^{\rho}_2)^{\frac{1}{\rho}}$ with $\alpha \neq \beta$ and $\rho=\frac{1}{2}$. 
1. Solve for the conditional input demand function, $x^{\#}_1(p_1,p_2,y_0)$ and $x^{\#}_2(p_1,p_2,y_0)$
	Solution:
$$\begin{align}\min\ w_1x_1+w_2x_2\\ \text{s.t. }(\alpha x^{\rho}_1+\beta x^{\rho}_2)^{\frac{1}{\rho}}=y_0\\ \Rightarrow \frac{\alpha}{\beta}\frac{x^{-\frac{1}{2}}_1}{x^{-\frac{1}{2}}_2}=\frac{w_1}{w_2}\\ x^{\#}_1=\frac{y_0}{(\alpha+\frac{w_1}{w_2}\frac{\beta^2}{\alpha})^2}=\frac{w^2_2 \alpha^2}{(w^2_2\alpha^2+w_1\beta^2)^2}y_0\\ x^{\#}_2=\frac{y_0}{(\beta+\frac{w_2}{w_1}\frac{\alpha^2}{\beta})^2}  \end{align}$$
2. In this case with the CES technology, verify that $\frac{dx^{\#}_1}{dp_2}=\frac{dx^{\#}_2}{dp_1}$
	Solution:
	$\frac{dx^{\#}_1}{dw_2}$
	$x^{\#}_1=y_0 t^{-2}$
	$t=\alpha+k\frac{\beta^2}{\alpha}$
	$k=\frac{w_1}{w_2}$
$$\begin{align}\frac{dx^{\#}_1}{dw_2}&=(y_0t^{-2})'(\alpha+k\frac{\beta^2}{\alpha})'(\frac{w_1}{w_2})'\\
&=y_0(-2)t^{-3}(\frac{\beta^2}{\alpha})(-1)w_1w^{-2}_2\\
&=y_0\frac{2(\frac{\beta^2}{\alpha})w_1w^{-2}_2}{(\alpha+\frac{w_1}{w_2}\frac{\beta^2}{\alpha})^3}\\
&=y_0\frac{2(\frac{\beta^2}{\alpha})w_1w^{-2}_2\cdot w_2^3\alpha^3}{(w_2\alpha^2+w_1\beta^2)^3}\\
&=y_0\frac{2{\alpha^2\beta^2}w_1w_2}{(w_2\alpha^2+w_1\beta^2)^3}
\end{align}$$
	$\frac{dx^{\#}_2}{dw_1}$
	$x^{\#}_2=y_0 t^{-2}$
	$t=\alpha+k\frac{\alpha^2}{\beta}$
	$k=\frac{w_2}{w_1}$
$$\begin{align}\frac{dx^{\#}_2}{dw_1}&=(y_0t^{-2})'(\alpha+k\frac{\alpha^2}{\beta})'(\frac{w_2}{w_1})'\\
&=y_0(-2)t^{-3}(\frac{\alpha^2}{\beta})(-1)w_2w^{-2}_1\\
&=y_0\frac{2(\frac{\alpha^2}{\beta})w_2w^{-2}_1}{(\beta+\frac{w_2}{w_1}\frac{\alpha^2}{\beta})^3}\\
&=y_0\frac{2(\frac{\alpha^2}{\beta})w_2w^{-2}_1\cdot w_1^3\beta^3}{(w_1\beta^2+w_2\alpha^2)^3}\\
&=y_0\frac{2{\alpha^2\beta^2}w_1w_2}{(w_2\alpha^2+w_1\beta^2)^3}
\end{align}$$
	Therefore, $\frac{dx^{\#}_1}{dp_2}=\frac{dx^{\#}_2}{dp_1}$
3. Use the Shephard's Lemma to show $\frac{dx^{\#}_1}{dp_2}=\frac{dx^{\#}_2}{dp_1}$ in the general case.
	Solution:
	According to the Shephad's Lemma
	$\frac{dc}{dp_1}=x^{\#}_1\quad \frac{d_c}{dp_2}=x^{\#}_2$
	$\Rightarrow \frac{d^{\#}_1}{dp_2}=\frac{d^2 c}{dp_1p_2}\quad \frac{d^{\#}_2}{dp_1}=\frac{d^2c}{dp_2p_1}$
4. Given the CES production function, what is the firm's short-run total cost function when $x_2$ is fixed in the short-run?
	Solution:
$$\left\{\begin{array}{**lr**} \bar{x}_2 \\ (\alpha x^{\rho}+\beta x^{\rho}_2)^{\frac{1}{\rho}}=y_0\end{array}   \right.$$
	$x_1=\frac{(x_1^{\rho}-\beta \bar{x}^{\rho}_2)^{\frac{1}{\rho}}}{\alpha}$
	$c=w_1\frac{(x_1^{\rho}-\beta \bar{x}^{\rho}_2)^{\frac{1}{\rho}}}{\alpha}+w_2\bar{x}_2$

#### Related Curve of Cobb-Douglas
总体思路
$U=x^{\alpha}_1x^{\beta}_2(x_1=\frac{\alpha}{\alpha+\beta}\frac{m}{p_1})\longrightarrow D(y,p)\longrightarrow V(m,\mathbf{p})\longrightarrow E\mathop{\longrightarrow}\limits^{Shephard's\ Lemma}  h_1\ h_2(\frac{\partial E}{\partial p_1}=h_1\ \frac{\partial E}{\partial p_2}=h_2)$
[Proof: Demand Functions for Cobb-Douglas Utility Functions](https://www.econgraphs.org/textbooks/intermediate_micro/consumer_theory/demand/cobb_douglas.html) 11/24 Reminder: $MRS=\frac{dx}{dy}$
$\mathbf{V}(m,\mathbf{p})=[\frac{\alpha}{\alpha+\beta}\frac{m}{p_1})]^{\alpha}[\frac{\beta}{\alpha+\beta}\frac{m}{p_2})]^{\beta}$
{ #IndirectUtilityCobbDouglas}


Leontief production function $f(x_1,x_2)=\min\{ax_1,bx_2\}$
[Finding Marshallian demands for Leontief production function with different powers](https://economics.stackexchange.com/questions/16553/finding-marshallian-demands-for-leontief-production-function-with-different-powe)
Consider the more general case:

$$
U(x,y) = \text{min}\{ax^\alpha,by^\beta\}
$$


Optimality requires (\* notation for optimal values omitted)

$$
ax^\alpha = by^\beta\
$$ 

Replacing one of these in the budget constraint leads to:

$$
p_x x + p_y \left(\frac{a}{b}\right)^{\frac{1}{\beta}} x^{\frac{\alpha}{\beta}} = w
$$


Here we see that only when $\alpha=\beta$$\alpha=\beta$, demand will be linear (on income). In this case:

$$
x = \frac{w}{p_x + p_y\left(\frac{a}{b}\right)^{\frac{1}{\alpha}}}
$$



CES technology $f(x_1,x_2)=(x^{\rho}_1+x^{\rho}_2)^{\frac{1}{\rho}}$
	[CES: Expenditure Function and Hicksian Demand](https://www.yorku.ca/bucovets/5010/consumer/s06.pdf)
	$u=[\sum\limits^n_{i=1}x_i^{\rho}]^{\frac{1}{\rho}}$
	$x_i=[\frac{p_i}{p_1}]^{\frac{1}{\rho}}x_1$
	$u=x_1[\sum\limits^{n}_{j=1}(\frac{p_j}{p_1})^{\frac{\rho}{\rho-1}}]^{\frac{1}{\rho}}$
	$x_1=p_1^{\frac{-1}{(1-\rho)}}[\sum\limits^n_{j=1}p_i^{\frac{\rho}{\rho-1}}]^{\frac{-1}{\rho}}u$ which is a Hicksian demand function
	$r\equiv \frac{\rho}{\rho-1}$
	$e(\mathbf{p},u)=[\sum\limits^n_{i=1}p^r_i]^{\frac{1}{r}}u$ expenditure function
	Proof is on the link
	[CES Utility: Solving for Compensated and Ordinary Demand Functions](https://www.youtube.com/watch?v=Z5vdkBs8oyA)
$$\begin{aligned}
\text{U}&=(x^{1/2}+y^{1/2})^2\quad\mathrm{~M=~}P_xx+P_yy  \\
&\mathsf{MU}_{x}=\frac{\partial U}{\partial x}=2(x^{1/2}+y^{1/2})\frac{1}{2}x^{-1/2}=(x^{1/2}+y^{1/2})x^{-1/2}  \\
&{\mathsf{MU}}_{y}={\frac{\partial U}{\partial y}}=2(x^{1/2}+y^{1/2}){\frac{1}{2}}y^{-1/2}=(x^{1/2}+y^{1/2})y^{-1/2} \\
&\frac{MU_{x}}{P_{x}}=\frac{MU_{y}}{P_{y}}   \\
&\frac{(x^{1/2}+y^{1/2})x^{-1/2}}{P_{\chi}}= \frac{(x^{1/2}+y^{1/2})y^{-1/2}}{P_{y}} 
\end{aligned}$$
	$\frac{x^{\frac{-1}{2}}}{P_x}=\frac{y^{\frac{-1}{2}}}{P_y}$
	$\frac{1}{P_x x^{\frac{1}{2}}}=\frac{1}{P_y y^{\frac{1}{2}}}$
	$y^{1/2}=x^{1/2}\frac{P_{x}}{P_{y}}\left(\mathrm{square~both~sides}\right)$
	$y=x(\frac{P_x}{P_y})^2$ plug into utility function to get compensated demand and plug into budget constraint to get ordinary demand
	Compensated demand for good $x$
	$y=x\left(\frac{P_x}{P_y}\right)^2$ plug into U$= ( x^{1/2}+ y^{1/2})
{ #2}
$
	$\cup=(x^{1/2}+\left[x\left(\frac{P_x}{P_y}\right)^2\right]^{1/2})^2$
	 $U=\begin{bmatrix}x^{1/2}+x^{1/2}\left(\frac{P_{x}}{P_{y}}\right)\end{bmatrix}^{2}$ 
	 $U=[x^{1/2}(1\:+\:\frac{P_{x}}{P_{y}})]^{2}$
	$\mathrm{U}=\mathrm{x}[1\:+\:\frac{P_{x}}{P_{y}}]^{2}$
	Ordinary demand for good $x$:
	$y=x\left(\frac{P_{x}}{P_{y}}\right)^{2}$ plug into M= $P_{x}x+P_{y}y$ 
	$\mathsf{M}=P_{x}x+P_{y}[x\left(\frac{P_{x}}{P_{y}}\right)^{2}]$
	$\mathsf{M}=x(P_{x}+\frac{P_{x}^{2}}{P_{y}})$
	$x=\frac{M}{P_{\chi}+\frac{P_{\chi}^{2}}{P_{y}}}$


## Labour Supply Measures of Consumer Welfare
Total (daily) income: 
$$w(T-L)$$
where w can be the hourly wage rate 
$L$: is the leisure hours 
$T$: total number of hours (e.g., 24 hours in a day)

$$pc+wL\leq wT$$
Alternatively, we have:
$$pc+wL\leq wT$$
$wT$ is called potential income

Consumer Choice
$U(c,L)$: twice method
Use the Lagrange Multiplier method
$$\Gamma(c,L,\lambda)=U(c,L)+\lambda(wT-wL-pc)$$
Optimality Condition
$$\begin{align}wL+pc=wT\\
MU_L/w=MU_c/p\end{align}$$

$$\frac{dL(p,w,m)}{dw}=\underbrace{\frac{\partial h(p,w,u)}{\partial w}}_{negetive\ (substitution\ effect)}+\frac{\partial L(p,w,m)}{\partial m}L^*$$
The sign is inherently ambiguous

### Testing the labor supply curve: David Card(1990), Mariel Boatlift
```
C:\Users\94291\Desktop\documant\Msc\Msc\Advanced Microeconomics\Current
```

### Labour Supply Curve
![Pasted image 20231026131148](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353601.png)

Welfare Measures
Suppose that we have two budgets, $(\mathbf{p}^0,m^0)$ and $(\mathbf{p}', m')$, that measure the prices and incomes that a given consumer would face under two different policy regimes.
It is convenient to think of $(\mathbf{p}^0,m)$ as being the status quo and $(\mathbf{p}', m')$ as being a proposed change, although this is not the only interpretation.
Then the obvious measure of the welfare change involved in moving from $(\mathbf{p}^0,m^0)$ to $(p', m')$ is just the difference in indirect utility:
$$v(\mathbf{p}',m')-v(\mathbf{p}^0,m^0)$$
If this utility difference is positive, then the policy change is worth doing, at least as far as this consumer is concerned; and if it is negative, the policy change is not worth doing.
It is convenient to have monetary measure of changes in consumer welfare
Recall that $\mu(\mathbf{q}; \mathbf{p}, m)$ measures how much income the consumer would need at prices $\mathbf{q}$ to be as well off as he or she would be facing prices $\mathbf{p}$ and having income $m$.==这个定义很重要但是似懂非懂== 11.14 Shi Ce: 在原先价格和预算约束下达到的效用，在新价格下有多少预算能达到相同的效用
That is, $\mu(\mathbf{q};\mathbf{p},m)$ is defined to be $e(\mathbf{q}, v(\mathbf{p}^0, m^0))$.
If we adopt this measure of utility, we find that the above utility difference becomes
$$\mu(\mathbf{q};\mathbf{p}',m')-\mu(\mathbf{q};\mathbf{p}^0,m^0)$$

Money-metric indirect utility function:
$$\mu(\mathbf{p};\mathbf{q},m)\equiv e(\mathbf{p},v(\mathbf{q},m))$$

Consumer surplus (CS) (associated with a price drop from $p^0$ to $p'$)
$$CS=\int^{p^0}_{p'}x(p)dp$$
$x(p):$ the demand function

Equivalent variation (EV):
$$EV=\mu(\mathbf{p}^0;\mathbf{p}^1,m)-\mu(\mathbf{p}^0;\mathbf{p}^0,m^0)=\mu(\mathbf{p}^0;\mathbf{p}^1,m^0)-m^0$$
Compensating variation (CV):
$$CV=\mu(\mathbf{p}^1;\mathbf{p}^1;m^1)-\mu(\mathbf{p}^1;\mathbf{p}^0,m^0)=m^1-\mu(\mathbf{p}^1;\mathbf{p}^0,m^0)$$
The first measure is known as the equivalent variation. It uses the current prices as the base and asks what income change at the current prices would be equivalent to the proposed change in terms of its impact on utility. " The second measure is known as the compensating variation. It uses the new prices as the base and asks what income change would be necessary to compensate the consumer for the price change.
![Pasted image 20231114081059](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353602.png)
Equivalent variation and compensating variation. In this  $p_2 = 1$ and the price of good 1 decreases from $p_0$ to $p_1$.  Panel A depicts the equivalent variation in income-how much additional money is needed at the original price po to make the consumer as well off as she would be facing $p_1$. Panel B depicts the compensating variation in incomehow much money should be taken away from the consumer to leave him as well off as he was facing price $p_0$.


Suppose $U(x_1,x_2)=x_1x_2$
$$P_1=\$9,P_2=\$1,I=\$72$$
$P_1$ falls and $P'_1=\$4$. 
Calculate CV and EV. 
What do you find?

Compensate Variation 24
4 to 6 is the substitution effect, 6 to 9 is income effect
There is a similar question in mid-term exam.
![058ef37454be9bdcf7779200c3d3083](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353604.jpg)


Since $h(p,w)=\frac{\partial e(p,u)}{\partial p}$
$$\begin{align}
CV=e(\mathbf{p}^0,u^0)-e(\mathbf{p}',u^0)=\int^{p^0}_{p'} h(p,u^0)dp=\int^{p'}_{p^0}x(t)dt \text{ (the last one is the fomular on textbook) }\\
EV=e(\mathbf{p}^0,u')-e(\mathbf{p}'',u')=\int^{p^0}_{p'} h(p,u')dp
\end{align}$$
In reference to the graph (for a price drop), we have in general
$$CV<\Delta CS<EV$$


Quasilinear Utility
Consider a quasilinear utility function of the following form:
$$U(x_0,x_1,\dots,x_k)=x_0+u(x_1,\dots,x_k)$$
where $x_0$ is a composite good (or numeraire)
- In the two-good case,
- $$U(x_0,x_1)=x_0+u(x_1)$$
- Normalize $p_0=1$ , utility maximization yields
- $$u'(x_1)=p_1$$
- which simply requires that the marginal utility of consumption of good 1 be equal to its price
- which implicitly defines the demand function, $x^*_1(p_1)$

For an interior solution  $x^*_1$, does not involve an income effect; so
$$EV=\Delta CS=CV$$
for the quasilinear utility function.


in this case,
$$\begin{align}
CS=u(x)-px\\
PS=px-c(x)
\end{align}$$
Thus, social welfare (social surplus) is
$$CS+PS=u(x)-c(x)$$
For a benevolent social planner who maximizes social surplus by
$$\max_x\ u(x)-c(x)$$
The FOC requires
$$u'(x)=c'(x)$$

## Perfect Competition in Partial and General Equilibrium Analysis
For a competitive firm, the profit function is
$$\max_y \pi=py-c(y)$$
where $p$ is a constant

FOC and SOC (for an interior optimum), based on [[Microeconomics#Properties of the profit function\|Properties of the profit function]]
$$\begin{align}
p=c'(y)\\
c''(y)\geq 0
\end{align}$$
which implicitly defines the supply function $y^*(p)$
$p(y)=c'(y)$: the inverse supply function

Supply Function
In the short run, we need to consider the corner case:
$$py-c_v(y)-F\geq -F$$
where $c(y)=c_v(y)+F$
The firm will choose $y>0$ if
$$p\geq \frac{c_v(y)}{y}$$
### Market Equalibrium
In equilibrium
$$\sum\limits^n_i x_i(p)=\sum\limits^n_j y_i(p)$$
where $i,j$ index individuals and firms, respectively.

With $m$ identical firms in the short-run
$$\sum\limits^n_i x_i(p)=my(p)$$
EX. $X(p)=a-bp$, and $Y(p,m)=\frac{mp}{2}$ equalibrium price $p^*=\frac{a}{b+m/2}$
In general, $\frac{dp}{dm}=?<0$ ==Don't know how to prove yet== 已经知道了
	
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/microeconomics/#market-equilibrium" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

$<div class="markdown-embed-title">

# Solution

</div>


## Market equilibrium
If we let $x_i(p)$ be the demand function of individual $i$ for $i = 1, . . . , n$ and $y_j(p)$ be the supply function of firm $j$ for $j = 1, . . . , m$, then an equilibrium price is simply a solution to the equation
$\sum^n_{i=1}x_i(p)=\sum^m_{j=1}y_j(p)$
Example: Identical firms
Suppose that the industry demand curve is linear, $X(p) = a - bp$, and the industry supply curve is that derived in the last example, $Y(p, m) = mp/2$. The equilibrium price is the solution to
$a-bp=\frac{mp}{2}$
which implies
$p^*=\frac{a}{b+m/2}$
Note that in this example the equilibrium price decreases as the number of firms increases

For an arbitrary industry demand curve, equilibrium is determined by
$X(p)=my(p)$
How does the equilibrium price change as $m$ changes? We regard $p$ as an implicit function of m and differentiate to find
$X'(p)p'(m)=my'(p)p'(m)+y(m)$
which implies
$p'(m)=\frac{y(p)}{X'(p)-my'(p)}$
Since $y(p)>0$,  
The industry demand has a negative slope, thus $X'(p)<0$
The industry supply has a positive slope, thus $y'>0$
Therefore, $p'(m)<0$, , the equilibrium price must decline as the number of firms increases. 

</div></div>
:

Application: Tax Incidence
With taxes (or subsidies), there are $p^s$ and $p^d$.
Unit tax / quantity tax (on consumers):
$$p^d=p^s+t$$
Ad valorem / value tax (on consumers):
$$p^d=(1+t)p^s$$
Irrelevance of the physical incidence
Economic incidence (of a unit tax)
In equilibrium,
$$D(p^d)=S(p^d-t)$$
Differentiating yields
$$\begin{align}
\frac{dp^d}{dt}D'(p^d)=\\
\frac{dp^d}{dt}=\frac{S'}{S'-D'}=\frac{1}{1+\frac{|\varepsilon_d|}{\varepsilon_s}}
\end{align}$$

**Partial Equilibrium analysis** is the study of howequilibrium is determined in only a single market (e.g. a single product market). 
**General Equilibrium analysis** is the study of howequilibrium is determined in all marketssimultaneously (e.g. product markets and labor markets).

### Criticism of Free Market
1. Market power: monopoly, oligopoly, etc. 
2. Externalities: e.g., pollution, education 
3. Public goods: e.g., fire station, national defense
4. Information asymmetry: e.g., used cars, insurance,
Coordination Problem: e.g., electricity

Equality, Justice, and Distributional Issuese.g., Trade benefits countries – but who receive the benefit? (Brexit, Anti-immigration sentiments worldwide)
Macroeconomic stability 
Collective value e.g. violence, pornography, etc.
## Problem Set 3
Chapter 8 Problems: 8.11, 8.16 
Chapter 9 Problems: 9.6, 9.9* 
Chapter 10 Problems: 10.1* 
Chapter 13 Problems: 13.2, 13.3*, 13.4, 13.5, 13.7, 13.8*

8.11. Consider a consumer who is demanding goods 1 and 2. When the price of the goods are (2,4), he demands (1,2). When the prices are (6,3), he demands (2,1). Nothing else of significance changed. Is this consumer maximizing utility?
	Solution:
	No, because his demand behavior violates GARP. When prices are (2, 4) he spends 10. At these prices he could afford the bundle (2, 1), but rejects it; therefore, $(1, 2) ≻ (2, 1)$. When prices are (6, 3) he spends 15. At these prices he could afford the bundle (1, 2) but rejects it; therefore, $(2, 1) ≻ (1, 2)$. ==对于GARP的定义需要更加清楚==

9.6. Let (q, m) be prices and income, and let $p = q/m$. Use Roy's identity to derive the formula
$$x_i(\mathbf{p})=\frac{\frac{\partial v(\mathbf{p})}{\partial p_i}}{\sum^k_{j=1}\frac{\partial v(\mathbf{p})}{\partial p_j}p_j}$$
Solution:
	According to 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/microeconomics/#roy-s-identity" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

$<div class="markdown-embed-title">

# Roy's Identity

</div>


#### **Roy's identity**.
If $\mathbf{x}(\mathbf{p}, m)$ is the Marshallian demand function, then
$x_i(\mathbf{p},m)=-\frac{\frac{\partial v(\mathbf{p},m)}{\partial p_i}}{\frac{\partial v(\mathbf{p},m)}{\partial m}}\text{ for }i=1,\cdots,k$
$\begin{aligned}\mathsf{Proof}{:}\\&u^*\equiv\nu(\boldsymbol{p},\boldsymbol{e}(\boldsymbol{p},u^*))\\\\&0=\frac{\partial v(\boldsymbol{p}^*,\boldsymbol{m}^*)}{\partial p_i}+\frac{\partial\nu(\boldsymbol{p}^*,\boldsymbol{m}^*)}{\partial m}\frac{\partial e(\boldsymbol{p},\boldsymbol{m}^*)}{\partial p_i}\\\\&x_i(\boldsymbol{p}^*,\boldsymbol{m}^*)\equiv h_i(\boldsymbol{p}^*,\boldsymbol{u}^*)=\frac{\partial e(\boldsymbol{p},\boldsymbol{m}^*)}{\partial p_i}=-\frac{\frac{\partial v(\boldsymbol{p},\boldsymbol{m})}{\partial p_i}}{\frac{\partial v(\boldsymbol{p},\boldsymbol{m})}{\partial\boldsymbol{m}_°}}\end{aligned}$
在知道indirect utility function的情况下用来计算demnand function 

</div></div>

	Write the indirect utility function as $v(\mathbf{p}) = v(\mathbf{q}/m)$ and differentiate with respect to $q_i$ and $m$:
$$\begin{align}
&\frac{\partial v}{\partial q_i}=\frac{\partial v}{\partial p_i}\frac{1}{m}\\
&\frac{\partial v}{\partial m}=-\sum^k_{i=1} \frac{\partial v}{\partial p_i}\frac{q_i}{m^2}=-\sum^k_{i=1} \frac{\partial v}{\partial p_i}p_i \frac{1}{m}
\end{align}$$
$$x_i(\mathbf{p})=-\frac{\frac{\partial v}{\partial q_i}}{\frac{\partial v}{\partial m}}=\frac{\frac{\partial v(\mathbf{p})}{\partial p_i}}{\sum^k_{j=1}\frac{\partial v(\mathbf{p})}{\partial p_j}p_j}$$

9.9. A consumer has a utility function $u(x, y, z) = \min\{x, y\} +z$. The prices of the three goods are given by $(p_x, p_y, p,)$ and the money the consumer has to spend is given by $m$.
(a) It turns out that this utility function can be written in the form $U(V(x, y), z)$. What is the function $V(x, y)$? What is the function $U(V, z)$? 
	Solution:
	The function $V(x,y)=\min\{x,y\}$, and $U(V,z)=V+z$
(b) What are the demand functions for the three goods? 
	Solution:
	The demand function for the z-good is $z=\frac{m}{p_z}$ if $p_z<p_x+p_y$
	If $p_z>p_x+p_y$, then the demand for the x-good and the y-good is given by $x=y=\frac{m}{p_x+p_y}$
	If $p_z=p_x+p_y$, then take any convex combination of these demands.
(c) What is the indirect utility function?
	Solution:
	The indirect utility function is
$$v(p_x,p_y,p_z,m)=\max\{\frac{m}{p_x+p_y},\frac{m}{p_z}\}$$
	11.14 Geng Hao $z$相对$xy$是substitution, $x,y$ is complementary
	

10.1. Suppose that utility is quasilinear. Show that the indirect utility function is a convex function of prices.
	Solution:
	We saw that in this case the indirect utility function takes the form $v(\mathbf{p})+m$. Hence the expenditure function takes the form $e(\mathbf{p},u)=u-v(\mathbf{p})$. [[Microeconomics#Properties of the expenditure function\|The expenditure function is necessarily a concave function of prices]], which implies that $v(\mathbf{p})$ is a convex function.
	==这个还是不是很清楚==
	11.14首先a negative of concave function is a convex function, this will not change if we add a constant
	A utility function is quasilinear in commodity 1 if it is in the form
$$u(x_1,\dots,x_L)=x_1+\theta(x_2,\dots,x_l)$$
	where $\theta$ is an arbitrary function In the case of two goods this function could be, for example, $u(x,y)=x+\sqrt{y}$
	In this case, we have
$$\begin{align}
U(x,y)=V(x)+y\\
P_x x+P_y y=m
\end{align}$$
$$y=\frac{m-P_xx}{P_y}$$
	FOC
$$\begin{align}V'(x)=\frac{P_x}{P_y}\\
x=V^{-1}(\frac{P_x}{P_y})
\end{align}$$
	Utility function $u=V\Big(V^{-1}(\frac{P_x}{P_y})\Big)+\frac{m-P_x\cdot V^{-1}(\frac{P_x}{P_y})}{P_y}$
	$V\Big(V^{-1}(\frac{P_x}{P_y})\Big)$ and $\frac{-P_x\cdot V^{-1}(\frac{P_x}{P_y})}{P_y}$ can be seen as a function of prices
	$\therefore$ indirect utility function $v(p)+m=u$

13.2. Show that the integral of the supply function between $p_0$ and $p_1$ gives the change in profits when price changes from $p_0$ to $p_1$.
	Solution
	By 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/microeconomics/#hotelling-s-lemma" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

$<div class="markdown-embed-title">

# Hotelling’s law

</div>


#### **Hotelling's Lemma**
Let $y_i(p)$ be the firm's net supply function for good $i$. Then
$y_i(p)=\frac{\partial \pi(\mathbf{p})}{\partial p_i}\text{ for }i=1,\dots,n$
	[Proof](https://www.youtube.com/watch?v=V6Rziu74uhA): 
$\begin{align}
\max \pi(y,x_1,x_2)=py-w_1x_1-w_2x_2\\
s.t.\ f(x_1,x_2)\geq q\\
\text{Define }G(q,x_1,x_2)=q-f(x_1,x_2)\leq 0\\
G\text{ has no parameter such as }p,w_1,w_2\\
V(p,w_1,w_2)\text{ is profit}\\
\frac{\partial V}{\partial p}=\frac{\partial \pi}{\partial p}-\lambda \frac{\partial G}{\partial p}=y-\lambda(0)=\hat{y}(p,w_1,w_2)\\
\frac{\partial V}{\partial w_i}=\frac{\partial \pi}{\partial w_i}-\lambda\frac{\partial G}{\partial w_i}=-\hat{x}_i(p,w_1,w_2)\quad (\text{Factor Demand Function})
\end{align}$ 
#### Exercise
When the price of an output increases by a small amount there will be two effects. 
First, there is a direct effect: because of the price increase the firm will make more profits, even if it continues to produce the same level of output. 
But secondly, there will be an indirect effect: the increase in the output price will induce the firm to change its level of output by a small amount. However, the change in profits resulting from any infinitesimal change in output must be zero since we are already at the profit-maximizing production plan. Hence, the impact of the indirect effect is zero, and we are left only with the direct effect.

3.1 . A competitive profit-maximizing firm has a profit function $\pi=(w_1,w_2)=\phi(w_1)+\phi(w_2)$. The price of output is normalized to be 1.
	1. What do we know about the first and second derivatives of the functions $\phi(w_i)$?
		Solution:
		Since the profit function is convex and a decreasing function of the factor prices, we know that $\phi_i'(w_i)\leq 0$ and $\phi_i''(w_i)\geq 0$
	2. If $x_i(w_1, w_2)$ is the factor demand function for factor $i$, what is the sign of $\partial x_i/\partial w_j$?
		Solution:
		It is zero. ==这个也没太懂== 
	3. Let $f (x_1, x_2)$ be the production function that generated the profit function of this form. What can we say about the form of this production function? (Hint: look at the first-order conditions.)
		Solution:
		The demand for factor $i$ is only a function of the $i^{th}$  price. Therefore the marginal product of factor $i$ can only depend on the amount of factor $i$. It follows that $f(x_1, x_2) = g_1(x_1) + g_2(x_2)$.

3.2. Consider the technology described by $y = 0$ for $x\leq 1$ and $y = \ln x$ for $x > 1$. Calculate the profit function for this technology.
	Solution:
	The firm can always choose $x=0$ and make zero profits
	When $y=\ln x$
	$\pi=p\ln x-wx$
	The first order condition are $\frac{p}{x}=w$, which gives us the demand function $x=\frac{p}{w}$ and the supply function $y=\ln (\frac{p}{w})$. The profits from operating at this pint are $p\ln (\frac{p}{w})-p$.
	In summary, $\pi(p,w)=\max \{p\ln(\frac{p}{w}-p,0)\}$

3.3 Given the production function $f (x_1, x_2) = a_1 \ln x_1 + a_2 \ln x_2$, calculate the profit-maximizing demand and supply functions, and the profit function, For simplicity assume an interior solution. Assume that $a_i> 0$. 
	Solution:
	The first-order conditions are
$\begin{align}
a_1\frac{p}{x_1}-w_1=0\\
a_2\frac{p}{x_2}-w_2=0
\end{align}$
	which can easily be solved for the factor demand functions. Substituting into the objective function gives us the profit function 

3.5. Given the production function $f (x_1, x_2) = \min\{x_1, x_2\}^a$, calculate the profit-maximizing demand and supply functions, and the profit function. What restriction must a satisfy?
	Solution:
	If $w_i$ is strictly positive, the firm will never use more of factor $i$ than it needs to, which implies $x_1 = x_2$. Hence the profit maximization problem can be written as 
$\max\ px^a_1-w_1x_1-w_2x_2$
	The first-order condition is
$pax^{a-1}_1-(w_1+w_2)=0$
	Demand function: $x_1=(\frac{w_1+w_2}{pa})^{\frac{1}{a-1}}$
	Supply function: $y=p(\frac{w_1+w_2}{pa})^{\frac{a}{a-1}}=p^{\frac{1}{1-a}}(\frac{w_1+w_2}{a})^{\frac{a}{a-1}}$
	In order for a maximum to exist, $a<1$ ==最后一个怎么证明的没搞懂==
		用second order condition证明是$0<a<1$ [[Microeconomics#Difficulties\|Difficulties]]
		10.19问JZH：$a$默认大于0,不需要深究


</div></div>
 we know that $\frac{\partial \pi(p,\mathbf{w})}{\partial p}=y(p)$; therefore,
$$\int^{p_1}_{p_0}y(p)dp=\pi(p_1,\mathbf{w})-\pi(p_0,\mathbf{w})$$

13.3. An industry consists of a large number of firms, each of which has a cost function of the form 
$$c(w_1,w_2,y)=(y^2+1)w_1+(y^2+2)w_2$$
(a) Find the average cost curve of a firm and describe how it shifts as the factor price $w_1/w_2$ changes. 
	Solution:
	The average cost curve is just
$$\frac{c(\mathbf{w},y)}{y}=\frac{y^2+1}{y}w_1+\frac{y^2+2}{y}w_2$$
	You should verify that it is a convex function that has a unique minimum at
$$y_m=\sqrt{\frac{w_1/w_2+2}{w_1/w_2+1}}$$
	(Derivative equals 0, already calculated)
	The derivative of $y_m$ with respect to $w_1/w_2$ is negative, so the minimum of the average cost shifts to the left (right) as $w_1/w_2$ increases (decreases). In fact it converges to 1 as the ratio approaches $∞$ and to $\sqrt{2}$ as it goes down to $0$.
(b) Find the short-run supply curve of an individual firm. 
	Solution:
	The marginal cost is
$$\frac{\partial c(\mathbf{w},y)}{\partial y}=2y(w_1+w_2)$$
	so short-run supply schedule is given by
$$y(p)=\frac{p}{2(w_1+w_2)}$$
(c) Find the long-run industry supply curve.
	Solution: ==有点没懂== 搞懂了
$$Y(p)=\left\{\begin{array}{**lr**} \text{arbitrarily large amount}\quad \text{if }p>2y_m(w_1+w_2) \\ 0\quad \text{otherwise} \end{array}   \right.$$
	When price is higher that optimal producing equalibrim in the short term, companies will enter
(d) Describe an input requirement set for an individual firm
	Solution:==有点没懂==
	From the cost function we have that $x_1 = y^2 + 1$ and $x_2 = y^2 + 2$. Also, we see that $x_1$ and $x_2$ are not substitutes at any degree. Therefore, the input requirement set for an individual firm is
$$V(y)=\{(x_1,x_2)\in[1,\infty)\times[2,\infty):y\leq \min\{\sqrt{x_1-1},\sqrt{x_2-2}\}\}$$
	2023/11/14 这道题其实和这个模型有关
	![Pasted image 20231114093220](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353605.png)

13.4. Farmers produce corn from land and labor. The labor cost in dollars to produce y bushels of corn is $c(y) = y^2$. There are 100 identical farms which all behave competitively.
(a) What is the individual farmer's supply curve of corn?
	Solution:
	$c(y)=y^2 \Rightarrow \frac{\partial c(y)}{\partial y}=2y$
	$\because$ Marginal cost =price
	$\therefore$ $p=2y\Rightarrow y=\frac{p}{2}$
(b) What is the market supply of corn?
	Solution:
	There are 100 identical farms which all behave competitively.
	$Y=100\cdot \frac{y}{2}=50y$
(c) Suppose the demand curve of corn is $D(p) = 200 - 50p$. What is the equilibrium price and quantity sold?
	Solution:
	$D(p)=Y(p)$
	we get $p^*=2$ and $y^*=1(Y^*=100)$
(d) What is the equilibrium rent on the land?
	Solution:
	The equilibrium rent on land r must equal the difference between each firm revenues and labor costs at the competitive equilibrium. Therefore,
$$r=p-c(y)=2-1^2=2-1=1$$

13.5. Consider a model where the U.S. and England engage in trade in umbrellas. The representative firm in England produces the export model umbrella according to a production function $f (K, L)$ where $K$ and $L$ are the amounts of capital and labor used in production. Let $r$ and $w$ be the price of capital and the price of labor respectively in England, and let $c(w, r, y)$ be the cost function associated with the production function $f (K, L)$. Suppose that initially the equilibrium price of umbrellas is $p^*$ and the equilibrium output is $y^*$. Assume for simplicity that all of the export model umbrellas are exported, that there is no production of umbrellas in the US., and that all markets are competitive.
(a) England decides to subsidize the production and export of umbrellas by imposing an export subsidy s on each umbrella, so that each umbrella exported earns the exporter $p + s$. What size import tax $t(s)$ should the U.S. choose so as to offset the imposition of this subsidy; i.e., to keep the production and export of umbrellas constant at $y^*$? (Hint: This is the easy part; don't get too subtle.) 
	Solution:
	In order to offset the output subsidy, the U.S. should choose a tax of the same size as the subsidy; that is, choose $t(s) = s$.
(b) Since it is so easy for the U.S. to offset the effects of this export subsidy, England decides instead to use a capital subsidy. In particular, they decide to subsidize capital purchases with a specific subsidy of $s$ so that the price of capital to English umbrella makers is $r - s$. The U.S. decides to retaliate by putting a tax $t(s)$ on imported umbrellas that will be sufficient to keep the number of umbrellas produced constant at $y^*$. What must be the relationship between the price paid by the consumers, $p$, the tax, $t(s)$, and the cost function, $c(w, r, y)$? 
	Solution:==没懂==
	
(c) Calculate an expression for $t'(s)$ involving the conditional factor demand function for capital, $K(w, r, y)$. 
(d) Suppose that the production function exhibits constant returns to scale. What simplification does this make to your formula for $t'(s)$?
(e) Suppose that capital is an inferior factor of production in umbrella making. What is unusual about the tariff $t(s)$ that will offset the capital subsidy in England?
==还没看，晚点回来看==

13.7. Consider an industry with the following structure. There are 50 firms that behave in a competitive manner and have identical cost functions given by $c(y) = y^2/2$. There is one monopolist that has 0 marginal costs. The demand curve for the product is given by
$$D(p)=1000-50p$$
(a) What is the monopolist's profit-maximizing output? 
	Solution: 
	$MC=0$
	$MR=20-\frac{2}{50}y$
	$MC=MR\Rightarrow y=500$
(b) What is the monopolist's profit-maximizing price? 
	Solution:
	When $y=500$,
	$p=5$
(c) How much does the competitive sector supply at this price?
	Solution:
	cost function $c(y)=y^2/2$
	Supply function $p=y$ According to [[Microeconomics#The industry supply function\|The indutry supply function]]
	Industry supply function $y=50p=50\times 5=250$ 
==还没看，晚点回来看==
11/21搞懂原因，MR不是$D(p)=1000-200p$ 而是 $p=20-\frac{2}{50}y$
坐标系的自变量、因变量搞错了。

13.8. U.S. consumers have a demand function for umbrellas which has the form $D(p) = 90 - p$. Umbrellas are supplied by U.S. firms and U.K. firms. For simplicity, assume that there is a single representative firm in each country that behaves competitively. The cost function for producing umbrellas is given by $c(y) = y^2/2$ in each country. 
(a) What is the aggregate supply function for umbrellas? 
	Solution: 
	marginal cost $c'(y)=y$ (Notice it is in each country)
	Price equals marginal cost gives us $p=y$
	(There are two contries) so $Y=p+p=2p$ 
	11.14 Geng Hao $MR=MC$ is the golden rule in economics
(b) What is the equilibrium price and quantity sold? 
	Solution:
	Set demand equal to supply $90-p=2p$ to find $p^*=30$ and $Y^*=60$
(c) Now the domestic industry lobbies for protection and Congress agrees to put a $3 tariff on foreign umbrellas. What is the new U.S. price for umbrellas paid by the consumers? 
	Solution:
	Let $p$ be the price paid by consumers. Then the domestic firms receive a price of p and the foreign firms receive a price of $p − 3$. Demand equals supply gives us
$$90-p=p+[p-3]$$
	Solving we have $p^*=31$
(d) How many umbrellas are supplied by foreign firms and how many are supplied by domestic firms?
	Solution:
	The supply of umbrellas by domestic firms is 31 and by foreign firms is 28.

### Additional Exercise
E1. Terry’s utility function over leisure $(L)$ and other goods $(Y )$ is $U(L, Y ) = Y + LY$. The associated marginal utilities are $MU_Y = 1 + L$ and $MU_L = Y$. He purchases other goods at a price of £1, out of the income he earns from working. Show that, no matter what Terry’s wage rate, the optimal number of hours of leisure that he consumes is always the same. What is the number of hours he would like to have for leisure?

E2. The long-run average cost for production of hard-disk drives is given by $AC(Q) = √wr(120−20Q + Q^2$), where $Q$ is the annual output of a firm, w is the wage rate for skilled assembly labor, and $r$ is the price of capital services. The demand for labor for an individual firm is
$$L(Q,w,r)=\frac{\sqrt{r}(120Q-20Q^2+Q^3)}{2\sqrt{w}}$$
The price of capital services is fixed at $r = 1$. 
a) In a long-run competitive equilibrium, how much output will each firm produce? 
b) In a long-run competitive equilibrium, what will be the market price? Note that your answer will be expressed as a function of $w$. 
c) In a long-run competitive equilibrium, how much skilled labor will each firm demand? Again, your answer will be in terms of $w$. 
d) Suppose that the market demand curve is given by $D(P) = 10,000/P$. What is the market equilibrium quantity as a function of $w$? 
e) What is the long-run equilibrium number of firms as a function of $w$? 
f ) Using your answers to parts (c) and (e), determine the overall demand for skilled labor in this industry as a function of $w$. 
g) Suppose that the supply curve for the skilled labor used in this industry is $Γ(w) = 50w$. At what value of w does the supply of skilled labor equal the demand for skilled labor? 
h) Using your answer from part (g), go back through parts (b), (d), and (e) to determine the long-run equilibrium price, market demand, and number of firms in this industry. 
i) Repeat the analysis in this problem, now assuming that the market demand curve is given by $D(P) = 20,000/P$.


E3*. The global propylene industry is perfectly competitive, and each producer has the long-run marginal cost function $MC(Q) = 40 − 12Q + Q^2$. The corresponding long-run average cost function is $AC(Q) = 40 − 6Q + Q^2/3$. The market demand curve for propylene is $D(P) = 2200 − 100P$. What is the long-run equilibrium price in this industry, and at this price, how much would an individual firm produce? How many active producers are in the propylene market in a long-run competitive equilibrium
	Solution:
	$MC(Q)=AC(Q)$
	$40-12Q+Q^2=40-6Q+\frac{1}{3}Q^2$
	$\therefore Q=9$
	$P=40-6\times 9+\frac{1}{3}9^2=13$
	The long-run equalibrium is 13, and the firm will produce 9 units of output.
	$D(P)=2200-100P=2200-100\times 13=900$
	$\frac{D(P)}{Q}=\frac{900}{9}=100$
	There are 100 active producers.

## Competitive Markets
A competitive firm is one that takes the market price of output as being given and outside of its control.
Let $\overline{p}$ be the market price. Then the demand curve facing an ideal competitive firm takes the form
$$D(p)=\left\{\begin{array}{**lr**} 0\quad \text{if }p>\overline{p}\\ \text{any amount} \quad \text{if }p=\overline{p}\\ \infty\quad \text{if }p<\overline{p}\end{array}   \right.$$
Since the competitive firm must take the market price as given, its profit maximization problem is very simple. It must choose output $y$ so as to solve
$$\max\limits_y\ py-c(y)$$
The first-order and second-order conditions for an interior solution are
$$\begin{align}
p=c'(y^*)\\
c''(y^*)\geq 0
\end{align}$$
**The inverse supply function**, denoted by $p(y)$, measures the price that must prevail in order for a firm to find it profitable to supply a given amount of output. According to the first-order condition, the inverse supply function is given by
$$p(y)=c'(y)$$
as long as $c''(y)>0$
FOC
$$p\equiv c'(y(p))\tag{13.1}$$
SOC
$$c''(y(p))\geq 0$$
We differentiate expression (13.1) with respect to $p$ to find
$$1=c''(y(p))y'(p)$$
Since normally $c''(y) > 0$, it follows that $y'(p) > 0$
Hence, the supply curve of a competitive firm has a positive slope, at least in the regular case.

Let us write the cost function as $c(y) = c_v(y) + F$, so that total costs are expressed as the sum of variable costs and fixed costs.
In this case, the firm will find it profitable to produce a positive level of output when the profits from doing so exceed the profits (losses) from producing zero:
$$py(p)-c_v(y(p))-F\geq -F$$
Rearranging this condition, we find that the firm will produce positive levels of output when
$$p\geq \frac{c_v(y(p))}{y(p)}$$
that is, when price is greater than average variable cost.
![Pasted image 20231116114509](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353606.png)

## The industry supply function
The **industry supply function** is simply the sum of the individual firm supply functions. If $y_i(p)$ is the supply function of the $i^{th}$ firm in an industry with $m$ firms, the industry supply function is given by
$$Y(p)=\sum^m_{i=1}y_i(p)$$
The **inverse supply function** for the industry is just the inverse of this function: it gives the minimum price at which the industry is willing to supply a given amount of output.

EXAMPLE: Different cost functions
Consider a competitive industry with two firms, one with cost function $c_1(y) = y^2$, and other with cost function $c_2(y) = 2y^2$. The supply functions are given by
$$\begin{align}
y_1=\frac{p}{2}\\
y_2=\frac{p}{4}
\end{align}$$
The industry supply curve is therefore $Y(p) = 3p/4.$ For any level of industry output $Y$, the marginal cost of production in each firm is $4Y/3$

EXAMPLE: identical cost functions
Suppose that there are m firms that have the common cost function $c(y) = y^2 + 1$. The marginal cost function is simply $MC(y) = 2y$, and the average variable cost function is $AVC(y) = y$. Since in this example the marginal costs are always greater than the average variable costs, the inverse supply function of the firm is given by $p = MC(y) = 2y$. 
It follows that the supply function of the firm is $y(p) = p/2$ and the industry supply function is $Y(p, m) = mp/2$. The inverse industry supply function is therefore $p = 2Y/m$. Note that the slope of the inverse supply function is smaller the larger the number of firms.

## Market equilibrium
If we let $x_i(p)$ be the demand function of individual $i$ for $i = 1, . . . , n$ and $y_j(p)$ be the supply function of firm $j$ for $j = 1, . . . , m$, then an equilibrium price is simply a solution to the equation
$$\sum^n_{i=1}x_i(p)=\sum^m_{j=1}y_j(p)$$
Example: Identical firms
Suppose that the industry demand curve is linear, $X(p) = a - bp$, and the industry supply curve is that derived in the last example, $Y(p, m) = mp/2$. The equilibrium price is the solution to
$$a-bp=\frac{mp}{2}$$
which implies
$$p^*=\frac{a}{b+m/2}$$
Note that in this example the equilibrium price decreases as the number of firms increases

For an arbitrary industry demand curve, equilibrium is determined by
$$X(p)=my(p)$$
How does the equilibrium price change as $m$ changes? We regard $p$ as an implicit function of m and differentiate to find
$$X'(p)p'(m)=my'(p)p'(m)+y(m)$$
which implies
$$p'(m)=\frac{y(p)}{X'(p)-my'(p)}$$
Since $y(p)>0$,  
The industry demand has a negative slope, thus $X'(p)<0$
The industry supply has a positive slope, thus $y'>0$
Therefore, $p'(m)<0$, , the equilibrium price must decline as the number of firms increases.
{ #FirmNumEquPrice}


## Entry

EXAMPLE: Entry and long-run equilibrium
If $c(y)=y^2+1$, then the breakeven level of output can be found by setting average cost equal to marginal cost:
$$y+\frac{1}{y}=2y$$
which implies that $y = 1$. At this level of output, marginal cost is given by $2$, so this is the breakeven price. According to our entry model, firms will enter the industry as long as they determine that they will not drive the equilibrium price below $2$. 
Suppose that demand is linear, as in the previous example. Then the equilibrium price will be the smallest $p^*$ that satisfies the conditions
$$\begin{align}
&p^*=\frac{a}{b+m/2}\\
&p^*\geq 2
\end{align}$$
As $m$ increases, the equilibrium price must get closer and closer to 2.

### Welfare Economics
First Theorem of Welfare Economics: A Walrasian equilibrium is Pareto efficient. 
Second Theorem of Welfare Economics: A Pareto efficient allocation is a Walrasianequilibrium, given that preferences are convex, continuous, and monotonic
textbook P235开始没怎么看懂 

### Taxes and subsidies
For example, a **quantity tax** is a tax levied on the amount of a good consumed. This means that the price paid by the demanders is greater than the price received by the suppliers by the amount of the tax:
$$p_d=p_s+t$$
A **value tax** is a tax levied on the expenditure of a good. It is usually expressed as a percentage amount, such as a 10 percent sales tax. A value tax at rate T leads to a specification of the form
$$p_d=(1+\mathcal{T})p_s$$
Subsidies have a similar structure; a **quantity subsidy** of amount s means that the seller receives s dollars more per unit than the buyer pays, so that
$$p_d=p_s-s$$

The demander's behavior depends on the price she faces and the supplier's behavior depends on the price that she faces. Hence we write $D(p_d)$ and $S(p_s)$. The typical equilibrium condition is that demand equals supply; this leads to the two equations:
$$\begin{align}
D(p_d)=S(p_s)\\
p_d=p_s+t
\end{align}$$
Inserting the second equation into the first, we can solve either
$$D(p_d)=S(p_s)$$
or
$$D(p_d)=S(p_d-t)$$
Another way to solve this kind of tax problem is to use the inverse demand and supply functions. In this case the equations become
$$P_d(q)=P_s(q)+t$$
or
$$P_s(q)=P_d(q)-t$$

The utility of consumption accruing to the consumer at the equilibrium $x^*$ is $u(x^*) -p_dx^*$. 
The profits accruing to the firm are $p_s x^* - c(x^*)$. 
Finally, the revenues accruing to the government are $tx^* = (p_d - p_s)x^*$
This is simply the area below the demand curve minus the area below the marginal cost curve, and is depicted in Figure
The difference between the surplus achieved with the tax and the welfare achieved in the original equilibrium is known as the deadweight loss; it is given by the triangleshaped region in Figure
![1700551978311](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353607.png)

## Monopoly and Pricing Strategies
苏联使用MPS而不使用GDP测算经济
A monopoly market consists of a single seller facing many buyers
The monopolist's profit maximization problem with the demand function :
$$\begin{align}\max\limits_p\ pD(p)-C(D(p))\\
\text{such that }D(p)\geq y
\end{align}$$
Alternatively, with the inverse demand function $p(y)$:
$$\max_y\ p(y)y-C(y)$$
FOC and SOC (for an interior optimum):
$$\begin{align}
p+p'(y)y=C'(y)\\
2p'+p''y-C''(y)\leq 0
\end{align}$$
It follows from the FOC:
$$p[1+\frac{1}{\varepsilon_p}]=C'(y)$$
where $\varepsilon_p=\frac{dy}{dp}\cdot \frac{p}{y}$ i.e., elasticity of demand facing the monopolist.Note that the elasticity will be a negative number as long as the consumers' demand curve has a negative slope, which is certainly the standard case

![Pasted image 20231121160414](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353608.png)
Determination of the monopoly output. The monopolist Figure produces where marginal revenue equals marginal cost.

From the FOC, we also have
$$\frac{p-C'}{p}=\frac{1}{\varepsilon_p}$$
The left-hand side is called the **Lerner index of market power**, ranging from 0 to 1

In the perfectly competitive case, the additional revenue a firm gains from selling an additional unit— its marginal revenue—is equal to the **market price**. The firm’s demand curve, which is a horizontal line at the market price, is also its marginal revenue curve.
For a perfectly competitive firm, the marginal cost curve is identical to the firm’s supply curve starting from the minimum point on the average variable cost curve.

### Price Discrimination
So far, we assume uniform pricing 
In reality, important questions often involve price dispersion 
Price discrimination: selling the same good at difference prices. 
1 st-degree price discrimination: perfect price discrimination 
2 nd-degree price discrimination: non-linear pricing 
3 rd-degree price discrimination: group pricing (e.g., museum tickets)


Price Discrimination is not always surplus decreasing

### Exchange Economy
==Note it is pure exchange market, no production==
The single-market story described above is a partial equilibrium model in that all prices other than the price of the good being studied are assumed to remain fixed. 
In the general equilibrium model all prices are variable, and equilibrium requires that all markets clear. Thus, general equilibrium theory takes account of all of the interactions between markets, as well as the functioning of the individual markets.

The basic concern of the theory of general equilibrium is how goods are allocated among the economic agents. The amount of good j that agent i holds will be denoted by $x^1_i$. Agent i's consumption bundle will be denoted by $\mathbf{x}_i = (x^1_i, . . . , x^k_i)$; it is a k-vector describing how much of each good agent $i$ consumes.  A feasible allocation is one that is physically possible; in the pure exchange case, ==this is simply an allocation that uses up all the goods==, i.e., on in which $\sum\limits^n_{i=1}\mathbf{x}_i=\sum\limits^n_{i=1}w_i$ ((In some cases it is convenient to consider an allocation feasible if $\sum\limits^n_{i=1}\mathbf{x}_i \leq \sum\limits^n_{i=1}w_i$) $w_i$ 是现有的每个人手上的资源分配
When there are two goods and two agents, we can use a convenient way of representing allocations, preferences, and endowments in a two-dimensional form, known as the **Edgeworth box**.
Suppose that the total amount of good 1 is $w^1 = w^1_1 + w^1_2$ and that the total amount of good 2 is $w^2 = w^2_1 + w^2_2$. The Edgeworth box has a width of w1 and a height of w2. A point in the box, $(x^1_1, x^2_1)$, indicates how much agent 1 holds of the two goods. At the same time, it indicates the amount that agent 2 holds of the two goods: $(x^1_2, x^2_2) = (w^1 - x^1_1, w^2 - x^2_1)$.
![1700555917319](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353609.png)
Edgeworth box. The length of the horizontal axis measures the total amount of good 1, and the height of the vertical axis measures the total amount of good 2. Each point in this box is a feasible allocation.

#### Walrasian equilibrium
Consider the particular case of pure exchange being described here.

$$\begin{align}
\max_{\mathbf{x}_i}u_i(\mathbf{x}_i)\\
\text{such that }px_i=pw_i
\end{align}$$
The answer to this problem, $\mathbf{x}_i(\mathbf{p}, \mathbf{p}w_i)$, is the consumer's demand function, which we have studied in Chapter 9. 

we typically define a **Walrasian equilibrium** to be a pair $(p^*,x^*)$, such that
$$\sum_i \mathbf{x}_i(\mathbf{p}^*,\mathbf{p}^*w_i)\leq \sum_i w_i$$
That is, $p^*$ is a Walrasian equilibrium if there is no good for which there is positive excess demand.

![1700557566707](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353610.png)
Walrasian equilibrium in the Edgeworth box. Each agent Figure is maximizing utility on his budget line.

##### Existence of Walrasian equilibria
the budget set of a consumer remains unchanged if we multiply all prices by any positive constant; thus, each consumer's demand function has the property that (According to [[Microeconomics#Properties of demand and supply functions\|Properties of demand and supply functions]])
$$\mathbf{x}_i(p,\mathbf{p}w_i)=\mathbf{x}_i(kp,k\mathbf{p}w_i)$$

As the sum of homogeneous functions is homogeneous, the aggregate excess demand function,
$$\mathbf{z}(\mathbf{p})=\sum^n_{i=1}[\mathbf{x}_i(\mathbf{p},\mathbf{p}w_i)-w_i]$$
is also homogeneous of degree zero in prices. 
If all of the individual demand functions are continuous, then z will be a continuous function, since the sum of continuous functions is a continuous function. Furthermore, the aggregate excess demand function must satisfy a condition known as Walras' law.

**Walras' Law** For any price vector $\mathbf{p}$, we have $\mathbf{pz(p)}\equiv 0$; i.e., the value of the excess demand is identically zero.
	Proof. We simply write the definition of aggregate excess demand and multiply by $\mathbf{p}$:
$$\mathbf{pz}(\mathbf{p})=\mathbf{p}\Big[\sum^n_{i=1}\mathbf{x}_i(\mathbf{p},\mathbf{p}w_i)-\sum^n_{i=1}w_i\Big]=\sum^n_{i=1}[\mathbf{px}_i(\mathbf{p},\mathbf{p}w_i)-\mathbf{p}w_i]=0$$
	since $\mathbf{x}_i(\mathbf{p}, \mathbf{p}w_i)$ must satisfy the budget constraint $\mathbf{px}_i = \mathbf{p}w_i$ for each agent $i= 1, ..., n$

Walras' law says something quite obvious: if each individual satisfies his budget constraint, so that the value of his excess demand is zero, then the value of the sum of the excess demands must be zero

Combining Walras' law and the definition of equilibrium, we have two useful propositions.

**Market clearing**. If demand equals supply in $k - 1$ markets, and $p_k > 0$, then demand must equal supply in the $k^{th}$ market.
	Proof 
	If not, Walras' law would be violated

**Free goods**. If $p^*$ is a Walrasian equilibrium and $z_j(p*)$ < 0, then $p^*_j= 0$. That is, if some good is in excess supply at a Walrasian equilibrium it must be a free good.
	Proof
	Since $p^*$ is a Walrasian equilibrium, $\mathbf{z}(\mathbf{p}^*)\leq 0$. Since prices are nonnegative, $\mathbf{p}^*\mathbf{z}(\mathbf{p}^*)=\sum^k_{i=1}p^*_i z_i(\mathbf{p}^*) \leq 0$. If $z_j(p^*) < 0$ and $p^*_j> 0$, we would have $\mathbf{p}^*\mathbf{z}(\mathbf{p}^*) < 0$, contradicting Walras' law. 

This proposition shows us what conditions are required for all markets to clear in equilibrium. Suppose that all goods are desirable in the following sense:

**Desirability** If $p_i = 0$, then $z_i(p) > 0$ for $i = 1,. . . , k$.

The desirability assumption says that if some price is zero, the aggregate excess demand for that good is strictly positive. Then we have the following proposition:

**Equality of demand and supply**. If all goods are desirable and $\mathbf{p}^*$ is a Walrasian equilibrium, then $\mathbf{z}(\mathbf{p}^*) = 0$.
	Proof.
	Assume $z_i(p*) < 0$. Then by the free goods proposition, $p^*_i = 0$. But then by the desirability assumption, $z_i(\mathbf{p}^*) > 0$, a contradiction

EXAMPLE: The Cobb-Douglas Economy
Let agent 1 have utility function $u_1(x^1_1,x^2_1)=(x^1_1)^a(x^2_1)^{1-a}$ and endowment $w_1=(1,0)$. Let agent 2 have utility function and endowment $w_2=(0,1)$. Then agent 1's demand function for good 1 is (According to [[Microeconomics#Related Curve of Cobb-Douglas\|IndirectUtilityCobbDouglas]])
$$x^1_1(p_1,p_2,m)=\frac{am_1}{p_1}$$
At prices $(p_1,p_2)$, income is $m_1=p_1\times 1+p_2\times 0=p_1$. Substituting, we have
$$x^1_1(p_1,p_2)=\frac{ap_1}{p_1}=a$$
Similarly, agent 2's demand function for good 1 is
$$x^1_2(p_1,p_2,m_2)=\frac{bm_2}{p_1}$$
At prices $(p_1,p_2)$, income is $m_2=p_1\times 0+p_2\times 1=p_2$. Substituting, we have
$$x^1_2(p_1,p_2)=\frac{b p_2}{p_1}$$
The equilibrium price is where total demand for each good equals total supply. By Walras' law, we only need find the price where total demand for good 1 equals total supply of good 1:
$$\begin{align}
x^1_1(p_1,p_2)+x^1_2(p_1,p_2)&=1\\
a+\frac{bp_2}{p_1}&=1\\
\frac{p^*_2}{p^*_1}&=\frac{1-a}{b}
\end{align}$$
Note that, as usual, only relative prices are determined in equilibrium.


Pareto Efficiency
(We can not make A better pff without hurting B)
## Paper Reading
### Consumption Responses to In-Kind Transfers: Evidence from the Introduction of the Food Stamp Program
```
[Hoynes&Schanzenbach_US_aej.ae09_FoodStampProgram.pdf](file:///D:/All%20Document/Msc/Advanced%20Microeconomics/Current/Hoynes&Schanzenbach_US_aej.ae09_FoodStampProgram.pdf)
```
We employ difference-in-difference methods to estimate the impact of program introduction on food spending.
canonical adj. 经典的

According to canonical economic theory, providing a transfer in-kind should lead to the same outcome as a similar-sized cash transfer as long as program participants are inframarginal.
inframarginal adj. 超边际的 [超边际分析方法](https://wiki.mbalib.com/wiki/%E8%B6%85%E8%BE%B9%E9%99%85%E5%88%86%E6%9E%90%E6%96%B9%E6%B3%95)

As a result, depending on consumer preferences, the provision of in-kind transfers (relative to cash) may have little to no impact on purchases of the actual goods being subsidized. Despite strong theoretical predictions about consumer behavior

Because the program is national, there is no variation in program parameters (such as stark differences in state benefit levels or eligibility) that are typically exploited by researchers to measure program impacts. ——所以这篇文章用来counties实施政策不同时间来作为variation

In the absence of programmatic variation, most researchers have studied the impact of the FSP by comparing food stamp recipients with eligible nonrecipients.
Since we would expect participants and nonparticipants to differ in important, and potentially unobservable, ways (Janet Currie 2006), researchers have employed a variety of methods to control for selection into the program——过去的方法
突然想起来Angrist的一个论断
```
The differences-in-differences (DD) method recognizes that in the absence of random assignment, treatment and control groups are likely to differ for many reasons.
```
如果不够random，selection bias 无法去除,DID或许是更好的方法
现有学者的观点:
In general, the literature conflicts with the canonical economic model and finds that food stamps increase food purchases among program participants by a much larger amount than would be predicted by the canonical economic model.
As a result, food stamp benefits worth $100 are thought to cause about a $17–$47 increase in food spending, while a cash transfer of $100 is associated with closer to a $5–$10 increase in food spending.
==But==, as mentioned above, these results have been based on studies that rely on strong and untested assumptions.

We use data from the Panel Study of Income Dynamics (PSID) from 1968–1978 to examine the impact of the FSP on food consumption.
- Specifically, we look at expenditures on food spent at home, meals out, and total food spending. 
- We test theoretical predictions that food stamps lead to a decrease in out of pocket spending on food and an increase in total food spending. 
- Further, we examine whether consumers are inframarginal—that is a dollar in cash income and a dollar in food stamp benefits generate equal impacts on food spending

We employ a difference-in-difference model, where the treatment is at the county level, with controls for county and year fixed effects and state linear time trends. In this model, identification requires that there are no contemporaneous county level trends that are correlated with food stamp introduction and family economic outcomes. 
We also estimate a triple difference model that uses variation across sub-groups with varying propensities for being affected by food stamps.

We control for possible confounders in two ways. ==这一部分没有看懂==
1. First, we examine the determinants of the FSP introduction, and find that earlier food stamp program introduction occurs in counties that are more populous, urban, black, low income, and with a smaller fraction of land used in agriculture
2. Second, FSP introduction took place during a period of great expansion in programs for the poor in the United States. To control for the possible coincident expansion of other programs such as Aid to Families with Dependent Children (AFDC), Medicaid, Medicare, and Social Security, we include county-by-year controls for federal spending on other social programs.
3. Finally, we estimate event study models that further support the validity of the research design.
underexploited adj. 未充分开发的

作者的观点
1. We find that the introduction of FSP leads to a decrease in out-of-pocket food spending and an increase in overall food expenditures. 
2. The expected effect on the propensity to eat meals out at restaurants is theoretically indeterminate
3. The results are precisely estimated for total food spending, with less precision in estimating the impacts on out-of-pocket food costs and meals out.
4. Further, we find evidence that the marginal propensity to consume food out of food stamp income is close to the marginal propensity to consume out of cash income.
5. In addition, those predicted to be constrained (at the kink in the food/non-food budget set) experience larger increases in food spending with the introduction of food stamps.-kink可能指的是BudgetFoodStampP

The remainder of the paper proceeds as follows. 
- Section I presents a history of the food stamp program. 
- Section II discusses the expected effects of the program, and 
- Section III reviews the existing literature. 
- Section IV describes the data, and 
- Section V presents the methodology. 
- Section VI presents our results, and 
- Section VII concludes.

#### Introduction of Food Stamp Program
began in 1961
the Food Stamp Act of 1964 (FSA)
This interest culminated in the passage of the 1973 Amendments to the Food Stamp Act, which mandated that all counties offer an FSP by 1975.

At the time the FSP was introduced and expanded, hunger and nutritional deficiencies were not uncommon among Americans.

Prior to the modern day FSP, some counties provided food aid through the commodity distribution program (CDP).

The above discussion suggests that counties with strong support for farming interests may adopt the FSP later in the period while those with strong support for the low-income population may adopt the FSP earlier in the period.
Consequently, the food stamp program introduction may not be completely exogenous.

the FSP represented an important increase in the quality and quantity of food in comparison to the CDP

Further, we find that those with a larger share of the population that is very young or old implement earlier, and counties in which more of the land is used in farming implement later.
We also find that the impacts of county characteristics are smaller (in absolute value) in counties in the south.

While these regression results show statistically significant impacts of the county characteristics on the timing of food stamp implementation, the quantitative importance of these predictors is small and most of the variation remains unexplained.
Nonetheless, in order to control for possible differences in trends across counties that are spuriously correlated with the county treatment effect, ==we include interactions of these 1960 pre-treatment county characteristics with time trends in all of our models==(总体是想表明事实FSA的时间和county本身的characteristics没有关系，最后一部加入的交互性值得研究研究)

However, to control for the possible coincident expansion of other programs, we also include annual measures of county per capita transfer payments for cash income support, medical care, and retirement and disability programs.1
#### Expected Effects pf Food Stamp Introduction
问题很多
![Pasted image 20231007152805](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353611.png)
The basic prediction of this transfer is that overall spending on food and other goods will increase as shown by the illustrated optimal points $A_0^*$ and $A_1^*$ . Out-of-pocket food expenses are expected to decrease (here, the change is $F_2−F_0$).

It is possible that a household with high demand for nonfood relative to food might be constrained by the in-kind nature of food stamps (relative to a cash transfer) and would locate at the kink, as in point $B_1^*$ . For these families, food stamps would lead to a larger increase in food consumption than an equivalent transfer in cash. Like [[Microeconomics#Kink Effect\|this]]

Prior to 1979 (and during the time period studied here), families had to make an up-front cash payment to receive the food stamp benefits. This feature, called the “purchase requirement,” did not change the magnitude of the benefits a family received.
![Pasted image 20231007155929](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353612.png)
As a result, there may be more people consuming at the kink in the budget constraint under the purchase requirement program than under the current program. This suggests that in our analysis, the impact of food stamps on food spending may be somewhat larger than it would be under the current (no purchase requirement) program or under a cash transfer scheme.

The PSID provides several measures of food expenditures: cash outlays for food at home, cash outlays for food away from home, and food bought with food stamps.
The prediction for spending on meals away from home is ambiguous given the positive income effect (due to the income transfer) and negative substitution effect (due to the reduction in the price of food at home).
#### Literature Review
$$fspend_i=\beta_0+\beta_1 cash_i+\beta_2 fstamp_i+\mathbf{Z}_i\gamma+\varepsilon_i$$ 
these naïve comparisons between participants and nonparticipants will overstate the impact of the program

Our research design takes this early literature to task and identifies the effects by variation in the timing of food stamp introduction across areas rather than the comparison of recipients and nonrecipients.
#### Data
To adjust for this nonrandom composition, the PSID includes weights designed to eliminate biases attributable to the oversampling of low-income groups and to attrition. All results use the weights provided by the PSID. (==是否意味着不够random的数都可以通过weight调整？==)

We use data from interview years 1968 to 1978. We stop the sample in 1978 so that our entire analysis period is before the end of the purchase requirement (which occurred in 1979). 

#### Methodology
$$y_{ict}=\alpha+\delta FSP_{ct}+\mathbf{X}_{it}\beta+\gamma_1\mathbf{Z}_{c60}t+\gamma_2 TP_{ct}+\eta_c+\delta_t+\lambda_s t+\varepsilon_{ict}$$
where $y_{ict}$ is the outcome variable (such as the log of total food spending) for family $i$ living in country $c$ in year $t$. $FSP_{ct}$ is an indicator variable equal to one if county $c$ in year $t$ has an $FSP$ program. $\mathbf{X}_{it}$ are family characteristics. $\mathbf{Z}_{c60}$ are 1960 county characteristics. $TP_{ct}$ are the REIS per capita county transfer income variables, $\eta_c$ are county fixed effects, $\delta_t$ are year effects, and $\lambda_s$ are state-specific linear time trends.
又让我想起Angrist的著作
![Pasted image 20231004165817](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353613.png)
	
#### Results for Expenditures on Food


female-headed households:
Household in which an adult female is the sole or main income producer and decision-maker
#### Conclusion
Using the PSID, we find that the FSP significantly increases food expenditures.
1. First, the poor react to in-kind transfers by reducing their out-of-pocket spending on the targeted good (although these results are not statistically significant).
2. Second, total consumption of the targeted good from all sources (cash outlays and in-kind transfers) increases.
3. Third, providing food stamp benefits in voucher form leads to a minimal distortion of the consumption choice relative to what it would be if the benefit were provided in cash.

Our findings contribute to the literature in two distinct ways
1. First, we provide important and new estimates of the impact of the food stamp program on consumption using a credible research design. 
2. Second, we test predictions of the theory of consumer choice and, in particular, the differential impacts of cash versus in-kind transfers.

Shi Ce:这篇文章的重要性在于联系了经济学理论和实证。用计量的方法去证明经济学理论。


#### Appendix
[Supplemental Nutrition Assistance Program](https://en.wikipedia.org/wiki/Supplemental_Nutrition_Assistance_Program)



### WHAT DRIVES MEDIA SLANT? EVIDENCE FROM U.S. DAILY NEWSPAPERS
```
C:\Users\94291\Desktop\documant\Msc\Msc\Advanced Microeconomics\Current
```
11.14 Shi Ce：好的实证论文都需要有理论基础支持

Firms respond strongly to consumer preferences, which account for roughly 20 percent of the variation in measured slant in our sample. 
By contrast, the identity of a newspaper’s owner explains far less of the variation in slant.
1. Introduction
	1. GOVERNMENT REGULATION OF NEWS MEDIA ownership in the United States is built on two propositions. 
	2. The first is that news content has a powerful impact on politics, with ideologically diverse content producing socially desirable outcomes. 
	3. The second proposition is that unregulated markets will tend to produce too little ideological diversity. 
	4. In contrast, evidence on the incentives that shape ideological content and on the role of ownership, in particular, is limited. 
	5. we propose a new index of ideological slant in news coverage and compute it for a large sample of U.S. daily newspapers. 
		1. We estimate a model of newspaper demand that incorporates slant explicitly, estimate the slant that would be chosen if newspapers independently maximized their own profits, and compare these profit-maximizing points with firms’ actual choices.
		2. We estimate the contributions of consumer and owner heterogeneity to cross-market diversity in slant and develop tentative implications for ownership regulation.
	6. Our slant index measures the frequency with which newspapers use language that would tend to sway readers to the right or to the left on political issues.
	7. We then index newspapers by the extent to which the use of politically charged phrases in their news coverage resembles the use of the same phrases in the speech of a congressional Democrat or Republican.
	8. Two key pieces of evidence suggest that our methodology produces a meaningful measure of slant. 
		1. First, many of the phrases that our automated procedure identifies are known from other sources to be chosen strategically by politicians for their persuasive impact. 
		2. Second, the index that we construct using counts of these phrases in news coverage is consistent with readers’ subjective evaluation of newspapers’ political leanings 
	9. ==We use our measure to estimate a model of newspaper demand==, in which a consumer’s utility from reading a newspaper depends on the match between the newspaper’s slant and the consumer’s own ideology
		1. Using [zip code-level data](https://sparkmap.org/support/understanding-zip-code-and-city-level-data-calculations/) on newspaper circulation, we show that right-wing newspapers circulate relatively more in zip codes with a higher proportion of Republicans, even within a narrowly defined geographic market. Left-wing newspapers show the opposite pattern
	10. Because we only use within-market variation to identify our model, our estimates are consistent even though slant is endogenous to the average political tastes in a market.(within-market variation理解不够) We show that our results are also robust to correcting for measurement error
	11. Treating newspapers as local monopolists, we compute the slant that each newspaper would choose if it independently maximized its own profits. The average profit-maximizing slant is close to the newspapers’ actual slant.
	12. ==We also estimate a model of the supply of slant==，.... also to the identity of its owner. 
	13. Overall, variation in consumer political attitudes explains roughly 20 percent of the variation in measured slant in our sample 
	14. An obvious concern in interpreting the relationship between slant and consumer attitudes is that it may reflect causation running from slant to consumer beliefs rather than the reverse.（判断是slant影响attitude还是反过来）To address this, we show that the relationship survives when we instrument for consumer political attitudes using religiosity.
	15. We find little evidence that the identity of a newspaper’s owner affects its slant.
	16. In the final section of the paper, we present additional evidence on the role of pressure from incumbent politicians (Besley and Prat (2006)), and the tastes of reporters and editors (Baron (2006)). ==The evidence we present suggests that neither of these forces is likely to explain a large share of the variation in slant.==
	17. This paper presents the first large-scale empirical evidence on the determinants of political slant in the news,
	18. Our work also advances the measurement of media slant
2. Data
	1. Our approach to measuring slant requires data on the frequency with which individual members of Congress use particular phrases.
	2. To increase the efficiency of our text analysis algorithm, we apply a standard preprocessing procedure that removes extremely common words (such as “to,” “from,” and “the”) and strips words down to shared linguistic roots (so that, for example, “tax cut” and “tax cuts” are identified as the same phrase)
	3. We define each newspaper’s geographic market as the PMSA in which it is headquartered. If a newspaper is not located inside a PMSA, we define its market to be the county in which it is located
	4. 
3. Measuring Slant
	1. Our approach to measuring the slant of a newspaper will be to compare phrase frequencies in the newspaper with phrase frequencies in the 2005 Congressional Record to identify whether the newspaper’s language is more similar to that of a congressional Republican or a congressional Democrat.
	2. First, for each politician, we compute a vector that gives the number of times each phrase appeared in their speeches. Second, we compute a mapping from the vector of counts to a measure of a politician’s ideology. Finally, we generate counts of each phrase in a newspaper’s text and apply the same mapping to generate an index of the newspaper’s ideology.
	3. We therefore add a “feature selection” step in which we use simple computations to identify a set of phrases that are highly diagnostic of the speaker’s political party.(这个的理解似乎也不深刻)
	4. Let $χ^2_{pl}$ denote Pearson’s $χ^2$ statistic for each phrase: ==为什么这么构造也值得思考==
		$x^2_{pl}=\frac{(f_{plr}f_{\sim pld}-f_{pld}f_{\sim plr})^2}{(f_{plr}+f_{pld})(f_{plr+f_{\sim plr}})(f_{pld}+f_{\sim pld})(f_{\sim plr+f_{\sim pld}})}$
	5. $χ^2$ is a test statistic for the null hypothesis that the propensity to use phrase p of length l is equal for Democrats and Republicans.
4. An Economic Model of Slant
	1. Our model is designed to capture three important features of newspaper markets. 
		1. First, consumers may prefer newspapers whose slant is close to their own ideology. 
		2. Second, firms will have an incentive to cater to this demand. 
		3. Finally, owner ideology may also affect firms’ choices of slant and this may lead slant to differ from the profit-maximizing level.
	2. Consumer Problem
		1. HYPOTHESIS D1: Fixing $\overline{u}_{zn}$ More conservative zip codes have a relatively greater taste for more conservatively slanted news
		2. HYPOTHESIS D2: Fixing $\overline{u}_{zn}$ and $y_n$ Demand has an inverted-U relationship to zip code ideology, peaking at $r_z = (y_n − α)/β$.
	3. Firm Problem
		1. HYPOTHESIS S1: $∂y_n/∂\text{ideal}_n > 0$. Slant is increasing in consumer Republicanism
		2. HYPOTHESIS S2: $∂y_n/∂μ_g > 0$. Slant is increasing in owner Republicanism
	4. However, we expect that most of the variation in consumer ideology is related to consumer characteristics such as geography, race, and religiosity that are not affected by newspapers, making the potential bias in our estimates from ==ignoring reverse causality relatively small.==
5. Identification and Estimation
6. Evidence of the Demand for Slant
	1. Figure 2 presents evidence on Hypothesis D1
7. Evidence on the Supply of Slant
	1. Consistent with Hypothesis S1, slant is highly related to consumer ideology.
8. Implications of the Model
	1. We can reject the hypothesis that the share of variance explained by consumers and owners is the same ($p = 0.003$)
9. Other Determinants of Slant
	1. (i) Incumbent politicians influence news content (Besley and Prat (2006)), and incumbent politicians’ ideology is correlated with consumer ideology. 
		1. Appendix B, we find no evidence that slant is related to the party affiliation of local elected officials.
	2. (ii) Reporters and editors are drawn from the local population, have ideologies correlated with those of local consumers, and are willing to sacrifice wage income to represent their own views in the newspaper (Baron (2006)).
		1. 这一部分的原理没看懂
10. Conclusion
	1. Our measure is computable with a minimum of subjective input, is related to readers’ subjective ratings of newspaper slant, and is available for newspapers representing over 70 percent of the daily circulation in the United States
	2. we show that consumer demand responds strongly to the fit between a newspaper’s slant and the ideology of potential readers, ==implying an economic incentive for newspapers to tailor their slant to the ideological predispositions of consumers==
	3. variation in consumer preferences accounts for roughly one-fifth of the variation in measured slant in our sample.
	4. By contrast, we find much less evidence for a role of newspaper owners in determining slant. While slant is somewhat correlated across co-owned papers, this effect is driven ==by the geographic clustering of ownership groups.==
	5. After controlling for the geographic location of newspapers, we find no evidence that the variation in slant has an owner-specific component.
	6. We also find no evidence that pressure from incumbent politicians(现任政治家) or the tastes of reporters are important drivers of slant.
	7. We wish to stress three important caveats(警告), however.
	8. Owners, politicians, or reporters may still exert significant influence on coverage of specific domains in which their interests are especially strong. For example, Gilens and Hertzman (2009)
	9. our results may not extend to settings with significantly different legal or institutional environments—less developed markets, more state ownership, less freedom of the press. (Anderson and McLaren (2009), Durante and Knight (2009)
	10. finding that ownership is not an important driver of content diversity does not imply that the market produces the optimal level of diversity
	11. How diversity and welfare are affected by the degree of local newspaper competition remains an important area for future research
11. Appendix

#### AI's summary
Brief introduction :

- This paper investigates the factors that drive media slant in U.S. daily newspapers by constructing a new index of media slant, estimating a model of newspaper demand, and comparing profit-maximizing points with actual choices made by firms.

Background:

- Background: The government regulation of news media ownership in the United States is based on the belief that news content has a significant impact on politics and that unregulated markets tend to produce too little ideological diversity.
- Past methods: Previous studies on media slant have relied on hand collection and coding of news content, limiting the number of sources analyzed. Existing measures of ideological content have not been used to analyze the determinants of slant.
- Motivation: The authors aim to address the limited evidence on the incentives that shape ideological content and the role of ownership in media slant by proposing a new index of ideological slant in news coverage and estimating a model of newspaper demand that incorporates slant explicitly.

Methods:

- a. Theoretical basis of the study:
    
    - The study aims to examine the incentives that shape ideological content and the role of ownership in determining media slant. It contributes to the literature on product positioning in the mass media and product differentiation.
- b. Technical route of the article (step by step):
    
    - The paper uses data from the 2005 Congressional Record to measure slant. It also obtains counts of the frequency of phrases in news coverage from the NewsLibrary and ProQuest Newsstand databases. The ownership and market characteristics of newspapers are matched with data from the 2001 Editor and Publisher International Yearbook CD-ROM. Demographic characteristics of newspaper markets are obtained from the 2000 U.S. Census. The paper also considers the political leanings of markets based on the share of votes going to George W. Bush in the 2004 presidential election.

Results:

- a. Experimental settings in detail:
    
    - The authors conducted several robustness checks to confirm their findings. They included controls for newspaper quality, used instrumental variables to account for consumer ideology, and estimated a model with newspaper fixed effects.
- Experimental results in detail:
    
    - The study finds that consumer demand plays a significant role in driving media slant, with newspapers tailoring their slant to match the ideological preferences of their readers. The variation in consumer preferences accounts for about one-fifth of the variation in measured slant. On the other hand, there is less evidence for the influence of newspaper owners or pressure from incumbent politicians in determining slant. The study also suggests that ownership diversity may not be a critical factor for ideological diversity in the media. However, the study acknowledges that its measure of slant is a broad aggregate and that specific domains where owners, politicians, or reporters have strong interests may still exert significant influence on coverage. The findings may not extend to settings with different legal or institutional environments, and the impact of local newspaper competition on diversity and welfare remains an important area for future research.

#### Extra Credit
Grade: 5/5
[Your Projects - Overleaf, Online LaTeX Editor](https://www.overleaf.com/project)
A. Introduction and Background 
(i). Is the paper mainly theoretical or empirical? 
	Solution:
	Both, theoretical and empirical. The authors first established a theoretical model and gave several hypotheses. After that, they used data and empirical tests to prove two hypotheses.
(ii). What is/are the question/questions the author attempts to answer in this paper?
	Solution:  
	The determinants of political slant in the news. The main determinant is the consumers' preference, instead of the newspaper’s owner, the incumbent politicians’ ideology, and reporters and editors.
B. Economic Content 
In economics, we study supply and demand for goods and services. When it comes to markets for news, ideas, and more broadly, information, there also exists a supply-and-demand relationship. 
In the context of this paper, what are specifically the supply and demand factors for news?
	Solution:
	The supply factors are the revenue of the newspaper.
	The demand factors are the utility of readers and consumers.
C. Economic Methodology 
(i). Describe the data on U.S. newspapers that the authors use to investigate the empirical questions.
	Solution:
	1. counts by speaker and party of two- and three-word phrases in the Congressional Record.
	2. the number of articles containing each phrase in each newspaper during calendar year 2005
	3. the owner of each newspaper as of 2000
	4. the share of votes in each market
(ii). Broadly speaking, what is a "media slant"? How do the authors define media slants specifically in this paper? 
	Solution: 
	Broadly speaking, "media slant" means "political bias".
    In this paper, "media slant " is defined as the newspaper’s language being more similar to that of a congressional Republican or a congressional Democrat.
(iii). A major pioneering contribution of this paper is to provide a practical measure of media slants. Explain in detail how the authors measure media slants of U.S. newspapers.
	Solution:
	Authers utilize Pearson's statistic for each phrase and compared phrase frequencies in the newspaper with phrase frequencies in the 2005 Congressional Record.
	$χ^2$ is a test statistic for the null hypothesis that the propensity to use phrase $p$ of length $l$ is equal for Democrats and Republicans.
(iv). In Section 5, what equations are used to estimate the supply and demand for newspapers? For each estimation, what are the main concerns for identification, and how do the authors address the potential endogeneity problem?
	Solution:
	Demand $\ln \frac{S_{zn}}{1-S_{zn}}=\delta_{mn}+\lambda^d_0 y_nr_z+\lambda^d_1 r_z+\lambda^d_2 e^2_z+X_z\phi^0+W_{zn}\phi^1+v_{zn}$
	Supply: $\hat{y}_n=\lambda^s_0+\lambda^s_1 R_n+\mu_s+w_n$
	the authors adopt an intruemnt varianles (the overall share of Republicans in newspaper n’s primary market) strategy to the potential endogeneity problem
(v.) In Sections 6 and 7, what do the authors do? What are their main findings regarding the supply and demand of media slants?
	Solution:
	Authers did empirical research to test the hypothesis in Section 4.
	Authers found that hypothesis D1 and S1 were correct. 
	Hypothesis D1: Fixing $\overline{u}_{zn}$ More conservative zip codes have a relatively greater taste for more conservatively slanted new.
	Hypothesis S1: HYPOTHESIS S1: $∂y_n/∂\text{ideal}_n > 0$. Slant is increasing in consumer Republicanism
D. Your responses 
The scope of modern economic analysis has extended well beyond goods and services that are traditionally viewed as commodities to previously less explored areas, such as family and marriage, politics, and media. 
(i) This paper does not particularly look at the role of advertising in modern media. What do you think is the role of advertising (and advertisers) in shaping what consumers see in media? 
	Solution:
	In this case, media firms sell a joint product to two different categories of buyers: the media firms to advitisers, and media content to media consumers.
	Advertisers pays to media , which is called "advertising finance' When "advertising finance" become a major income of media, there is no incentive under advertising-based finance to cater to the taste of viewers who would not buy the products advertised. This means that the programming choice made by medias may not reflect the preference of all views, leading to market failure in which the provision of media does not fully satisfy consumer demand.
(ii) Consumers want to eat apples, so farmers grow apples. However, what do you think are the underlying problems if "consumers read what they want to read"? Try to phrase your explanation in a (more) economic way.(She ce:为什么在媒体市场提供给消费者想看的是不好的事情)
	Solution:
	1. Unlike apples, media news is public good, which is non-excludable. Public goods have wider impact comparing with normal goods. A slant media can affect a large number of people.
	2. The slant media which supply reader what they want to read will lead to a fragmentation of the media landscape. Cosummers will reinforce their existing ideas and thus suffer from information asymmetry.
	3. Information asymmetry will contribute to market inefficiency and failure.
11.14 Shi Ce: 复杂经济学计算成本很大，收益很小
微观上现有均衡理论基本足够了，宏观上现有理论还不够
#### [Porter Stemming Algorithm](https://tartarus.org/martin/PorterStemmer/)
The Porter stemming algorithm (or ‘Porter stemmer’) is a process for removing the commoner morphological and inflexional endings from words in English. 
波特词干算法（或“波特词干分析器”）是一种从英语单词中删除常见形态和屈折词尾的过程。
### To Build Outward or Upward? The Spatial Pattern of Urban Land Development in China
Second extra credit
```
D:\AllDocument\Msc\Advanced Microeconomics\Current
```

a theoretical model to demonstrate how a city leader whose career advancement depends on city economic growth chooses the spatial pattern of urban land development.
Two major testable predications are derived. First, city leaders with high career incentives are more likely to expand the city outward in order to boost land sale revenues for financing public infrastructure and enhancing economic growth. Second, the average use intensity of newly developed land is lower for city leaders with stronger career incentives due to the trade-off between a city’s upward and outward expansion.

Contract 容积率

SheCe:这个模型在近几年有所改变

## Mid-term
October 20(Friday): 3:00-5:00PM, YIA LT3
Midterm exam covers lecture notes 1-5 and chapters 1-5,7,8 snd example in Ch.6 (page 87)
Extended office hours (of Shi Ce):
	2-3 PM on Oct. 19
	1-2 PM on Oct.20
Hao's additional office hour
	10-11 AM on Oct. 20
	In addition to Hao's regular office hours
3rd tutorial session

Close book, close-notes, etc
5-6 short answer questions
Extra-credit opportunity

Calculator is allowed!
No smartphone 

1. (20 points) Consider a general, “well-behaved” production function, $f(x_1,x_2)$ , with two inputs. The input prices are denoted by $w_1,w_2$.   
	a. In this two-input case, show that (i) the input demand functions are homogenous of degree 0 using the first-order conditions, and (ii) the profit function is homogenous of degree 1 in all prices.
		(i) 和[[Microeconomics#Quiz 2\|Quiz2]]挺像的
		(ii)AI's answer
		To show that the profit function is homogeneous of degree 1 in all prices, we need to demonstrate that it changes proportionally to changes in input prices.
		Let's consider two sets of input prices, $(w_1, w_2)$ and $(\lambda w_1, \lambda w_2)$, where $\lambda$ is a positive constant.
		The profit function with the original prices $(w_1, w_2)$ is given by: $$\pi(w_1, w_2) = pf(x_1, x_2) - w_1x_1 - w_2x_2$$
		The profit function with the scaled prices $(\lambda w_1, \lambda w_2)$ is given by: $$\pi(\lambda w_1, \lambda w_2) = p f(x_1, x_2) - \lambda w_1 x_1 - \lambda w_2 x_2$$
		Now, let's consider the ratio of the profit function with scaled prices to the profit function with original prices: $$\frac{\pi(\lambda w_1, \lambda w_2)}{\pi(w_1, w_2)} = \frac{p f(x_1, x_2) - \lambda w_1 x_1 - \lambda w_2 x_2}{pf(x_1, x_2) - w_1x_1 - w_2x_2}$$
		Simplifying the equation: $$\frac{\pi(\lambda w_1, \lambda w_2)}{\pi(w_1, w_2)} = \frac{p f(x_1, x_2)}{pf(x_1, x_2)} \cdot \frac{1 - \lambda \frac{w_1}{p} \frac{x_1}{f(x_1, x_2)} - \lambda \frac{w_2}{p} \frac{x_2}{f(x_1, x_2)}}{1 - \frac{w_1}{p} \frac{x_1}{f(x_1, x_2)} - \frac{w_2}{p} \frac{x_2}{f(x_1, x_2)}}$$
		As $\lambda$ approaches 1, the above expression simplifies to: $$\lim_{\lambda \to 1} \frac{\pi(\lambda w_1, \lambda w_2)}{\pi(w_1, w_2)} = \frac{1 - \frac{w_1}{p} \frac{x_1}{f(x_1, x_2)} - \frac{w_2}{p} \frac{x_2}{f(x_1, x_2)}}{1 - \frac{w_1}{p} \frac{x_1}{f(x_1, x_2)} - \frac{w_2}{p} \frac{x_2}{f(x_1, x_2)}}$$We can observe that this expression is equal to 1, indicating that the profit function changes proportionally to changes in input prices. Therefore, the profit function is homogeneous of degree 1 in all prices.
	b. Show that the sign of  $\frac{d y^*}{d w_1}$ is ambiguous, where $y^*$ is the output function. Briefly explain the intuition behind this result.
		AI's solution
		To understand why the sign of $\frac{d y^*}{d w_1}$ is ambiguous in a general, "well-behaved" production function $f(x_1,x_2)$ with two inputs, let's consider the intuition behind this result.
		In a production function, the output $y^*$ is a function of the inputs $x_1$ and $x_2$. The input prices are denoted by $w_1$ and $w_2$. The goal is to determine how changes in input prices affect the optimal level of output.
		When the price of input $x_1$ changes, it can have two effects on the optimal level of output $y^*$. On one hand, a decrease in the price of $x_1$ makes it relatively cheaper compared to $x_2$, which might lead firms to use more of $x_1$ and less of $x_2$ in production. This substitution effect could increase the optimal level of output, resulting in a positive $\frac{d y^*}{d w_1}$.
		On the other hand, a decrease in the price of $x_1$ also reduces the cost of producing a given level of output. This cost effect might lead firms to reduce the overall level of inputs used, including $x_1$, which could decrease the optimal level of output. This income effect could result in a negative $\frac{d y^*}{d w_1}$.
		Therefore, the sign of $\frac{d y^*}{d w_1}$ is ambiguous because it depends on the relative strength of the substitution effect and the income effect. The net effect of a change in input prices on the optimal level of output will depend on the specific characteristics of the production function and the relative importance of the inputs.

2. (24 points) Solve the following problems on preference and demand.
	a. In a two-commodity world, for a set of indifference curves representing the same underlying preference, prove that (i) an indifference curve cannot be “thick,” and (ii) any two indifference curves cannot intersect each other.  
	b. Consider the indirect utility function given by
$$v(p_1,p_2,m)=\frac{m}{p_1+p_2}$$
	Find the associated demand functions, expenditure function, and direct utility function.
	Solution from AI:
		a. 
		(i) To prove that an indifference curve cannot be "thick," we need to show that all points on the indifference curve have the same level of utility. If there were points on the indifference curve that have different levels of utility, it would imply that the individual is indifferent between these points, which contradicts the definition of an indifference curve.
		(ii) To prove that an indifference curve cannot intersect another indifference curve, we need to show that if two indifference curves intersect, it would imply **a violation of the transitivity of preferences**.
		Let's assume that there are two indifference curves, IC1 and IC2, that intersect at point P. This means that at point P, the individual is indifferent between the combinations of goods represented by IC1 and IC2.
		Now, let's consider two other points, A and B, on the indifference curves such that A is on IC1 and B is on IC2. Since point P is on both curves, it means the individual is indifferent between A and P as well as between B and P.
		If we connect points A and P with a line, and points B and P with another line, these lines would intersect at point P. This implies that the individual is indifferent between A and B, which violates the transitivity of preferences. Transitivity states that if an individual prefers A to B and B to C, then the individual must also prefer A to C.
		Therefore, we can conclude that indifference curves cannot intersect each other.
		b.
		same as 7.4 on textbook
		Demand function $x_1=\frac{m}{p_1+p_2},x_2=\frac{m}{p_1+p_1}$
		expenditure function $e(p_1,p_2,u)=u(p_1+p_2)$
		$u(x_1,x_2)=\min\{x_1,x_2\}$
		10.20 DYC:一眼看出是leontief function

3. (28 points) In a two-commodity world, consider a representative consumer with the following Cobb-Douglas utility:
$$U(x_1,x_2)=x^{\alpha}_1x^{\beta}_2$$
	and the commodity prices and income are denoted by $p_1,p_2$ and $m$, respectively. Suppose that $x_1$ is food and $x_2$ is a composite good (“everyting else”).
	a. Find the demand functions, $x^*_1(p_1,p_2,m)$ and $x^*_2(p_1,p_2,m)$. Show your work step by step.
		Solution:
$$\left\{\begin{array}{**lr**} U=x^{\alpha}_1x^{\beta}_2\quad x_1\text{ is food }x_2\text{ is others }\\ p_1x_1+p_2x_2=m\end{array}   \right.$$
		$x_1=\frac{\alpha}{\alpha+\beta}\cdot\frac{m}{p_1}$
		$x_2=\frac{\alpha}{\alpha+\beta}\cdot \frac{m}{p_2}$
	b. Now, the consumer receives a food voucher of the amount _B_. We use  $x^{total}_1$ and $x^{oop}_1$ to denote total and out-of-pocket food consumption levels, respectively. Write out the consumer’s budget constraint in this case.
		Solution:
		Food Voucher B, $x^{total}_1>x^{oop}_1$
$$\left\{\begin{array}{**lr**} x^{oop}_1 \geq 0\\ x_2 \geq 0\\ p_1x^{total}_1+p_2x_2=m\\ x^{total}_1 \geq \frac{B}{p_1}   \end{array}   \right.$$
	c. Solve for the optimal consumption bundles in this scenario with a food voucher. Show that with the food voucher, (i) total food consumption increases, and (ii) out-of-pocket food expenditure decreases compared to the consumer’s original choices.
		Solution:
$$\begin{align}&\max x^{total(\alpha)}_1x^{\beta}_2\\ \text{s.t.}&\left\{\begin{array}{**lr**} p_1x_1^{total}+p_2x_2=m+B\\ p_1x^{total}_1 \ge B   \end{array}   \right.\end{align}$$
$$x^{total}_1=\left\{\begin{array}{**lr**} \frac{\alpha}{\alpha+\beta}\frac{m+B}{p_1}, \\ \frac{B}{p_1}\quad x^{oop}_1=0\end{array}   \right.$$
		We can get this answer  by review this [Proof: Demand Functions for Cobb-Douglas Utility Functions](https://www.econgraphs.org/textbooks/intermediate_micro/consumer_theory/demand/cobb_douglas.html)
	d. Related to the paper by Hoynes and Schanzenbach (2009), “_Consumption Responses to In-Kind Transfers: Evidence from the Introduction of the Food Stamp Program_” (which we read in class), state one research question the authors try to answer. Briefly describe the estimation strategy used to empirically examine that question. State one assumption necessary for a causal interpretation of its main estimation results.
		ChatPDF's answer:
		Research question: Do in-kind transfers lead to increased purchases of the subsidized goods? 
		Estimation strategy: The authors use a difference-in-differences approach to estimate the causal effect of the introduction of the Food Stamp Program (FSP) on food expenditures. They compare changes in food expenditures for households in counties that adopted the FSP to changes in food expenditures for households in counties that did not adopt the FSP, before and after the introduction of the program. They also use a regression analysis to control for demographic and county-level variables that may affect food expenditures 19. 
		Assumption for causal interpretation: The authors assume that there are no unobserved confounding variables that affect both the adoption of the FSP and food expenditures. In other words, they assume that the adoption of the FSP is exogenous, or unrelated to any other factors that may affect food expenditures. If this assumption is violated, the estimated effect of the FSP on food expenditures may be biased 19.
		------------
		I ask ChatPDF a question:
		If you are a professor in macroeconomics, what questions you will ask in midterm exam regarding to this paper? you need to give the answers to these questions as well.
		AI's answer:
		As a professor in macroeconomics, I might ask the following questions on this paper:  
		1. What is the difference between in-kind transfers and cash transfers? How might this difference affect the effectiveness of transfer programs in reducing poverty and improving welfare? 
		Answer: In-kind transfers provide vouchers for specific goods, such as food and housing, while cash transfers provide recipients with money that they can use to purchase any goods or services they choose. In-kind transfers may be more politically acceptable than cash transfers, but they may also be less effective in reducing poverty and improving welfare if recipients do not value the subsidized goods as much as they value other goods. This paper examines the impact of in-kind transfers on consumer behavior, specifically whether the introduction of the Food Stamp Program (FSP) led to increased purchases of food.  
		2. What is the research question that the authors try to answer in this paper? What is their main finding? 
		Answer: The research question is whether in-kind transfers lead to increased purchases of the subsidized goods. The authors use a difference-in-differences approach to estimate the causal effect of the introduction of the FSP on food expenditures. They find that the FSP significantly increased food expenditures for households in counties that adopted the program, compared to households in counties that did not adopt the program. ==However, the effect was smaller for households that were not initially food-constrained, suggesting that the FSP was more effective in increasing food purchases for households that faced liquidity constraints.== 
		3. What are some of the limitations of the authors' empirical approach? How might these limitations affect the validity of their results? 
		Answer: One limitation of the authors' empirical approach is that it relies on the ==assumption that there are no unobserved confounding variables that affect both the adoption of the FSP and food expenditures. ==If this assumption is violated, the estimated effect of the FSP on food expenditures may be biased. Another limitation is that the authors do not have data on the quality of the food purchased, so it is possible that the FSP led to increased purchases of low-quality food. Finally, the authors' results may not be generalizable to other in-kind transfer programs or to other contexts, as the effectiveness of transfer programs may depend on the specific goods or services being subsidized and the characteristics of the population being served.
		4. What are some of the demographic and county-level variables that the authors control for in their regression analysis? Why are these variables important to include in the analysis?
		Answer: The authors control for a variety of demographic and county-level variables in their regression analysis, including household income, education, race, and age, as well as county-level poverty rates, unemployment rates, and urbanization rates. These variables are important to include in the analysis because they may affect both the adoption of the FSP and food expenditures.
		5. What is the difference between the triple difference and the difference-in-differences approach? Why do the authors use the triple difference approach in addition to the difference-in-differences approach?
		Answer: The difference-in-differences approach compares changes in food expenditures for households in counties that adopted the FSP to changes in food expenditures for households in counties that did not adopt the FSP, before and after the introduction of the program. The triple difference approach adds a third comparison group of households that were not eligible for the FSP, but were similar to the eligible households in terms of demographic and county-level characteristics. The authors use the triple difference approach to control for any pre-existing differences between the eligible and ineligible households that may affect food expenditures.
		==第一次获知triplr difference-in-difference的使用，感觉很有收获==
		6. What are some of the policy implications of the authors' findings? How might policymakers use this information to design more effective transfer programs?
		Answer: The authors' findings have several policy implications. First, they suggest that in-kind transfers may be more effective in increasing food purchases than cash transfers, especially for households that face liquidity constraints. Second, they suggest that the effectiveness of transfer programs may depend on the specific goods or services being subsidized and the characteristics of the population being served. Finally, they suggest that policymakers should consider the potential trade-offs between the political acceptability of in-kind transfers and their effectiveness in reducing poverty and improving welfare.


4. (8 points) In Finkelstein (2004), “_Static and Dynamic Effects of Health Policy: Evidence from the Vaccine Industry_,” the author conducts welfare analysis using the following expression for total social benefits associated with vaccination:
$$V*E*H$$
	where $V$ is the vaccination rate, _E_ is the maximal efficacy of a vaccine, and _H_ is the monetary value of the social benefits of complete vaccination with a perfectly effective vaccine. 
	Explain the channels through which vaccine innovation can bring additional social health benefits in the long run.

5. (20 points) Solve the following problems on production and cost. 
	a. Given the cost function:
$$c(w_1,w_2)=w_1w_2y/(w_1+w_2)$$
	where $w_1, w_2$  denote input prices.
	Find the conditional input demand functions, $x^{\#}_1(w_1,w_2,y)$ and $x^{\#}_2(w_1,w_2,y)$, and use them to recover the underlying production function $y=f(x_1,x_2)$  _._ What is the form of this technology?
	Solution:
		According to Shephard Lemma: $\frac{\partial c}{\partial w_1}=x^{\#}_1$
		$x^{\#}_1=\frac{w_2^2y}{(w_1+w_2)^2}$
		Similarly, $x^{\#}_2=\frac{w_1^2 y}{(w_1+w_2)^2}$
		10/20 Shi Ce's answer
		To understand the form of technology
		we need to eliminate $w_1,w_2$
		$\sqrt{x^{\#}_1}=\frac{w_2}{w_1+w_2}\sqrt{y}\ (1)$
		$\sqrt{x^{\#}_2}=\frac{w_21}{w_1+w_2}\sqrt{y}\ (2)$
		$(1)+(2)$
		$y=(x_1^{\frac{1}{2}}+x_2^{\frac{1}{2}})^2$
		It is the CES technology 
	b. Consider the production function:
$$f(x_1,x_2,x_3,x_4)=\min\{2x_1+x_2,x_3+2x_4\}$$
	Find the conditional input demand function for each factor and the cost function for this technology.
	AI's solution
	The production function is given by:
$$f(x_1​,x_2​,x_3​,x_4​)= \min\{2x_1​+x_2​,x_3+2x_4\}$$
	To find the conditional input demand function for each factor, we need to find the input that minimizes the cost of producing a given output. The cost function for this technology can then be derived from the input demand functions.
	The production function can be rewritten as:

$$f(x_1,x_2,x_3,x_4)=\left\{\begin{array}{**lr**} 2x_1+x_2\quad \text{if }2x_1+x_2\leq x_3+2x_4 \\ x_3+2x_4\quad \text{if }2x_1+x_2>x_3+2x_4\end{array}   \right.$$
		We can see that $x_1$​ and $x_2$​ are perfect substitutes, and $x_3$​ and $x_4$​ are also perfect substitutes. Therefore, if $w_i$​ denotes the price per unit of input $x_i$​, then:
		- $x_1$​ is used to produce the output when $\frac{w_1}{2}​​<w_2$​ and $x_2​=0$
		- $x_2$​ is used to produce the output when $\frac{w_1}{2}​​>w_2$​​ and $x_1​=0$
		- x3​ is used to produce the output when $w_3<\frac{w_4}{2}$​​ and $x_4​=0$
		- x4​ is used to produce the output when $w_3​>\frac{w_4}{2}$​​ and $x_3​=0$
		So if we want to produce one unit of output when the input prices satisfy $\frac{w_1}{2}<w_2$​ and $w_3<\frac{w_4}{2}$​​, then we must employ $x_1=\frac{1}{2}$ and $x_3=1$ so as to minimize cost, and the cost is given by ​​$\frac{w_1}{2}+w_3$​.
		When the input prices satisfy $\frac{w_1}{2}>w_2$ and $w_3<\frac{w_4}{2}$​​, then we must employ $x_2​=1 and $x_3​=1$ in order to minimize cost, and the cost is given by $w_2+w_3$​.
		For other two combinations, we can write the cost of producing one unit of output as $\min(\frac{w_1}{2},w_2)+\min(w_3,\frac{w_4}{2})$. More generally, if we want to produce q units, cost function is
$$C(w_1,w_2,w_3,w_4,q)=[\min(\frac{w_1}{2},w_2)+\min(w_3,\frac{w_4}{2})]q$$
		10/20 感觉和[[Microeconomics#Problem Set 2\|textbook上5.11]]有点像 { #Midterm5}


### 2023 Mid-term
AVG 68
SD 17
Final exam will be not accumulative

1. In a two-commodity world, consider the following function:
$$U(x_1,x_2)=\alpha\ln x_1+\beta\ln x-2+c$$
and the commodity prices and income are denoted by $p_1,p_2$ and $m$, respectively.
	a. Find the demand functions, $x^*_1(p_1,p_2,m)$ and $x^*_2(p_1,p_2,m)$
		Solution:
	b. Suppose $\alpha=1,\beta=1,c=2023,p_2=1,m=72$ for the above utility maximization problem, and $p_1$ falls from 9 to 4. Use the **Hicks decompsition** to decompose the effect of the price drop on $x^*_1$ into substitution effect and the income effect. In other words, how many units of change in $x^*_1$ are due to the pure substituion effect, and how many are due to income effect.
		Solution: same as [[Microeconomics#The Hicks decomposition of a demand change\|the Hicks decomposition of a demand change]]

2. Consider the following CES technology $f(x_1,x_2)=(x^{\rho}_1+bx^{\rho}_2)^{1/\rho}$. The input prices are denoted by $w_1,w_2$, respectively.
	a. Solve the conditional input demand functions, $x^{\#}_1(w_1,w_2,y)$ and $x^{\#}_2(w_1,w_2,y)$ . Derive and sign $\frac{dx^{\#}_1}{dy}$ for this specific case.
	b. Show that the sign of $\frac{dx^{\#}_1}{dy}$ is ambiguous for the general case with two inputs.

3. Prove the followiing statements.
	a. For a general production function, $f(x_1,x_2)$, with two inputs, show $\frac{dx^*_1}{dp}=-\frac{dy^*}{dw_1}$, where $y^*$ is the output supply function.
		Solution:
		We assume $\pi^*=py-w_1x_1-w_2x_2$
		According to [[Microeconomics#**Hotelling's Lemma**\|Hotelling's Lemma]]
		$y_i=\frac{\partial \pi}{\partial p_i}$
		$\therefore \frac{d y_i}{dw_1}=\frac{\partial^2 \pi}{\partial p_i\partial w_1}=\frac{\partial^2 \pi}{\partial w_1\partial p_i}$
		$\because \frac{\partial \pi}{\partial w_1}=-x_1$
		$\therefore \frac{\partial^2 \pi}{\partial w_1\partial p_i}=-\frac{dx^*_1}{dp}$
		$\therefore \frac{dx^*_1}{dp}=-\frac{dy^*}{dw_1}$
	b. For a continuous and twice differentiable cost function, $c(y)$, marginal cost cost always equals average cost at the point of minimum average cast.
		Solution:
		$MC=\frac{\partial c(y)}{\partial y}\quad AC=\frac{c(y)}{y}$
$$\min\limits_y\ \frac{c(y)}{y}$$
		$\frac{d\ AC}{dy}=\frac{y\cdot c'(y)-c(y)}{y^2}=0$
		$\therefore c'(y^*)y^*=c(y^*)\Rightarrow c'(y^*)=\frac{c(y^*)}{y^*}$ 
		$\therefore MC=AC$

4. In a two-commodity world, consider a representative consumer with following Cobb-Douglas utility:
$$U(x_1,x_2)=(x^{\rho}_1+x^{\rho}_2)^{\frac{1}{\rho}}$$
and the commodity price and income are denoted by $p_1,p_2$ and $m$, respectively. Suppose that $x_1$ is food and $x_2$ is acomposite good("everything else").
	a. Find the demand functions, $x^*_1(p_1,p_2,m)$ and $x^*_2(p_1,p_2,m)$. Show your work step by step.
	b. Now, the consumer receives a food voucher of the amount $B$. We use $x^{total}_1$ and $x^{oop}_1$ to denote _total_ and _out-of-pocket_ food consumption levels, respectively. Write out the consumer's budget constraint in this case. 
	c. Solve for the optimal consumption bundles in this scenario with a food vouvher. Show that with the food voucher, (i) total food consumption increases, and (ii) out-of-pocket food expenditure decreases compared to the consumer's original choices.
	Solution:
	(looks tutor write $x,y$ as $x_1,x_2$, $p_x,p_y$ as $P_1,P_2$)
$$\begin{align}
u=(w_x x^{\rho}+w_y y^{\rho})^{\frac{1}{\rho}}, P_x x+P_y y\leq M\\
\frac{MU_x}{MU_y}=(\frac{w_x}{w_y})(\frac{y}{x})^{1-\rho}=\frac{P_x}{P_y}\Rightarrow y^*=(\frac{P_x}{P_y})^{\frac{1}{1-\rho}}(\frac{w_y}{w_x})^{\frac{1}{1-\rho}}
\end{align}$$
	We write $\sigma=\frac{1}{1-\rho}$ ([[Microeconomics#Chapter 1\|Problem1-2-elasticity of substitution]]). $P_x x+P_y (\frac{P_x}{P_y})^{\sigma}(\frac{w_y}{w_x})^{\sigma}x=M \Rightarrow$
	 $P_x x^*+P_y (\frac{P_x}{P_y})^{\sigma}(\frac{w_y}{w_x})^{\sigma}x^*=M \Rightarrow P^{1-\sigma}_x x^*+P^{1-\sigma}_y (\frac{w_y}{w_x})^{\sigma}x^*=MP^{-\sigma}_x$
	$x^*=\frac{MP^{-\sigma_x}}{(P^{1-\sigma}_x+P^{1-\sigma}_y(\frac{w_y}{w_x})^{\sigma})}\mathop{\Rightarrow}\limits^{expenditure} P_x x^*=\frac{P^{1-\sigma}_x}{(P^{1-\sigma}_x+P^{1-\sigma}_y(\frac{w_y}{w_x})^{\sigma})}M$
	With voucher B,
$$x^{\text{Total}}=\left\{\begin{array}{**lr**} \frac{(M+B)P^{-\sigma_x}}{(P^{1-\sigma}_x+P^{1-\sigma}_y(\frac{w_y}{w_x})^{\sigma})}\text{ if }\frac{(M+B)P^{-\sigma_x}}{(P^{1-\sigma}_x+P^{1-\sigma}_y(\frac{w_y}{w_x})^{\sigma})}>\frac{B}{P_x}\\ x^{\text{total}}=\frac{B}{P_x}, \text{otherwise} \end{array}   \right.$$
$$P_x x^{\text{OOP}}=\left\{\begin{array}{**lr**} \frac{(M+B)P^{-\sigma_x}}{(P^{1-\sigma}_x+P^{1-\sigma}_y(\frac{w_y}{w_x})^{\sigma})}-B=\frac{P^{1-\sigma}_xM-P^{1-\sigma}_y(\frac{w_y}{w_x})^{\sigma}B}{(P^{1-\sigma}_x+P^{1-\sigma}_y(\frac{w_y}{w_x})^{\sigma})}<P_x x^{\text{OLD}},\text{in case 1}\\ 0<P_x x^{\text{OLD}},\text{otherwise} \end{array}   \right.$$
	d. Related to the paper by Hoynes and Schanzenbach (2009), "_Consumption Responses to In-Kind Transfers: Evidence from the Introduction of the Food Stamp Program_" (which we read in class), explain why one might be concerned about the potential **endogeneity** of the roll-out of food stamp policies in U.S countries. Brief describe one empirical exercise that can be used to address such a concern.


5. Solve the following problems on production and cost
	a. Given the cost function:
$$c(w_1,w_2,y)=\frac{w_1w_2y}{(w_1+w_2)}$$
	where $w_1,w_2$ denote input price.
	Find the conditional input demand functions, $x^{\#}_1(w_1,w_2,y)$ and $x^{\#}_2(w_1,w_2,y)$, and use them to recover the underlying production $y=f(x_1,x_2)$. What is the form of this technology?
		Solution: Smae as [[Microeconomics#Mid-term\|Midterm5]]
	b. Consider the production function: 
$$f(x_1,x_2,x_3,x_4)=\min\{2x_1,x_2\}+\min\{x_3,3x_4\}$$
	Find the conditional input ddemand function for each factor and the cost function for this technology
	==Perhapes I need to see exercise 5.11 on textbook== [[Microeconomics#Problem Set 2\|5-11]] ==But I still do not know==


## Quiz 3
Consider a monopolist that serves two separate market segments (e.g., two geographic markets or two distinct demographic groups) with demand curves given by $p_1=a_1-b_1q_1$ and $p_2=a_2-b_2q_2$, respectively. For tractability, we assume $b_1=b_2=b$, and $a_1>a_2$.
Compare the social surplus under price discrimination (DP) versus uniform pricing (UP). Under which scheme do we observe a higher total output (i.e., $q_1+q_2$)? How about prices in each market under the two different scenarios?
(本题可以拆封成下面三块)
How to find the optimal discriminatory prices and quantities?
	Solution:
	$p_1=a_1-b_1q_1\Rightarrow MR=a_1-2b_1q_1$ 
	Assume $MC=c$  
	$MR=MC\Rightarrow q^M_1=\frac{a_1-c}{2b}\Rightarrow p^M_1=\frac{a_1+c}{2}$
	Similarly, $q^M_2=\frac{a_2-c}{2b}\Rightarrow p^M_2=\frac{a_2+c}{2}$
How to find the optimal uniform price and quantities?
	Solution:
	Dynamic Pricing
	$p_i=a_i-bq_i\Rightarrow q_i=\alpha_i-\beta p_i$ where $\alpha_i=\frac{a_i}{b},\beta=\frac{1}{b}$
$$\max\ (p_1-c)q_1^{(p_1)}+(p_2-c)q_2^{(p_2)}$$
$$\begin{align}q_i=\alpha_i-\beta p_i\\ \frac{\partial \pi}{\partial p_1}=\alpha_1-\beta p_1-\beta p_1+\beta c=0\\ p_1=\frac{\alpha_1+\beta c}{2\beta} \end{align}$$
	Uniform Pricing
$$\max\ (\overline{p}-c)q_1(\overline{p})+(\overline{p}-c)q_2(\overline{p})$$
$$\begin{align}q_1=\alpha_1-\beta \overline{p}\\q_2=\alpha_2-\beta \overline{p} \\ \frac{\partial \pi}{\partial \overline{p}}=\alpha_1-\beta \overline{p}-\beta \overline{p}+\beta c+\alpha_2-\beta \overline{p}-\beta \overline{p}+\beta c=0\\ \overline{p}=\frac{\alpha_1+\alpha_2+2\beta c}{4\beta} \end{align}$$
	If all the curves are linear, then $\overline{p}=\frac{p_1+p_2}{2}$
	$q_1=\frac{3a_1-a_2-2c}{4b}$ and $q_2=\frac{3a_2-a_1-2c}{4b}$
Which scheme yields higher social surplus?
	Social surplus of unifrom price is greater than social surplus of dynammic price
	![Pasted image 20231117123317](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353614.png)
	Dynammic Pricing:
	surplus are two triangles and two rectangle
	social surplus$=\underbrace{\frac{1}{2}\times(a_1-\frac{a_1+c}{2})\times \frac{a_1-c}{2b}}_{consumer\ surplus\ of\ p_1}+\underbrace{(\frac{a_1+c}{2}-c)\times\frac{a_1+c}{2b}}_{producer\ surplus\ of\ p_1}+\underbrace{\frac{1}{2}\times(a_2-\frac{a_2+c}{2})\times \frac{a_2-c}{2b}}_{consumer\ surplus\ of\ p_2}+\underbrace{(\frac{a_2+c}{2}-c)\times \frac{a_2-c}{2b}}_{producer\ surplus\ of\ p_2}$
	$=\frac{3[(a_1-c)^2+(a_2-c)^2]}{8b}$
	Uniform Pricing:
	social surplus
	$=\frac{1}{2}\times (a_1-\frac{a_1+a_2+2c}{4})\times\frac{3a_1-a_2-2c}{4b}+\frac{1}{2}\times (a_2-\frac{a_1+a_2+2c}{4})\times\frac{3a_2-a_1-2c}{4b}+(\frac{a_1+a_2+2c}{4}-c)\times(\frac{3a_1-a_2-2c}{4b}+\frac{3a_2-a_1-2c}{4b})$
	$=\frac{(3a_1-a_2-2c)^2+(3a_2-a_1-2c)^2}{32b}+\frac{(a_1+a_2-2c)^2}{8b}$
	Social surplus of UP-Social surplus of DP= $\frac{2[(a_1-c)^2-(a_2-c)^2]^2}{32b}$
	$\because a_1>a_2$
	$\therefore [(a_1-c)^2-(a_2-c)^2]^2>0$
	$\therefore$ Social surplus of UP>Social surplus of DP

## Problem Set 4
due Nov 22nd
Chapter 14 Problems: 14.2, 14.3, 14.4, 14.6, 14.7, 14.10, 14.14*, 14.15, 14.19, 14.20* 
Chapter 17 Problems: 17.4, 17.6, 17.8, 17.11*

14.14* The monopolist can also be thought of as choosing the price and letting the market determine how much is sold. Write down the profit maximization problem and verify that $p[1 + 1/\varepsilon] = c'(y)$ at the optimal price.
	Solution:
	The monopolist's profit maximization problem with the demand function :
$$\max\limits_p\ pD(p)-C(D(p))$$
	Alternatively, with the inverse demand function $p(y)$:
$$\max_y\ p(y)y-C(y)$$
	FOC and SOC (for an interior optimum):
$$\begin{align}
p+p'(y)y=C'(y)\\
2p'+p''y-C''(y)\leq 0
\end{align}$$
	It follows from the FOC:
$$p[1+\frac{1}{\varepsilon_p}]=C'(y)$$
	where $\varepsilon_p=\frac{dy}{dp}\cdot \frac{p}{y}$ i.e., elasticity of demand

14.20*. A monopolist maximizes $p(x)x-c(x)$. In order to capture some of the monopoly profits, the government imposes a tax on revenue of an amount t so that the monopolist's objective function becomes $p(x)x - c(x) - tp(x)x$. Initially, the government keeps the revenue from this tax.
(a) Does this tax increase or decrease the monopolist's output?
	Solution:
	The first-order condition is $(1 − t)[p(x) + p ′ (x)x] = c ′ (x)$, or $p(x) + p ′ (x)x = c ′ (x)/(1 − t)$.
	This expression shows that the revenue tax is equivalent to an increase in the cost function, which can easily be shown to reduce output.
	11/30 ShiCe说要用 $\frac{dq}{dt}$ 得出结论 ==课后还得研究研究==
(b) Now government decides to award the revenue from this tax to the consumers of the monopolist's product. Each consumer will receive a "rebate" in the amount of the tax collected from his expenditures. The representative consumer who spends $px$ receives a rebate of $tpx$ from the government. Assuming quasilinear utility, derive an expression for the consumer's inverse demand as a function of $x$ and $t$.
	Solution:
	$u(x)+m-px+tpx$
	FOC:
	$u'(x)-(1-t)p=0$
	$p=\frac{u'(x)}{1-t}$
(c) How does the monopolist's output respond to the tax-rebate program
	Solution:
	Substituting the inverse demand function into the monopolist’s objective function, we have
	$(1-t)p(x)x-c(x)=(1-t)\frac{u'(x)}{1-t}x-c(x)=u'(x)x-c(x)$
	Since this is independent of the tax rate, the monopolist’s behavior is the same with or without the tax
==这题没懂==

17.4 There are two consumers A and B with the following utility functions and endowments:
$$\begin{align}
& u_A(x^1_A,x^2_B)=a\ln x^1_A+(1-a)\ln x^2_A\quad w_A=(0,1)\\
& u_B(x^1_B,x^2_B)=\min (x^1_B,x^2_B)\quad w_B=(1,0)
\end{align}$$
Calculate the market clearing prices and the equilibrium allocation.
	Solution:
	According to [[Microeconomics#Related Curve of Cobb-Douglas\|IndirectUtilityCobbDouglas]]
	In a form $u(x_1,x_2)=a\ln x_1+b\ln x_2$
	$x^1_A=\frac{am_1}{p_1}$
	$m_1=p_1\times 0+p_2\times 1=p_2$
	$\therefore x^1_A=\frac{ap_2}{p_1}$
	$x^2_A=\frac{am_1}{p_2}=a$
	According to $u_B(x^1_B,x^2_B)=\min (x^1_B,x^2_B)\quad w_B=(1,0)$
	$x^1_B=x^2_B$
	$p_1x^1_B+p_2x^2_B=p_1$
	$\therefore x^1_B=x^2_B=\frac{p_1}{p_1+p_2}$
	To find clearing prices:
	$x^1_A+x^1_B=1\Rightarrow \frac{ap_2}{p_1}+\frac{p_1}{p_1+p_2}=1$ (If you really need a answer, you can choose $p_1=1$)

17.6 We have two agents with indirect utility functions:
$$\begin{align}
v_1(p_1,p_2,y)=\ln y-a\ln p_1-(1-a)\ln p_2\\
v_2(p_1,p_2,y)=\ln y-b\ln p_1-(1-b)\ln p_2
\end{align}$$
and initial endowments
$$w_1=(1,1)\quad w_2=(1,1)$$
Calculate the market clearing prices.
	Solution:
	==问题在于这里demand为什么和Cobb-Douglas一样==
	[The Cobb-Douglas Utility Function本身就可以写成ln形式，甚至左边还可以写成u，无需加ln号](https://www.econgraphs.org/textbooks/intermediate_micro/scarcity_and_choice/preferences_and_utility/cobb_douglas.html#:~:text=The%20general%20form%20of%20a%20Cobb-Douglas%20function%20over,can%20be%20particularly%20useful%20when%20performing%20linear%20regressions.)
	According the Example in [Indirect utility function - Wikipedia](https://en.wikipedia.org/wiki/Indirect_utility_function#:~:text=The%20indirect%20utility%20function%20is%20the%20inverse%20of,Marshallian%20demand%20functions%20where%20is%20the%20consumer%27s%20income.) , the indirect utility of Cobb-Douglas is in a form of $v(p_1,p_2,w)=Kp^{-a}_1p^{-b}_1w$
	For instance, for $u(x_1,x_2)=x^{0.6}_1x^{0.4}_2$, its indirect utility $v(p_1,p_2,w)=(0.6^{0.6}\times 0.4^{0.4})w^{0.6+0.4}p^{-0.6}_1p^{-0.4}_2$
	When $v(p_1,p_2,w)=Kp^{-a}_1p^{-b}_1w$ take $\ln$ on both side, it looks like the indirect utility functions in this question
	Therefore, it is a Cobb-Douglas function
	$x^1_1=\frac{ay_1}{p_1},x_2=\frac{by_2}{p_1}$
	$y_1=y_2=p_1+p_2$
	Since $x^1_1+x^1_2=2$
	$\Rightarrow a+a\frac{p_2}{p_1}+b+b\frac{p_2}{p_1}=2$
	$\Rightarrow \frac{p_2}{p_1}=\frac{2}{a+b}-1$

17.11*. Person A has a utility function of $u_A (x_1, x_2) = x_1 + x_2$ and person B has a utility function $u_B(x_1,x_2)=\max(x_1,x_2)$. Agent A and agent B have identical endowments of $(1/2,1/2)$.
(a) Illustrate this situation in an Edgeworth box diagram.
	![Pasted image 20231124200411](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353615.png)
(b) What is the equilibrium relationship between $p_1$ and $p_2$?
	Solution: ==还没懂== 11/25推了一下，但还是晕的
	$u_A (x_1, x_2) = x_1 + x_2$
	$MRS=1=\frac{p_1}{p_2}$
	$p_1=p_2$
	TA: 考虑$p_1<p_2,p_1>p_2,p_1=p_3$
	When $p_1<p_2$, $x^A_1=\frac{\frac{1}{2}p_1+\frac{1}{2}p_2}{p_1}=\frac{1}{2}+\frac{1}{2}\frac{p_2}{p_1}$ 
(c) What is the equilibrium allocation?
	Solution:
	The equilibrium allocation must give one agent all of one good and the other agent all of the other good.
	![Pasted image 20231124203319](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353616.png)
	(两条utility线一开始切到还不是极限，B可以持续扩大直到达到上图的角点解)

Additional Exercises: 
E1. Newsprint (the paper used for newspapers) is produced in a perfectly competitive market. Each identical firm has a total variable cost $TVC(Q) = 40Q + 0.5Q^2$. A firm’s fixed cost is entirely nonsunk and equal to 50. 
a) Calculate the price below which the firm will not produce any output in the short run. 
b) Assume that there are 12 identical firms in this industry. Currently, the market demand for newsprint is $D(P) = 360 − 2P$, where D(P) is the quantity consumed in the market when the price is P. What is the short-run equilibrium price?

E2. Consider the markets for butter $(B)$ and margarine $(M)$, where the demand curves are $Q = 20 – 2P_M + P_B$ and $Q = 60 – 6P_B + 4 P_M$ and the supply curves are QM = 2PM and $Q_B = 3P_B$. 
a) Find the equilibrium prices and quantities for butter and margarine. 
b) Suppose that an increase in the price of vegetable oil shifts the supply curve of margarine to $Q_M = P_M$. How does this change affect the equilibrium prices and quantities for butter and margarine? Using words and graphs, explain why a shift in the supply curve for margarine would change the price of butter.

E3. Suppose that the demand for steel in Japan is given by the equation $Q^d_S = 1200 – 4P_S + P_A + P_T$, where $QS$ is the quantity of steel purchased (millions of tons per year), $PS$ is the price of steel (yen per ton), $PA$ is the price of aluminum (yen per ton), and $PT$ is the price of titanium (yen per ton). The supply curve for steel is given by $Q^S_S = 4P_S$. Similarly, the demand and supply curves for aluminum and for titanium are given by $Q^d_A = 1200 – 4P_A + P_S + P_T$ (demand curve for aluminum), $Q^S_A = 4P_A$ (supply curve for aluminum), $Q^d_T = 1200 – 4P_T + P_S + P_A$ (demand curve for titanium), and $Q^S_T = 4P_T$ (supply curve for aluminum). 
a) Find the equilibrium prices of steel, aluminum, and titanium in Japan. 
b) Suppose that a strike in the Japanese steel industry shifts the supply curve for steel to QSS = PS. What does this do to the prices of steel, aluminum, and titanium? 
c) Suppose that growth in the Japanese beer industry, a big buyer of aluminum cans, fuels an increase in the demand for aluminum so that the demand curve for aluminum becomes $Q^d_A = 1500 – 4P_A + P_S + P_T$. How does this affect the prices of steel, aluminum, and titanium?

E4*. Two consumers, Ron and David, together own 1,000 baseball cards and 5,000 Pokémon cards. Let $xR$ denote the quantity of baseball cards owned by Ron and $yR$ denote the quantity of Pokémon cards owned by Ron. Similarly, let $xD$ denote the quantity of baseball cards owned by David and $yD$ denote the quantity of Pokémon cards owned by David. Suppose, further, that for Ron, $MRS^R_{x,y} = yR/xR$, while for David, $MRS^D_{x,y} = yD/2xD$. Finally, suppose $xR = 800, yR = 800, xD = 200$, and $yD = 4,200$. 
a) Draw an Edgeworth box that shows the set of feasible allocations in this simple economy. 
	![Pasted image 20231124201158](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353617.png)
	
b) Show that the current allocation of cards is not economically efficient. 
	Solution:
	For economically efficient, $MRS^R$ should be equal to $MRS^D$
	However, $MRS^R_{x,y}=\frac{y^R}{x^R}=\frac{800}{800}=1$ $MRS^D_{x,y}=\frac{y^D}{2x^D}=\frac{4200}{400}=10.5$
	$MRS^R_{x,y}\neq MRS^D_{x,y}$ therefore this allocation is not economically efficient
c) Identify a trade of cards between David and Ron that makes both better off.
	Solution:
$$\left\{\begin{array}{**lr**} \frac{y^R}{x^R}=\frac{y^D}{2x^D}\\ x^R+x^D=1000\\ y^R+y^D=5000 \end{array}   \right.\Rightarrow \text{infinite allocations and exchange}$$
	One of the trades is David gives 10 pokemon cards to Ron, in exchange of one piece of baseball card from Ron. Therefore, both people will be better off.



## Pricing Strategies, Game Theory and Oligopoly Analysis
Types of Market Structure

| Degree of Product Differentiation |                     |                                     | Number of Firms |
| --------------------------------- | ------------------- | ----------------------------------- | --------------- |
|                                   | Many                | Few                                 | One             |
| Firms produce identical products  | Perfect Competition | Oligopoly with homogeneous products | Monopoly        |
| Firms produce different products    | Monopolistic Competition    |    Oligopoly with differentiated products   |   ------  |

There is no single model for oligipoly
- Bertrand model: identical or differentiated products;
- Cournot model: identical products; quantity competition 
- Stackelberg model: firms act sequentially

Single-agent decisions: e.g., classic consumer decision, firm decisions in
$\Rightarrow$ Optimization techniques (differentil calculus, etc.)
Interdependent/strategic decisions: e.g., oligopoly, conspicuous consumption (“show off”)
$\Rightarrow$ Game theory+optimization

Game Elements
Players: $I$; agents participating in the game (Toyota, Honda)
Strategies: $s_i\in S_i$; Actions that each player may take under any possible circumstance (Build, Don't build)
Outcomes: The various possible results of the game
Payoffs: $u_i(s_1,\dots,s_I)$; The benefit that each player gets from each possible outcome of the game (the profits entered in each cell of the matrix)

Information: A full specification of who knows what when (full information) 
Timing: Who can take what decision when and how often the game is repeated (simultaneous, one-shot) 
- We will focus on static, simultaneous-moce games with complete information

For a 2-player game with a finite number of actions and simultaneous moves, a payoff matrix can be used to represent the game.

Nash Equilibrium occurs when each player chooses a strategy that gives him/her the highest payoff, given the strategy chosen by the other player(s) in the game.
A strategy profile $s=(s_1,\dots,s_I)$ constitutes a Nash equilibrium of a game if for every $i=1,\dots,I$
$$u_i(s_i,s_{-i})\geq u_i(s'_{i},s_{-i})$$
for all $s'_i\in S_i$
($s_{-i}$ is a vector of strategies played by other player except $i$)

In a Nash equilibrium, no player could be better off by switching to a different strategy. 
A Nash equilibrium is a necessary condition if there is a unique predicted outcome to a game. 
There can be multiple Nash equilibria in a game

A **dominant strategy** is a strategy that is better than any other strategy that a player might choose, no matter what strategy the other player follows.
A strategy profile $s=(s_1,\dots,s_I)$ constitutes a Nash equilibrium of a game if for every $i=1,\dots,I$
$$u_i(s_i,s_{-i})> u_i(s'_{i},s_{-i})$$
for all $s'_i\in S_i$
- When a player has a dominant strategy, that strategy will be the player's Nash Equilibrium strategy

A player has a **dominated strategy** when the player has another strategy that gives it a higher payoff no matter what the other player does.
A strategy $s_i\in S_i$ is (strictly) dominated for player $i$ in a game if there exists another strategy $s'_i\in S_i$, such that for all $s_{-i}\in S_{-i}$
$$u_i(s'_i,s_{-i})>u_i(s_i,s_{-i})$$
- A strictly dominated strategy will not be a player's Nash equilibrium strategy.

Why look for dominant or dominated strategies? 
A dominant strategy equilibrium is particularly compelling as a "likely" outcome 
Similarly, because dominated strategies are unlikely to be played, these strategies can be eliminated from consideration in more complex games. This can make solving the game easier

### Bertrand Competition with Homogenous Product
$n$ Firms set price $p_i\in \mathbf{R}_{\geq 0}$, taking as given the price(s) $\mathbf{p}_{-i}$ set by other firm(s), to maximize profit,
$$\pi_i=(p_i-c)d_i(p_i,\mathbf{p}_{-i})$$
Homogeneous product
Simultaneous
Non-cooperative
Identical (constant) Marginal Costs: $c$

Given the formation,
$$d_i(p_i,\mathbf{p}_{-i})=\left\{\begin{array}{**lr**} D(p_i)\quad \text{if }p_i<\min\mathbf{p}_{-i}\\ \frac{D(p_i)}{N} \quad \text{if }p_i=\min\mathbf{p}_{-i}\\ 0\quad \text{if }\text{if }p_i>\min\mathbf{p}_{-i}\end{array}   \right.$$
$N$: number of "winning" firms

$\mathbf{p}^B=(p_1=c,\dots,p_n=c)$ (i.e., every firm sets $p_i=c$) is the unique Nash Equilibrium of this game
1. Why is it a Nash equilibrium? (Existence)
	Suppose all firms set $p_i=c$
	Consider an arbitrary firm $i$
	- If $p_i>c, \pi_i=0$ (not better off)
	- If $p_i<c,\pi_i<0$ (worse off)
	Indeed, $\mathbf{p^B}$ is a Nash equilibrium
2. Why is it the only Nash equilibrium? (Uniqueness)
	1. Indeed, for any firm, the strategy $p_i<c$ is (weakly) dominated by $p_i=c$;
	2. Given that other firms $p_{-i}>c$, one has incentive to set $p_i-\varepsilon\geq c$ $\Rightarrow$ there exist no Nash Equilibrium involving such strategies

“**Bertrand paradox**”: with homogenous products, if firms compete by choosing prices, they will optimally choose $p_i=c$; 
“Choosing prices” : market power; 
“$p_i=c$” : no market power. 
How can we revise the Bertrand model? 
- Quantity competition: Cournot 
- Bertrand with product differentiation 
- Sequential move (Stackelberg)

### Cournot Competition
Set-up
- Firms set outputs (quantities) 
- Homogeneous Products 
- Simultaneous move 
- Non-cooperative 
In a Cournot game, each firm sets its output (quantity) taking as given the output level of its competitor(s), so as to maximize profits. 
Price adjusts according to demand.

Given 
- an inverse demand function, p(Q)
- $Q=q_1+q_2$
- Identical constant marginal costs: $c$

Firm 1's profit maximization problem:
$$\max_{q_1} \pi_1=p(Q)q_1-cq$$
FOC implies:
$$p'q_1+p(Q)-c=0$$
When we solve for $q^c_1(q_2)$ , this is called a best-response function (in Cournot). 
The Nash equilibrium is the intersection of the best response functions.

Example: Linear Demand
Suppose
$$p(Q)=a-bQ\quad C(q_i)=cq_i$$
Find $q^c_1,q^c_2,p^c$, and the associated profits.
	Solution:
	$\max\limits_{q_1} \pi_1=p(Q)q_1-cq_1$
	$=(a-b(q_1+q_2)-c)q_1$
	$=aq_1-bq^2_1-bq_1q_2-cq_1$
	FOC:
	$a-2bq_1-bq_2-c=0$
	$q^c_1=\frac{a-c}{2b}-\frac{q_2}{2}$
	Same for firm 2
	$q^c_2=\frac{a-c}{2b}-\frac{q_1}{2}$
	Since $q^c_1=q^c_2$
	$q^c_1=q^c_2=\frac{a-c}{3b}$
	$Q^c=q^c_1+q^c_2=\frac{2(a-c)}{b}$
	$p^c=a-Q^cb=a-\frac{2}{3}(a-c)=\frac{1}{3}a+\frac{2}{3}c$
	![Pasted image 20231123191110](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353618.png)

In the linear case, is downward-sloping, indicating that quantity choices in a Cournot model with a linear demand are strategic substitutes; 
When is not “too convex,” quantity choices are strategic substitutes.
We study $\frac{dq^c_i}{dq_j}$ using ’s first-order condition.
$\frac{dq^c_i}{dq_j}=-\frac{p''q_1+p'}{SOC}$ $p''q_1+p'$ is negative, $SOC=p''q_1+2p'$ is negative
$SOC=p''q_1+2p'$
	1. $p''<0$ concave
	2. $p''>0, p''q_1+p'<0$ not too convex
==这一小块其实也不怎么懂==

### Stackelberg Competition
涉及到了先后顺序与双方博弈的模型
Backward induction: 
In stage 2, firm 2 (the follower) moves given $q^*_1$ :
$\max\limits_{q_2}\ \pi_2=P(Q)q_2-cq_2=(a-bq^*_1-bq_2)q_2-cq_2$
FOC (of firm 2)
$q_2=\frac{a-c}{2b}-\frac{q^*_1}{2}$

In stage 1, firm 1 (the leader) moves, anticipating 2’s strategy: $q_2=\frac{a-c}{2b}-\frac{q^*_1}{2}$
$\max\limits_{q_1}\ \pi_1=P(Q)q_1-cq_1=(a-bq^*_1-bq_2)q_1-cq_1$
FOC (of firm 1):
$q^s_1=\frac{a-c}{2b}$ 
	$a-2bq_1-b(\frac{a-c}{2b}-\frac{q_1}{2})q_1-c=0$
	$\Rightarrow a-2bq_1-\frac{a-c}{2}+bq_1-c=0$
	$\Rightarrow \frac{a-c}{2}-bq_1=0$
	$\Rightarrow q_1=\frac{a-c}{2b}$
(之前有疑惑，后来重新算了一遍，是对的$q_2(q_1)$也要拆开)
Plugging it back to firm 2’s reaction function:
$q^s_2=\frac{a-c}{4b}$

![Pasted image 20231130130248](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353619.png)


Given $P=a-bQ$

|                              | $Q$ | $P$ |
| ---------------------------- | --- | --- |
| Monopoly                     | $\frac{1}{2}\frac{a-c}{b}$    | $\frac{1}{2}a+\frac{1}{2}c$    |
| Cournot duopoly              | $\frac{2}{3}\frac{a-c}{b}$    |  $\frac{1}{3}a+\frac{2}{3}c$   |
| Cournout-Stackelberg duopoly |  $\frac{3}{4}\frac{a-c}{b}$   | $\frac{1}{4}a+\frac{3}{4}c$    |

### Bertrand Competition w/ Product Differentiation



## Quiz 4
The market demand curve in an industry is given by $P = a - bQ$. Any firm hasan identical marginal cost c per unit of output.
(a) Suppose that there is only one firm in the market, Find the monopoly quantity,price, and profit.
	Solution:
	$P = a - bQ\Rightarrow MR=a-2bQ$
	$MC=c$
	$MR=MC\Rightarrow q^m=\frac{a-c}{2b}\ p^m=\frac{a+c}{2}$ 
(b) Suppose that there are two firms competing by choosing levels of output. Find the Cournot equilibrium quantity for each firm. Find the market price and profit for each firm.
Solution:
	$\max\limits_{q_1} \pi_1=p(Q)q_1-cq_1$
	$=(a-b(q_1+q_2)-c)q_1$
	$=aq_1-bq^2_1-bq_1q_2-cq_1$
	FOC:
	$a-2bq_1-bq_2-c=0$
	$q^c_1=\frac{a-c}{2b}-\frac{q_2}{2}$
	Same for firm 2
	$q^c_2=\frac{a-c}{2b}-\frac{q_1}{2}$
	Since $q^c_1=q^c_2$
	$q^c_1=q^c_2=\frac{a-c}{3b}$
	$Q^c=q^c_1+q^c_2=\frac{2(a-c)}{3b}$
	$p^c=a-Q^cb=a-\frac{2}{3}(a-c)=\frac{1}{3}a+\frac{2}{3}c$
(C) Compare the total profits in (a) and (b). In which case would the consumers be better off?
	$\pi^m=p^mq^m-cq^m=(p^m-c)q^m=(\frac{a+b}{2}-c)\frac{a-b}{2}=\frac{a-b}{2}\frac{a-b}{2}=\frac{(a-b)^2}{4}$
	$\pi^c_1=(p^c-c)q^c_1=\frac{1}{3}(a-c)\frac{1}{3}\frac{a-c}{b}=\frac{(a-c)^2}{9b}$
	$\pi^{total}=\pi^c_1+\pi^c_2=\frac{2(a-c)^2}{9b}$ ($\pi^c_1=\pi^c_2$)
	$p^c-p^m=\frac{1}{6}(a-c)<0$ (since $q^m=\frac{a-c}{2b}$ $\Rightarrow a-c>0$) 
	In Oligipoly, consumers is better off
	Oligopoly 和Monopoly的区别
	![Pasted image 20231123192438](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353620.png)
	If there are N-firms
	$q^c_i=\frac{1}{N+1}\frac{a-c}{b}$
	$Q^c=Nq^c_i=\frac{N}{N+1}\frac{a-c}{b}$
	$p^c=\frac{1}{N+1}a+\frac{N}{N+1}c$
	$\frac{dp^c}{dN}=\frac{-a}{(N+1)^2}-\frac{-c}{(N+1)^2}=\frac{c-a}{(N+1)^2}<0$ (since $q^m=\frac{a-c}{2b}$ $\Rightarrow a-c>0$) 
	Therefore, the price will continue to decrease when we add more firms
(d) Now, assuming that Firm 1 is a Stackelberg leader, find the Stackelberg equilibrium quantities for each firm, Find the market price and profit for each firm
	Solution: [[Microeconomics#Stackelberg Competition\|#Stackelberg Competition]]
(e) Compare the total profit in (d) with (a) and (b). Are the consumers better off in case(d)?


## Problem Set 5
Chapter 15 Problems: 15.1, 15.3, 15.5*, 15.6, 15.8, 15.9* 
Chapter 16 Problems: 16.1, 16.3, 16.4*, 16.10*, 16.12

15.5. Consider the game matrix given here.

|     | Column |       |
| --- | ------ | ----- |
|     | Left   | Right |
| Top |   a,b     |   c,d    |
| Bottom    |  e,f      | g,h      |

(a) If (top, left) is a dominant strategy equilibrium, then what inequalities must hold among $a, . . . , h$? 
	Solution:
	$a\geq e\quad c\geq g\quad b\geq d\quad f\geq h$
(b) If (top, left) is a Nash equilibrium, then which of the above inequalities must be satisfied? 
	Solution:
	Only $a\geq e, b\geq d$
(c) If (top, left) is a dominant strategy equilibrium, must it be a Nash equilibrium?
	Yes

15.9. Consider the following coordination game

|     |     | Column    |     |
| --- | --- | --- | --- |
|     |     | Left    | Right    |
| Row    | Top    |  2,2   | -1,-1    |
|     | Bottom    |  -1,-1   | 1,1    |

(a) Calculate all the pure strategy equilibria of this game.
	Solution:
	(Top, Left) and (Bottom, Right) are both equilibria
(b) Do any of the pure strategy equilibria dominate any of the others?
	Solution:
	Yes. (Top, Left) dominates (Bottom, Right).
(c) Suppose that Row moves first and commits to either Top or Bottom. Are the strategies you described above still Nash equilibria?
	Yes
(d) What are the subgame perfect equilibria of this game?
	(Top,Left)

16.4. Using the linear demand functions in the previous problem, show that quantities are always lower and prices higher in Cournot competition than in Bertrand competition.
	Solution:
	[Price and Quantity Competition in a Differentiated Duopoly on JSTOR](https://www.jstor.org/stable/2555525) 这篇文章中有详细的计算
	```
	D:\AllDocument\Msc\Advanced Microeconomics\Current
	```
	In the Cournot case firm 1 chooses $q_1$ to maximize $(\alpha-\beta_1q_1-\gamma q_2)q_1$, taking as given $q_2$
	nd in the Bertrand case it chooses $p_1$ to maximize $p_1(a_1-b_1p_1-cp_2)$, taking $p_2$ as given.
	Both expressions are perfectly dual
	It is easily seen that the Cournot reaction of firm 1 to output $q_2$ is $(\alpha-\gamma q_2)/2\beta_1$,
	and correspondingly the Bertrand reaction to $p_2$ is $(a_1+cp_2)/2b_1$
	Let $\Delta=4\beta_1\beta_2-\gamma^2$ and $D=4b_1b_2-c^2$
Table 1: Equilibrium Levels of Price and Quantity

|     | Price | Quantity |
| --- | ----- | -------- |
|Bertrand     | $\frac{2a_1b_2+a_2c}{D}$      |   $b_1p^B_1$       |
|Cournot     | $\beta_1q^c_1$      |  $\frac{2\alpha_1\beta_2-\alpha_2\gamma}{\Delta}$        |
	
	$p^C_i-p^B_i=\frac{\alpha_i\gamma^2}{\Delta}\geq 0$
	$q^B_i-q^C_i=\frac{a_ic^2}{D}\geq0$
	Cournot competition is more "monopolistic" than Bertrand competition
	==增加了了解，但是还是没怎么懂，记得再看看==

16.10. Consider an industry with 2 firms, each having marginal costs equal to zero. The (inverse) demand curve facing this industry is
$$P(Y)=100-Y$$
where $Y=y_1+y_2$ is total output
(a) What is the competitive equilibrium level of industry output? 
	Solution:
	$MR=100-2y_1$
	$MC=0$
	$MR=MC\Rightarrow y_1=50$
	Similarly, $y_2=50$
	$Y=y_1+y_2=100$
(b) If each firm behaves as a Cournot competitor, what is firm 1's optimal choice given firm 2's output? 
	Solution:
	$\max\limits_{q_1} \pi_1=p(Q)q_1-cq_1$
	$=(100-(y_1+y_2))y_1$
	$=100y_1-y_1y_2-y^2_1$
	FOC:
	$-2y_1-y_2+100=0$
	Therefore, $y_1=50-\frac{y_2}{2}$
(c) Calculate the Cournot equilibrium amount of output for each firm. 
	Solution:
	Similarly, $y_2=50-\frac{y_1}{2}$
	$100-2y_1=50-\frac{y_1}{2}$
	$\Rightarrow y_1=\frac{100}{3}$
	==这个答案为什么是50== 看错了，下一题答案才是50
(d) Calculate the cartel amount of output for the industry. 
	Solution:
	Definition of Cartels
	If the firms were able to collude and act like a monopolist, they would jointly solve the following problem:
$$\max_{q_1,\cdots,q_n} \sum^n_{i=1} \pi_i=P(Q)Q-\sum^n_{i=1}C(q_i)$$
	In this case,
$$\max_{y_1,y_2}\ \pi_{tot}=P(y_1,y_2)(y_1+y_2)-c_1(y_1)-c_2(y_2)$$
	FOC.
$$\begin{align}
P(y_1,y_2)+P'(y_1,y_2)(y_1+y_2)-c'(y_1)=0\\
P(y_1,y_2)+P'(y_1,y_2)(y_1+y_2)-c'(y_2)=0
\end{align}$$
	Solve for $y_1$
	Given $P(Y)=100-Y=100-y_1-y_2,MC=0$
$$\begin{align}
(100-y_1-y_2)+(-1)(y_1+y_2)=0\\
100-y_1-y_2-y_1-y_2=0\\
y_1+y_2=50
\end{align}$$
	Cartel Amount $y_1+y_2=50\Rightarrow Y=50$
(e) If firm 1 behaves as a follower and firm 2 behaves as a leader, calculate the Stackelberg equilibrium output of each firm.
	Solution:
	Stakleberg equation output
	Stage 2: follower's move/reaction given leader's choice $y^*_1$
$$\max_{q_2}\ \pi_2=P(Y)y_2-c(y_2)$$
	Same as question (b)
$$y_2=\frac{100-y_1}{2}$$
	Substitute $y_2$ into Leader's $\pi$ max problem (anticipating by backward induction)
$$\begin{align}\max_{y_1}\ \pi_1&=P(Y)y_1-c(y_1)\\
&=(100-Y)y_1-c(y_1)\\
&=(100-y_1-(\frac{100-y_1}{2}))y_1-c(y_1)\\
&=(\frac{100-y_1}{2})y_1-c(y_1)
\end{align}$$
	FOC on $y_1$
	$50-y_1-c'(y_1)=0$
	$\because c'(y)=MC=0$
	$\therefore y_1=50$
	Plug $y_1$ into $y_2(y_1)=\frac{100-50}{2}=25$
	Therefroe, firm #1 (leeader) output $y_1=50$, firm #2 (follower) output $y_2=25$

Danniseの宿題
```
D:\AllDocument\Msc\Advanced Microeconomics\Dannise Hw Micro 16.10 (#4)
```
## Quiz 5
1. Consider a quasi-linear utility function, $U(x_1,x_2)=\sqrt{x_1}+x_2$, with $P_1$ and $P_2$ being the prices of $x_1$ and $x_2$, respectively. For an interior optimum, we have
$$x^*_1=\frac{1}{4}(\frac{P_2}{P_1})^2\text{, and }x^*_2=\frac{m}{P_2}-\frac{1}{4}\frac{P_2}{P_1}$$
When $P_1$ increases from $0.5 to $2, calculate the Compensating Variation (CV) and the Equivalent Variation (EV).

2. As shown in the following figure, a consumer buys two goods, food and housing, and like both goods. When she has budget line $BL1$, her optimal choice is basket $A$. Given budget line $BL2$, she choose basket $B$, and with $BL3$, she chooses basket $C$.
![Quiz 5](https://raw.githubusercontent.com/meteor0823/BlogImage/main/202312042353621.jpg)
On the graph, shade in (and clearly label) the areas that are revealed to be less preferred to baske $B$, and explain why you indicated these areas. Also shade in (and clearly label) the areas that are revealed to be (more) preferred to basket $B$, and explain why you indicated these areas.

## Final Exam

9:30-11:30 AM, Dec 15 in ELB LT4
Dec. 5th Tutorial No.6 (9-10 AM, ELB401)
Extra-credit assignment II: 0-5 points on your final exam, due December 23, 2022(To be posted)
Check your grades online

8:30-10:30 AM on Dec 12 (Tue)
1-4 pm on Dec 14 (Thu)

TA office hours:
Geng: 9-11 AM on Dec 14 (Thu)+regular hours

5-6 short-answer questions
can bring calculate

SheCe 下学期要Industry organization phd level
IO theory demand prediction


