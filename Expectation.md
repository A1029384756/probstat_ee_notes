Does $X$ have a *typical value*?

**Ex:** (A/C) Career of $1000$ repair calls, what per/call average number of units are worked on?

|$x$|$p(x)$|
|---|---|
|2|.1|
|3|.2|
|4|.3|
|5|.4|

This is equal to: $\frac{2*100 + 3*200+4*300+5*400}{1000} = \frac{4000}{1000}=4.0$

>This can be written as $2*p(2)+3*p(3)+4*p(4)+5*p(5)$

**Def:** Let $X$ be a discrete, random variable. Then its *expectation* is: $E(X) = \sum_{\text{all } X}Xp(X)$

**Case:** Let $X$ be a Geometric ($p$) random variable (i.e. a coin toss or lottery ticket).
On *average*, how many trials will we need to find a success?
$E(X) = \sum_{\text{all } X}Xp(X) = \sum_{X=1}^\infty X*(1-p)^{X-1}*p$ <- infinite series (not strictly geometric)

$E(X)= \frac{p}{1-p}[1+(1-p)+(1-p)^2+(1-p)^3+...]$
$=\frac{p}{p}[\frac{1}{1-(1-p)}]=\frac{1}{p}=E(x)$

**Ex:** Coin toss, $p=0.5$, $E(x)=\frac{1}{0.5}=2.0$ games
**Ex:** Lottery ticket, $p=0.2$, $E(x)=\frac{1}{0.2}=5.0$ tickets

> This *only* works when using a *geometric random variable*

How typical of a value of $X$ is $E(X)$. How much random variation of $X$ from $E(X)$ will we see?

Summary measure of uncertainty in $X$. -> **Variance**

> An often rewriting of $E(X)$ is $E(X) = \mu$

Deviation of an outcome will be $X - \mu$
Typical *size* of the deviation.
To get the size, use the *squared deviation* => $(X - \mu)^2$

**Def:** The *variance* of a random variable $X$ is (Let $\mu = E(X)$)
$Var(X) = E((X-\mu)^2)$

**Ex:** Meeting has a door prize.  Prize consists of reaching into a box with $1, $5, $10, and $20.
$X = \{1,5,10,20\}$
$p(x)=0.25$ => $E(x) = 0.25*1+0.25*5+0.25*10+0.25*20$ => $9 = $\mu$

$Var(x)=\frac{(1-9)^2+(5-9)^2+(10-9)^2+(20-9)^2}{4}=\frac{202}{4}=50.5$


Let $X=\{0,1,2,3,...\}$ (a *count* variable).
Tail probability method:
$E(X)=\sum_{y=0}^\infty P(X >y) = \sum_{y=0}^\infty 1-F(y)$

**Ex:** (A/C)
|$x$|$p(x)$|$F(x)$|$1-F(x)$|
|---|---|---|---|
|0|0|0|0|1|
|1|0|0|0|1|
|2|0.1|0.1|0.9|
|3|0.2|0.3|0.7|
|4|0.3|0.6|0.4|
|5|0.4|1.0|0.0|
|6|0|1.0|0.0|
|7|0|1.0|0.0|
