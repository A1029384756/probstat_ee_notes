Let $X = \{0,1,2,3,...\}$ <-- counting variable
$\pi_x(q)=E(q^x)=\sum_{x=0}^\infty q^xp(x)$

Applications:
1. Quality control (post-testing)
2. $E(x) = \pi'_x(q=1)$
	1. $\pi''_x(q)= [\pi'_x(q)]'$
	2. $[E(xq^{x-1})]' = E[(xq^{x-1})']$
	3. $E(x(x-1)q^{x-2})$

$\pi_x(q) = \frac{pq}{1-q(1-p)}$
$\pi'_x(q) = \frac{p}{(1-1(1-p))^2}$
$\pi''_x(q) = \frac{2p(1-p)}{(1-q(1-p))^3}$
$var(x) = \frac{1-p}{p^2}$
