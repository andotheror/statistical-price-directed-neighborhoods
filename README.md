# The Statistical Price of Directed Neighborhoods

## Abstract

Conditional-average learning asks for the average target label in every graph neighborhood from i.i.d. labeled vertices. Its recent combinatorial characterization leaves a logarithmic sample- complexity gap: the upper bound contains $\alpha_2\log(1/\epsilon)/\epsilon$, while the lower bound is only $\alpha_2/(\epsilon\log\alpha_2)$. We determine exactly when the accuracy logarithm is real. For undirected neighborhoods, we prove that the original empirical-neighborhood learner has expected squared error at most 

$$\frac{\alpha_1}{m+1}+\frac{7\alpha_2}{2m}.$$

 The proof integrates its pointwise variance through a measure-valued weighted Caro-Wei inequality. This removes the logarithm without changing the algorithm, including on uncountable domains. Conversely, for directed neighborhoods we construct $q$ disjoint transitive tournaments and a single known alternating concept for which every learner suffers $\Omega((q/m)\log(1+m/q))$ error with constant probability. The unknown object is only the marginal distribution. Independent mass imbalances hidden in unsampled pairs accumulate over nested suffixes, one harmonic scale at a time. A matching undirected lower bound follows from disjoint edges. Consequently, at constant confidence the worst-case sample complexity for parameters $(\alpha_1,\alpha_2)=(d,q)$ is $\Theta((d+q)/\epsilon)$ for undirected graphs and $\Theta((d+q\log(1/\epsilon))/\epsilon)$ for directed graphs. A distribution-dependent neighborhood-leverage quantity explains both rates. Thus edge direction causes a genuine logarithmic statistical penalty even when the target concept is known, $\alpha_1=0$, and $\alpha_2=1$.

## Contributions

Our results are summarized in Table~.

First, we prove a sharp expected-risk upper bound for the existing learner on every measurable
undirected graph:

$$\mathbb E L(h_S)\le \frac{\alpha_1}{m+1}+\frac{7\alpha_2}{2m}.$$

The central step is a weighted Caro-Wei inequality for probability measures. The finite weighted
inequality is classical and has stronger power-weighted forms in feedback-graph learning. The novelty is that its direct integration of the
conditional-average estimator removes the entire accuracy logarithm. An i.i.d. discretization
argument extends the inequality to arbitrary measurable domains.

Second, we prove that the directed logarithm is unavoidable in its strongest qualitative regime.
Our hard concept class is a singleton, so $\alpha_1=0$ and the learner knows every label before
sampling. On $q$ disjoint one-way chains, $\alpha_2=q$. The unknown marginal puts a fixed total
mass on each adjacent zero-one pair but hides an independent sign in its within-pair mass split.
Not observing a pair reveals exactly no information about its sign. Every suffix average contains
the sum of its missing signs. Averaging the resulting posterior variances over all suffixes produces
the harmonic number $H_s$ and risk $\Omega(q\log(1+m/q)/m)$. A Hilbert-space fourth-moment
argument upgrades Bayes expectation to a constant-probability minimax lower bound.

Third, a separate Assouad construction on $q$ undirected edges proves $\Omega(q/m)$ risk with a
known concept. Combining these constructions with ordinary PAC hardness gives the exact worst-case
envelopes in Table~. We also introduce a distribution-dependent neighborhood
leverage. It is at most $\alpha_2$ for undirected graphs and equals $\Theta(qH_s)$ on the hard
directed family, exposing the quantity that direction allows to grow.

## Keywords

conditional averages, directed graphs, neighborhood learning, minimax rates, sample complexity, Caro-Wei inequality

## Files

- `main.pdf`
- `main.tex`
- `references.bib`
- `iclr2027_conference.sty`, `iclr2027_conference.bst`, `natbib.sty`, `fancyhdr.sty`
- `main.pdf.ots`, `README.md.ots` OpenTimestamps priority proofs
