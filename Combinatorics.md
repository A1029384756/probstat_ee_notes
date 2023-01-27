### Staging Rule
- If an outcome is determined in two stages, with $n$ possibilities for stage $1$ and $m$ possibilities for stage $2$,  $\text{outcomes} = n*m$.
- **Ex:** Buy a car. 
	- Colors: yellow, red, and blue.
	- Displacement: 1.7, 2.2, 2.8, 3.5 liters
	- How many cars?
	*# Cars* = $3 \text{rows} * 4 \text{columns} = 12 \text{cars}$

### Ordered lists with replacement
- $k$ elements in list, $n$ free choices for each element
- Counting number of lists
	- $\text{num lists} = n * n * ... * n = n^k$
	- Equal 1st elem, times 2nd elem, to the $k$ elem
- **Ex:** Computer "words" which are strings of 16 bits.
	- How many possible words?
	- $n = 2, k = 16$
	- $\text{num words} = 2^{16} = 65,536$
- **Ex:** Random passwords.
	- $4$ random letters
	- $\text{num possible passwords} = 26^4 = 456,976$
	- $n =26$
	- $k = 4$
	- What is the *probability* that the password app will give a string of *all* vowels?
	- $P(\text{all vowels}) = \frac{5^4}{26^4} = 0.00137$
- **Ex:** # of Virginia license plates (3 letters and 4 digits)
	- $\text{plates} = 26 * 26* 26 * 10 * 10 * 10 * 10$ <- 1st letter times 2nd letter times 3rd letter times first digit times second digit and so on (likelihood of each)
	- $175,760,000$ plates


### Ordered lists without replacement
- Lists of $k$ elements with $n$ possibilities for each element but with *no duplications*.
- $= n * (n-1) * (n-2) * ... * (n-k+1)$
- **Permutations** of $n$ things takes $k$ at a time
* Order *does* matter
- **Ex:** Industrial fair.
	- Contest at said fair for the best new products.
	- Results: Gold, Silver, Bronze medals
	- Companies enter $12$ new products.
	- Calculate the number of possible award announcements:
		- Gold medal possibilities = $12$
		- Silver medal possibilities = $11$
		- Bronze medal possibilities = $10$
		- $\text{num announcements} = 12 * 11 * 10 = 1320$
- **Notation:** $n^{(k)}$ -> Parentheses indicate permutation
- **Notation:** $_nP_k$ -> Used in textbook
- **Notation:** $P_{(n, k)}$ -> Used by calculators
- "$n$ permute $k$"

### Complete lists without replacement
- List of $n$ elements where all permutations must be found
- $n^{(n)}=n!=n^{(k)}*(n-k)!$
- Thus, $n^{(k)}=\frac{n!}{(n-k)!}$
- **Ex:** After awards, judges rank the runner's up.
- All possible rankings = $12!$
- Before lunch, medals are awarded and after lunch, runner's up are ranked
- Before much medals -> $12^{(3)}$
- After lunch medals -> $9!$
- Total permutations = $12^{(3)} * 9!$

### Ordered sets of $k$ things chosen without replacement from $n$ possibilities
- *Combinations* of $n$ things taken $k$ at a time
- Order *does not* matter
- **Notations:**
	- $({n \atop k})$
	- $_nC_k$
	- $C_{(n, k)}$
 - 12 products in a contest, judges assign Gold, Silver, and Bronze medals.
	Stage 1 -> Before lunch, judges choose 3 finalists
	Stage 2 -> After lunch, the 3 are given Gold, Silver, and Bronze medals
	 -  $12^{(3)} = ({12 \atop 3})*3!$ <- No order
	 - $({12 \atop 3}) = \frac{12^{(3)}}{3!}=220$
 - Generally, $({n \atop k}) = \frac{n^{(k)}}{k!}$
 - **Ex:** There were 14 defective chips. In how many ways can I end up with three of them?
	 - $({14 \atop 3}) = \frac{14^{(3)}}{3!}=364$
 - $({n \atop k})=\frac{n^{(k)}}{k!}=\frac{n!}{k!(n-k)!} = \frac{n^{(n-k)}}{(n-k)!}$
 - **Ex:** $25$ chem labs on campus.
	 - Money in budget to replace the showers in 19 labs.
	 - In how many ways can we pick the labs to get the new showers?
	 - $({25 \atop 19}) = \frac{25^{(19)}}{19!} = \frac{25^{(6)}}{6!}$
 - "$n$ choose $k$"

### Applications of Combinatorics
**Ex:** New office building with $80$ very nice office. $15$ VIP's want a new office.
- **Procedure:** Send a map of building to $15$ people and have each e-mail their choice of office.
- What happens if $2$ people choose the same office?
- $P(\text{there are office conflcts})$ <- hard problem 
- $P(\text{no office conflicts}) = \frac{80^{(15)}}{80^{15}} = 0.247$
**Ex:** R&D Department. 9 proposals for new products to be investigated.
- **Budget:** We can fund 3 of those proposals with high priority, 4 other proposals with medium priority, and the rest (2) with low priority.
- **Stage 1:** Who gets high priority => num ways = $({9 \atop 3})$
- **Stage 2:** Who gets medium priority => num ways = $({6 \atop 4})$
- Rest get low priority
- $\text{num assignments } = ({9 \atop 3})*({6 \atop 4}) = 1260$
- $\text{num assignments } = \frac{9!}{3!6!}*\frac{6!}{4!2!}=\frac{9!}{3!4!2!}$

### Multinomial Counting
- $n$ things are each assigned to one of categories $1,2,3,...,k$. Done in such a way that $n_1$ are in category $1$, $n_2$ are in category $2$,..., and $n_k$ in category $k$.
- $\text{num assignments } = ({n \atop n_1})*({{n-n_1} \atop n_2})*({{n-n_1-n_2} \atop n_3})...=\frac{n!}{n_1!n2!n3!...n_k!}$ => Multinomial count
- **Notation:** $\text{num assignments } = ({n \atop {n_1n_2n_3...n_k}})$ <- kind of stupid
- **Fact:** What if $k=2$?
	- $\frac{n!}{n_1!(n-n_1)!} = ({n \atop n_1}) = ({n \atop n_2})$

### Hypergeometric Probability
$N = \text{ population}$
$R = \text{ num of objects in population that are distinguished}$
$n = \text{ sample size, num of objects in population chosen}$

**Ex:**  Box of $100$ chips, $14$ defective, pick $20$ chips at random,
- $P(\text{3 defective, 17 good}) = \frac{({14 \atop 3})*({86 \atop 17})}{({100 \atop 20})}=0.270$
- $N = 100$
- $R = 14$
- $n = 20$
- $x = 3$

$P(\text{x distinguished objects in sample}) = \frac{({k \atop x})*({{N-k} \atop {n-x}})}{({N \atop n})}$