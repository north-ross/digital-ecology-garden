---
{"dg-publish":true,"permalink":"/math-methods/probability/probability-of-exponential-decay/"}
---


Given the exponential decay operation
$$x(t)=x(0)e^{-\alpha t}$$
$\alpha$ is the rate of decay
$\alpha(dt)$ is the probability of decay in the next infinitessimal time interval $dt$.

$$P(\text{exisiting at time }t)={x(t)\over x(0)}=e^{-\alpha t}$$
let's find the probability that one particle did not decay at any time between time 0 and time $t$.

If we consider infinitely many small intervals $dt$, where $n\cdot dt=t$ (thus $n$ is close to infinity)

$$P(\text{not decaying in }dt)=1-\alpha dt$$
So, the probability of the particle not decaying during any of these tiny intervals:
$$P(\text{exisiting at time }t)=(1-\alpha dt)^n$$
Taking the logarithm:
$$ln(P(\text{exisiting at time }t))=n\cdot ln(1-\alpha dt)$$
Consider the plots of $y=ln(x)$ (blue) and $y=x-1$ (green):
```desmos-graph
left= -2
bottom= -2
top=2
right=3
---
y=\ln(x)
y=x-1
```
We can see that $ln(x) \approx x-1$ when $x\approx 1$. Since we were considering $x = 1- \alpha dt$, this means that when 

At this point, $-n\alpha dt$


# Conclusion
Exponential distribution: The probability of dying between $t$ and $t + dt$ is given by:
$$P(\text{decay between }t\text{ and }t+dt)=e^{-\alpha t}\alpha dt$$

We call the important part of this the probability density function:
$$f(t) = e^{-\alpha t}\alpha$$