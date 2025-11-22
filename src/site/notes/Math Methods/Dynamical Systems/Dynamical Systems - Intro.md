---
{"dg-publish":true,"permalink":"/math-methods/dynamical-systems/dynamical-systems-intro/"}
---

Part 1: Simple models and calculus
Part 2: Probability
Part 3: Vectors andmatrices

## Write down anything about math
Derivative of ln(x) = 1/x

## Exponentials, parabola, population genetics
$f(x) = x^2$
Even parabola centered on 0,0

$$f(x) = 2x(1-x)
 = 2x - 2x^2 $$
	
or
$$H = 2pq = 2p(1-p)$$
(Hardy-Weinberg formula for heterozygote frq in population genetics)

This is an inverted(downward opening) parabola centered on $(x, y) = (0.5, 0.5)$ 

## Hyperbola, saturating functions
$$φ(x)=βx / (1 + αx)$$
This function will converge at a point called by mathematicians an *asymptote* and by biologists a *saturation point* equal approximately to $β/α$ (limit to infinity). We call this a concave function since its rate of increase gets smaller over time. 

Positive exponential functions and parabolas are *convex* functions since they increase more and more over time.

## Exponential curve for population growth
$$ N(t) = N_{0} e^{rt}$$
If the coefficient r is greater, the amount of time required to reach a given population is reduced.

### Radioactive decay
$e^{-x}$ with a negative exponent can be used to show these negative values
$$L(t)= a -be^{-{\mu}t}$$
Where $a$ = 3, $b=1.5$ and $\mu = 0.7$
```desmos-graph
left = -0.5
bottom = -0.5
---
a = 3
b = 1.5
\mu = 0.7
y= a - be^{-\mu t}
```
