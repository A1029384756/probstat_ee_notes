**Def:** A discrete random variable has $S = \{x_1,x_2,x_3,...\}$ where $X_i$'s are numbers.

**Ex:** (A/C Repair)
|#units|probability|
|---|---|
|2|.1|
|3|.2|
|4|.3|
|5|.4|

$S = \{2,3,4,5\}$

**Def:** The probability mass/distribution function is $p(x)=P(X=x)$

|$x$|$p(x)$|$F(x)$|
|---|---|---|
|2|.1|.1|
|3|.2|.3|
|4|.3|.6|
|5|.4|1|
||1||

Always, $\sum_{all x_i}p(x_i) = 1$
Notation, $\sum_{all X}p(X) = 1$

**Ex:** Let $X$ be the number of football games required to finally win the coin toss as the start. $S = X = \{1,2,..,8,9,...\}$
$P(X=1)=P(\text{win toss}) = 0.5 = p(1) = 0.5$
$P(X=2)=P(\text{lose then win}) = 0.5*0.5 = p(2) = 0.25$
$P(X=3)=P(\text{lose, lose, then win}) = 0.5*0.5*0.5 = p(3) = 0.125$
$P(X=x)=P(\text{L,L,...,W}) = 0.5^x = p(3)$

### Kolmagorov's Axiom
Let $B_1, B_2, B_3,...$ be events so that for $c \neq j, B_i \cap B_j = \varnothing$ (disjoint)
Let $A = B_1 \cup B_2 \cup B_3 \cup ...$, then $P(A) = P(B_1) + P(B_2) + P(B_3) + ... = \sum _{i=1}^\infty P(B_i)$ (countable additivity)

**Ex:** (Coin toss)
$P(\text{first win toss after an odd number of games}) = p(1) + p(3) + p(5) + ... + p(i)$

**Def:** The *cumulative distribution* function of $X$ is $F(x) = P(X \leq x)$

**Ex:** (A/C)
$P(\text{finish within 4 units}) = P(X = 2,3,4) = p(2)+ p(3) + p(4) = 0.1 + 0.2 + 0.3 = 0.6$
$F(4) = P(X \leq 0.4) = 0.6$

**Ex:** (Coin toss)
$P(\text{win the toss within 4 games}) = F(4)$
$F(x) = P(X \leq x) = 1 - P(X > x) = 1 - P(\text{lose first x tosses}) = 1 - 0.5^x$
$F(4) = 1- 0.5^4=0.9375$

$P(a < X \leq b)$ where $a$ and $b$ are constants?

**Ex:** $P(\text{takes more than 1 but no more than 4 games to win toss}) = P(1 < X \leq  4)$
