---
{"dg-publish":true,"permalink":"/math-methods/dynamical-systems/time-scale-separation/"}
---

Imagine two situations (prey and predator) with the [[Math Methods/Dynamical Systems/Equilibria and Stability\|logistic growth]] :

1. Prey, changes fast:
$$
{dN\over dt} = r(1-N/K)N - \beta NP
$$
2. Predator, changes very slowly:
$${dP\over dt} = \gamma \beta NP - \delta P$$

$K$ is prey carrying capacity
$\beta$ is capture rate of searching predators
$\delta$ is predator death rate
$\gamma$ is conversion rate - if predator eats one prey, it turns it into $\gamma$ offpsring
$r$ is prey growth rate

Since the number of predators changes slowly, we can sort of consider $P$ as a constant in formula 1. This gives us the prey "quasi-equilibrium"  $\hat N_2 = {r-\beta P\over r} K$, if $r > \beta P$.

(using same method as [[Math Methods/Dynamical Systems/Harvested Logistic Model\|Harvested Logistic Model]])

For the predator function, if the prey can be assumed to always be close to its quasi-equilibrium, we can model the predator change over this slower time (years for example):
$${dP\over dt} = {\left[ \gamma \beta {r-\beta P \over r}K - \delta \right]} P$$
$${dP\over dt} = \left[(\gamma \beta K - \delta) - {\gamma \beta^2 K \over r}P \right] P$$
$${dP\over dt} = (\gamma \beta K - \delta) \left[1 - {P \over {r \over \gamma \beta^2 K}(\gamma \beta K - \delta)} \right] P$$
This last one looks like the logistic function again. So we know that we have the *intrinsic growth rate* $\gamma \beta K - \delta$ and the *carrying capacity* ${r \over \gamma \beta^2 K}(\gamma \beta K - \delta)$

This shows that the trivial equilibrium $\hat P_1 = 0$ is stable if $\delta > \gamma \beta K$, meaning the predator population will always trend to zero if this is met.

The predator is only *viable* if $\gamma \beta K > \delta$ - they need to be able to catch enough prey, produce enough offspring and prey needs a large enough carrying capacity to exceed their death rate.

# Predator population model
```desmos-graph
left=-0.5
top=5
---
g = 1
B = 1
K = 3
d = 1.2
R = 0.8

y=(gBK-d) (1-x/((R/gB^2K)gBK-d))x
```
