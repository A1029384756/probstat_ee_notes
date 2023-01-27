Events $A$
$P(A)=\text{probability of outcome in A}$
$A$ is a [[Sets|set]] (collection)

1. $P(S) = 1$
2. Let $A$ be any event. $P(A) \geq 0$ (if you get negative values, you done goofed)
3. The probability for any events $A,B$ → $P(A \cup B) = P(A) + P(B)$ ← Order is commutative
  - **Ex:** $P(\text{rain or snow tomorrow})$ -> $P(\text{rain})=0.2, P(\text{snow but no rain})=0.1$,P(\text{rain or snow}=P(\text{rain})+P(\text{snow}-\text{rain})=0.2+0.1+0.3$


### Consequences of these Rules
**Def:** If $A \cap B = \varnothing$ such that $A$ and $B$ have no outcomes in common, we say that $A$ and $B$ are *disjoint* or *mutually exclusive*.
**Ex:** In $5$ card poker hands, $A = \text{3 of a kind}$, $B = \text{straight}$ <- Cannot have both

> As a result $B = B-A$
> So, $P(A \cup B) = P(A) + P(B-A)$ <- using rule 3.
> Since $A$ and $B$ are mutually exclusive, this is also equal to $P(A) + P(B)$

**Ex:** $P(\text{fuse does not work})$
- Possibilities
  1. Fuse burned out
  2. Fuse has a short
- $P(\text{fuse burned out}) = 0.02$
- $P(\text{short}) = 0.01$
- $P(\text{does not work}) = P(\text{fuse burned out} + P(\text{short}= 0.03$

> Remember $A \cap A' = \varnothing$
> $A, A'$ are disjoint
> $A \cup A' =$ [[Sets#Special Sets|S]]
> $P(S) = P(A \cup A') = P(A)+P(A')
> $P(A') = 1-P(A)$
> This is known as the **Law of Complements**

**Ex:** New office building -> $P(\text{no office conflicts}) = 0.247$
- $P(\text{there are no office conflicts})$ is disjoint with the problem
- $P(\text{conflicts})=1-0.247=0.753$

> Since $P(A)+P(A')=1$, then P(A)=1-P(A')
> By rule $2$, $P(A') \geq 0$, thus, $P(A) \leq 1$

For **any** event $A$, $0 \leq P(A) \leq 1$.

Let $B_1,B_2,B_3,...,B_k$ be a collection of events so that any $i \neq j$, $B_i \cap B_j = \varnothing$. (All sets are mutually exclusive)
Thus, $P(B_1 \cup B_2 \cup B_3 \cup ... \cup B_k) = P(B_1) + P(B_2) + P(B_3) + ... + P(B_k) = \sum_{i=1}^{k} P(B_i)$
