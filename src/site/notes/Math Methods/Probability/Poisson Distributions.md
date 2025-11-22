---
{"dg-publish":true,"permalink":"/math-methods/probability/poisson-distributions/"}
---

# Comparison to [[Math Methods/Probability/Binomial Distribution\|Binomial Distribution]]
A Poisson distribution is an extreme case of the binomial distribution when $n$ is very large and $p$ is very small. Thus, the product $np$ is "normal". We call this product $\lambda = np$

$$P(k)={\lambda^k\over k!}e^{-\lambda}$$

We could prove this formula from the [[Math Methods/Probability/Binomial Distribution#Binomial Formula\|Binomial Formula]] $P(k)={n \choose k}p^k(1-p)^{n-k}$. For our purposes it suffices to that the two formulas are basically the same.

# Example: Mutations over time
Like in [[Evolutionary Biology/Population Genetics#Mutation\|Population Genetics]]

Probability of getting one specific gene in one generation:

Mutation rate in one allele in one generation: 
$p=10^{-6}$
Looking at Drosophila, which has $n=10^4$ genes

$\lambda = np=0.01$

Probability of no mutations ($k=0$):
$$P(k)={\lambda^k\over k!}e^{-\lambda}$$
Not sure why she wrote this:
$P(0)=(1-10^{-6})^{10^4}$

Using Poisson dist:
$P(0)={(0.01^0)\over 0!}e^{-0.01}={1\over1}e^{-0.01}=0.990055$

# Probability of female having surviving offspring
[[Eco-Evo Dynamics/Population Dynamics\|Population Dynamics]]
If fecundity $\lambda = 2$ 
(a female on average needs to produce two offpsring to maintain population. $p$ is probability of survival of offspring and $n$ is offspring population so in a stable population $np=2$)

$P(0)={2^0 \over 0!}e^{-2}=e^{-2}=...$
$P(1)={2^1\over 1!} e^{-2}=2e^{-2}$
$P(2)={2^2\over 2!} e^{-2}=2e^{-2}$
$P(3)={2^3\over 3!} e^{-2}={4\over3}e^{-2}$
Then it decreases from here.
# What is the lowest possible $n$ for Poisson to be valid
- In theory, $n$ must be near infinity
- In reality, the approximation is close enough when the product lambda is close enough to the result of the binomial distribution. Think of the example graphs from the slides.
# Skellam model for plant population size
We have $m$ possible sites for plants. $n$ sites occupied and $m-n$ are empty

Each plant produces $\alpha$ seeds, so we have $\alpha n$ seeds produced each year.

If we have many sites, $m \to \infty$

Probability of a site being occupied $p$
$p={1\over m} \to 0$
Seeds produced:
$\alpha n \to \infty$

$\lambda = \alpha n p = \alpha {n\over m}$

Let's call the fraction of sites occupied $n/m$: $=x$ 
And $\xi$ is the number of seeds in our "focal" site.

$$P(k)={\lambda^k\over k!}e^{-\lambda}$$
## Fraction of sites occupied in the next time step
In the next year, every site will be occupied ($m=n, x=1$), minus the ones that had zero seeds. $P(0)$ from a Poisson distribution will give us the probability of zero seeds reaching a site:

$$P(0)={\lambda^0\over 0!}e^{-\lambda}=e^{-\lambda}$$

So, combining our theory with this equation gives us:
$$x_{t+1}=1-P(0)=1-e^{-\alpha x_t}$$

## At [[Math Methods/Dynamical Systems/Equilibria and Stability\|equilibrium]]
When there is no change, $x_{t+1}=x_t$. We call this value $\hat{x}$.
$$\hat{x}=1-e^{-\alpha \hat{x}}$$
If we plot $x_{t+1}$ (y axis) and $x_t$ ($\alpha = 2$ for this example):
```desmos-graph
bottom=-0.5
top=2
left=-0.5
right=4
---
a= 2
y=1-e^{a(-x)}
```

We cannot solve this for x. But we can solve it for alpha, so let's try that, and use that solution to figure out how the equilibrium varies with alpha:

$$ln(e^{-\alpha \hat{x}})=ln(1-\hat{x})$$
$$\alpha=-{ln(1-\hat{x})\over \hat{x}}$$
Here is a new function. What does this look like? Plotting alpha as a function of $\hat{x}$:
```desmos-graph
left=-0.1
right=1.5
---
y=-(\ln(1-x))/x
```

If we swap axes (x as a function of alpha):
```desmos-graph
bottom=-0.1
top=1.5
---
x=-(\ln(1-y))/y
```
So, as alpha (seeds produced per occupied site) increases to 5, the equilibrium value of x approaches 1.

Each plant needs to produce at least one seed for the model to work. When alpha is one (produces one seed), the equilibrium population size (ratio) is zero.

When alpha gets close to five, nearly every site is occupied - every site gets many seeds and there is lots of competition.

## Introducing a second species ([[Ecology/Competition\|Competition]])
Let's say there is a second species that is more fecund but less competitive. If seeds from both species land in the same site, species A will always outcompete, but species B produces more seeds overall. This is a competition-colonization [[Evolutionary Biology/Trade-off\|Trade-off]].

Eva leaves this as an exercise to us to try and figure out how these relate.