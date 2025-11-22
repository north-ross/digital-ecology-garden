---
{"dg-publish":true,"permalink":"/math-methods/probability/probability-mean-and-variance/"}
---

# Mean
From our example from [[Math Methods/Probability/Binomial Distribution#Example Dice rolling\|Binomial Distribution about dice rolling]]. We roll a dice ten times and get:

$$average = {2+5+4+2+6+6+3+1+2+1\over 10}$$
Another way to write this is tallying up our unique numbers and multiplying each by the occurence fraction:
$$average={2\over10}1+{3\over10}2+{1\over10}3+{1\over10}4+{1\over10}5+{2\over10}6=3.3$$
$$average=\sum values * fractions$$
This is using [[Math Methods/Probability/Probability - Fundamentals#Frequency and Probability\|frequency]]. Imagine we are instead using the "fraction of infinitely many", the probability.

Our expectation $E$, also known as the mean, is the fraction we would get with infinitely many trials with known probabilities for each time.
$$E(\xi)=\sum value \cdot probability$$
$$E(\xi)={1\over6}1+{1\over6}2+{1\over6}3+{1\over6}4+{1\over6}5+{1\over6}6=3.5$$
Note that our expectation (mean) is different from our average. The average is the random variable, it might change between experiments and with sample size. The mean (expectation) will never change. A higher number of trials will make the average more likely to approach the mean.

In this course, the average will be used as our random variable, we will examine how the average changes between experiments and its variance (error bars). The expectation will never have error bars.

$E(\xi)=\sum_k x_k P_k$

"take the product of the value with the probability and add it up for every possible value."

# Example: gambling
Cast a die. 
- If you get 5 or 6, you get 10€. Call this $x_1$. $P_1=1/3$
- 4 gives you 3€. Call this $x_2. P_2=1/6$
- 1 2 or 3 means you need to pay 5€. $x_3=-5, P_3=1/2$
Our random variable $\xi$ is the total money we will get.

$$E(\xi)=\sum_{k=1}^3 x_k P_k$$
$$E(\xi)=10\cdot{1\over3}+3\cdot{1\over6}-5\cdot{1\over2}=1.333...$$
So, if we play the game infinitely many times, we will gain 1.333€ per round, although we might lose money at some point and gain money at others. If you keep playing the game then you will eventually gain this much per round overall.

# Expectation of the sum of two dice
We have a blue die and a red die.
$\xi$ is the number on the blue die
$\eta$ is the number on the red die

$$E(\xi + \eta)={(5+1)+(3+1)+...\over n}$$ In this case, since we are looking for the expectation, $n \to \infty$ 

We can rearrange this to add up the blue dice numbers and red numbers separately:

$$E(\xi + \eta)={(5+3+...)\over n}+{(1+1+...)\over n}=E(\xi)+E(\eta)$$
"The expectation of the sum is the sum of the expectation"

# Expectation of Sum in [[Math Methods/Probability/Binomial Distribution\|Binomial Distribution]]:
Probability of $\xi=1$ 
$\xi_1$ is either $\xi_1=1$ (meaning yes) with probability $p$, or $\xi_1=0$ (no, with probability $1-p$)

Continue for $\xi_2$...

The expectation for $\xi_1$:
$E(\xi_1)=1\cdot p + 0\cdot(1-p)=p$

This is true for each $\xi_{n}=p$

So, the expectation of the sum in a binomial dist is:
$$E(\xi_1+\xi_2+...+\xi_n)=np$$

This of course also carries on to the [[Math Methods/Probability/Poisson Distributions\|Poisson Distributions]], where $\lambda=np$, so the expectation of the sum is just equal to $\lambda$.