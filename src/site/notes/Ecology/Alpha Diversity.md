---
{"dg-publish":true,"permalink":"/ecology/alpha-diversity/"}
---

# Taxonomical
- Structure of an ecological community with respect to:

![[Lecture 8_Community Ecology Lecture Slides.pdf#page=19&rect=59,92,908,318|Lecture 8_Community Ecology Lecture Slides, p.19]]
Magurran et al 2004 - "The bible on measuring diversity"
## Richness-based metrics (such as species richness)
- Species richness is the most common richness metric
- Increases with sampling effort
	- Species accumulation curves: plot of number of samples vs number of species
	- only accurate if sampled at asymptote which can never really be reached
- highlights rare species - species with many rare species are over-emphasized
- Assumes entire species is sampled
### $Chao$
- Useful when there are many undetected/invisible species
- This is an estimate of absolute number of species based on the rare species
![[Lecture 8_Community Ecology Lecture Slides.pdf#page=27&rect=60,11,944,306&color=yellow|Lecture 8_Community Ecology Lecture Slides, p.27]]
- Issue: If you have no double species, you need to use an "adaptation":
$$Chao = S_\text{obs} + \frac{(F_1 - 1)^2}{2}$$
- $Chao2$ is another estimate that works with just presence/absence data
## In-between metrics (between richness and evenness)
### **Shannon Index**
- Assumes you have represented all species in the sample
![[Lecture 8_Community Ecology Lecture Slides.pdf#page=34&rect=9,7,933,431&color=yellow|Lecture 8_Community Ecology Lecture Slides, p.34]]
- Since it's a sum, you go over each species and sum them all up
- If you have a low number, that indicates a few species dominate the community
- Unconstrained, so it's not useful to compare two communities with different overall species richness
	- Ranges from $0$ to $ln(\text{community species richess})$
- Requires abundance data (does not work with presence/absense)
## Evenness-based metrics
- (distribution of abundances), balance of species

In this example, they have the same richness, but Cat's Hill is more even:
![[Lecture 8_Community Ecology Lecture Slides.pdf#page=20&rect=66,42,887,491&color=yellow|Lecture 8_Community Ecology Lecture Slides, p.20]]
### Simpson's Index $D$:
- Probability that any two individuals drawn at random are from the same species
- This is a measure of **dominance** not ***evenness***
- Maximum is 1, in a community with only one species, or close to that if you have a community completely dominated by one species
- Therefore, it's often expressed as $1-D$ or $1/D$ so that it increases with diversity
![[Lecture 8_Community Ecology Lecture Slides.pdf#page=37&rect=278,53,926,299&color=yellow|Lecture 8_Community Ecology Lecture Slides, p.37]]
- Or in R (with sample data from our example in slides):
```R
v <- c(
  35, 26, 25, 21, 16, 11
)
D <- 0
for (i in v){
  D <- D + (i/sum(v))^2
}
> D
[1] 0.186233
```
### Simpson's measure of evenness $E_{1/D}$
- Confusingly this is different from Simpson's Index
![[Lecture 8_Community Ecology Lecture Slides.pdf#page=41&rect=90,130,888,336&color=yellow|Lecture 8_Community Ecology Lecture Slides, p.41]]
#  [[Ecology/Functional Trait\|Functional]]
- Measuring traits and how they function in the ecosystem
- Using a "functional space" plot (x = trait 1, y=trait 2), we can measure these three components:
- Three main components
![[Lecture 8_Community Ecology Lecture Slides.pdf#page=46&rect=14,-1,960,424&color=yellow|Lecture 8_Community Ecology Lecture Slides, p.46]]
## Functional Richness
- Total variation in the functional traits
## Functional Evenness
- Decreases when:
	- Functional distances among species are less even
	- Abundances are less evenly distributed among species
## Functional dispersion
- How far the abundance is from the mean of both
# [[Evolutionary Biology/Phylogenetics\|Phylogenetics]]
- Breadth of evolutionary history
- Essentially, you just add up the branch lengths on a phylogenetic tree