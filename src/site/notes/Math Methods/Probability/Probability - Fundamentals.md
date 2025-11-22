---
{"dg-publish":true,"permalink":"/math-methods/probability/probability-fundamentals/"}
---

# Frequency and Probability
- The frequency is the measured amount. For example, if you roll a six sided dice 60 times, you might find you get a six 9 times. 
- As you increase the number of throws to infinite, you get closer to the true probability of 1/6
# Random variable
We use the Greek letter xi $\xi$ to mean the next number shown on a dice. $P$ is used to mean probability. So $P (\xi = 6)$ means probability that the next number is six. This is $1/6$. Often, $P(6)$ is used as shorthand for this.
# Event
$$P(\xi \text{ is odd}) = P(1) +P(3) +P(5) = 3/6$$If we make some categories: small numbers are 1 and 2 and large are 5 and 6. 
$$P(\xi \text{ is small}) = P(1) + P(2) = 2/6$$
$$P(\xi \text{ is small or large}) = P(1) + P(2) + P(5) + P(6) = 4/6$$
However, in this case:
$$P(\xi \text{ is small or odd}) = P(1) + P(2) + P(3) + P(5) = 4/6$$
We can't just add $P(\xi \text{ is odd})$ and $P(\xi \text{ is small})$ because they are not mutually exclusive (1 is both small and odd)

## Certain and impossible events
- Even if the probability is 1 or zero, that doesn't always mean that it is certain or impossible. We say "almost certain"
# Example: Testing a sports team for blood doping
A sports team has 11 members. Two of them are blood doping. What is the probability that you test three of them and find no doping?
$$P(\text{no doping detected}) = 9/11 * 8/10 * 7/9$$
Since each time you test one member, there are less remaining to test.
# Example: Sampling a large population to find a rare mutant.
In a very large wild population of plants, 1% have a rare mutation. What's the probability of finding *at least one* mutant in the population based on a sample size of $n$?

It's difficult to find *at least one*. Since we would need to account for lots of situations: The first one sampled is a mutant, or the first one isn't but the second is, or the first two are mutants, etc...

It's easier to find the probability that there are *no* mutants. Then $1 -$ this probability will give us the probability that there is at least one.

$$P(\text{no mutants}) = 0.99 * 0.99 * 0.99*0.99... = 0.99^n$$
>Note that unlike the previous example, this time we do not change the probability after sampling each individual. This is because we are looking at a very large population and we assume that removing 1 individual doesn't affect the overall frequency of this mutation in the population.

Therefore: $$P(\text{at least 1 mutant}) = 1-0.99^n$$
If we are designing an experiment where we need to capture some of these mutants, what sample size would we need to be 95% confident that we catch at least one?
$$P(\text{at least 1 mutant}) = 0.95 = 1-0.99^n$$
Solve for $n$:
$$0.99^n = 1-0.95$$
$$ln(0.99^n) = ln(0.05)$$
$$n={ln(0.05) \over ln(0.99)} = 298.07$$
So in practice we would use a sample size of 300.


# [[Math Methods/Probability/Conditional Probability\|Conditional Probability]]
In the UK, 10% of males are left handed but only 8% of females.
There is a 50% probability that someone is male or female.

$$P(\text{male} | LH) = 0.1 $$
$$P(\text{female} | LH) = 0.08 $$

The probablility someone is male and left handed:
$$P(\text{male and LH}) = P(male) * P(LH|male)$$
Same for female. So overall $P(LH)$ in the population is $$P(LH) = P(\text{male and LH}) + P(\text{female and LH})$$
$$P(LH) = P(\text{male})*P(LH|male) + P(\text{female})*P(LH|female)$$
$$P(LH) = 0.5*0.1 + 0.5*0.08$$
This continues in the next lecture [[Math Methods/Probability/Conditional Probability\|Conditional Probability]]
# [[Math Methods/Probability/Law of total probability\|Law of total probability]]


