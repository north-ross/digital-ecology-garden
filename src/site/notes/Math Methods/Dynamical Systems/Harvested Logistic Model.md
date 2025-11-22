---
{"dg-publish":true,"permalink":"/math-methods/dynamical-systems/harvested-logistic-model/"}
---

$${dN\over dt}=rN \left[ 1-{N\over K} \right] -hN$$
This is the [[Logistic Model\|Logistic Model]] modified to include the rate of harvest $h$.

# Equilibria
Let's first reformat it to look more like the original logistic equation (from [[Math Methods/Dynamical Systems/Equilibria and Stability\|Equilibria and Stability]], since r and h are both constants:
$$
{dN \over dt}= (r-h)N[1-{N \over (K/r)(r-h)}]
$$
Now this has the growth $r$ (in original logistic equation) = $r-h$
And the carrying capacity $K$ is now ${r-h \over r} K$

So, just like the original, we have a trivial equilibrium at $\hat N_1 = 0$ and other at the carrying capacity $\hat N_2 = {r-h \over r} K$.

# Stability
Using the product rule, we can find that $f'(0) = r-h$ . So, at $\hat N_1$, its negative (stable) when $r<h$ and unstable otherwise.

The reverse is true for $\hat N_2$.

In other words, if the rate of harvest is higher than the growth rate, the population is only stable when $N=0$ (it is extinct). If the rate of harvest is less than the growth rate, it is stable at the carrying capacity (including factor)

# Bifurcation Diagram
![[mathematical-methods-lecturenotes.pdf#page=54&rect=56,469,546,744|mathematical-methods-lecturenotes, p.54]]
0 is always an equilibrium. We can never talk about negative population sizes. So realistically, h>r
We call this point when $h=r$ a transcritical bifurcation point, since this is a point where the two equilibria switch stability.

## Fold bifurcation point
An example of another kind of bifurcation point is in [[Math Methods/Dynamical Systems/Predator-prey dynamics with Holling type II functional resonse\|Predator-prey dynamics with Holling type II functional resonse]]:

($P$ is number of predators here)

![[mathematical-methods-lecturenotes.pdf#page=57&rect=55,460,546,737&color=red|mathematical-methods-lecturenotes, p.57]]

$P_T$, the transcritical bifurcation point, is where $N=0$. 

The new one is the fold bifurcation point $P_F$, the maximum number of predators. This is what conservation biologists are afraid of. At first, it seems like the population is decreasing with number of predators, but is still stable. However, once we reach this fold bifurcation point, the population can crash without warning. It a transcritical bifurcation point at N=0, the population can still increase if it is very small. But with this fold bifurcation, even if a population is reintroduced, it will still decrease until the number of predators are reduced ($P < P_F$ and the population is above this point.) This is called hysteresis (dependence of a system on its history).

# More complex example
[[Math Methods/Dynamical Systems/Time Scale Separation\|Time Scale Separation]]