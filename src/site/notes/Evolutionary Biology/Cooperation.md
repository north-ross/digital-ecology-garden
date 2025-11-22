---
{"dg-publish":true,"permalink":"/evolutionary-biology/cooperation/"}
---

- Actions taken at a cost to an individual which are beneficial to another
- Usually in nature these are related organisms which share part of their geonome
- Difference from [[Ecology/Facilitation\|Facilitation]] - this usually refers to interspecies interactions, but cooperation can be within OR between species
# Altruistic cooperation
- Benefits others but is costly for the actor, such as decreasing their reproductive output
# Coefficient of relatedness $r$
General method:
$$
r = \sum{(0.5)^L}
$$
This describes meiosis.
Where $L$ is the generation link, and 0.5 is the probability that a copy of a particular gene will be passed on.

| $r$   | $L$ | descendant          | non-descendant                   |
| ----- | --- | ------------------- | -------------------------------- |
| 0.5   | 1   | offspring           | full sibling                     |
| 0.25  | 2   | grandchildren       | half-sibling; nieces and nephews |
| 0.125 | 3   | great-grandchildren | cousins                          |
# Hamilton's Rule
In order for altruism to evolve:
$$
rb > c
$$
Where:
- $r$ is coefficient of relatedness
- $b$ is the benefit to recipients
- $c$ is the cost to the actor
## Example: Long-tailed Tits
- If a nest is failed, some individuals might decide to not try again, but instead assist a close relative in raising their offspring
- They recognize offspring by similar calls and behaviour
## Example: Meerkat helpers
- Subordinate members ("helpers") provide altrustic care to the pups
- It's costly to "babysit" instead of foraging (they can lose up to 8% of their body weight)
![[course cooperation 071024_Van Meyel.pdf#page=3&rect=19,17,320,297|course cooperation 071024_Van Meyel, p.3]]
- But there must be some advantage in order for this to evolve: 
![[course cooperation 071024_Van Meyel.pdf#page=4&rect=3,32,642,469&color=note|course cooperation 071024_Van Meyel, p.4]]
- Overall, the daily weight gain of pups is increased by having more members watching out for predators
# Cost-Benefit Ratio and environment
- Generally, we find more cooperative behaviours in harsh or unpredictable conditions
- It was long thought that harsh conditions select for this behaviour
- In 2017, a new phylogenetic study of cooperative breeding in birds showed that this is a bit misleading and in fact the causality is opposite:
	- Species with cooperative behaviours are more likely to be able to colonize harsh environments
# Example: Pine Sawflies and cooperative defense in larval stage
- They live and feed in very dense groups in larval stage
- They raise their heads and puke a foamy fluid at the same time when one is being predated on
	- They sequester defensive compond from compounds in pine needles (in their diet)
- This is more advantageous to the group if they all contribute to the defense
- They cause economic damage to pine trees:
	- Host plant defends against pine sawflies by producing toxic chemicals like terpene
	- The sawflies need to invest into protecting themselves from this compound
	- They have evolved to use this compound against predators
- We can study how this collective defense under different conditions
## Amount of contribution
- There is a lot of variation in how much an individual contributes to the group
- There are some individuals who do not defend at all, even just against themselves
## Experiment in diet variation
- Phenoloxidase activity: Higher values have higher immune defense
- Given low-resin and high resin diet, and also simulated a predator attack (high attack intensity vs low intensity), stimulating a defensive reaction
	- The [[Evolutionary Biology/Trade-off\|Trade-off]] here is:
		- low-resin diet is less toxic, but they can produce fewer defenses
		- high-resin diet
- Within the high-resin diets, there was more variation between high and low intensity attack behaviour
	- Environment is an important factor in cooperative behaviour
- Larvae who did not defend were not "out of" defensive fluid, they just chose not to cooperate
## Benefits of freeloading?
- Non-defending males grew faster than defending males
	- Not as significant in females
# How does cooperation evolve?
[[Evolutionary Biology/Kin Selection\|Kin Selection]] is often a mechanism to evolve cooperation, but not the only one.

| Mechanism         | Description                                                                               |
| ----------------- | ----------------------------------------------------------------------------------------- |
| [[Evolutionary Biology/Kin Selection\|Kin selection]] | Genetics are shared between actor and recipient and this outweighs the cost of the action |
| By product        |                                                                                           |
| [[Evolutionary Biology/Reciprocity\|Reciprocity]]   | you scratch my back, i'll scratch yours                                                   |

![[Cooperation benefits flowchart.canvas|Cooperation benefits flowchard]]
# Heritability of Competition
- Quantitative evidence of heritability of [[Evolutionary Biology/Behavioural Evolution\|behavioural traits]] are often lower than morphological traits (based on meta-analysis)
- Most are due to environmental/[[Ecology/Maternal effect\|maternal effect]] (social environment)
	- The genotypes of other individualsin the environment is called **Indirect Genetic Effects** (IGE) that need to be taken into account
- However there is some genetic variation that is part of this - this is difficult to quantify though
## Example in animal breeding:
- In animal agriculture, they are sometimes selecting for animals that grow as fast as possible
	- In piglets, selecting only for growth rate can result in piglets that are less competitive for certain teats
	- Similarly in plant breeding, if you have plants in kin groups you might get faster ==responses in terms of selection?? Less variation?==
# Applied Example:
- Antimicrobial resistance of pathogens
- How is resistance evolved?
	- Biofilms are tolerant to antimicrobials
	- Inhibiting biofilm formation makes them more susceptible to antimicrobials
- We need to be able to limit evolution of resistance
- Some biofilm forming agents are "public goods" like EPS
	- EPS is costly to producing cells
- Some strains are non-EPS producers, others are EPS resistanct
- Adding EPS inhibitors on surfaces will make it harder for biofilms to form
	- Evolution of resistance to EPS inhibition, since in this case the resistant strain is outcompeted by the strains which are non-producers but are susceptible to other antimicrobials