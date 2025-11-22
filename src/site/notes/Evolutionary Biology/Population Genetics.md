---
{"dg-publish":true,"permalink":"/evolutionary-biology/population-genetics/"}
---

Prof. Frederic Guillaume, Nov 3 2025

Related to [[Ecology/Population Ecology\|Population Ecology]]
# References
Primer on PopGenetics Genomics, Daniel Hartl, Oxford 2020 (background reading)
# Intro
- Evolutionary Dynamics of genetic variation on a population
- Kind of variation, how its maintained and how it changes
	- Why are individuals in a population or between populations different from each other?
	- This is of course the basis of [[Evolutionary Biology/Evolution - Intro\|Evolution - Intro]], and the result of [[Evolutionary Biology/Natural Selection\|Natural Selection]]
## Mutation
- The ultimate source of genetic variation
- Due to errors in DNA replication
- Mutation rate depends on the size of the geonome - more complex organisms with larger geonomes have a higher mutation rate, but more of their geonome does not code for anything. So there are more silent mutations
### Structural mutations
- Some mutations lead to structural changes in the chromosomes, making them bigger or smaller or splitting or joining them
	- Deletion, duplication, 
	- "macro" mutations that are important for speciation because they stop chromosomes from recombination:
		- inversion, fission, fusion
### Effects of mutation
- Silent mutations effect a part of the gene sequence that doensn't translate into proteins
- Neutral (or synonymous, if they don't affect protein coding) mutations might affect proteins, but don't affect fitness
- Selection Coefficient $s$ describes the effect of a mutation on fitness. Higher $s$ means that a mutation will become more frequent in a population over time. Most mutations have $s$ negative or close to 0 (mildly deleterious), some neutral, and very few are positive.
## Evolutionary Forces
Population genetics describes how mutation frequency changes over time and is explained by evolutionary forces:
- mutation
- selection
- genetic drift
- migration
- recombination
## Genotype and Allele frequencies
- If we consider random mating for the alleles$A_1$ and $A_2$ (three genotypes):
![[EEB-020-PopulationGenetics-2025.pdf#page=11&rect=3,76,306,237|EEB-020-PopulationGenetics-2025, p.11]]
- To convert from number to frequency: divide the number by the total population. e.g. $A_1A_1$ frequency is 0.5 and the others are 0.25.
	- For allele number and and frequency, the actual number of the alleles counted
### Genotype frequencies

|          | Num | Frq         |
| -------- | --- | ----------- |
| $A_1A_1$ | 4   | $4/8 = 0.5$ |
| $A_1A_2$ | 2   | $2/8=0.25$  |
| $A_2A_2$ | 2   | $2/8=0.25$  |
### Allele frequencies

|       | Num | Frq                 |
| ----- | --- | ------------------- |
| $A_1$ | 10  | $p = 10/16 = 0.625$ |
| $A_2$ | 6   | $q = 6/16 = 0.375$  |

- We use $p$ and $q$ to denote allele frequencies, 
- e.g. $p = {\sum A_1 \over 2N}$, with $N = \sum (\text{individuals})$

If you are only given genotype frequencies (and not $N$), you can alternatively calculate allele frequencies $p$ and $q$ directly from genotype frequencies $D, H, R$ (Dominant Homozygote, Heterozygote, Recessive Homozygote):
$$p=D+{1\over2}H$$
$$q=R+{1\over2}H =(1-p)$$
# [[Math Methods/Dynamical Systems/Hardy-Weinberg Equilibrium\|Hardy-Weinberg Equilibrium]]
- In a large population with random mating and following allele frequencies in one locus, after one generation of random mating we end up with the following distributions of genotype frequencies:
![[EEB-020-PopulationGenetics-2025.pdf#page=12&rect=87,27,284,114|EEB-020-PopulationGenetics-2025, p.12]]

## Assumptions of H-W
- No mutation
- No selection
- no migration
- infinitely large population
- random mating, equal number of offspring
- generations are non-overlapping
- meiosis is fair, no segreagation distortion.

So, if there are differences from H-W, that means that one of these is happening.
# [[Evolutionary Biology/Population Genetics - Selection\|Selection]]
- Evolution is fastest when genetic variation in fitness is largest, i.e. when p = q = 0.5
- Selection will cause loss of deleterious mutations and fixation of beneficial mutations.
# [[Evolutionary Biology/Population Genetics - Migration\|Migration]]
(refering to gene flow between [[Ecology/Population Ecology\|populations]], mediated by dispersal)
- Migration works to homogenize allele frequencies between populations
- It can work counter to or along with selection
- Migration rate: $m$
# [[Evolutionary Biology/Population Genetics - Genetic Drift\|Genetic Drift]]
- Reproduction is a **random process**
- Smaller population size increases genetic drift
- Genetic drift reduces heterozygosity
# [[Evolutionary Biology/Population Genetics - Effective Population Size\|Effective Population Size]]
- We can calculate an effective population size for a population that is more useful for modelling
- 
# Population consequences of inbreeding
- Reduction of fitness found in inbred individuals caused by expression of deleterious mutations in homozygotes
- Most new mutations are mildly deleterious and recessive - increased homozygosity causes expression of more deleterious mutations that are otherwise hidden in heterozygotes
- Increased homozygosity is caused by random mating in small populations, or mating among relatives in large populations.
$$\delta = 1 - {W_F \over W_0}$$

## Mutation accumulation in small populations
- In a small effective population where $N_e < (2|s|)^{-1}$, the dynamics of mildly deleterious mutations is dominated by drift. New mutations will quickly become fixed. Since most new mutations are deleterious, small populationswill slowly accumulate them and get reduced fitness and population size. Too many accumulating mutations causes mutational meltdown.
## Example: Florida Panthers and [[genetic rescue\|genetic rescue]]
Isolated panther population with high inbreeding depression. Eight pumas from Texas were introduced to fight inbreeding depression and it worked in decreasing heterozygosity.
# [[Evolutionary Biology/Population Structure\|Population Structure]]
- We can measure genetic difference between populations with $F_{ST}$. The rate of migration (gene flow) can be high enough to change population structure.
# [[Evolutionary Biology/Linkage Disequilibrium\|Linkage Disequilibrium]] (LD)
