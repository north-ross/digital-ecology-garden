---
{"dg-publish":true,"permalink":"/ecology/population-ecology/"}
---

Marjo 2025-09-16
[[Lecture 7_population Ecology_2025.pdf]]

# Estimating Population Size
## Unitary Organisms
### Direct Count
Not usually possible except in specific locations
### Estimating population 
#### Based on probability
$$N = \frac{\text{Number of individuals in the sample}} {\text{Estimated probability of detection } (P)}$$
Example: In Åland, students usually get 60% of the population in a transect
#### Mark-recapture method
![[Lecture 7_population Ecology_2025.pdf#page=11&rect=128,143,956,388|Lecture _population Ecology_2025, p.11]]
#### Quadrant
Pick a small area and count all organisms in it, then extrapolate to entire study area
#### Accumulation curve
- Total number of unique genotypes taken from environmental samples
![[Lecture 7_population Ecology_2025.pdf#page=13&rect=32,73,948,420|Lecture 7_population Ecology_2025, p.13]]
## Modular organisms
- Difficult to define what is an individual
- Must evaluate the fraction of organisms within a sample are that are detected
	- e.g. percent ground cover by this organism
	- use genetic tools to isolate individuals
# Population Growth Rate
![[Lecture 7_population Ecology_2025.pdf#page=16&rect=22,58,947,491|Lecture _population Ecology_2025, p.16]]
Determined by:
- Births
- Deaths
- Immigration
- Emigration
Mathematical modesls can predict future population sizes given current information:

## Models
### Discrete-time growth rate models 
- (discrete periods where population can increase
- e.g. birds with one generation per year and synchronous reproduction
- geometric growth
- Simplified system - change in population is difference between births and deaths
- $\lambda$ is the proportional change over the unit of time. When given the exponent of t, we can predict that many units in the future
![[Lecture 7_population Ecology_2025.pdf#page=21&rect=365,51,900,315|Lecture _population Ecology_2025, p.21]]
### Continuous Time growth rate models (more complicated)
- Exponential growth
- Incorporates density-dependence ([[Ecology/Lotka-Volterra Model\|carrying capacity]])
	- High population density influences both birth and death rates of sparrows in a study
### Simplifications used in above models
- By ignoring immigration and emigration (or estimating the rate of [[Ecology/Evolutionary Ecology\|dispersal]])
	- factor this rate into the model per generation
- Assume no age structure - younger populations will increase faster
	- This can be solved by making a matrix data structure and apply different growth rates to age categories (age specific fecundity / survivorship)
### Factors used in models
#### Density-Dependent factors
- Disease, competition, food availability
#### Density-independent
- Temperature, moisture, unpredictable disturbances, habitat loss
## Summary
Simple models can help predict growth rates, but more complex models are needed to include other influences like dispersal, age structure and environmental influences.

# [[Ecology/Life History Adaptations\|Life History Adaptations]]
Life history traits are adaptations affecting:
# Spatially Structured Populations
- A [[Metapopulations\|Metapopulations]] is a group of spatially separated populations which sometimes interact (dispersal)
- Small populations are prone to extinction, but can be recolonized by other populations
- Metapopulation (the system as a whole) persists in a dynamic equilibrium between local extinctions and recolonizations
## Ilko Hansi 1999
used a model to test his mathematical theories on the butterfly populations of Åland. He found:
- Local extinctions and recolonization is influenced by:
	- Size of habitat and population density
	- Habitat connectivity
	- Stochasticity (random events)
	- Inbreeding
- Applications for conservation biology with small patches
![[Lecture 7_population Ecology_2025.pdf#page=50&rect=35,98,545,363|Lecture _population Ecology_2025, p.50]]