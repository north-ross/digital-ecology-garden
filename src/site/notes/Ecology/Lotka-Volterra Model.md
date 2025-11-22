---
{"dg-publish":true,"permalink":"/ecology/lotka-volterra-model/"}
---

Shiny App to help understand the model: https://ecoevoapps.shinyapps.io/lotka-volterra-competition/

- This model describes how a population will grow until it reaches the carrying capacity. Growth -> 0 as N -> K
![[Lecture 3_SpeciesInteractions_Slides_2025-1.pdf#page=12&rect=26,63,896,504|L3_SpeciesInteractions_Slides_2025-1, p.12]]
 $$\frac{d N_1}{d t} = r_1 N_1 \frac{K_1 - N_1 - \alpha_{12}*N_2}{K_1}$$
$\alpha_{12}$ represents the effect of competition between species 1 and 2. When $N_2=0$ then $N_1 = K_1$ and $N_2 = {K_2}/{\alpha_{21}}$.

By calculating values for these constants, we can hypothesize how two species will interact with changing conditions

Experiment on grassland communities shows that competitive interactions between many species in an environment with an agressive introduced species, thereis not ver much competition between native species.

## Predation in Lotka-Volterra model:
$$\frac{dN_h}{dt} = r_hN_h - cN_hN_p$$
$N_h$ = number of hosts (prey)
$N_p$ = number of predator
$c$ = predator efficiency
$$\frac{dN_p}{dt} = fcN_hN_p - d_pN_p$$
$d_p$ = Predator death rate
$fc$ = Predator reproductive efficiency
