---
{"dg-publish":true,"permalink":"/math-methods/probability/homework/week-2-homework/"}
---

6, 8, 13, 15, 16
# Question 6. *Test of independence.* 
> An ecologist collects presence-absence data of two different species of plants in sample quadrats, and wants to know whether the plants occur independently. The data is: 
> 
> (a) Both plants: 25% of quadrats, plant A only: 25%, plant B only: 5% 
> (b) Both plants: 15% of quadrats, plant A only: 35%, plant B only: 15%

Without doing a statistical test, we can assume that if the distributions are independent, then $P(A\text{ and }B) = P(A) \cdot P(B)$ (in an infinite sample size)

(a) 
$P(A)= P(A\text{ and }B) + P(A \text{ only}) = 0.25+0.25$
	$=0.50$
$P(B)= P(A\text{ and }B) + P(B \text{ only}) = 0.25+0.05$
	$=0.30$
$P(A) \cdot P(B) = 0.15 \ne P(A\text{ and }B)$

So, these are not independent - it seems that B is more likely to occur with A.

(b)
$P(A)= P(A\text{ and }B) + P(A \text{ only}) = 0.15+0.35$
	$=0.50$
$P(B)= P(A\text{ and }B) + P(B \text{ only}) = 0.15+0.15$
	$=0.30$
$P(A) \cdot P(B) = 0.15 = P(A\text{ and }B)$

In this dataset they are independent, it seems A and B occur together as much as they occur apart.

In reality, we would do a *Chi-square* test to compare these and check for independence.
# Question 8. *Blood transfusion.*

$A_R$ means recipient is type A. $A_D$ means donor is type A.

Let's find conditional probabilites of a fatal transfusion for each recipient blood type. Since each donor blood type is independent, we add the probabilities for each blood type that's fatal for the recipient.

$P(fatal|A_R) = P(B_D) + P(AB_D) =0.166+0.081= 0.247$
$P(fatal|B_R) = P(A_D) + P(AB_D)=0.442+0.081=0.523$ 
$P(fatal|AB_R) = 0$
$P(fatal|O_R) = 1 - P(O_D)=1-0.312=0.688$

It's never fatal for $AB_R$ since they can receive any blood. $P(fatal|AB_R) = 0$. Every other blood type is fatal for $O_R$, so the probability is just $1-P(O_D)$

Now, from the law of total probability:

$P(any|fatal) = P(A_R)P(fatal|A_R)+P(B_R)P(fatal|B_R)+P(AB_R)P(fatal|AB_R)+P(O_R)P(fatal|O_R)$
$P(any|fatal) = (0.442)(0.247)+(0.166)(0.523)+(0)+(0.312)(0.688)$
$P(any|fatal) =0.4106$

# Question 13. *Rare disease screening*.
A medical test picks out a disease in 100% of the cases when it really occurs, but 5% false positives. The disease affects 0.1% of the population. Your test comes back positive - what is the probability you really have the disease.

We are looking for $P(infected|positive test) (= P(inf.|test))$ for short.

We have: 
$P(test|healthy) = 0.05$
$P(test|infected) = 1$
$P(infected)=0.001$
$P(healthy)=0.999$

Based on Bayes' Theorem:
$$P(infected|test)={P(test|infected)P(infected) \over P(test)}$$
So, we need to get $P(test)$ from the law of total probability:
$P(test)=P(test|healthy)P(healthy)+P(test|infected)P(infected)$
$P(test)=0.05\cdot0.999 + 1 \cdot 0.001 =0.0509$
$$P(infected|test)={1 \cdot 0.001 \over 0.0509}=0.0196=1.96\%$$
That's lower than I thought.

If you wanted to take another test about this, you would use $P(infected|test)$ as your prior probability and calculate a new total probability and posterior.
# Question 15. *Bayesian statistics*
Let $q$ be the probability that we get a tail and 1-q be the remaining probability.

The coin might be fair (q=0.5), but might be loaded in favor of heads or tails (q<0.5 or q>0.5).

We want to estimate the parameter $q$ of a given coin. If we toss the coin six times and get 6 tails in a row, the traditional estimate would be q=6/6=1, predicting that it will always give a tail.

If our prior belief is that the coin is fair, we can specify the prior probability of the coin being fair and the probability that it will differ from fairness to different degrees (classes).

Imagine we only have three classes:

| Class      | $q$ | Prior probability |
| ---------- | --- | ----------------- |
| fair coins | 0.5 | 0.98              |
| tail coins | 1   | 0.01              |
| head coins | 0   | 0.01              |
a. Given the above "prior probability" predictions, what is the posterior probability of us getting 6 tails in 6 trials.

