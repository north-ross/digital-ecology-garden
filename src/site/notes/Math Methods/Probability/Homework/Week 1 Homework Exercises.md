---
{"dg-publish":true,"permalink":"/math-methods/probability/homework/week-1-homework-exercises/"}
---


## Question 1. *Hiding behind randomness*.
> Questions like “Have you ever cheated on your spouse?” or “Do you have a neurotic disorder?” people don’t like to answer. A way to preserve privacy and yet collect useful data in polls is to ask the question with these instructions: Flip a coin. If tail, answer truthfully. If head, flip a coin again and say “yes” if tail, “no” if head. Now a “yes” is not embarrassing, it can be just from the flips; so people are not tempted to lie. 
> 
> When asking a large number of people, we got a fraction $q$ who said “yes”. What is the fraction of those for whom the real answer is “yes”?
[[Math Methods/Probability/Probability - Fundamentals\|Probability - Fundamentals]]
The fraction $q$ of people who answered yes is the sum of two parts: Those who answered yes randomly, and those who truly answered yes because of the second coin toss. The probability of each of these events is the product of the probability of the first coin toss result and the probability of the second event.

$$q = P(\text{tails}_1)\cdot P(Y_{true}) + P(\text{heads}_1)\cdot P(\text{tails}_2)$$
Assuming we have a fair coin, the probability of each coin toss is the same ($1\over2$).
$$q = {P(Y_{true})\over2} + {1\over4}$$
$$P(Y_{true})=2q-{1\over2}$$
The probability of someone giving a true yes answer is $2q-0.5$. 
## Question 2. *Genetic risks.*
>A couple is facing the risk that their children may suffer from a genetic disorder, because both the husband and the wife are known to be heterozygote ($Aa$) carriers of the harmful recessive allele $a$ (the homozygote $aa$ individuals are affected by the disorder, all others are healthy). The couple plans to have two children, and wants to know the prospects for their health: What is the probability that both children will be healthy?
[[Math Methods/Probability/Probability - Fundamentals\|Probability - Fundamentals]]
Probability of one child being an $aa$ homozygote: ${1\over4}$
Probability of one child being healthy: $1-{1\over4}=3/4$
Probability of two children being healthy: ${3\over4} \cdot {3\over4}=9/16$

So, the probability of two healthy children is 9/16 or 56%.
## Question 3. *Marriage of relatives*
>Close relatives are not allowed to marry but if they do, their children are very often affected by serious genetic problems. This is because most of us carry 2-3 recessive lethal genes and some more that are not lethal but harmful. In unrelated people, these harmful recessive alleles are most likely in different loci so that their children are healthy heterozygotes. Descendants of a single person may however carry harmful recessives in the same locus; and if they marry, their children can be recessive homozygotes.

>The figure shows a pedigree with marriage between cousins. A and B are the shared grandparents; C and D are sisters, who marry unrelated persons; E and F are cousins; and G is their child. $a$ denotes a harmful recessive allele present in A. Calculate the probability that G inherits $a$ from both parents and is therefore a recessive homozygote $aa$ exhibiting the symptoms of the disorder caused by $a$. Next, calculate the probability that G is not a recessive homozygote for any of the 3 unlinked harmful alleles that A carried and also not for another 3 unlinked alleles that were present in B. (In reality we cannot know that A and B carry exactly 3 harmful alleles each, but this illustrates the probability of having a healthy child in a cousin marriage with roughly realistic numbers.)
[[Math Methods/Probability/Probability - Fundamentals\|Probability - Fundamentals]]
1. Probability of G being a recessive homozygote $aa$.
The probability of $a$ being present in daughter C (inherited from parent A) is the same as the probability that it is in daughter D: 1/2. We call this probability $P(a_1)$ (generation 1).

$P(a_C) = P(a_D)=P(a_1)={1\over2}$

The probability of $a$ being further inherited by E or F is half of the probability of their parent having it:

$P(a_E)=P(a_F)={P(a_1)\over2}={1\over4}$

