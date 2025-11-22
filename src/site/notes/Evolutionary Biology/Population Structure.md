---
{"dg-publish":true,"permalink":"/evolutionary-biology/population-structure/"}
---

Drift decreases heterozygosity within populations
- [[Evolutionary Biology/Population Genetics - Genetic Drift\|Genetic Drift]] increases differences in allele frequency between populations
- [[Evolutionary Biology/Population Genetics - Migration\|MIgration]] (gene flow) homogenizes allele frequences among populations.
Therefore, we can show mathematically that gene flow between populations counteracts the effect of genetic drift. If the rate of decrease in heterozygosity is proportional to migration rate $m$, the rate of heterozygosity will be balanced.

Reduction in gene flow leads to genetic divergence among populations. This can even be seen in this example with snails on the other side of a street which have different allele frequencies.

## Index of differentiation
$F_{ST}$ is an **index of differentiation** used to measure how genetically differentiated two populations are:$$F_{ST} = {H_T - \bar{H}_S \over H_T}$$
Where:
- $H_T$ is the expected heterozygosity in the total population
	- In practise, measured with observed frequencies:
	- $H_T = 2 \cdot 1/n \sum_i^n p_i \cdot 1/n \sum_i^n q_i =2\bar{p} \bar{q}$
	- Where $n$ is number of sub-populations
- $\bar{H}_S$ is the average of expected heterozygosity in the sub-populations
	- $H_S=1/n\sum_i^n 2p_i q_i=2\bar{pq}$
Therefore, in practice you could also say:$$F_{ST}= {\bar{p} \bar{q} - \bar{pq} \over \bar{p} \bar{q}}$$
Or, at a single locus: (==what does this mean==)
$$F_{ST}= {\text{Var}\{p\} \over \bar{p} \bar{q}}$$
### Key message
Index of differentiation $F_{ST}$ is proportion of total variation that is caused by differences between populations
- $F_{ST} = 0$ means the populations are genetically identical
- $F_{ST} = 1$ means they are fixed for different alleles.
## Divergence among populations due to [[Evolutionary Biology/Population Genetics - Selection\|selection]]
Populations under different ecological conditions can have diverse allele frequencies due to selection. We can use $F_{ST}$ to scan for signs of selection between populations. Example given of oceanic vs freshwater threespine stickleback.

## Migration-Drift Balance
$$F_{ST}={1 \over 1+4N_em}$$
- $N_em$ is the effective number of migrants entering each population at each generation
- $N_em \ge 1$ leads to enough gene flow to counteract the loss of genetic diversity from drift and a lack of variation between populations ($F_{ST} \approx 0$)
- $F_{ST}$ decreases with $m$ - more migration leads to less differences between populations
- **Isolation-by-distance** is obtained when $F_{ST}$ increases with geographical distance, when $m$ becaomes lower between more distant populations.