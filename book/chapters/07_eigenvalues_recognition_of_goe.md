# 7. Recognition of a Universal Class

> *Mathematics possesses an inexplicable effectiveness*
> *in describing the structures of nature.*
> — Eugene P. Wigner

## What changes when crossing the boundary

Up to this point, the procedure has been strictly constructive.

An arithmetic signal was defined, a change of scale was fixed, and a deterministic operator $M$ was constructed by explicit symmetrisation. The spectrum of this operator was then measured, and a complete statistical protocol was established.

The decisive point is that none of this required probabilistic hypotheses, stochastic sampling, or random models. The operator remained the same. What varied was solely the observation regime.

At the beginning of this part of the book, a change of status occurs: the measured statistics cease to be merely descriptive records and are instead confronted with known spectral classes.

This comparison introduces no new objects. It introduces only a vocabulary of recognition.

## Spectral classes as reference patterns

In spectral analysis, certain families of operators exhibit robust, stable, and recurrent statistical behaviours. When a spectrum displays statistical signatures that remain stable under changes in size and scale, it is said to be compatible with a universal class.

Two reference classes will be used in this chapter:

* the **uncorrelated class**, associated with spectra whose spacings behave as approximately independent variables (often modelled by an exponential law);
* the **locally repulsive correlated class**, associated with spectra that suppress very small spacings and exhibit global statistical rigidity (whose canonical prototype is the *Gaussian Orthogonal Ensemble*, GOE).

The introduction of these classes is not a hypothesis about $M$. It is an instrument for interpreting measurements that have already been performed.

## The first signature: level repulsion

Let us consider the empirical distribution $P(s)$ of the normalised spacings, as defined in the previous chapter.

**Notebook 07** (`07_eigenvalues_recognition_of_goe.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/07_eigenvalues_recognition_of_goe.ipynb) shows that, for sufficiently large values of $N$ and for large initial scales $X_0$, the empirical density begins to exhibit a decisive feature: the probability of very small spacings becomes strongly suppressed.


In descriptive terms, $P(s)$ approaches a shape that:

* is approximately zero at $s = 0$;
* increases from zero to a maximum at $s > 0$;
* decays for larger spacings.

This pattern is not compatible with uncorrelated spectra.
It is the minimal signature of local level repulsion.

## The scalar statistic and the reference value

The ratio between adjacent spacings,

$$
r_i = \frac{\min(s_i, s_{i+1})}{\max(s_i, s_{i+1})},
$$

yields a mean value $\langle r \rangle$ that summarises the degree of local spectral correlation.

The crucial point is that, for universal classes, $\langle r \rangle$ assumes characteristic values.

In particular, for the GOE, the literature establishes an approximately constant reference value:

$$
\langle r \rangle_\text{GOE} \approx 0.536
$$

whereas for uncorrelated spectra the typical value is substantially smaller:

$$
\langle r \rangle_\text{nc} \approx 0.386
$$

When the protocol of **Notebook 07** is applied to the operator $M$, it is observed that, in appropriate regimes of $N$ and $X_0$, the measured value of $\langle r \rangle$ systematically approaches the GOE reference value.

This convergence is robust under moderate variations of the protocol parameters (*bulk* selection, logarithmic window, and minimal numerical perturbations), indicating that it is not a local coincidence.

## Global rigidity of the spectrum

Local level repulsion is only part of the universal signature.

A second, independent characteristic is statistical rigidity: the fluctuation in the number of eigenvalues within spectral intervals grows much more slowly than in uncorrelated spectra.

The number variance $\Sigma^2(L)$, defined in the previous chapter, measures precisely this fluctuation.

**Notebook 07** demonstrates that, in regimes where $P(s)$ exhibits suppression at $s = 0$ and $\langle r \rangle$ approaches the GOE reference value, the empirical curve of $\Sigma^2(L)$ departs from linear growth ($\Sigma^2(L) \sim L$) — characteristic of Poisson-type systems — and instead assumes a **logarithmic growth** ($\Sigma^2(L) \sim \ln(L)$).

This transition constitutes robust evidence of spectral rigidity in the operator $M$. It indicates that the levels not only repel locally, but also preserve long-range correlations that stabilise the structure of the system.

Two independent statistics — local ($P(s)$) and global ($\Sigma^2$) — thus converge towards the recognition of the same universal class.

## Determinism and universality

There is one aspect that deserves to be made explicit.

The GOE is traditionally introduced as a random ensemble of real symmetric matrices. The universality observed in that context refers to the fact that many families of operators, under broad conditions, exhibit the same statistics in the spectral bulk.

In the present work, the operator *M* is not random. It is constructed deterministically from an elementary arithmetic function and a fixed change of scale.

The observation made here is therefore more restricted and more concrete:

> a deterministic operator, constructed exclusively from prime counting and symmetrisation, can exhibit spectral statistics compatible with the universal GOE class.

Nothing beyond this is claimed.

What this observation establishes is an experimental fact: a universal class can emerge without any external randomness being injected into the procedure.

## Protocol parameters and stability of the phenomenon

To avoid the recognition of the universal class depending on arbitrary choices, it is necessary to make explicit which protocol parameters affect the result and in what way.

In **Notebook 07**, three parameters play a dominant role:

* `span`, which controls the extent of the logarithmic window and therefore the internal variability of the sampled signal;
* `jitter`, which introduces a minimal numerical perturbation, reducing artificial alignment effects;
* `alpha`, which defines the analysed *bulk*, minimising edge effects.

The relevant phenomenon is not the attainment of an exact value in a single configuration, but the qualitative stability of the signatures (local repulsion, $\langle r \rangle$ value, and rigidity) under moderate variations of these parameters.

When such stability is observed, class recognition ceases to be a coincidence and becomes a diagnosis.

## Delimitation of what has been recognised

It is essential to maintain the distinction between three levels:

1. **Constructive** — $M$ was defined by an explicit and deterministic expression.
2. **Observational** — spectral statistics were measured in large-$N$ regimes and at high initial scales $X_0$.
3. **Classificatory** — the measured signatures were compared with known universal patterns.

The third level does not alter the first two. It merely names an observed behaviour.

In this chapter, the behaviour recognised is the statistical membership of the spectrum of the operator $M$, in appropriate regimes, in the universal GOE class.

---

## Point of rest

Up to this point, the statistical protocol has been applied to the spectrum of the operator $M$ in progressively extended regimes.
Multiple independent statistics have converged consistently towards the same spectral class.

The observed behaviour has been identified as compatible with the GOE class.
No new objects have been introduced. No additional hypotheses have been assumed.

In the next chapter, we will investigate how this diagnosis behaves under systematic scale sweeps and under controlled modifications of the operator, delineating the minimal conditions for the emergence of the observed universality.

---

[$\gets$ Previous Chapter](./06_scale_regimes_and_spectral_statistics.md) | [Contents](../../index.md) | [Next Chapter $\to$](./08_the_discovery_lens.md)
