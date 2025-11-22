---
{"dg-publish":true,"permalink":"/math-methods/dynamical-systems/optimal-virulence-of-pathogen-homework/"}
---

This is related to the function we learned in [[Ecology/Disease Ecology\|Disease Ecology]]
![[hw.pdf#page=10&rect=63,74,552,571|hw, p.10]]
![[hw.pdf#page=11&rect=59,651,536,720|hw, p.11]]

## Disease reproduction and virulence
$\alpha$ -> Rate of death (virulence)
$v$ -> rate of recovery
rate of dissapearance = $\alpha + v$ (ignoring natural death which is small)

average length of infection: $1/(\alpha + v)$ time units
$\beta$ -> number of other hosts infected per unit time
$R_0$ -> basic disease reproduction number
$$
R_0 (\beta) = {\beta \over \alpha + v}
$$
## Relation of virulence to transmission:
$$
\alpha (\beta) = a \beta
{ #2}
 + b \beta + c
$$
Where $a>0$ and $b,c \ge 0$ 
## Optimal rate of infection for reproduction
Combine the two functions:
$$
R_0 (\beta) = {\beta \over (a \beta
{ #2}
 + b \beta + c) + v}
$$
Take derivative (quotient rule):
$$
R'_0(\beta) = {-a\beta^2+c+v \over a \beta
{ #2}
 + b \beta + c + v}
$$
Optimum will be when derivative is zero. We can ignore the denominator and solve for $\beta$ to get $$\beta_{opt} = \pm \sqrt{c+v \over a}$$
## Virulence at optimal rate of infection:
$$\alpha (\beta_{opt}) = 2c + v + b \sqrt{c+v \over a}$$
# Optimal virulence increases with treatment
Since increasing rate of recovery $v$ makes $\beta_{opt}$ (and thus $\alpha$) increase.
# Probability of death with changing recovery rate
$p = \alpha / (\alpha + v)$ is the probability of death.
If $\alpha$ assumes its optimal value with increasing recovery rate $v$, the formula is:

