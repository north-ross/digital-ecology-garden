---
{"dg-publish":true,"permalink":"/evolutionary-biology/assignment-population-genetics-north-ross/"}
---

[[Evolutionary Biology/Population Genetics\|Population Genetics]]
# Selection
## Question 1
If the genotype fitnesses of $AA$, $Aa$, $aa$ are $1.0, 0.9, 0.6$ and $p_0 = 0.7$, calculate $p_1, p_2$ and $p_3$, the allele frequencies of allele $A$ after 1, 2, and 3 generations of selection.
$w_{AA} = 1.0$
$w_{Aa} = 0.9$
$w_{aa} = 0.6$
$p_0=0.7$
$q_0=1-p_0=0.3$

First, I will calculate the mean fitness at generation 0 $\bar{w_0}$:
$$\bar{w_0}=p_0^2w_{AA} + 2p_0q_0 w_{Aa} + q_0^2w_{aa}$$
$$\bar{w_0}=(0.7)^2(1.0) + 2(0.7)(0.3) (0.9) + (0.3)^2(0.6)$$
$$\bar{w_0}= 0.49 + 0.378+0.054 = 0.922$$
Now, we can find the change in allele frequency after selection:
$$p_1={p_0(p_0w_{AA}+q_0w_{Aa})\over \bar{w_0}}$$
$$p_1={(0.7)((0.7)(1.0)+(0.3)(0.9))\over 0.922} = 0.736$$
Now we repeat for the following two generations:
$$\bar{w_1}=p_1^2w_{AA} + 2p_1q_1 w_{Aa} + q_1^2w_{aa}=0.933396$$
$$p_2={(0.736)((0.736)(1.0)+(1-0.736)(0.9))\over 0.933396} = 0.7681981$$
$$\bar{w_2}=p_2^2w_{AA} + 2p_2q_2 w_{Aa} + q_2^2w_{aa}=0.943$$
$$p_3={(0.777)((0.777)(1.0)+(1-0.777)(0.9))\over 0.943} = 0.796$$

So, the values are: $p_1 = 0.736, p_2=0.768, p_3=0.796$

The probability increases since this is a positive mutation with relative fitness ($w_{AA}/\bar{w} = 1.0/0.922$) > 1.

## Question 2

| Genotype | Survival Rate $s$ | Fecundity (eggs per female) $f$ | Absolute fitness $W$ |
| -------- | ----------------- | ------------------------------- | -------------------- |
| $A_1A_1$ | 0.90              | 50                              | 45                   |
| $A_1A_2$ | 0.85              | 55                              | 46.75                |
| $A_2A_2$ | 0.75              | 70                              | 52.5                 |
Since the absolute fitness is the number of surviving offspring per female, and we know the number of eggs and egg-to-adult survival rate, we simply multiply the two to get the absolute fitness $W$. In this case, the most fit genotype is $A_2A_2$. Despite having the lowest survival rate, it produces enough young to compensate for this and has highest absolute fitness.

## Question 3
1. *What are the fitnesses of the two other genotypes relative to $w_{11} = 1$?*
Since we set $w_{11}$ to 1, we will get the other relative fitnesses from $W_{12} / W_{11}$ and $W_{22} / W_{11}$. See the table below

| Genotype | Absolute fitness $W$ | Relative Fitness to $W_{11}$ |
| -------- | -------------------- | ---------------------------- |
| $A_1A_1$ | $W_{11}=45$          | $w_{11} = 1$                 |
| $A_1A_2$ | $W_{12}=46.75$       | $w_{12} = 1.03889$           |
| $A_2A_2$ | $W_{22}=52.5$        | $w_{22}=1.166667$            |
2. *If the frequency of the A2 allele is p = 0.5, what will be its frequency after one generation of selection? (use the relative fitness values $w_{ij}$ in your calculations)*
First, we need to calculate the mean fitness for the population. 

> Note that since $p+q=1$ and $p=0.5$, $p=q$. So I will only use $p$ in the equation:

$$\bar{w}=p^2w_{11} + 2p^2 w_{12} + p^2w_{22}$$
$$\bar{w}=(0.5)^2*(1) + 2(0.5)^2 * (1.03889) + (0.5)^2*(1.16667) = 1.0611$$
Now, we use this mean fitness to find the change in $p$ over one generation:
$$p'={p^2(w_{22}+w_{12})\over \bar{w}}$$
$$p'={(0.5)^2*((1.16667)+(1.038889))\over (1.0611)}=0.5196$$
The allele frequency of $A_2$ increases slightly from 0.5 to 0.5196.

3. *What will be the allele frequency when it reaches equilibrium?*
Since the only two equilibrium states are $p=0$ and $p=1$, and this is a beneficial mutation that increases in frequency each generation, the frequency at equilibrium will be $p=1$ (fixed mutation).

# Hardy-Weinberg Equilibrium
## Question 1
*The table shows the number of individuals affected for several recessive traits (diseases). Assuming random mating proportions, what is expected frequency of heterozygotes for each recessive allele?*

If these are affected by this recessive gene, they must be heterozygotes for the recessive trait. So the allele frequency $q$ will be given by the square root of the homozygote frequency $R$. Then, we can calculate $p$ from $1-q$, then get the heterozygote frequency from $2pq$.

| Trait | Recessive homozygotes $R$ (per million) | $q = \sqrt{R}$ | $p=1-q$  | Heterozygote frequency $H=2pq$ |
| ----- | --------------------------------------- | -------------- | -------- | ------------------------------ |
| a     | 2786                                    | 0.052783       | 0.947217 | 0.099993                       |
| b     | 658                                     | 0.025652       | 0.974348 | 0.049987                       |
| c     | 287                                     | 0.016941       | 0.983059 | 0.033308                       |
| d     | 160                                     | 0.012649       | 0.987351 | 0.024978                       |
| e     | 102                                     | 0.010100       | 0.989900 | 0.019995                       |
## Question 2
Given the values of the heterozygotes, we can calculate the allele frequencies $p$ and $q$, based on $p=D + H/2$ where $D$ is dominant heterozygote genotype frequency and $H$ is homozygote frequency. The reverse case is $q=R+H/2$.

|     | A allele frequency $p$ | a allele frequency $q$ |
| --- | ---------------------- | ---------------------- |
| a   | 0.345                  | 0.655                  |
| b   | 0.395                  | 0.605                  |
| c   | 0.42                   | 0.58                   |
| d   | 0.355                  | 0.645                  |
Now, we can calculate the expected genotype frequencies based on Hardy-Weinberg formulas:

|     | Expected AA frequency $p^2$ | Expected Aa frequency $2pq$ | Expected aa frequency $q^2$ |
| --- | --------------------------- | --------------------------- | --------------------------- |
| a   | 0.119025                    | 0.45195                     | 0.429025                    |
| b   | 0.156025                    | 0.47795                     | 0.366025                    |
| c   | 0.1764                      | 0.4872                      | 0.3364                      |
| d   | 0.126025                    | 0.45795                     | 0.416025                    |
Now, we can calculate the difference between the observed and expected frequencies. This tells us how close to H-W a population is.

|     | AA        | Aa       | aa        |
| --- | --------- | -------- | --------- |
| a   | -0.039025 | 0.07805  | -0.039025 |
| b   | -0.066025 | 0.13205  | -0.066025 |
| c   | -0.0464   | 0.0928   | -0.0464   |
| d   | 0.053975  | -0.10795 | 0.053975  |

This shows that population *b* has the most deviation from H-W (they measured 13 more heterozygotes than expected) and the one most like H-W is population *a* (only *7.8*% more heterozygotes than expected). All the populations except *d* have more heterozygotes than expected, while *d* has fewer than expected. 
# Genetic Drift
## Question 1
*Suppose that a diploid population of size $N = 50$ undergoes a change in heterozygosity from 0.50 to 0.42 in a single generation. Is it plausible to attribute this magnitude of change to random genetic drift?*

We expect heterozygosity to decrease by $1/2N$ each generation. In our population of N=50, we expect it to decrease by $0.01$ each generation (0.50 to 0.49). So this change is not likely to be caused by genetic drift alone. Perhaps this is being affected by selection or gene flow (migration).

## Question 2
A colony of *N=28* mice gets a new neutral allele. Probability of fixation is 1/2*N* = 0.01786 and expected time to fixation for a new mutation is 4*N* = 112 generations.

## Question 3
*What is the effective population size of a herd of 10 dairy cows and 1 bull? What is it for 40 cows and 1 bull? For 10 cows and 2 bulls?*

We use the formula for calculating effective population size with a variation in number of reproducing adults:
$$N_e = {4N_m N_f \over N_m + N_f}$$

