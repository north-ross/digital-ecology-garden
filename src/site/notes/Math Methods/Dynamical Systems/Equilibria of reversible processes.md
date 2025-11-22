---
{"dg-publish":true,"permalink":"/math-methods/dynamical-systems/equilibria-of-reversible-processes/"}
---

## First, simple example
![[mathematical-methods-lecturenotes.pdf#page=50&rect=255,432,337,487|mathematical-methods-lecturenotes, p.50]]
$x$ = conc. of A
$K-x=$ conc. of B
$$
{dx \over dt} = -\alpha x + \beta (K-x) = f(x)
$$
$$
f(x) = \beta K - (\alpha + \beta)x
$$
### Equilibria
FInd the equilibria ($f(x) = 0$):
$$
\beta K = (\alpha + \beta)x
$$$$
\hat{x} = {\beta \over \alpha + \beta}K
$$
There is only one equilibrium here, since there is only one solution to $f(x)$ (linear function).

### Stability
$f'(x)=-(\alpha + \beta)$ 
This is always negative for all possible values of x, so the only equilibrium is globally stable.

## Second example

![[mathematical-methods-lecturenotes.pdf#page=51&rect=67,62,559,236&color=red|mathematical-methods-lecturenotes, p.51]]
### Equilibria
$\hat{c}$ is the solution to the quadratic equation - no easy way to do this, needs the quadratic formula. We will just not solve it but know that's what it is.
### Stability
$f'(c) = -k_1(a_0-c) - k_1(b_0-c) - k_2 <0$
This is always negative, since $a_0 - c$ and $b_0 - c$ are both concentrations and must be positive, and the rates $k_1,k_2$ are both positive.

This means that any equilibrium that exists must be stable, since the derivative is always negative

Since equilibria always must alternate between stable and unstable, there must only be one true equilibrium. This is a problem, since the quadratic formula will give us two solutions. Let's plot the function to examine:

$a_0=0.5, b_0=0.6, k_1 = 0.8, k_2 = 0.4$
```desmos-graph
left=-0.3;right=1.5; bottom=-1;top=1
---

y = 0.8(a-x)(b-x) - 0.4x
a=0.5
b=0.6
(0, 0.8*a*b)|label: k_1*a_0*b_0
(a, -(0.4 * a))|label: The actual maximum value of c
```
Looks like theres two solutions, but due to conservation of mass, A + B = C must be true.

So c must be less than or equal to the mnimum of 

So actually, the second (higher) root around $c = 1.4$ isn't real, since c must be less than or equal to the minimum of A and B. 
$$c \le min(a_0,b_0)$$
In this case, the minimum of these two is $a_0 = 0.5$, so this is actually the maximum value of our formula. So there is only one, stable equilibrium around c ~ 0.2.

# Predator-prey dynamics with functional resonse
![[mathematical-methods-lecturenotes.pdf#page=55&rect=63,76,558,542&color=red|mathematical-methods-lecturenotes, p.55]]
## Equilibria:
Trivial equilibrium $\hat{N}=0$
Two quadratic solutions: $\hat{N} = -1/\beta T$ and $\hat{N} = K$
Then, there are more equilibria along the line $f(x) = \beta P$, since this is where the quadratic must be equal to this to solve to zero
- Stable equilibrium at the intersection of this line and the parabola when
### Special equilibrium
If there was a very precise number of predators such that  $\beta P$ is equal to the exact maximum of our parabola, this equilibrium would be both stable and unstable, and also the only equilibrium other than the trivial one. We call this point $P_F$ the fold bifurcation point

## Bifurcation Diagram
This can be used to show the stability of the equilibria:.

We plot N as a function of P:
![[mathematical-methods-lecturenotes.pdf#page=57&rect=55,460,546,737&color=red|mathematical-methods-lecturenotes, p.57]]
The transcritical bifurcation point $P_T = 0$. We will come back to this later.