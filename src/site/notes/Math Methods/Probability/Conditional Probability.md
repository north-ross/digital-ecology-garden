---
{"dg-publish":true,"permalink":"/math-methods/probability/conditional-probability/"}
---

Useful for **subpopulations**.

Based on conditional probability, like the previous example with different rates of left handedness in males and females.

# Conditional probability formula
In our left-handedness example where men and women have different left handed rates:

Pobability of left handed-ness in general population = (Probability of males being left handed $\times$ Probability of being a male) $+$ (Probability of women being left handed $\times$ probability of being a woman)
$P(LH) =P(LH|♂)P(♂)+P(LH|♀)P(♀)$
# General Formula for conditional probability
([[Math Methods/Probability/Law of total probability\|Law of total probability]]):

$$P(A) = P(A|B)P(B)+P(A|\text{not }B)P(\text{not }B))$$
# Independence
## Example: Probability of brown eyes in men and women
Imagine there was a difference in probability of brown eyes between men and women:
$P(\text{brown eyes}|♂)$
$P(\text{brown eyes}|♀)$

$P(\text{brown eyes}) =P(\text{brown eyes}|♂)P(♂)+P(\text{brown eyes}|♀)P(♀)$

However, in reality, there is no difference, these conditions are independent. Therefore:
$P(\text{brown eyes}|♂)$=$P(\text{brown eyes}|♀)$

Since the two events are independent, the probability of being male and having brown eyes is just the product. There is no need for conditional probabilities, since they are just equal. 

However, for conditional probability, we need to use different probabilities for the sub-populations.
# Murder Example
Based on a stab wound, we can determine the killer is left-handed. What is the probability that the killer is male?

Probability of being left handed if they are male: $P(LH|♂)$
Probability of being male if they are left handed: $P(♂|LH)$

These two products should be equal in probability:
$$P(♂|LH)\cdot P(LH)=P(LH|♂)\cdot P(♂)$$
Therefore, we can re-arrange to find probability of being male and left handed:

$$P(♂|LH) = {P(LH|♂)P(♂)\over P(LH)} = {0.1 *0.5 \over 0.09} = 5/9$$
So it's slightly more likely that the murderer is a man than a woman.

# [[Math Methods/Probability/Bayes' Theorem\|Bayes' Theorem]]
This is because of Bayes' Theorem, a basic obvious relationship between probabilities, that is very important. See the link
# Haemophilia example
This is a recessive trait that is carried on the x-chromosome.

![[Haemophilia Family Tree.canvas]]

Here is an example with a family with two daughters and one son. The son has haemophilia. Since it's carried on the x chromosome, he must have inherited it from his mother, who must be a carrier of this recessive gene (heterozygote).

The probability of their daughter "B" being a carrier is 0.5. She received the chromosome from either her father or mother, and the mother must be a carrier. 

If the daughter "B" has three healthy sons without hemophilia, this is evidence that she might not be a carrier.  What is the probability that she is a carrier, given this?
$P(B \text{ carrier})=0.5$
$P(B \text{ carrier}| \text{3 healthy sons})=?$

Let's first determine what the probability of producing 3 healthy (without haemophilia) sons from a carrier. The probability of the first son being a carrier is 0.5, then we multiply by 0.5 again each time after that.
$$P(\text{3 healthy sons}|B \text{ carrier})={1\over2} \cdot {1\over2} \cdot {1\over2} = \left({1\over2}\right)^3 = {1\over 8}$$
Now, we use Bayes' theorem to get the posterior probability:
$$P(B \text{ carrier}| \text{3 healthy sons})={P(\text{3 healthy sons}|B \text{ carrier})P(B \text{ carrier}) \over P(\text{3 healthy sons})}$$

We still need the probability of 3 healthy sons. Get this from law of total probabilty:
$$P(\text{3 h. sons}) = P(\text{3 h. sons}|B \text{ car.})P(B \text{ car.})+ P(\text{3 h. sons}|B\text{ not car.})P(B\text{ not car.})$$
$$=(1/8)*(1/2) + 1*(1/2) = 9/16$$
(100% chance of 3 healthy sons if B is not a carrier)

Back to Bayes' theorem:
$${(1/8) * (1/2) \over 9/16} = 1/9$$
So, the posterior probability is 1/9. There is a good chance that she is not a carrier, but in order to be 100% sure she would need infinitely many sons.

