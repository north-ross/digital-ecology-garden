---
{"dg-publish":true,"permalink":"/math-methods/probability/bayes-theorem/"}
---

Whenever you want to switch conditional probabilities, use this.

$$P(B|A)={P(A|B)P(B) \over P(A)}$$
$P(A)$ comes from the law of total probability
$P(B)$ is the "prior probability" - this is an unconditional probability. In our example, probability of being male
$P(A|B)$ is probability of A with condition B - this must be known from collecting data. In our example this is the probability of left-handedness in males, which is known.

$P(B|A)$ is the posterior probability - this is what we are always trying to calculate. This is based on the prior probability and some data on this population. In our example, this is the probability that a left-handed person is male.

# Bayes Factor
[[Math Methods/Probability/Homework/Week 2 Homework#Question 16. *Bayes factor*.\|Week 2 Homework#Question 16. *Bayes factor*.]]

When you cannot calculate the total probability (due to lack of information), you can use the Bayes Factor to compare two hypotheses