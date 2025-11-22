---
{"dg-publish":true,"permalink":"/math-methods/dynamical-systems/equilibria-and-stability/"}
---

# Logistic Model Example
## Finding solutions
We can find a solution for this one. But what if we couldn't?
$$
{dN \over dT} = r(1-N/K)N = f(N)
$$
This is a continuous-time model over the time interval $dt$ short time interval

We need to find the values of $N$ where there is no change in $N$ (or $f(N) = 0$).  These points are the equilibria. 
### Trivial Equilibrium
The first solution of this one is obvious:
$$
r(1-N/K)N = 0
$$
$$
\hat{N_1} = 0
$$
This makes sense - there is no growth when the population is zero. THis is the Trivial Equilibrium
### Non-trivial equilibrium
$$\hat{N_2} = K$$
This is the carrying capacity - there is no growth at this point
## Stability Analysis
![[mathematical-methods-lecturenotes.pdf#page=49&rect=52,516,546,762|mathematical-methods-lecturenotes, p.49]]
$K = 10, r = 1$
```desmos-graph
left = -0.5
bottom = -3
right = 15
---
(0,0)|open|label:Trivial equilibrium (unstable)
(K,0)|label:Carrying capacity: Globally stable
r = 1|hidden
K = 10
y=r(1-x/K)x
```
Any popultation lower than $N=K$ trends towards $N=K$. Anything higher than $N=K$ trends to $K$

This shows us that $N=0$ is an unstable equilibrium and $N=K$ is stable equilibrium
# [[Math Methods/Dynamical Systems/Allee Effect\|Allee Effect]]
- See the linked page
## Condition for stability
A point of equilibrium $x$ is stable when $f'(x) < 0$ (and $f(x)=0$) . 
If the derivative is positive, it's a stable equilibrium, if it's negative, it's unstable. 

# Examples:
[[Math Methods/Dynamical Systems/Harvested Logistic Model\|Harvested Logistic Model]]
[[Math Methods/Dynamical Systems/Equilibria of reversible processes\|Equilibria of reversible processes]]
[[Math Methods/Dynamical Systems/Predator-prey dynamics with Holling type II functional resonse\|Predator-prey dynamics with Holling type II functional resonse]]