B has a daughter named "C". What's the chance of her being a carrier?
$P(C \text{car.}|\text{3 healthy brothers})=P(C \text{car.}|B \text{car.})P(B \text{car.}|\text{3 h. sons})+P(C \text{car.}|B\text{ not car.})P(B\text{ not car.}|3\text{ h. sons})$
$=(1/2)*(1/9)+0*(8/9)=1/18$
Probability of C being a carrier if B is not a carrier is 0, since then she could not have inherited it.

If B didn't have 3 sons, then we wouldn't know anything about the conditional probability. In this case, the probability of C being a carrier would be 1/4, since the only thing we know is that B has a 1/2 chance, and C inhertited half her genes from B.

# Bayesian Inference
## Example: Regina vs Adams court case (1996 England)
A woman was assaulted in the street in the night and could not identify the man. They identified Adams as the suspect, but Regina could not identify Adams, and he had an alibi.

A DNA sample was produced, and it matched Adams with very high confidence.

The lab said that the probability of DNA match: $P(match|innocent) = {1\over200,000,000}$

This seems very low. However, in fact, we are looking for the probability of innocence, given a DNA match: ($P(innocent|match)$)

We are looking at the wrong conditional probability - this is common practice in the courtroom, often called the "prosecutor's fallacy" due to its use by prosecutors to prove guilt in the courtroom.

At this point, the court invited a statistics professor from Oxford who taught the jury about Bayes' Theorem and gave them examples, homework exercises, calculators, so they can decide what the real probability is.

$$P(innocence|match) = {P(match|innocence)P(innocence)\over P(match)}$$
To get P(match), we use the law of total prob.:

$$P(match)=P(match|innocence)P(innocence) + P(match|guilty)P(guilty)$$
We know that P(guilty) is the reverse of P(innocence): $P(guilty) = 1 - P(innocence)$ 

And the probability of a match if he is guilty is 100%. $P(match|guilty)=1$

However, we still don't know the P(innocence) before the DNA test (the prior probability). This is actually just $1 - {1\over 50,000}$ (50,000 is the population of men in the town).

Back to our law of total prob:
$$P(match)=P(match|innocence)P(innocence) + P(match|guilty)P(guilty)$$
$$P(match)=\left(\left({1 \over 200\text{ million}}\right)\cdot  \left(1-{1\over 50,000}\right)\right) + \left((1) \cdot \left({1\over 50,000}\right)\right)=0.0000200...$$
Putting this back into Bayes' Theorem:

$$P(innocence|match) = {({1\over 200\text{ million}})\cdot(1-{1\over 50,000})\over (0.0000200...)}=0.00024993...\approx 0.025 \% \approx{1\over4000}$$

This means $P(innocent|match)= 0.02\%$ - much higher than our 1/200 million.

One assumption not taken into account - the attacker could have come from another town which would make prior P(innocence) even smaller (if we assume it could be a man from anywhere in the country, n=50,000,000). This assumption would increase the posterior probability of innocence with a DNA match $P(innocence|match)$ to 20%.

Later, it was found that the DNA results were wrong, and in fact it was 1/2 million instead of 1/200 million. This doesn't make much of a difference to a layperson, but in fact this makes the posterior probability (assuming the assaulter was from the town) $P(innocence|match)$ much higher (0.024 or 2.4%, increased from 0.024%).

Ultimately, probability in this case isn't related to frequencies or science - the true answer is quantifiable, and Adams knows what the answer is. Maybe statistics is not the most applicable here.
# Hypothesis testing
Given q is the probability of tails in a coin toss.

Our null hypothesis is that q=0.5 if it is a fair coin:
$H_0: q=0.5$

If we toss the coin $n=6$ times, and our data gives us 6 tails:

What is $P(H_0|data)$?

This is hard to calculate, let's try:

$P(data|H_0)=({1 \over 2})^6 = 0.0156$

This is less that 0.05, so we can reject our null hypothesis. However, this is based on the prosecutor's fallacy and is actually not correct. There are problems with classical statistics. We need a two-sided test:

$P(6\text{ tails}|H_0)+P(6\text{ heads}|H_0)=0.03333$

This is higher, but we can still reject our null hypothesis.

## Trying this using Bayes' theorem
$$P(H_0|data)={P(data|H_0)P(H_0) \over P(data|H_0)P(H_0)+P(data|H_1)P(H_1)+...}$$
It's kind of impossible to do this, since there are infinitely many alternative hypotheses? For example, let's say $H_1: q=0.6, H_2: q=0.7...$. Each of these alternative hypotheses has their own probability $P(H_0), P(H_1), P(H_2)$.

In Bayesian statistics, we assign probabilities to each of these alternative hypotheses and call this the "prior distribution". In our case, since most coins are fair, the null hypothesis is our most likely scenario. 