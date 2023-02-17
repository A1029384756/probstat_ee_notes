**Def:** The *conditional probability* of an event $B$ is *given* or *conditioned* based on event $A$ is $P(A|B)$.

> **Idea:** $A$ is known, $B$ is unknown

| |Prefer|Not|
|----|----|----|
|Mac|18|32|
|Windows|94|56|

$P(\text{Prefer | Mac}) = \frac{18}{50}= \frac{ \frac{18}{200}}{ \frac{50}{200}} = \frac{P(\text{Prefer and Mac})}{P(\text{Mac})}= \frac{0.09}{0.25}=0.36$

> Generally $P(B|A) = \frac{P(A \cap B)}{P(A)}$ where $A$ is known and $B$ is not.

**Ex:** Bird watching, $P(\text{eagle})=0.24$ and $P(\text{bald eagle})=0.06$ based on experience
Your friend says "Look an eagle!" What is the probability that it is a bald eagle.

$P(\text{bald | eagle}) = \frac{P(\text{bald eagle})}{P(\text{eagle})} = \frac{0.06}{0.24}=0.25$

Solve $P(A \cap B) = P(A)P(B|A)$ -> Sequential Probability
$P(A \cap B \cap C) = P(A)P(B \cap C|A) = P(A)P(B|A)P(C|A \cap B)$

Most information is irrelevant for the problem you are studying.
**Def:** If $P(B|A)=P(B)$ we say $B$ is independent of $A$.

Let $B$ be independent of $A$:
$P(A \cap B) = P(A)P(B|A)=P(A)P(B)$

**Ex:** Random password. Gives random password string of $4$ letters.
$P(\text{all vowels})$
$P(\text{first vowel} \cap \text{second vowel} \cap \text{third vowel} \cap \text{fourth vowel}) = P(1st)P(2nd|1st)P(3rd|2nd\cap first)P(4th | 1st \cap 2nd \cap 3rd)$
These are independent of one another however => $P(1st)P(2nd)P(3rd)P(4th)=(\frac{5}{26})^4=0.00137$

### Bayes Theorem
$P(E|F) = \frac{P(E)P(F|E)}{P(F)}$
but, $P(A) = \sum_{i=1}^nP(B_i)P(A|B_i)$
