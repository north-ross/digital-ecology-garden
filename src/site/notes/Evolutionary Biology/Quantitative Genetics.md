---
{"dg-publish":true,"permalink":"/evolutionary-biology/quantitative-genetics/"}
---

Fred Guillame, 2025-11-12
# Quantitative Traits
- Traits in a [[Evolutionary Biology/Population Genetics\|population]] influenced by their genes and the environment
Phenotypic value of individual $i$:
$$P_i=G_i+E_i$$
Or, Phenotype value of $i$ is genotype effect + environmental effect on gene expression

Quantitative traits are continuously distributed- the phenotypic distribution is often normal.

## Phenotypic Distribution of a trait

Phenotypic distribution $\approx N(\bar{P}, \sqrt{V_P})$, AKA a normal distribution centered around average phenotype ($\bar{P}$) and standard dev equalto the square root of phenotypic variance.

Average Phenotype $\bar{P}$ given by:

$$\bar{P}=\bar{G}+\bar{E}$$
$\bar{E}$, the average environmental effect, is a random distribution centrered around zero that shows the effect of the environment on the phenotype - represents micro-environmental variation/noise, caused by random disturbances during development

If we assume that the environmental effects are not directional and centered on zero, then we find that $\bar{P}=\bar{G}$ 

## Environmental effects
### Permanent effects
- Temperature can affect body size in ectothermic animals like insects
- Insects raised in higher temperatures can have smaller body size since they develop faster
	- Plastic effect - not because of selection, changes in one generation
### Labile effects (non-permanent)
- Hydragea flower color depends on soil pH
- Snowshoe hares and other  mammals have colors that change with seasons
# [[Ecology/Phenotypic Plasticity\|Phenotypic Plasticity]]
- Depending on the environment, one genotype can have multiple phenotypes
- Plasticity has a genetic basis and can evolve when it varies among genotypes - when there are "G by E" (genotype by environment interactions)
	- The environmental effect on the trait **depends on** the genotype
	- See the third chart below:
![[EEB-020-QuantitativeGenetics-2025.pdf#page=9&rect=25,66,334,192|EEB-020-QuantitativeGenetics-2025, p.9]]

## Phenotypic plasticity and [[Evolutionary Biology/Natural Selection\|adaptation]]
- Plasticity can be **adaptive** when the expressed phenotype is closer to the optimum phenotype in a new environment
- Can be **maladaptive** if the expressed phenotype is further away from the optimum for this environment
## Canalization, assimilation, compensation
![[EEB-020-QuantitativeGenetics-2025.pdf#page=11&rect=2,21,358,269|EEB-020-QuantitativeGenetics-2025, p.11]]
### Canalization
- When you have a lot of the same environment, there is less plasticity in the genotypes - like a river being narrowed into a canal
### Assimilation
- When genotypes lose plasticity when adapting to a new environment
### Compensation
- If the genotype has maladaptive (bad) plasticity that makes it adapt the wrong way, it will have to compensate to reacha new optimum, they might become canalized

# Trait variation

## Phenotypic variance:
![[EEB-020-QuantitativeGenetics-2025.pdf#page=13&rect=-1,39,359,223|EEB-020-QuantitativeGenetics-2025, p.13]]
Like the phenotype, the variance in phenotype is also made of a genetic and environmental component, and also their interactions with each other and co-occurences (e.g. if a certain genotype is more common in a population that lives in a certain environment)

About covariance - if you measure tree growth across finland, you will have certain genotypes that are better adapted to southern or normal climates. This is when genotypes are found preferentially in one environment. This will naturally increase $V_P$.

The GxE - the same genotype in different environments has a different response (phenotype) (Phenotypic plasticity).

If there is no plasticity, no interaction between genotype and environment and no correlation of genotypes and environments, then the phenotypic variance is just $V_P=V_G+V_E$. For instance, in a common garden experiment. 

## Decomposition of genetic variance
Let's look in more detail at $V_G$, the component of trait variation due to genetic differences among individuals. This is made of a few of its own components:

$V_A$: Additive genetic variance
$V_D$: Dominance variance (based on dominance *within* loci)
$V_I$: Epistatic variance (epistatic effects *betweeen* loci) 
- The effect of a given allele on a trait might depend on which alleles are present somewhere else in the geonome. This is called an epistatic effect.

$V_A$ is inherited, so it's the most important component

The other two are not, or only partially inherited in closely related individuals. They depend on the genotype at specific loci - since only one allele is inherited, these are usually not the same between generations (at least they aren't statistically significant)

Dominance and epistasis cause deviation around the mean genotype.
- The more dominance and epistasis there are, there is more variation around mean genotype in a population. However this won't necessarily continue in the next generation.

## Gene effects and population mean
![[EEB-020-QuantitativeGenetics-2025.pdf#page=16&rect=3,26,355,232|EEB-020-QuantitativeGenetics-2025, p.16]]
Let's say this is describing an effect on height.

- A1A1 has an additive effect- for example it increases body height by 0.02m.
- Conversely, A2A2 decreases body height by 0.02m.
- Heterozygotes have no additive effect on body height (0), but if there is a dominance effect (for example if A1A1 is dominant) then heterozygotes might be slightly taller (e.g. 0.01m)
	- The reason the heterozygote is drawn twice on the graph is because it is showing two different dominance scenarios:
		- If there is no dominance than A1A2 has zero effect on height
		- If A1A1 is slightly dominant than A1A2 causes a slight increase in height.
Based on our equation from [[#Phenotypic Distribution of a trait]]:

$\bar{P}=\bar{G}=a(p-q)+2pqd$

And the genetic component of variance $V_G$, which is equal to $V_A + V_D$ (ignoring epistatic effects). 

$V_A$ is equal to $2pq(a+d(p-q)^2)$ and $V_D=(2pqd)^2$ ==(not sure why)...==

So, $V_G = 2pq(a+d(p-q)^2) + (2pqd)^2$

If $d=0$, then $V_G = 2pqa^2$
# Analysis of quantitative traits
Using quantitative genetics, we can analyze the genetic makeup of phenotypic traits without having to study their molecular basis. 

We can ignore how the coding for the trait works but still understand the genetic architecture, which is a function of $\bar{P}, V_A, V_D, V_I, V_E$

Their inheritance and response to selection can be understood using $h^2$ and $R_P=h^2S_W$

$h^2$ - [[heritability\|heritability]] $={V_A\over V_P}$ or $${cov(O, \bar{P})\over Var(O)}$$, where $\bar{P}$ is the "midparent value", average phenotype between parents, and O is the offpsring value. In a common-garden with no environmental effects, cov(O, P) will be equal to the additive genetic component of phenotypic variance, and Var(O) is the phenotypic variance in the offspring, like $V_P$.

Therefore, we can measure $h^2$ with an experiment where we compare traits in parents and offpsring raised in common garden.
# Inheritance of quant traits
We use $h^2$ or heritability to see how heritable a trait is. This is the slope of the graph measuring parent vs offpsring phenotype for the trait: 1 = very heritable, 0, not heritable

## Interpreting $h^2$
- Differences in  can be related to differences in $V_A$ (additive variation) and $V_E$ (variation due to environment). I guess it's not so much related to $V_I$ and $V_E$ since these are not heritable themseleves, but environment isn't either??? 
	- $V_D$ and $V_E$ could also affect heritability, but they are usually pretty small so we ignore them in this model
	- Since this model is a regression and we use it for predictions, we can't consider all of these.
- $h^2$ informs us how much $V_E$ contributes to trait variation in a population. High $h^2$ means phenotypic variaion is likely due to genetic differences between individuals
- Low $h^2$ means its more due to environmental effects
- $h^2$ is not informative of genetic basis of the trait, like number of loci, mutation rate, amount of genetic variation....
- But it can be used to predict evolutionary changes ([[Evolutionary Biology/Population Genetics - Selection\|selection]]). The response to selection of a trait $z$ is predicted as: $$\Delta \bar{z}=h^2S$$
- The "**breeders equation**"
	- Because breeders have been using this to select cattle for example for a certain trait - they need to know the heritability and selection differential to try and get a desired trait
	- Where $S$ is the selection differential ($\bar{z}^*(\text{selected})-\bar{z}(\text{before selection})$ )
![[EEB-020-QuantitativeGenetics-2025.pdf#page=24&rect=255,11,358,94|EEB-020-QuantitativeGenetics-2025, p.24]]
# Selection on quantitative traits
- We can use a **[[Fitness Function\|Fitness Function]]** to represent selection on a trait related to variation in fitness
- By examining differences in survival between years, we can caluclate selection differential $S$.
- These are different for different modes of [[Modes of Selection\|Modes of Selection]]
	- Directional, stabilizing, disruptive:
![[EEB-020-QuantitativeGenetics-2025.pdf#page=26&rect=56,16,310,241|EEB-020-QuantitativeGenetics-2025, p.26]]

- This depends on the position of the population on the fitness "landscape". Example with crossbills - 
	- population 1 increases to the optimum for hemlocks (mean 8.5 -> 8.8mm bill), 
	- population 2 is disrupted into two means hemlock specialists and lodgepole specialists (mean 9.1 -> 8.8 or mean 9.1 -> 9.5)
	- population 3 is stabilized around lodgepoles (9.5 -> 9.5mm bill)
## Measuring strength of directional selection
This is done with a selection gradient $\beta$. (the regression coefficient from relative fitness on to phenotypic value)
- Measured with the regression of relative fitness onto phenotypic vlaue:
$$\beta={Cov\{z,w\}\over V_P}$$
So, it's related to the covariance of response to selection ($z$) and relative fitness ($w$).
$\beta$ is related to selection differential $S$ as $\beta=S/V_P$, since $S=Cov\{z,w\}$ apparently...

So another way of writing $\Delta \bar{z}=h^2S$ is as $\Delta \bar{z}=V_A \beta$  
- $h^2 = V_A / V_P$
- $S = \beta  V_P$
- $\Delta \bar{z} =({V_A\over V_P})({\beta V_P})=V_A \beta$

# Rate of evolution of a quantitative trait
![[EEB-020-QuantitativeGenetics-2025.pdf#page=29&rect=26,46,337,208|EEB-020-QuantitativeGenetics-2025, p.29]]

# Response to natural selection
Natural selection of course acts on fitness. If we consider fitness to be a quantitative trait, it's rate of evolution is:
$$\Delta \bar{w}=h^2_wS_w$$where $S_w=Cov\{w,w\}=V_{P(w)}$

Therefore, $\Delta \bar{w}=V_{A(w)}$, since $h^2 ={V_A\over V_P}$

This is consistent with the [[Evolutionary Biology/Modern Synthesis of Darwinism\|Modern Synthesis of Darwinism]], which states that:

>the rate of increase in mean fitness of a population ascribable to gene frequency changes is exactly equal to the additive genetic variance in fitness

# Heritability vs $V_A$
Since $h^2$ is a ratio of two variances, differences in $h^2$ between populations, traits or species could be because of changes in additive or phenotypic variance. So we can't use $h^2$ to predict $V_A$

## Evolvability
- Evolvability is the coefficient of variation in $V_A$ , divided by $\bar{z}^2$.
	- We divide by $\bar{z}^2$ because it's a scale-free quantity that allows us to compare across traits, populations, species.
- It depends only on $V_A$ not phenotype variation.
- Note that this is different from heritability and they are not correlated.

# Estimating $V_A$
- $V_A$ can be estimated from phenotypic resemblance among relatives
- The phenotypic resemblance is measured as the *phenotypic covariance* between individuals
- any tendency for relatives to resemble one another more than non-relatives must be due to genetic similarity, unless they share a more similar environment than others
# General formula for phenotypic resemblance between relatives
$$cov(X_1, X_2)=rV_A+uV_D$$
Where $r$ is the probability that they share the allele (relatedness)
And $u$ is the probability that they share the same genotype at both alleles

In this kind of experiment, we call the breeding males the "sires" and the breeding females the "dames"
![[EEB-020-QuantitativeGenetics-2025.pdf#page=37&rect=14,57,347,207|EEB-020-QuantitativeGenetics-2025, p.37]]

We can compare full sib families and halfsib families and thus calculate $V_A$, since there is no $V_D$ in the half-sibs. Isn't there some chance?

Examples:
Red deer in the island of Roan
Great tit studies 
Sheep somewhere in Scotland

You can apply these methods to determine $V_A$ and selection of fitness - allowing us to make predictions on how populations will change over time if we know the effect of selection and evolvability. 

# Genetic architecture of quantitative traits
## QTL mapping
- identification of genetic loci associated with trait variation **between** populations.
- Look at how phenotype and genotype vary in controlled breeding
- Linear regression across the geonome for each locus to find correlation
- Only works for very large effects affected by a few loci
## Genome-Wide Association Study
- Examines associations between genetic markers within natural populations
- Works for diverse unrelated individuals and no controlled preeding required
- Requires very large sample size

## Comparing methods
**QTL** is better for controlled experiments with very different discrete phenotypes.

**GWAS** is better for population-wide studies with continuous phenotype distributions, where no controlled breeding can be done
- Example - bud set in aspen along latitudinal gradient in Sweden, identifying its genetic basis.
- It was found that there is one locus on one chromosome that is strongly associated with bud-set - genes that are important for bud set and flowering time were identified
- A regression for that particular SNIP shows a correlation between bud set time and the different alleles - TT homozygotes are much later than GG homozygotes with heterozygotes in between.

GWAS studies have taught us that most important traits are polygenic and controlled by many (>100) genes, each one has a small or intermediate effect and are hard to detect. Some traits are strongly influenced by a few major loci that explain more than 5% of phenotypic variation
- These are called **oligogenic** traits, like in our bud set example.

# [[Polygenicity\|Polygenicity]] implications
- All the genes have to code for many different traits, but there is a limited number of loci in the genome, so most genes are **pleiotropic** and code for multiple traits
- The same trait value can be reached by combining different combinations of alleles (high **redundancy** in the genome)
- Selection on polygenic traits can cause fast adaptation based on existing genetic variation, since selection response does not depend on new mutations