From Bayes' theorem:
$$P(fair|\text{6 tails}) = {P(\text{6 tails}|fair)P(fair)\over P(\text{6 tails})}$$
From the law of total prob:
$P(\text{6 tails})=P(\text{6 tails}|fair)P(fair)+P(\text{6 tails}|tailcoin)P(tailcoin)+P(\text{6 tails}|headcoin)P(headcoin)$$P(\text{6 tails})=(0.5)^6 * 0.98 + 1^6 * 0.01 + 0^6 * 0.01=0.0253$

So, back to Bayes':
$$P(fair|\text{6 tails}) = {(0.5)^6 (0.98)\over 0.0253}=0.605$$
Repeat for tail coins:
$$P(tail|\text{6 tails}) = {(1) (0.01)\over 0.0253}=0.3951$$
For head coins it will of course be zero. since P(6 tails|head coin)=0

b. Repeat except the prior probability is 1/3 for each type of coin:
$P(\text{6 tails})=(0.5)^6 * {1\over3} + 1^6 * {1\over3} + 0^6 * {1\over3}=0.3385$

$$P(fair|\text{6 tails}) = {(0.5)^6 ({1\over3})\over 0.3385}=0.015$$
$$P(tail|\text{6 tails}) = {(1) ({1\over3})\over 0.3385}=0.985$$
If there is a 1/3 chance of the coin always giving tails and equal probabilities of fair or heads, we have a 98.5% chance that our coin is a tail coin.

c. What happens to the posteior probabilities if we assume P(tail coin) = 0? or that P(fair coin)=1?

| Class      | $q$ | Prior probability - scenario 1 | Prior probability - scenario 2 |
| ---------- | --- | ------------------------------ | ------------------------------ |
| fair coins | 0.5 | 0.985                          | 1                              |
| tail coins | 1   | 0                              | 0                              |
| head coins | 0   | 0.015                          | 0                              |
Scenario 1:
$P(\text{6 tails})=(0.5)^6 (0.985) + 1^6 * 0 + 0^6 * {0.015}$
$$P(fair|\text{6 tails}) = {(0.5)^6 (0.985)\over (0.5)^6(0.985)}=1$$

If we discount the possiblilty of the coin being tails only, we still have a zero chance of the coin being heads only. So both scenarios will give almost the same result - probability of a fair coin is 100%.

# Question 16. *[[Math Methods/Probability/Bayes' Theorem#Bayes Factor\|Bayes factor]]*.
>Also uses [[Math Methods/Probability/Binomial Distribution\|Binomial Distribution]])

*Wolbachia* bacteria can infect insects eggs and distorts the sex ratio to create more females.

Our three hypotheses are $H_0$ there is no sex ratio distortion, $H_1$ there is W infection, $H_2$ there is some other sex ratio distortion.
$P(H_0)=0.9$ and $p=q=0.5$
$P(H_1)=0.09$ and $p=0.8$, $q=0.2$
$P(H_2)=0.01$ and unknown sex ratio

First set of data: $n=30, k=21$ (where $k$ is number of females)
$$P(data|H_0)={n \choose k}p_{H_0}^k q_{H_0}^{(k-1)}$$
	$={30 \choose 21}0.5^{21} * 0.5^9={30!\over21*9}*0.5^{30}=0.0133$
$P(data|H_1)={30 \choose 21}0.8^{21} * 0.2^9={30!\over21*9}*0.5^{21} * 0.5^9=0.0676$

And the Bayes factor is 0.197

Since we are just looking at the factor we don't need the total probability to get the posterior probability ratio. We couldn't calculate the total probability since we don't know the sex ratio from $H_2$.$${P(H_0|data)\over P(H_1|data)}={P(data|H_0)P(H_0)\over P(data|H_1)P(H_1)}={0.0133 * 0.9\over0.0676*0.09}=1.97$$
It's still more likely that we have the null hypothesis (no sex ratio distortion), but its getting close.

If in our next test we have $n=30, k=26$, using the same formula but this time let's just look at the factors$${P(H_0|data)\over P(H_1|data)}={P(data|H_0)P(H_0)\over P(data|H_1)P(H_1)}={{30 \choose 26}* 0.5^{30} * 0.9\over {30 \choose 26}*0.8^{26}*0.2^{4}*0.09} ={0.5^{30}\over 0.8^{26}*0.2^4}*10=0.00192$$
So now it is much more likely that there is a Wolbachia infection than that there is a normal sex ratio.

Given this scenario, let's plot the resultant Bayesian values as a function of $k$ with constant $n$:
```desmos-graph
left = 19
right=26
top=12
---
y= 10*(0.5)^{30} / ((0.8)^{x} * 0.2^{(30-x)})
```
So once we reach $k=22$, it becomes more likely that you have a Wolbachia infection than normal sex ratio. Note that this function is not continuous will only make sense with integers.