# 11. The Anatomy of Chaos — Eigenvector Analysis

> *What we observe is not nature itself,*  
> *but nature exposed to our method of questioning.*  
> — Werner Heisenberg

In the previous chapters, the analysis focused on the **eigenvalues** of the operator $ M $.  
They provided the spectral locations of the system’s excitations and, through their statistics, made it possible to distinguish uncorrelated regimes (Poisson) from correlated regimes (GOE).

In this chapter, the focus shifts to the **eigenvectors** of the operator.

If eigenvalues indicate *where* spectral structures are located, eigenvectors reveal *how* this complexity is distributed internally.
They encode the structural patterns of the system and allow us to determine whether the observed regime is merely statistically compatible or **structurally ergodic**.

## Beyond eigenvalues

In systems associated with quantum chaos, it is not sufficient for spectral spacings to exhibit level repulsion.  
It is also necessary that the eigenvectors be **delocalised**, filling the space in an approximately uniform manner.

This property distinguishes genuinely chaotic systems from those that are merely perturbed or artificially randomised.

To investigate this aspect, we introduce two complementary tools:

* the *Participation Ratio*;
* the statistics of eigenvector components.

## Tool I — Participation Ratio

The *Participation Ratio* ($ PR $) quantifies the degree of spreading of an eigenvector.

For a normalised eigenvector

$$
v = (v_1, v_2, \dots, v_n),
$$

it is defined as

$$
\mathrm{PR} = \frac{(\sum_{i=1}^{n} |v_i|^2)^2}{\sum_{i=1}^{n} |v_i|^4}.
$$

Its interpretation is straightforward:

* localised eigenvectors have small $ PR $, of order unity;
* delocalised eigenvectors have $ PR $ proportional to $ N $.

In Random Matrix Theory, eigenvectors of the GOE class are **ergodic**.  
For them, the normalised ratio

$$
\frac{PR}{N}
$$

concentrates around the universal value

$$
\frac{1}{3}.
$$

This value constitutes a structural signature of quantum chaos, independent of the detailed form of the operator.

## Tool II — Component statistics

A second, independent theoretical prediction concerns the distribution of individual eigenvector components.

For matrices in the GOE class, the components of a typical bulk eigenvector behave as random variables drawn from a **real Gaussian distribution**, with zero mean and variance fixed by normalisation.

This prediction can be tested directly:

* select an eigenvector from the centre of the spectrum;
* construct the histogram of its components;
* compare it with the theoretical Gaussian curve;
* quantify compatibility using the Kolmogorov–Smirnov test.

A high *p*-value indicates no statistical evidence to reject the Gaussian hypothesis.

## The empirical laboratory

**Notebook 11** (`11_eigenvector_anatomy.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/11_eigenvector_anatomy.ipynb) implements these two analyses systematically, allowing direct comparison between two observation regimes:

* linear sampling;
* logarithmic sampling.

For each case, four plots are produced:

* the histogram of the components of a bulk eigenvector;
* the corresponding theoretical Gaussian curve;
* the distribution of $ PR/N $ across the spectrum;
* a visual comparison between regimes.

## Results — genuine signal and methodological artefact

The results display an instructive contrast between the two observation regimes.

### Logarithmic scale — the genuine signal of chaos

Under logarithmic parametrisation, one observes that:

* eigenvector components consistently follow a Gaussian distribution;
* the Kolmogorov–Smirnov test returns high *p*-values;
* the distribution of $ PR/N $ is sharply concentrated around $ 1/3 $.

These results indicate that the eigenvectors are **ergodic** and that the observed complexity is not superficial, but a structural property of the operator.

### Linear scale — the methodological phantom

Under linear parametrisation, the results initially appear similarly compatible with the GOE: approximately Gaussian components and values of $ PR/N $ close to $ 1/3 $.

This resemblance, however, is misleading.

In this regime, the constructed matrix is structurally impoverished and requires the introduction of small numerical perturbations (`jitter`) to avoid artificial degeneracies.

The eigenvectors then primarily reflect the statistical properties of the injected noise rather than the underlying arithmetic structure.

What is measured in this case is not the chaos of the primes, but a **methodological artefact**.

## Structural diagnosis

The comparison between the two regimes allows a clear diagnosis:

> ergodic eigenvectors obtained without artificial noise injection constitute the unequivocal signature of a genuinely chaotic regime.

The logarithmic scale satisfies this condition.  
The linear scale does not.

## Applied perspective — a cryptographic primitive

The observed properties suggest potential applications in areas such as cryptography.

Parameters such as $ X_0 $, $ N $, and the arithmetic function $ \Delta_\pi(x) $ may be interpreted as a private key, from which highly complex eigenvectors are generated deterministically.

The inverse problem — reconstructing these parameters from an ergodic eigenvector — presents high computational complexity.

This constitutes a *quantum primitive* not in the physical sense, but in the statistical one: the exploited properties coincide with those of quantum chaotic systems, without requiring quantum hardware.

This possibility remains speculative, but it illustrates the conceptual reach of the developed formalism.

---

## Point of rest

Up to this point, the spectral analysis has been extended from the eigenvalues to the eigenvectors of the operator $M$.

It has been shown that the GOE regime manifests not only in level statistics, but also in the internal geometry of the states: the eigenvectors are ergodic, the Participation Ratio confirms their structural delocalisation, and the Gaussian distribution of components emerges consistently.

This set of observations made it possible to clearly distinguish genuine signal from methodological artefacts. **Notebook 11** provides the direct empirical basis for these conclusions.

With this, the characterisation of the chaotic regime associated with the operator $M$ is complete, both in its spectrum and in the internal structure of its states.

In the next chapter, we conclude the conceptual journey, bringing together the results obtained into a unified structural reading.

---

[$\gets$ Previous Chapter](./10_conditions_for_chaos.md) | [Contents](../../index.md) | [Next Chapter $\to$](./12_mirror_observer.md)
