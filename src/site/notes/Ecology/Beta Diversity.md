---
{"dg-publish":true,"permalink":"/ecology/beta-diversity/"}
---

Differences between two sites.
- Higher beta diversity = more different sites
# Taxonomic

# [[Ecology/Spatial Ecology\|Spatial]]
- Two communities become more dissimilar as distance increases
# Temporal
- Two communities may become more dis-similar as time between them increases, e.g. gain or loss in diversity
# Is high beta-diversity good?
- Depends on dispersal/recolonization capacity of the species and how they exist in the ecosystem

## Measures
### Sorensen's
- Effective for Presence/Absence data (no counts needed)
![[Lecture 8_Community Ecology Lecture Slides.pdf#page=55&rect=85,93,944,299&color=yellow|Lecture 8_Community Ecology Lecture Slides, p.55]]
In our example, we had 10 species that were shared between Juri and I's sample vs Ece and Lynneva's sample, we had one species not in theirs, and they had 5 that we didn't have. Therefore:
$a = 10, b=1, c=5$
$$C_S = \frac{2(10)}{2(10) + (1) + (5)} = 0.77$$
### Bray-Curtis Index (AKA Sorenson's quantitative index)
- This is similar to Sorenson's but accounts for number of individuals
- $N_j$ is the lower abundance number of the species found in both sites
- In our example, we had:
$N_j = 1+3+6+1+2+3+1+{...}= 20$
$$C_N = 1-\frac{2N_j}{(N_a + N_b)}$$
# Non-taxonomic
- [[Ecology/Functional Trait\|Functional]] and phylogenetic metrics can be used again as in Alpha
- Often partitioned into **nestedness** of communities and **turnover** of communities, although in reality beta-diversity is a result of both of these
## Nestedness
- Loss or gain of species/functions/phylogeny
- One site has a subset of species found in another
## Turnover
- Replacement of species/functions/phylogeny in a community
- Complete turnover = no change