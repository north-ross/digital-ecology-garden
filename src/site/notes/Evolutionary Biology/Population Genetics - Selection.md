---
{"dg-publish":true,"permalink":"/evolutionary-biology/population-genetics-selection/"}
---

How [[Evolutionary Biology/Natural Selection\|Natural Selection]] works on population genetics
- Changes allele frequencies unidirectionally
- Rate of frequency change depends on strength of selection, how important it is
- If the deleterious allele is lost from the population, it has been *purged*
## Absolute Fitness
- The likelihood that a certain genotype survives to adulthood.
- $w_{ij}$ is the absolute fitness of genotype $A_iA_j$ 
## Mean fitness
Proportion of survivors in population after selection, according to H-W:
$$\bar{w} = p^2w_{11} + 2pqw_{12} + q^2w_{22}$$
Frequencies of the new genotypes must be divided by $\bar{w}$ to sum to 1:
![[EEB-020-PopulationGenetics-2025.pdf#page=18&rect=3,15,363,57&color=red|EEB-020-PopulationGenetics-2025, p.18]]

### Genotype to allele frequencies:
The frequency of $A_1$ is $p = p^2 + pq$ or frequency of $A_1A_1$ heterozygotes + half the frequency of heterozygotes (since each heterozygote has one $A_1$ allele)

So, after selection with change in absolute fitness:
![[EEB-020-PopulationGenetics-2025.pdf#page=19&rect=5,87,309,143&color=red|EEB-020-PopulationGenetics-2025, p.19]]
## Relative Fitness
Relative fitness is absolute fitness divided by mean fitness: $w_{ij} / \bar{w}$

This is important since we want to know how an individual preforms **relative to others** in the population. This tells us how advantageous a gene is

- ==Measure of the selective advantage of a genotype or allele in a population==
- If $w_{ij} / \bar{w} > 1$ , then $A_iA_j$ will increase in frequency in the population
- Often expressed relative to one genotype. For exaple, if $A_2$ results in selection change $s$:
![[EEB-020-PopulationGenetics-2025.pdf#page=20&rect=97,24,272,63|EEB-020-PopulationGenetics-2025, p.20]]
## Dominance and recessivity
- There is a relationship between selection coefficient $s$ and dominance coefficcient $h$.
- $h > 0.5$ means the gene is dominant.
![[EEB-020-PopulationGenetics-2025.pdf#page=22&rect=8,24,358,195|EEB-020-PopulationGenetics-2025, p.22]]
- For recessive mutations that are positive, it takes a longtime for the allele to become fixed (many generations)
## Deleterious mutations (negative selection)
- Very deleterious (deadly) are often highly recessive, otherwise they would be purged from the population quickly
- They are not "seen" by selection, so they can be maintained within a population
## Conclusions
- Evolution is fastest when genetic variation in fitness is largest, i.e. when p = q = 0.5
- Selection will cause loss of deleterious mutations and fixation of beneficial mutations.
- We are still only considering infinite populations with random mating