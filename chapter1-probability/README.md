# Chapter 1: Probability
Introduces the basic ingredients of probability theory and elementary combinatorial methods from a non measure theoretic point of view.
## Summary

<img src="https://github.com/isaiapedro/statistics-study/blob/main/chapter1-probability/resources/ch1-index.png" width="500" height="500" />


# Resume

### 1.2) Sample Spaces

Set of *all possible outcomes* for an experiment. Example: Ω = {hhh, hht, hth, ..., ttt} is the set of all possible outcomes for heads and tails after throwing a coin three times.

Event are subsets of Omega (Ω), for instance, the subset of outcomes for three heads in a row is A = {hhh}.
<br>
<br>
The **union** of two events is the event C that either A occurs or B occurs or both occurs.

$$C = A  ∪  B$$

<br>

The **intersection** of two events is the event that both A and B occurs.

$$C = A  ∩  B$$

<img src="https://github.com/isaiapedro/statistics-study/blob/main/chapter1-probability/resources/venn.png" width="400" height="400" />

The **complement** of an event $A^c$ is the event that A does not occurs.
<br>
<br>
If A and C are two events and $$A  ∩  C =∅ $$, A and C are said to be **disjoint**
<br>
<br>
***Laws of Set Theory:***
<br>
<br>
<center>
    Commutative Laws:
</center>
<br>

$$ A  ∪  B = B  ∪  A $$

$$ A  ∩  B = B  ∩  A $$
<br>
<br>
<center>
    Associative Laws:
</center>
<br>

$$ (A  ∪  B)  ∪  C = A  ∪  (B  ∪  C) $$

$$ (A  ∩  B)  ∩  C = A  ∩  (B  ∩  C) $$
<br>
<br>
<center>
    Distributive Laws:
</center>
<br>

$$ (A  ∪  B)  ∩  C = (A  ∩  C) ∪  (B  ∩  C) $$

$$ (A  ∩  B)  ∪  C = (A  ∪  C) ∩  (B  ∪  C) $$
<br>
<br>
### 1.3) Probability Measures

Is a function P from subsets of Ω that satisfies the following axioms:
- P(Ω) = 1.
- If A ⊂ Ω, then $$P(A)>=0$$.
- If A<sub>1</sub> and A<sub>2</sub> are disjoint, then:

$$ P(A_1 ∪ A_2) = P(A_1) + P(A_2) $$

The following properties are consequences of the previous axioms:
<br>
<br>
<ins>Property A:</ins>
<br>

$$ P(A^c) = 1 - P(A) $$

<br>
<br>

<ins>Property B:</ins>
<br>

$$ P(∅) = 0 $$

<br>
<br>

<ins>Property C</ins>:
<br>
  
<div align="center">

If A ⊂ B, then $$P(A) <= P(B)$$.

</div>

<br>
<br>

<ins>Property D:</ins> **Addition Law**
<br>

$$ P(A  ∪  B) = P(A) + P(B) - P(A  ∩  B) $$

<br>
<br>

### 1.4) Computing Probabilities: Counting Methods

If A can occur in any of *n* mutually exclusive ways and all elements have equal probability, then:

$$ P(A) = \frac{A}{Ω} $$

- A = number of ways A can occur
- Ω = total number of outcomes
<br>
<br>

**Multiplication Principle:**

<br>

If one experiment has *m* outcomes and another experiment has *n* outcomes, there are $m\cdot n$ possible outcomes for the two experiments.

<br>

**Extended Multiplication Principle:**

<br>

If there are p experiments and the first has *n<sub>1</sub>* possible outcomes, the second has *n<sub>2</sub>* outcomes and the *p*th *n<sub>p</sub>*, there are $n_1 \cdot n_2 \cdot ...\cdot n_p$ possible outcomes for the *p* experiments.

<br>

### **Permutations**

<br>

For a set of size *n* and a sample size of *r*, there are *n<sup>r</sup>* different ordered samples with replacement and $n\cdot (n-1)\cdot (n-2)\cdot ... \cdot (n-r+1)$ different ordered samples without replacement.

The number of orderings of *n* elements is $n\cdot (n-1)\cdot (n-2)\cdot ... \cdot 1 = n!$

<br>

### **Combinations**

<br>

The number of unordered samples of *r* objects selected from *n* objects without replacement is the **binomial coefficient**:

<img src="https://github.com/isaiapedro/statistics-study/blob/main/chapter1-probability/resources/binomial.png" width="400" height="400" />

<br>

Suppose that *n* items are in a lot and a sample of size *r* is taken. The lot contains *k* defective items, so what's the probabilty of the sample containing *m* defective items?

Call the event A, the probabilty of A is the number of ways A can occur divided by the total amount of outcomes.

<br>

<img src="https://github.com/isaiapedro/statistics-study/blob/main/chapter1-probability/resources/likelihood.png" width="250" height="250" />

<br>

One method of estimation is called **maximum likelihood**, and is to choose the value of *m* that makes the observed outcome most probable.

<br>

The number of ways that *n* objects can be grouped into *r* classes with *n<sub>i</sub>* in the *i*<sub>th</sub> class is:

<br>

<img src="https://github.com/isaiapedro/statistics-study/blob/main/chapter1-probability/resources/binom-ext.png" width="280" height="280" />

<br>

### 1.5) Conditional Probability

<br>

Let A and B be two events with $P(B) ≠ 0$. The conditional probability of A given B is defined to be:

<br>

$$ P(A|B) = \frac{P(A  ∩  B)}{P(B)} $$

<br>

Multiplication Law

<br>

$$ P(A  ∩  B) = P(A|B) \cdot P(B) $$

<br>

***Law of Total Probability***


Let B<sub>1</sub>, B<sub>2</sub>, ..., B<sub>n</sub> be such that $U_{i=1}^n B_i = Ω$.

For any event A:

$$ P(A) = \sum_{i=1}^n P(A|B_i) \cdot P(B_i) $$

<br>

***Bayes' Rule***

Let A and B<sub>1</sub>, ..., B<sub>n</sub> be events where the B<sub>i</sub> are *disjoint*, $U_{i=1}^n B_i = Ω$ and $P(B_i)>0$.

<br>

$$ P(B_j|A) = \frac{P(A|B_j)\cdot P(B_j)}{\sum_{i=1}^n P(A|B_i)\cdot P(B_i)} $$

<br>

### 1.6) Independence

<br>

A and B are said to be **independent events**:

If $P(A|B) = P(A)$ and $P(B|A) = P(B)$.


<br>

$$ P(A  ∩  B) = P(A) \cdot P(B) $$

<br>

A collection of events A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub> is **mutually independent** if for any subcollection,

<br>

$$P(A_{i1}  ∩  ... ∩ A_{im}) = P(A_{i1})\cdot ... \cdot P(A_{im})$$

<br>


## Exercices

The exercise's file is [this](https://github.com/isaiapedro/statistics-study/blob/main/chapter1-probability/chapter1.ipynb). You can open it in a notebook to follow along, good study!