| Number of cows $N_f$ | Number of bulls $N_m$ | Effective population size $N_e$ |
| -------------------- | --------------------- | ------------------------------- |
| 10                   | 1                     | 3.636                           |
| 40                   | 1                     | 3.902                           |
| 10                   | 2                     | 6.667                           |
## Question 4
*What is the effective population size in a population of African lions, in which each breeding male controls a harem of five females and the total population consists of 200 males and 200 females?*

If the reproducing males control the entire population of females and the remaining males do not mate at all, that means that only 40 (200 / 5) males contribute to the effective population size. Therefore, using the same formula from question 3:
$$N_e = {4N_m N_f \over N_m + N_f}$$
$$N_e = {4*(40)*(200) \over 40+200} = 133.33$$
So, the effective population size is 133.33.
# Migration and population structure

## Question 1
$A_1$ Allele frequency in generation 0 of population $i$: $p_{i0} = 0.4$
In population $j$, the $A_1$ allele is constant at $p_j=0.6$ 
Migration rate between $i$ and $j$: $m=0.10$

1. *Calculate the frequency of $A_1$ in population $i$ in the next two generations*
$\Delta p_i = m_{ij}(p_j-p_{i0})$
$p_{i1} = m_{ij}(p_j-p_{i0})+p_{i0}$
$p_{i1} = (0.10)(0.6-0.4)+0.4=0.42$
Generation 1: $p_{i1}=0.42$

$p_{i2} = m_{ij}(p_j-p_{i1})+p_{i1}$
$p_{i1} = (0.10)(0.6-0.42)+0.42=0.438$
Generation 2: $p_{i2}=0.438$

2. *Is the change in allele frequency in generation 2 less than the change in generation 1? Why?*
The change between generations 2 and 1 is less than the change between 1 and 0. Allele frequency change is faster when there are large differences in allele frequencies between the two populations, and by generation 1 the populations have become more similar (there is less genetic difference between them). 

3. *What will the allele frequency become in the population after many generations?*
Since the $A_1$ allele is constant in population $j$, population $i$ will also eventually reach this level due to gene flow. 
In a more realistic scenario, we would expect allele frequency to fluctuate due to selective pressure, genetic drift, and the effect of individuals from $i$ migrating to $j$.
## Question 2
We have two genotyped populations of snails. We want to estimate the number of migrants per generation between the populations.

1. Calculate $F_{ST}$
The index of differentiation $F_{ST}$ is calculated with the following formula:
$$F_{ST} = {H_T - \bar{H}_S \over H_T}$$
This measures the difference between expected heterozygosity in the Total population ($H_T$) and the average of expected heterozygosity between the subpopulations. In order to calculate these values, we first need to find the allele frequencies $p_1$, $p_2$ (for allele $A$) and $q_1$, $q_2$ (for allele $a$), calculated from our genotype frequencies in the two populations:

$p_1= AA_1 + Aa_1/2$
	$= 0.056 + 0.288/2= 0.200$
	
$q_1= aa_1 + Aa_1/2$
	$= 0.656 + 0.288/2= 0.800$
	
$p_2= AA_2 + Aa_2/2$
	$= 0.672 + 0.256/2= 0.800$
	
$q_2= aa_2 + Aa_2/2$
	$= 0.072 + 0.256/2= 0.200$
	

Now, we can use the given formulas to find $H_T$ (expected total population heterozygosity):
$H_T = 2 \cdot {1\over n} \sum_i^n p_i \cdot {1\over n} \sum_i^n q_i$
$H_T = 2 \cdot {1\over 2} (p_1 +p_2) \cdot {1\over 2} (q_1+q_2)$
$H_T = {1\over 2} (0.200 +0.800) \cdot (0.800+0.200) = 0.500$

And $\bar{H_S}$ (average subpopulation heterozygosity):
$\bar{H_S}={1\over n}\sum_i^n 2p_i q_i$
$\bar{H_S}={1\over2}(2p_1q_1 + 2p_2q_2)$
$\bar{H_S}=(0.200 * 0.800) + (0.800 * 0.200)=0.320$

So, $F_{ST}=(0.500 - 0.320) / 0.500 = 0.360$

2. Using the following relationship valid for two populations and your $F_{ST}$ value, provide an estimate of effective number of migrants per generation $N_em$ between the two populations.
$$F_{ST}={1 \over 1+16N_em}$$
$$16N_em={1 \over F_{ST}}-1$$
$$N_em={1-F_{ST} \over 16F_{ST}}={1-0.360 \over 16(0.360)}=0.111$$
There is effectively 0.111 migrants per generation - meaning in 10 generations there will be around one migrant that affects the other's gene pool. 