**Def:** Variance --> measure of uncertainty in $X$

> $E(x)=\mu$

$X-\mu$ is the *deviation*
$(X-\mu)^2$ is the *squared deviation*

$Var(X) = E((X - \mu)^2)$ <- see [[Expectation]]

**Def:** Let $g(x)$ be any function of a random variable. Then its [[Expectation|expectation]] $E(g(x)) = \sum_{\text{all } x} g(x)p(x)$

For $X$ discrete, $Var(x)  E((x-\mu)^2)=\sum_{\text{all } x} (x-\mu)^2p(x)$

**Ex:** (Door prize)
$X = \{1,5,10,20\}$
$p(x)=\frac{1}{4}$
$E(x)=\frac{1}{4}(1 + 5 + 10 + 20) = 9 = \mu$
$Var(x) = \frac{1}{4}[(1-9)^2+(5-9)^2+(10-9)^2+(20-9)^2] = \frac{202}{4}=50.5$

**Ex:** (A/C)
|$x$|$p(x)$|$x-\mu$|$(x-\mu)^2$|$(x-\mu)^2p(x)$|
|---|---|---|---|---|
|2|0.1|-2|4|0.4|
|3|0.2|-1|1|0.2|
|4|0.3|0|0|0|
|5|0.4|1|1|0.4|

> What *does* $Var(x)$ mean?
> Why is it hard to assign a meaning?
> 	The **units** are difficult --> *squared* units

**Def:** The *standard deviation* of a random variable $X$ is $\sigma = \sqrt{Var(x)}$

**Ex:** (Door prize)
$Var(x) = 50.5 (\text{dollars})^2$
$\sigma = \sqrt{50.5} \approx 7.1$

> $\sigma$ is the *typical* deviation from average

### Simpler Variance Calculations
$Var(x) = E((x-\mu)^2) = E(x^2 - 2\mu x + \mu^2)$
$=E(x^2)+E(-2\mu x) + E(\mu^2)$
$=E(x)^2-2\mu E(x)+\mu^2$
$=E(x^2)-2\mu^2 + \mu^2$
$=E(x^2)-\mu^2$
Since $(x-\mu)^2 \geq 0$, $Var(x) \geq 0$
Thus, $E(x)^2 \leq E(x^2)$
