---
{"dg-publish":true,"permalink":"/evolutionary-biology/linkage-disequilibrium/"}
---

Also known as **LD**
- Consider 2 loci A and B - are the allele frequencies at the two loci independent?
- This means there are four possible haplotypes (combinations of the four alleles)
- If loci A and B are [[Math Methods/Probability/Conditional Probability#Independence\|independent]], we expect to observe all four haplotypes in the gene pool to be equal to the product of allele frequencies: 
$$freq(A_iB_j) =p_{A_iB_j}= p_{Ai}p_{B_j}$$
This is the expected frequency if they are independent. 

$D$ is what we call linkage disequilibrium, when haplotype frequencies depart from their expectations. $D=p_\text{observed}-p_\text{expected}$, or $D=p_{A_iB_j}-p_{A_i}p_{B_j}$  

Evolutionary processes can cause linkage disequilibrium by making certain allele combinations more common than others

## Effects on LD
- Mutation creates LD
- Selection can create LD if it favours some haplotypes over others because speicific allele combinations have higher fitness
- Gene flow creates LD if allele frequencies differ between populations
- Recombination decreases LD by re-arranging haplotypes 
	- During meiosis
	- This happens at recombination rate $r$
## Decay of LD
- Decays at rate $(1-r)$ each generation:$D'=(1-r)D$
- After $t$ generations: $D_t \approx D_0e^{-rt}$ (when $r\ll 1$)
	- Usually $r$ is in the order of $10^{-7}$ or $10^{-9}$ between adjacent nucleotides
![[EEB-020-PopulationGenetics-2025.pdf#page=91&rect=3,21,353,241|EEB-020-PopulationGenetics-2025, p.91]]

## Using LD to find selection
- When a new beneficial mutation arises, it will:
	- Be in LD with nearby alleles
	- Quickly rise in frequency because of selection
	- Reduce genetic diversity at nearby loci because of *genetic hitchhiking*
We call this [[Selective Sweep\|Selective Sweep]]

When a beneficial mutation arises in a population, the nearby genes that are associated with it will also increase in frequency with it and become less diverse in the population. The mutation has "swept" through the population, taking with it the nearby genetic variation

This can happen even in synonymous (neutral) alleles, if they are associated with a beneficial mutation.