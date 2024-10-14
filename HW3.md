# 1: Problem 2, Page 64
* $n = 4$ is the number of fair coin tosses
* Note: Probability of head is equal to probability of tail

### a: $X$ represents number of heads before the first tail
* $p_X(0) = .5$
* $p_X(1) = .5 * .5$
* $p_X(k) = .5 ^ {k + 1}$
  * Note: $k \in [0, 3]$
* $F_X(k) = \sum_{i\in [0, k]} p_X(i)$
* $F_X(k) = \sum_{i\in [0, k]} .5 ^ {i + 1}$
* $F_X(k) = .5 \sum_{i\in [0, k]} .5 ^ {i}$
* $F_X(k) = .5 * \frac{1 - .5^{k + 1}}{1 - .5}$
* $F_X(k) = .5 * \frac{1 - .5^{k + 1}}{.5}$
* $F_X(k) = 1 - .5^{k + 1}$

### b: $Y$ represents number of heads following the first tail
* $p_Y(0) = p_X(0) * .5^3 + p_X(1) * .5^2 + p_X(2) * .5 + p_X(3)$
* $p_Y(1) = p_X(0) * .5^3 + p_X(1) * .5^2 + p_X(2) * .5 + p_X(3)$
* $p_Y(k) = \sum_{i \in [0, 3]} p_X(i) * .5^{3 - i}$
* $p_Y(k) = \sum_{i \in [0, 3]} .5 ^ {i + 1} * .5^{3 - i}$
* $p_Y(k) = \sum_{i \in [0, 3]} .5 ^ 4$
* $p_Y(k) = .5 ^ 4 \sum_{i \in [0, 3]} 1$
* $p_Y(k) = 4 * .5 ^ 4$
  * Note: $k \in [0, 3]$
* $p_Y(k) = .25$
* $F_Y(k) = .25k$

### c: $Z$ represents number of heads minus number of tails
* Note: $k \in [-4, 4]$
* $p_Z(-4) = \binom{4}{0, 4} * .5^4$
* $p_Z(-3) = 0$
* $p_Z(-2) = \binom{4}{1, 3} * .5^4$
* $p_Z(-1) = 0$
* $p_Z(0) = \binom{4}{2, 2} * .5^4$
* $p_Z(1) = 0$
* $p_Z(2) = \binom{4}{3, 1} * .5^4$
* $p_Z(3) = 0$
* $p_Z(4) = \binom{4}{4, 0} * .5^4$
* TODO: ?? how are we supposed to make this into an actual function?
  * Need pdf and cdf functions

### d: $W$ represents the number of tails times the number of heads
* Note: $k \in [0, 4]$
* $p_W(0) = [\binom{4}{4, 0} + \binom{4}{0, 4}] * .5^4$
* $p_W(1) = 0$
* $p_W(2) = 0$
* $p_W(3) = [\binom{4}{3, 1} + \binom{4}{1, 3}] * .5^4$
* $p_W(4) = \binom{4}{2, 2} * .5^4$
* TODO: ?? how are we supposed to make this into an actual function?
  * Need pdf and cdf functions

# 2: Problem 14, Page 65
* $X$ represents total number of attempts
* $p_X(1) = p_1$
* $p_X(2) = (1-p_1)p_2$
* $p_X(3) = (1-p_1)(1-p_2)p_1$
* $p_X(4) = (1-p_1)^2(1-p_2)p_2$
* $p_X(5) = (1-p_1)^2(1-p_2)^2p_1$
* $p_X(k) = (1-p_1)^{\lfloor \frac{k}{2} \rfloor}(1-p_2)^{\lfloor \frac{k - 1}{2} \rfloor}p_1^{k \% 2}p_2^{(k + 1) \% 2}$
  * Note: $k \in \mathbb{Z}, k \geq 1$
  * Note: $\%$ represends the 'mod' operators
* Let $Y$ = { $p_1$ winning }
* $P(Y) = \sum _{i \in \{i \in \mathbb{N}: i \% 2 = 1 \}} p_X(i)$
  * TODO: ?? How do I simplify this? 

# 3: Problem 18, Page 65
??

# 4: Problem 24, Page 66
??

# 5: Problem 26, Page 66
??

# 6
### Q: Suppose a certain disease is twice as likely to develop when someone smokes as compared to when they do not smoke. If 32 percent of people are smokers, what percentage of people having the disease are smokers?
* Let $p$ be the probability someone develops disease when not smoking
* Let $X$ = { smoker }, $Y$ = { develop disease }
* $P(Y|X) = 2p$ and $P(Y|X^c) = p$
* $P(X) = .32$ and $P(X^c) = .68$
* $P(Y) =\ ?$
* $P(Y) = P(Y|X)P(X) + P(Y|X^c)P(X^c)$
  $\\ \to P(Y) = 2p * .32 + p * .68$
  $\\ \to P(Y) = 1.32p$
* $P(X|Y) =\ ?$
  $\\ \to P(X|Y) = \frac{P(Y|X)P(X)}{P(Y)}$
  $\\ \to P(X|Y) = \frac{2p * .32}{1.32p}$
  $\\ \to P(X|Y) = \frac{2p * .32}{1.32p}$
  $\\ \to P(X|Y) = \frac{16}{33}p$

# 7
### Q: Three cooks labeled A, B, and C can each bake a special cake, but with different levels of skill, and sometimes they fail to successfully bake the cake. When the cooks try to bake the cake, the failure probabilities are respectively 0.02, 0.03, 0.05. In the restaurant where they work, A bakes this cake 50% of the time, B bakes it 30% of the time, and C bakes it 20% of the time. What proportion of the failures are caused by A?
??