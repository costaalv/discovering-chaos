# 13. The Universality of Chaos — Scale Sweeps

> *Nature uses only the longest threads to weave its patterns,*  
> *so that each small piece of its fabric*  
> *reveals the organisation of the entire tapestry.*  
> — Richard Feynman

## A local law or a universal one?

In the previous chapters, we established a central result: when prime numbers are observed through the lens of logarithmic scaling, the spectrum of the operator $ M $ robustly exhibits the statistics of the *Gaussian Orthogonal Ensemble* (GOE), the hallmark of quantum chaos.

This observation was initially made within specific windows of the number line, centred around values such as $ X_0 = 10^7 $ or $ 10^8 $. An inevitable question then arises: is this a local phenomenon, confined to particular regions, or a universal property of the distribution of prime numbers?

Random Matrix Theory offers a clear prediction: genuinely chaotic systems display universal statistics, independent of microscopic details. This chapter tests that prediction directly in the arithmetic context.

## The experiment: sweeping across scales

To investigate the universality of the phenomenon, we perform a systematic sweep across several orders of magnitude of the number line. Keeping fixed both the construction of the operator $ M $ and the logarithmic observation lens, we vary only the starting point $ X_0 $, exploring values ranging from $X_0 = 10^3 \quad \text{to} \quad X_0 = 10^8$.

At each scale, we compute one of the most stable and informative statistics in spectral theory: the mean ratio of adjacent level spacings,

$$
\langle r \rangle = \left\langle \frac{\min(s_i, s_{i+1})}{\max(s_i, s_{i+1})} \right\rangle.
$$

This statistic has well-known universal values:

- $\langle r \rangle \approx 0.386$ for Poisson;
- $\langle r \rangle \approx 0.536$ for GOE.

The hypothesis under test is both simple and strong: if the GOE regime is universal, the value of $\langle r \rangle$ should converge to the GOE prediction and become independent of the scale $X_0$.

## The sweep laboratory

**Notebook 13** (`13_scale_sweeps.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/13_scale_sweeps.ipynb) implements this experiment in an automated fashion. For each value of $X_0$, the operator is constructed, its spectrum is computed, and the statistic $\langle r \rangle$ is extracted.

The final outcome is a plot of $\langle r \rangle$ as a function of $\ln(X_0)$, which allows the statistical regime to be tracked continuously across scales.

This procedure eliminates interpretations based on isolated cases and exposes the global structure of the phenomenon.

## The transition to universal chaos

Analysis of the results reveals three clearly organised regimes along the scale axis.

### The low-scale regime: the echo of order

For small values of $X_0$, typically $10^3$ and $10^4$, the statistic $\langle r \rangle$ remains close to the Poisson value. In this regime, the distribution of primes is still strongly influenced by discrete irregularities and local arithmetic effects. The correlations required for the emergence of chaos are not yet fully developed.

### The transition zone: the awakening of chaos

Around $X_0 \approx 10^4$, a rapid transition is observed. The value of $\langle r \rangle$ increases sharply, moving away from the Poisson regime and approaching the GOE value. This behaviour indicates that the system reaches a critical level of complexity, at which long-range correlations begin to dominate the spectral statistics.

### The asymptotic regime: GOE universality

Beyond scales of order $10^7$, the value of $\langle r \rangle$ stabilises unequivocally at the value predicted for the GOE. More importantly, it becomes essentially independent of $X_0$.

We thus enter the asymptotic regime: the observed statistics no longer carry information about a specific position on the number line and instead reflect a universal law.

## Synthesis

The scale sweep reveals that the transition observed in earlier chapters is not a local artefact, but the manifestation of a deep and universal structure. The duality between Poisson and GOE does not represent a contradiction, but rather a geometric journey along the prime number line.

As the scale increases, the system leaves local order behind and converges towards a regime of universal chaos, in perfect agreement with the predictions of Random Matrix Theory.

The music of the primes is not a regional accident. It is a structural constant of the arithmetic universe — audible only when observed at the correct scale.

---

## Point of rest

Up to this point, a precise distinction has been established between a local phenomenon and a universal diagnosis.
The notion of universality has been defined operationally as independence with respect to the starting point $X_0$, rather than as an asymptotic extrapolation or a qualitative argument.

Under this criterion, a scale-sweep protocol was formulated in which the construction of the operator $M$ and the logarithmic observation lens remain fixed, while only the starting point $X_0$ is displaced across several orders of magnitude. To track this sweep, the statistic $\langle r \rangle$ was adopted as a compact and robust indicator of spectral correlation, enabling direct comparison between regimes without the introduction of additional assumptions.

The observed outcome organises itself into three well-defined regions: an initial regime compatible with Poisson statistics, a transition zone centred around $X_0 \approx 10^4$, and an asymptotic regime in which $\langle r \rangle$ stabilises near the characteristic GOE value. Above a critical scale, the diagnosis ceases to depend on the position along the number line and instead reflects a stable statistical behaviour.

Universality thus ceases to be an intuitive inference and becomes an operational result. There exists a regime in which the operator $M$, observed on the logarithmic scale, persistently exhibits spectral signatures compatible with the GOE class under sweeps of $X_0$.

In the next chapter, this stability will be put to the test. We will investigate which variations of the protocol preserve the observed diagnosis and which degrade it, explicitly delineating the minimal conditions required for the persistence of the identified universality.

---

[$\gets$ Previous Chapter](./12_mirror_observer.md) | [Contents](../../index.md) | [Next Chapter $\to$](./14_alternative_operators.md)
