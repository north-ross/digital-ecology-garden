---
{"dg-publish":true,"permalink":"/math-methods/probability/homework/week-3-homework/"}
---

# 10. Eigen's Paradox
[[Math Methods/Probability/Probability - Fundamentals#Example Sampling a large population to find a rare mutant.\|Probability - Fundamentals]]
![[hw_part2.pdf#page=4&rect=86,398,513,554|hw_part2, p.4]]
Probability of a mutation per nucleotide without enzymes: $p=0.01$

Probability of no mutation: $q=1-p=0.99$

Since each nucleotides chance of mutation is independent, the probability of no mutation in strand of length $n$ is $q^n$.

To have 1 mutation in 5 copies - $P(\text{no mutation})=1/5$
$${1\over5}=(0.99)^n$$
$$n={ln(1/5)\over ln(0.99)}\approx160$$
So given this probability, maximum length of nucleotide chain that is 1 mutation in 5 is 160

# 14. Frequency of identical twin births
[[Math Methods/Probability/Bayes' Theorem\|Bayes' Theorem]]
![[hw_part2.pdf#page=5&rect=84,445,514,604|hw_part2, p.5]]
$P(twins)=P(id,all)+P(frat,all)=0.003+0.017=0.02$
$P(id,twins)={0.003\over0.02}=0.15$
This is the prior probability - the probability that twins are monozygotic (identical) given that they are twins.

Using Bayes' theorem we can get the posterior probability given that the twins are the same sex:

$$P(id|same sex)={P(same sex|id)P(id)\over P(\text{same sex twins})}$$
Total probability:
$P(\text{same sex twins})=P(samesex|id)P(id)+P(samesex|frat)P(frat)$
	$=(1)(0.15)+(0.5)(0.85)=0.575$


$$P(id|same sex)={(1)(0.15)\over (0.575)}=0.2609$$

> [!NOTE] Skipping the part where we only look within twins
> If we skip the first part where we determine the probability that they are monozygotic given that they are twins and only use the probability from all births in our Bayes' Theorem, we will still get the same result. We are dividing each number by 0.02, so these could be factored out. However it's probably best to include this step, since the numbers make more logical sense in this case.

Now, let's see what happens when the frequency of fraternal twin births goes up:

New frequency:
$P(twins)=P(id,all)+P(frat,all)=0.003+0.03=0.033$
$P(id,twins)={0.003\over0.033}=0.0909$

This gives a new posterior probability of 0.1818 - lower than the previous one. A lower prior probability results in a lower posterior prob.
# 17. Cohort survival
[[Math Methods/Probability/Binomial Distribution\|Binomial Distribution]]
![[hw_part2.pdf#page=7&rect=86,635,528,746|hw_part2, p.7]]
## (a) Plotting the binomial distributions
We build a binomial distribution $Bin(5, 0.7^t)$, where $t$ is the number of years. $P(k)$ is the probabililty of $k$ birds surviving. Below I plot three cases for $P(k)$: $t=1$ (red), $t=3$ (green) and $t=10$ (blue). Note that histograms would be better to plot here but I'm not sure how to do that. These probabilities are only valid for integer values of $k$ that are 5 or less. Ignore the parts in between in the integers.

Formula: $$P(k)={5 \choose k}0.7^{tk} (1-0.7^t)^{5-k}$$
```desmos-graph
bottom=-0.1
top=1
right=7
left=-0.5
---
n=5
p=0.7

y = (n! / (x!(n-x)!)) * p^x * (1-p)^{n-x}|red|dashed
\binomialdist(n,p)|red

y = (n! / (x!(n-x)!)) * p^{3x} * (1-p^3)^{n-x}|green|dashed
\binomialdist(n,p^3)|green

y = (n! / (x!(n-x)!)) * p^{10x} * (1-p^{10})^{n-x}|blue|dashed
\binomialdist(n,p^{10})|blue

```


## (b) Years until 95% chance that all birds have died
This is where surviving birds $k=0$ and probability of survival $P(k)=0.95$ . If we plot $P$ as a function of $t$, with $n=5, k=0$ , then show $P(t)=0.95$ as a dotted blue line:
```desmos-graph
bottom=-0.1
top=1
right=20
left=-1
---
n=5
p=0.7

y = (n! / (0!(n-0)!)) * p^{0x} * (1-p^x)^{n-0}|red
y=0.95|blue|dashed
```
Again, imagine that this is using discrete histogram bars or dots on the integer values of $t$ since it was not stated that this is a constant rate.

We can see that these intersect around $t=13$ - so it will be 13 years until there is a 95% probability of 0 birds surviving. 

Alternatively we could solve this with some algebra. It's not so bad if we start with $k=0$, since $n$ choose $0$ is always equal to $1$:
$${n \choose 0}={n!\over0!(n-0)!}={n!\over(1)(n)!}=1$$
So our equation is:
$$P(k)={n \choose 0}p^{0t}(1-p^t)^{n-0}$$
$$P(k)=(1)(1)(1-p^t)^n$$
$$ln(P(k))=n\cdot ln(1-p^t)$$
$$exp\left({ln(P(k))\over n}\right)=1-p^t$$
$$t={ln\left(1-exp\left({ln(P(k))\over n}\right)\right)\over ln(p)}$$
$$t={ln\left(1-exp\left({ln(0.95)\over 5}\right)\right)\over ln(0.7)}=12.86$$
Same as before - we need to wait 13 years to be at least 95% sure. If we assume it was a constant rate, then we would have 12 years and 10 months, but this was not stated and its likely that it is not constant throughout the year.
# 18. Cancer diagnosis
[[Math Methods/Probability/Binomial Distribution\|Binomial Distribution]]
![[hw_part2.pdf#page=7&rect=79,379,516,568|hw_part2, p.7]]

# 19. Binomial random number generators
[[Math Methods/Probability/Binomial Distribution\|Binomial Distribution]]
(a) In a uniform distribution, the probability of getting a number between 0 and 0.2 is just 0.2.
