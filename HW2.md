# 1 - Problem 18, Page 28
We sample $m$ items randomly without replacement.

Let $A$ = {at least one item in $m$ is defective}.

$P(A) = .9$

We want to find $m$

This is like the birthday problem. It's easier to find the complement.

Let $A^c$ = {no items in $m$ are defective}. 

$P(A^c) = 1 - P(A) = .1$

Let $j \in [0, m)$ be the $j$th item we sample.

$P(A^c) = \Pi _j \frac{n - k - j}{n - j} = \frac{\frac{(n - k)!}{(n - k - m)!}}{\frac{n!}{(n - m)!}}$

$P(A^c) = \frac{(n-k)!(n-m)!}{(n-k-m)!n!}$

$P(A^c) = \frac{(n-k)!(n-m)!}{(n-k-m)!n!}$

$P(A^c) = \frac{(n-k)!}{n!} \frac{(n-m)!}{(n-k-m)!}$

$P(A^c) = \frac{1}{n(n-1)...(n-k+1)} \frac{(n-m)(n-m-1)...(n-m-k+1)}{1}$

$P(A^c) = \frac{(n-m)(n-m-1)...(n-m-k+1)}{n(n-1)...(n-k+1)}$

When applying the hint:

$P(A^c) = (\frac{n-m}{n})^k = .1$

Now we can solve for $m$:

$\frac{n-m}{n} = .1^\frac{1}{k}$

$n - m = .1^\frac{1}{k}n$

$-n + m = - .1^\frac{1}{k}n$

$m = n - .1^\frac{1}{k}n$

## a: let $n = 1000,k=10$
$m = 1000 - .1^\frac{1}{10}*1000 = 206$ samples

## b: let $n = 10000,k=100$
$m = 10000 - .1^\frac{1}{100}*10000 = 228$ samples

# 2 - Problem 46, Page 30
Let $X$ = {a red ball is drawn}

Let $A$ = {drawn from Urn A}, $B$ = {drawn from Urn B}

$P(A) = P(B) = .5$

## a: $P(X) =\ ?$
$P(X|A) = \frac{3}{3+2} = .6$

$P(X|B) = \frac{2}{2+5} = \frac{2}{7}$

$P(X) = P(X|A)P(A) + P(X|B)P(B)$

$P(X) = .6*.5+\frac{2}{7}*.5 = .44$

## b: $P(A|X) =\ ?$
Bayes rule: $P(A|X)P(X) = P(X|A)P(A)$

$P(A|X) = \frac{P(X|A)P(A)}{P(X)}$

$P(A|X) = \frac{.6*.5}{.44} = .68$

# 3 - Problem 54, Page 31
Let $0$ represent today.

## a: $P(R_{1})=\ ?$
$P(R_0) = p, P(R_0^c) = 1 - p$

$P(R_1) = P(R_1|R_0)P(R_0) + P(R_{1}|R_0^c)P(R_0^c)$

$P(R_{1}|R_0) = \alpha, P(R_{1}^c|R_0) = 1 - \alpha$

$P(R_{1}^c|R_0^c) = \beta, P(R_{1}|R_0^c) = 1 - \beta$

$P(R_{1}) = \alpha p + (1 - \beta) (1 - p)$

$P(R_{1}) = \alpha p + (1 - p) - \beta (1 - p)$

$P(R_{1}) = \alpha p + 1 - p - \beta + \beta p$

$P(R_{1}) = (1 - \beta) + (\alpha + \beta - 1) p$

## b: $P(R_{2})=\ ?$
From c:

$x_2 = b + ab + a^2p$

$P(R_2) = 1 - \beta + (1 - \beta)(\alpha + \beta - 1) + (\alpha + \beta - 1)^2p$

## c: $P(R_n)=\ ?$
From a:

$P(R_n) = (1 - \beta) + (\alpha + \beta - 1) P(R_{n-1})$

Let $x_i = P(R_i), x_0 = p$

This looks in the form of $x_n = b + ax_{n - 1}$

Where $b = 1 - \beta, a = \alpha + \beta - 1$

$x_1 = b + ap$

$x_2 = b + a(b + ap) = b + ab + a^2p$

$x_3 = b + a(b + ab + a^2p) = b + ab + a^2b + a^3p$

$x_4 = b + a(b + ab + a^2b + a^3p) = b + ab + a^2b + a^3b + a^4p$

$x_n = \Sigma _{j=0}^{n - 1} a^jb + a^np$

$x_n = b\Sigma _{j=0}^{n - 1} a^j + a^np$

Let's solve the summation first:

$\Sigma _{j=0}^{n - 1} a^j = \frac{1-a^n}{1-a}$

Now plug in:

$P(R_n) = b\frac{1-a^n}{1-a} + a^np$

where $b = 1 - \beta, a = \alpha + \beta - 1$

If $a > 1$:

$P(R_\infty) = \frac{-\infty}{-C} + \infty$

$P(R_\infty) = \infty$

If $a < 1$:

$P(R_\infty) = b\frac{1}{1-a}$

# 4: Problem 60, Page 36
Let $A$ = {item produced in first shift}

Let $B$ = {item produced in second shift}

Let $C$ = {item produced in third shift}

Since all shifts had equal productivity:

$P(A) = P(B) = P(C) = \frac{1}{3}$

Let $D$ = {item defective}

$P(D|A) = .01$

$P(D|B) = .02$

$P(D|C) = .05$

$P(D) = P(D|A)P(A) + P(D|B)P(B) + P(D|C)P(C)$

$P(D) = .01*\frac{1}{3} + .02*\frac{1}{3} + .05*\frac{1}{3} = \frac{2}{75}$

$P(C|D) =\ ?$

$P(C|D) = \frac{P(D|C)P(C)}{P(D)}$

$P(C|D) = \frac{.05*\frac{1}{3}}{\frac{2}{75}} = \frac{5}{8}$

# 5: Problem 74, Page 33
Let's say the circuit looks like this:

xx--1--2--xx

--|---3---|--

xx--4--5--xx

Let:

$A$ = {Node 1 fails}

$B$ = {Node 2 fails}

$C$ = {Node 3 fails}

$D$ = {Node 4 fails}

$E$ = {Node 5 fails}

$P(A) = P(B) = P(C) = P(D) = P(E) = p$

Let $U$ = {Upper fails}

$U = A \cup B$

$P(U) = P(A) + P(B) - P(A\cap B)$

$P(A\cap B) = P(A) * P(B) = p^2$

$P(U) = 2p - p^2$

Let $M$ = {Middle fails}

$P(M) = P(C) = p$

Let $L$ = {Lower fails}

$P(L) = P(D) + P(E) - P(D\cap E)$

$P(D\cap E) = P(D) * P(E) = p^2$

$P(L) = 2p - p^2$

Let $F$ = {Circuit fails}

$F = U \cap M \cap L$

$P(F) = P(U) * P(M) * P(L)$

$F = (2p - p^2)^2p$

Let $W = F^c$ = {Circuit works}

$P(W) = 1 - P(F)$

$P(W) = 1 - (2p - p^2)^2p$