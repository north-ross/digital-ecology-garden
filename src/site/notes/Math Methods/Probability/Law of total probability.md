---
{"dg-publish":true,"permalink":"/math-methods/probability/law-of-total-probability/"}
---

Let's try to generalise this example a bit. We will call left-handedness "condition A", and gender is condition B. For condition A, we are only interested in one state, but condition $B$ has two states (for the sake of this exercize) $B_1$ (male) and $B_2$(female).

Probability of A and $B_1$, as we showed above, is thus:
$$P(A \text{ and } B_1) = P(A|B_1)*P(B_1)$$
And then the reverse:
$$P(A \text{ and not } B_1) = P(A|\text{not } B_1)*P(\text{not }B_1)$$

We need to add these two together to get the complete $P(A)$.

Now, let's imagine a different scenario where we have 3 mutually exclusive conditions $B_1, B_2, B_3$. 

$$P(A \text{ and } B_1) = P(A|B_1)*P(B_1)$$
$$...$$
$$P(A \text{ and } B_3) = P(A|B_3)*P(B_3)$$
In order to get the total $P(A)$ we need to add them all together: $$P(A) = P(A \text{ and } B_1) + P(A \text{ and } B_2) + P(A \text{ and } B_3)$$
If we generalize this as a sum with number of conditions $i$:
$$\sum_i P(A|B_i)P(B_i)$$
We call this the [Law of Total Probability](https://en.wikipedia.org/wiki/Law_of_total_probability).