---
{"dg-publish":true,"permalink":"/ecology/spatial-dependence/"}
---

# Definition
The similarity of a variable as a function of spatial location only

# Example - [[Island Biogeography\|Island Biogeography]]
- Ignoring the distance from mainland, let's see what the relationship to distance from one island and their richness (Pairwise comparison)
- Positive correlation between distance and difference in richness

# Autocorrelation
![[Lecture 9-SpatialEcology.pdf#page=29&rect=263,187,712,368|Lecture 9-SpatialEcology, p.29]]
$w_{ij}$ is the spatial weight of $i$ and $j$ (related to its distance)
- Values near zero mean no pattern
- Positive values is that neighbors tend to be similar
- Negative is neighbors tend to be different (in a pattern)
$S$ is the sum of all $w_{ij}$
## Example:
A correlogram looks at the Moran's I for groups of data with a similar distance (pairwise comparison and shows them all on a graph

# Spatial Dependence as a Problem, or as a signal
- Autocorrelation means that nearby observations are more related than expected by chance
- This can result in a false positive for another statistical test
	- In ecology it is very common to have spatial patterns in data, so it is important to isolate which variable you are looking at and try to see if something explains it
- Linear models are the basic tool used in biology,
	- The residuals are unexplained variation after accounting for predictors
### Assumption of independence
Linear models assume that these residuals are independent and identically distributed, but if spatial autocorrelation exists this will bias the results by creating variability in the residuals.
This means either:
- We have a statistical problem, and samples are not independent
- We could be missing an important variable which has a spatial structure, which is not accounted in our model
## Example ([[Island Biogeography\|Island Biogeography]])
- If we look at a linear model between species richness and island area, it is spatially autocorrelated
	- This is accounted for by the distance from the mainland
	- If we plot the model residuals vs distance from mainland, it shows that there is a clear correlation between distance from the mainland and our variable
- If instead we model the richness vs Area and distance to continent in a new model, we remove these residuals and have a higher degree of correlation and significance. Moran's I is also close to 0
# Adding more variables
By adding more variables to the [[Ecological Modeling\|model]], we can reduce autocorrelation down to not significant values
- each variable is spatially structured:
	- Mean Temperature
	- Annual actual evapotranspiration
	- mean daily temperature in coldest month
	- range in elevation
	- annual potential evapotranspiration
- This is related to [[PaleoenvironmentalReconstruction/Principal Component Analysis\|Principal Component Analysis]]