The probability of G inheriting $a$ from one parent is half of this (1/8). The probability of inheriting $a$ from both parents, making G a heterozygote, is ${1\over8} \cdot {1\over8}={1\over64}$ or 1.56%.

2. Probability of being healthy for three unlinked harmful alleles in grandparent A and another in grandparent B.
If G has the same probability of inheriting each of these alleles and they are all independent, then $(1-{1\over64})^6=90.98\%$

## Question 7. *[[Math Methods/Probability/Law of total probability\|Total probability.]]*
>About 33% of African American people develop high blood pressure during their lives, whereas in people of Caucasian origin, this occurs only with probability 25%. In a town where 40% of people are African Americans and the rest are Caucasians, what percentage of people will need care for high blood pressure?

$P(A)$: high blood pressure
$P(B_1)=0.40$: Amount of African-Americans
$P(B_2) = 0.60$: Amount of Caucasians
$P(A|B_1)=0.33$: Probability of high blood pressure for African-Americans
$P(A|B_2)=0.25$: Probability of high blood pressure for Caucasians

Using the law of total probability $P(A) = \sum_i P(A|B_i)P(B_i)$:

$P(A) = P(A|B_1)P(B_1)+P(A|B_2)P(B_2)$
$P(A) = (0.33)\cdot (0.40) + (0.25)\cdot (0.60)$
$P(A)=0.282$

So, about 28% of people in this town are likely to develop high blood pressure in their lives.
## Question 12. *The birthday problem.*
>Calculate the probability that (at least) two persons share their birth days in a group of (i) 5 people; (ii) 30 people. Hint: calculate first the probability of the opposite, i.e., that no two persons have the same birthday. The probability that my birthday is different from yours is 364/365. 

1. Probability that at least two persons share a birth day in a group of 5 people.

There are 365

P(all birthdays are distinct) = $$P(distinct_5)={365\over365} \cdot {364\over365} \cdot {363\over365} \cdot {362\over365} \cdot {361\over365}\approx0.9729$$
So, the probability of no shared birthdays is $P = 0.0271$ ($1-P(distinct_5)$)
> [!Wrong answer]
> Let's call our people A, B, C, D, E.
> 
> The probability that person A has a different birthday from the four other people is $({364\over365})^4$
> 
> Now, we need to find this probability for each of the other birthday relations and multiply them all. However, we already accounted for everyone's birthday relation with person A, so we can ignore that relationship when looking at the chances for person B - we only need to compare with three people now. This trend continues until there is only one more relation to compare (person D with person E).
> 
> $$({364\over365})^4 \cdot ({364\over365})^3 \cdot ({364\over365})^2 \cdot ({364\over365})^1 = ({364\over365})^{10}$$
> 
> So the probability of at least two people sharing a birthday in a group of 5 is $1-({364\over365})^{10}=0.0271$ or 2.7%.
> 
> The problem I made is that the numerator should decrease every time as you eliminate birthdays

2. Probability that at least two persons share a birthday in a group of 30.

We can generalize this using a "big Pi" product:

$$P(\text{no shared birthdays})=\prod_{k=0}^{30}{365-k\over365}$$
Calculating this out gives us the correct answer - which was close to my approximation (below), but that was incorrect - in this example the numerator should decrease every time you check a new birthday.
> [!Wrong answer that I tried earlier]
> Using the same logic as before, we need to determine:
> $$({364\over365})^{29} \cdot ({364\over365})^{28}\cdot ({364\over365})^{27}...$$
> 
> A faster way to do this is thinking about the sum of the exponents. This is a sequence of integers from 1 to 29, and thus the formula  $\sum_{i=1}^{n}n = {1\over2}n(n+1)$  is applicable here. So, our general formula for determining the probability that at least two persons share a birthday in a room of size $n$ persons is:
> $$P(\text{shared birthday})=1-\left({364\over365}\right)^{{1\over2}n(n-1)}$$
> 
> 
> So, in our case this is $1-({364\over365})^{435}=0.697$ or about 70%.

