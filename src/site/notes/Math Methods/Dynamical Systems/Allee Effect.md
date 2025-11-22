---
{"dg-publish":true,"permalink":"/math-methods/dynamical-systems/allee-effect/"}
---

Let's look at a function with another equilibrium:

```desmos-graph
left = -0.5
right = 7
---
y = -5\sin(x)
```

There are two locally stable equilibria at N=0 and N=6 ish. There is an unstable equilibria between them - this is the Allee threshold. 

In this example, a very small population below or at the Allee threshold will be declining, but once they pass that threshold they will have a positive $f(x)$ reaching up to the higher stable equilibria. Important in conservation bio

This principle applies to even more complex functions - stable and unstable equilibria **always alternate**.