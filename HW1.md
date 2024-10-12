# 1
## a
$\Omega$ = {11, 12, 13, 14, 15, 16, 21, 22, 23, 24, 25, 26, 31, 32, 33, 34, 35, 36, 41, 42, 43, 44, 45, 46, 51, 52, 53, 54, 55, 56, 61, 62, 63, 64, 65, 66}

## b
A = {14, 15, 16, 23, 24, 25, 26, 32, 33, 34, 35, 36, 41, 42, 43, 44, 45, 46, 51, 52, 53, 54, 55, 56, 61, 62, 63, 64, 65, 66}

B = {21, 31, 32, 41, 42, 43, 51, 52, 53, 54, 61, 62, 63, 64, 65}

C = {41, 42, 43, 44, 45, 46}

## c
$A \cap C = \{41, 42, 43, 44, 45, 46\}$

$B \cup C = \{21, 31, 32, 41, 42, 43, 44, 45, 46, 51, 52, 53, 54, 61, 62, 63, 64, 65\}$

$A \cap (B \cup C) = \{32, 41, 42, 43, 44, 45, 46, 51, 52, 53, 54, 61, 62, 63, 64, 65\}$

# 2
$\binom{52}{5}\binom{47}{5}\binom{42}{5}\binom{37}{5}\binom{32}{5} = \frac{52!}{47!5!}*\frac{47!}{42!5!}*\frac{42!}{37!5!}*\frac{37!}{32!5!}*\frac{32!}{27!5!}$ ways to deal the cards

# 3
How many ways can we arrange {s, t, a, t, i, s, t, i, c, a, l, l, y}?

Count: 2s, 3t, 2a, 2i, 1c, 2l, 1y, 13 total letters

$\binom{13}{2, 3, 2, 2, 1, 2, 1} = \frac{13!}{2!3!2!2!1!2!1!}$ ways to arrange statistically

# 4
In the deck, there are 52 possible positions, we need to choose 4 positions for the aces.

$|\Omega| = \binom{52}{4} = \frac{52!}{58!4!}$

Of these positions, there are 49 ways the aces can be adjacent to each other.

P({aces are adjacent}) = $\frac{49}{\frac{52!}{58!4!}}$

# 5
In total, there are $\binom{60}{30,30}$ ways to select the students.

$|\Omega| = \binom{60}{30,30} = \binom{60}{30}$

There are two ways the close friends are all in the same class, they can either all be in the first class or the second class.

After selecting which class the close friends are in, there are $\binom{55}{25,30}=\binom{55}{25}$ ways to select the remaining students.

P({all close friends in same class}) = $\frac{2*\binom{55}{25}}{\binom{60}{30}} = \frac{2*\frac{55!}{25!30!}}{\frac{60!}{30!30!}}$

There are $\binom{5}{4, 1} = \binom{5}{4}$ ways to separate the close friends into one group of 4 and one group of 1.

The group of 4 can either be in the first classroom or the second classroom.

After selecting which class the close friends are in, there are $\binom{55}{26,29}=\binom{55}{26}$ ways to select the remaining students.

P({4 close friends in the same class}) = $\frac{2*\binom{5}{4}*\binom{55}{26}}{\binom{60}{30}}=\frac{2*\frac{5!}{4!1!}*\frac{55!}{26!29!}}{\frac{60!}{30!30!}}$

There is one way to separate Marcelle from her other friends when splitting the children into 2 groups.

Marcelle can either be in the first classroom or the second classroom.

After selecting which class the close friends are in, there are $\binom{55}{26,29}=\binom{55}{26}$ ways to select the remaining students.

P({Marcelle separated from her friends}) = $\frac{2*\binom{55}{26}}{\binom{60}{30}}=\frac{2*\frac{55!}{26!29!}}{\frac{60!}{30!30!}}$