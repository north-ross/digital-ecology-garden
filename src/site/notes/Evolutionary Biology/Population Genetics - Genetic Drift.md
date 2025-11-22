---
{"dg-publish":true,"permalink":"/evolutionary-biology/population-genetics-genetic-drift/"}
---

- The allele frequency after reproduction $p'$ is not konwn exactly.
- Fluctuation of genotype frequencies depends on population size - it will be much more variable in smallerpopulations and not match [[Math Methods/Dynamical Systems/Hardy-Weinberg Equilibrium\|Hardy-Weinberg Equilibrium]] as much.
## Binomial Distribution
- [Wikipedia](https://en.wikipedia.org/wiki/Binomial_distribution)
The probability of receiving a certain number of copies of one allele in a new generation is given by the [[Math Methods/Probability/Binomial Distribution\|Binomial Distribution]]:
$$\text{Var}\{p\} = {pq \over 2N}$$
- Smaller $N$ means larger variation, meaning genetic drift is stronger in small populations. In small populations, alleles are more likely to be purged or become fixed compared to a larger one.
- These are the equilibrium points ($p=0$ and $p=1$)
- Probability of fixation of a new mutation: $p=1/2N$
- Expected time to fixation is directly proportional to $N$ and inversely proportional to $p$.
	- For a new mutation, time to fixation is around $4N$? Units?
# Heterozygosity changes
Heterozygote frequency $H$ at time $t$ is given by:
$$H_t = H_0 \left( 1- {1\over 2N} \right)^t$$
Meaning that heterozygosity changes by $\Delta H = -{1 \over 2N}$ each generation.

# Founder Effect
- A genetic bottleneck event can have long lasting effects on health of concerned population.
# Conclusions
- Leads to random fixation of alleles at a locus
- Because of fixation, genetic drift results in less heterozygosity, meaning genetic diversity will erode over time
- INcreases the variance in allele frequencies between populations, meaning populations will become more genetically different from each other (assuming no [[Evolutionary Biology/Population Genetics - Migration\|Population Genetics - Migration]])