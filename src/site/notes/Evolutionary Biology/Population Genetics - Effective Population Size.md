---
{"dg-publish":true,"permalink":"/evolutionary-biology/population-genetics-effective-population-size/"}
---

(From [[Evolutionary Biology/Population Genetics\|Population Genetics]] lecture)

- Previously we were only looking at populations that satisfy H-W populations with random mating, non-overlapping generations and constant size, except for the fact that their size is not infinite.
- The [Wright-Fisher](https://stephens999.github.io/fiveMinuteStats/wright_fisher_model.html) model accounts for this finite size, but still relies on other assumptions that are almost never true in nature
- This model is still useful if we convert the actual population into a population of "effective" individuals which do satisfy W-F conditions.
- $N_e$ is the size of an ideal population having the same amount of drift as an observed population of size $N$ - it is a measurement of the strength of genetic drift.
- Amount of drift given by sampling variance in W-F model:
$$\text{Var}\{p\}_\text{exp} = {pq\over2N}$$
Effective population size is:
$$N_\text{exp} = {pq \over 2 \text{Var}\{p\}_\text{obs}}$$

In most cases, $N_e < N$ because:
- Populations change over time
- Number of males and females in the effective population are not equal - for example fewer males contribute to reproduction than females
- some individuals have more reproductive success than others
- variance in reproductive number is greater than expected by chance (i.e. not Binomial)
## Mutation-drift balance
- At ==mutation-drift balance (?)==, heterozygosity and $N_e$ are linked: $$\theta = 4N_e \mu$$where:
	- $\mu$ is the per-nucleotide mutation rate 
	- $\theta$ is per-nucleotide heterozygosity at neutral sites. 
		- Meaning the probability of heterozygosity on all neutral mutation gene loci divided by the number of nucleotides.
- Therefore, we can calculate $N_e$ if we know $\theta$ and $\mu$ for our population.
## Why does $N_e < N$?
### Variation in population size over time
- [Harmonic mean](https://en.wikipedia.org/wiki/Harmonic_mean) population size where population size changes over time $t$: $$N_e ={t \over \sum_{i=1}^t N_i^{-1}}$$
- Harmonic mean gives more weight to small numbers
- We use this mean since small populations lead to large reductions in diversity (bottleneck)
### Variation in number of reproducing adults
$$N_e = {4N_m N_f \over N_m + N_f}$$
- $N_m$ is number of males and $N_f$ is number of females
- If $N_m = 1$ and $N_f = 100$, then $N_e = 4$
- If $N_m = N_f$, $N_e = 2N_f =N$
- Highly polygynous species will have a small $N_e$ . ==harmonic mean?==
### Variation in number of progeny per adult

$$N_e = {4N-2 \over \sigma_k^2+2}$$
- $\sigma_k^2$ is the variance in the number of offspring per adult
- If $\sigma_k^2$ = the variance of a Binomial random process $2(N-1)/N$, then $N_e = N$.
- If $\sigma_k^2$ is larger then expected under random processes, then $N_e < N$. 
	- If the number of offpsring per adult varies more than what is expectedby chance, effective population size is smaller than census size of population.
- If it is smaller than expected, we get $N_e > N$. 
	- So, in a population where every individual has the same number of offpsring, the effective population is higher? 
	- ==What does this actually mean?==

## Genetic Drift and Natural [[Evolutionary Biology/Population Genetics - Selection\|Selection]]
- Genetic drift causes fluctuations in allele frequencies, even if they are under selection
- It's possible that the effect of genetic drift is strong enough to dominate the evolutionary trajectory of allele frequency in a population.
- Genetic drift **sets a limit to natural selection**. So, an allele is **effectively neutral** when:$$|s| < {1 \over 2N_e}$$
- So, because of genetic drift, in a small enough population beneficial mutations can become purged and deleterious mutations can become fixed.
- Inbreeding coefficient $F$ can be estimated by the amount of heterozygosity in a population, which is lower in small populations: $$F = {H_\text{expected} - H_\text{observed}\over H_\text{expected}} \text{, with } H_\text{expected}=2pq$$
- $F>0$ expresses the excess of homozygosity relative to H-W expectation - meaning there is lots of inbreeding and many alleles are fixed
