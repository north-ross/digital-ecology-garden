---
{"dg-publish":true,"permalink":"/evolutionary-biology/assignment-quantitative-genetics-north-ross/"}
---

[[Evolutionary Biology/Quantitative Genetics\|Quantitative Genetics]]
# Determining the effect of inbreeding on genetic variance in Tribolium castaneum flour beetles as measured by phenotypic variance among half-sib crosses. 

Jan Lukovský, North Ross 

## Question 1. Description of experiment results. 

The data produced for this experiment is a collection of measurements of the right metaepisternum of *Tribolium castaneum* beetles bred from a replicated half-sib/full-sib cross. These come from two types of experimental lines – an “inbred” and “outbred” treatment, where the “inbred” lines were intentionally inbred for one more generation than the outbred lines. Producing three lines within each category allows for experimental replication to ensure consistent results. By comparing the variation between half-siblings within each line, we can infer the additive component of genetic variation in the inbred and outbred treatment groups. Breeding each control line for the same number of generations in the same conditions will also reduce the environmental component on phenotypic variation, allowing us to determine only the genetic component. 

The right metaepisternum size was measured from an average “centroid size” from the centroid of the part to each landmark on the outside of the body part. This method was repeated twice for each individual, then the mean of the two centroid sizes was used in our overall calculations to reduce error in the measurement process. 

The mean right metapeisternum centroid size in the inbred lines was 402.4 with a standard deviation of 13.4, while the same part in the outbred lineages was slightly larger at 414.6 (σ2 = 16.7). As seen in Figure 1, each replicant line within the treatment groups had similar distributions of body part size. There is some overlap between the upper quartiles of individuals in the inbred line and the lower quartiles in the outbred lines. Nearly all of the lines had less than three outliers, except for the outbred line LO2. 


**Figure 1**. Boxplot showing the variation in right metaepisternum size of experimentally inbred and outbred lineages of Trilobium castaneum beetles. 

## Question 2. Comparison of the genetic architecture of body size in the inbred and outbred lines. 

### Hypotheses 

We expect the additive component of genetic variance ($V_A$), as measured by one quarter of the covariance of phenotypic body size variation between half-siblings) to be higher in the outbred lines compared to the inbred lines. This is because more alleles will be fixed in the inbred population due to the effects of inbreeding depression, so overall genetic diversity (and thus variance) will be lower.  

Additionally, the model we are using to calculate $V_A$ is only true for populations with no inbreeding. Due to the inbreeding in both lines at the start of our experiment, all individuals in each line are somewhat related to each other. Therefore, there is a non-zero chance that our “half-sibs” share their entire genotype. The covariance between half sibs is usually related to $V_A$ using the following equation, where probability of sharing an allele $r=¼$ and probablility of sharing a genotype $u=0$:$$cov(X_1, X_2)=rV_A+uV_D$$Since we determined that there is a small chance that the two individuals share a genotype, there is a small component of genetic variation due to dominance ($V_D$) that also influences our covariance model. Since inbreeding dominance effects usually serves to mask certain phenotypes from the population, we expect that this component of genetic variation will be negative, and it will be larger in the more inbred line. Therefore, we expect that our calculated “$V_A$” will be smaller in the inbred lineages. 

Evolvability ($CV_a$) is the capacity of a population to respond to selection. We would expect that a population with a higher additive genetic diversity would have a greater ability to respond to selection since it contains more heritable genes for potentially beneficial mutations for different selective pressures. In pure numeric terms, evolvability is a function of the additive component of genetic variance divided by the square of the mean population phenotype. Although the mean body size is larger in the outbred population, it is only slightly larger, and we expect a large reduction in $V_A$ due to inbreeding that we expect will account for this. 

### Results 

**Table 1.** Comparison of the additive component of genetic variance $V_A$, phenotypic variance $V_P$, evolvability $CV_a$ and heritability $h^2$. 

|               | Additive Genetic Variance $V_A$ | Phenotypic Variance $V_P$ | Evolvability $CV_a$ | Heritability $h^2$ |
| ------------- | ------------------------------- | ------------------------- | ------------------- | ------------------ |
| Inbred lines  | 2.661                           | 134.524                   | 0.016               | 0.020              |
| Outbred lines | 149.690                         | 216.320                   | 0.871               | 0.692              |
### Discussion 

As predicted in our hypothesis, the inbred lines showed a 98% reduction in additive genetic variance despite only having one more generation of inbreeding than the outbred lines. This extreme reduction in genetic variance has a strong effect on evolvability which was also 54% lower in the inbred population, although this was offset by the larger mean body size (phenotype) in the outbred population.  

In a natural population suffering from inbreeding depression, we would expect that this reduction in evolvability would lead to the population having less capacity to respond to natural selection and suffering a higher risk of extinction. In addition to the increase in deleterious mutations expected due to inbreeding depression, this represents another issue that populations suffering from inbreeding depression face. 

## Additional analysis  

After preforming microstellite genetic analysis on both lines, we can calculate the index of genetic differentiation $F_{ST}$ between lines within the inbred and outbred treatment groups. Since the inbred lineage has less genetic variance within each line, we expect that different lines would be more different to each other since more alleles will have fixed during the thirty generations of regular breeding within each line. This hypothesis is supported by our results, which show that the inbred lineage has a higher $F_{ST}$ at 0.379 compared to 0.102 observed in the outbred lineage. Therefore, the inbred lineages have diverged genetically from each other more than the outbred lineages. 

Figure 2 shows a boxplot of allelic richness at nine different neutral loci in the outbred and inbred lines. The median allelic richness at each locus is higher or equal to the median value in the outbred than the inbred lines – none of the neutral loci in the inbred lines have a median value above three alleles. Therefore, the outbred lines have preserved more neutral genetic diversity than the inbred population. This is consistent with our measurements of phenotypic variation and resultant calculated additive genetic variation – the inbred lines have less genetic variation than the outbred lines. 

 

**Figure 2.** Comparison of allelic richness of netural loci based on microstellite analysis of inbred and outbred lines.