---
{"dg-publish":true,"permalink":"/math-methods/probability/binomial-distribution/"}
---

[[Math Methods/Probability/Probability - Fundamentals\|Probability - Fundamentals]]
We're planning a yes/no survey
Repeat $n$ times independently - must be independent (do not change results based on answers)

$p$ is the true probability of someone saying yes
Random variable $\xi$ = # of "yes"

As $n \to \infty$ , ${\xi / n} \to p$.

$P(\xi=0)=P(0)=(1-p)^n$ 

$P(n)=p^n$ 

This list of probabilities (P(1), P(2), P(3)...) is the **distribution**

# Example - Probability of one yes:
So for example, in a survey $n=5$, what's the probability of getting one yes $P(1)$?

This would be for example:

YNNNN, or $p(1-p)^4$
NYNNN, or $(1-p)p(1-p)^3=p(1-p)^4$ 
....

There are five different ways we can write this sequence, but they all have the same probability. 

Therefore, the total probability of getting 5 yeses is 5 times each single probability:
$P(1)=5p(1-p)^4$
## Calculating number of trials $n$ given $p$ for probability of 1
$$P(1)=np(1-p)^{n-1}$$
Since there are $n$ ways to order this distribution.
# Probability of $k$ yeses:
$P(k)=(\text{\# of permutations})\cdot p^k(1-p)^{n-k}$

First, the last part is pretty easy, just $p^k(1-p)^{n-k}$, just adjusting the number of yeses and noes to be $k$ instead of 1.

Now, the more complex part is adding the $n$ at the start. In the last example, there were $n$ ways to organize the answers (YNNNN, NYNNN, ...). This gets more complicated with more yeses. We call this the **number of permutations**. 

We can say this like:
- How many different orderings of $k$ yeses and $n-k$ noes?
- How many different ways can one pick k places out of n?

We use this notation to describe these problems, read as "n choose k"
$${n}\choose{k}$$
To solve this, imagine we have n different people and we are putting them in order. The number of permutations would be given by:
$$n(n-1)(n-2)(n-3)...(1)=n!$$
Shorthand for this is n **factorial** ($n!$) 


> [!NOTE] Zero Factorial
> $0! = 1$. Don't ask why, that's just how it is.

This is true for $n$ objects that only have one state. In our case, we are looking at the binomial distribution, so there are two states. This makes things a bit more complex, since we need to order both the Ys with respect to the Ns, but also the individual Ys and Ns.

Let's order like this, secretly labelling them with marks:
$Y_1Y_2N_1N_2N_3$

What if we reorganized them to:
$Y_2Y_1N_1N_2N_3$

If they weren't marked, we wouldn't be able to notice a difference. There is a difference between the marked and unmarked sequences. 

How many ways can we order the yeses without changing the unmarked sequences? This is equal to $k!$, in this example with $k=2, 2!=2$. 

For the noes, we can order them $(n-k)!$ ways without changing the "unmarked" sequence.

So overall, there are $k!(n-k)!$ ways of ordering this sequence without changing the "unmarked" sequence.

Now let's consider a different "unmarked" sequence,
$N_1Y_1Y_2N_2N_3$

Just like in the last ordering, there are also $k!(n-k)!$ ways to order these. In fact, each "unmarked" sequence has the same number of ways of organizing its "marked" components.

This means that to get the total number of permutations, if we have the markings on, we can consider $n!$ different orders. There are $n \choose k$ different orders and each marked answer can be organized $k!(n-k)!$ ways. 

$$n!={n \choose k}k!(n-k)!$$

Based on this, we can re order to: 
$${n \choose k}={n! \over k!(n-k)!}$$
Note this is only true for the binomial distribution where there are two states.

# Binomial Formula
Back to our formula for $P(k)$:
$$P(k)={n \choose k}p^k(1-p)^{n-k}={n! \over k!(n-k)!}p^k(1-p)^{n-k}$$

# Changes in $P()$ with increasing $n$ and $k$.
## Example: Dice rolling
Probability of rolling one six on the dice in 6 trials
$n=6$
$p=1/6$
$k=1$
This can be written like: $Bin(6, {1\over6})$:
$$P(1)={6! \over 1!\cdot 5!}\left({1\over6}\right)^1\left({5\over6}\right)^5$$
$P(1)=6({1\over6})({5\over6})^5=0.402$

Probability of rolling two sixes out of 12 trials
$n=12, p=1/6, k=2$
$$P(2)={12! \over 2!\cdot 10!}\left({1\over6}\right)^2\left({5\over6}\right)^{10}=0.296$$

Probability of rolling 10 sixes out of 60 trials:
$n=60, p=1/6, k=10$
$$P(10)={60! \over 10!\cdot50!}\left({1\over6}\right)^2\left({5\over6}\right)^{10}=0.137$$
When we try to calculate this, we run into a problem: $60!$ is enormous, about $8\times10^{81}$. A normal calculator can't handle a number this big.

## Why do larger trials move away from $P(1)$?

10 / 60 should be close to the true probability 1 in 6. But 11 / 60 is different, and so is 9/60. As we increase $n$, the small probabilities keep adding up, and the very small probabilities will add up and increase as we increase the number of die. So, despite having the same ratio, the probability of getting this ratio decreases.

# Example: rates of reaction

A simple reaction:

open channel $\rightleftharpoons$ closed channel

Rate of open channel -> closed channel: $\alpha$, reverse rate is $\beta$.

$\alpha dt$ = Probability that an open channel closes in the next dt time
$\beta dt$ = Probability that a closed channel opens in the next dt time.

This could also apply to ecological functions like the amount of time a predator spends hunting before changing behaviours...

At equilibrium, a fraction $x$ of many channels are open: Therefore, $x=P(open)$
Considering $N\to \infty$ channels

At equilibrium,
$xN$ channels are open
$(1-x)N$ channels are closed

Number of clos**ings** at equilibrium: $\alpha dt xN$
Number of open**ings** at equilibrium: $\beta dt (1-x)N$

The number of closings and openings must be equal at equilibrium, so we can cancel out some terms:
$$\alpha dt xN=\beta dt (1-x)N$$
$$\alpha x=\beta-\beta x$$
$$(\alpha + \beta) x=\beta$$
$$x={\beta \over \alpha + \beta}$$

Back to our probability of being closed $1-x$:
$$P(closed)=1-({\beta \over \alpha + \beta})={\alpha\over \alpha + \beta}$$

Now, let's consider probabiltiy. We have $n$ channels.
$$\text{Bin}(n, {\beta \over \alpha + \beta})$$ $$P(k\text{ open channels})={n \choose k}\left({\beta \over \alpha + \beta}\right)^k\left({\alpha \over \alpha + \beta}\right)^{n-k}$$
If we decide that $\beta = 2\alpha$, then the Prob(open) = ${2\alpha \over \alpha + 2\alpha} = 2/3$, Then Prob(closed) = 1/3

Imagine $n=3$, and the probabilty that 1/3 or fewer of the channels are open 
	$= P(1)+P(0)$
	$=3\cdot {2\over3} \cdot {1\over3}^2 + {3 \choose 0}{2\over3}^0{1 \over 3}^3 = 0.259$
	