# 6. Spectral Statistics and Scale Regimes

> *The relevant information is not in the levels,*
> *but in the intervals between them.*
> — Freeman Dyson

## Operational introduction

In the previous chapters, a deterministic operator $M$ was constructed and its spectral decomposition was introduced in finite regimes.

In this chapter, the focus shifts from the individual values of the eigenvalues to the **statistical relations between them**.

The goal is to define and apply measures that allow one to characterise the collective behaviour of the spectrum of the operator $M$ as the domain is enlarged and as the initial scale $X_0$ — which enters explicitly into the definition of the operator — is shifted along the number line.

No hypothesis of universality is assumed. The tools are introduced prior to any interpretation.

## From a discrete spectrum to the statistical regime

In finite dimension, the spectrum of $M$ consists of a discrete and ordered set of real eigenvalues:

$$
\lambda_1 \leq \lambda_2 \leq \cdoys \leq \lambda_n.
$$

As $N$ increases, it becomes natural to investigate not only the absolute values of these eigenvalues, but also the **statistical structure of the spacings between them**.

These relations are sensitive to internal correlations of the operator and constitute the central object of the analysis that follows.

## Normalised spacings

We define the consecutive spacings:

$$
s_i = \lambda_{i+1} - \lambda_i.
$$

To allow comparison across different scales and matrix sizes, the spacings are normalised by the local mean spacing:

$$
\hat{s}_i = \frac{s_i}{\langle s \rangle}.
$$

The empirical distribution of these values provides a first statistical characterisation of the spectrum.

At this stage, no theoretical form is postulated.

## The spacing distribution $P(s)$

The function $P(s)$ is defined as the histogram of the normalised spacings $\hat{s}_i$.

It describes the relative frequency of different separations between consecutive eigenvalues and allows one to distinguish between regimes with or without significant spectral correlations.

**Notebook 06** (`06_scale_regimes_and_spectral_statistics.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/06_scale_regimes_and_spectral_statistics.ipynb) computes $P(s)$ for different values of $N$ and $X_0$, while keeping the operator fixed.

The observed distribution will be analysed only in a comparative manner in the subsequent chapters.

## Ratio of adjacent spacings

To reduce dependence on explicit rescaling, we introduce the ratio of adjacent spacings:

$$
r_i = \frac{\min(s_i, s_{i+1})}{\max(s_i, s_{i+1})}.
$$

This quantity is bounded in the interval $[0, 1]$ and allows one to define a simple scalar statistic given by:

$$
\langle r \rangle = \frac{1}{N-2} \sum_{i=1}^{N-2} r_i,
$$

where the sum is taken over indices $i$ in the spectral *bulk*.

The mean value $\langle r \rangle$ provides a compact indicator of the degree of correlation between consecutive eigenvalues.

In this chapter, this statistic is introduced **solely as a conceptual tool**.

## Number variance $\Sigma^2(L)$

A third statistical measure considers fluctuations in the number of eigenvalues contained within intervals of length $L$.

We define $\Sigma^2(L)$ as the variance of the number of eigenvalues contained in spectral windows of length $L$, after appropriate normalisation.

This measure provides complementary information about the global rigidity of the spectrum.

**Notebook 06** implements only the calculation of *P(s)* for a structural scale and a contrast observation.
The statistics $\langle r \rangle$ and $\Sigma^2(L)$ are introduced here as conceptual tools. Their operational implementation will be carried out in later notebooks.

## Scale regimes and experimental protocol

All the statistics introduced depend on two fundamental parameters:

* the size of the operator, $N$;
* the initial observation scale, $X_0$.

In this chapter, the statistical tools are applied systematically to investigate how the spectrum of $M$ responds to variations in these parameters.

No interpretation is attached to the results at this point. The focus remains on defining the protocol and ensuring the consistency of the measurements.

It is emphasised that any statistical regularities that may be observed are not attributed to intrinsic properties of the arithmetic sequence itself, but to the operator constructed from it.

## Delimitation of scope

In this chapter:

* fundamental spectral statistics were introduced;
* the measures were applied to the operator $M$;
* the dependence on $N$ and $X_0$ was made explicit;
* no universal class was named;
* no physical explanation was proposed.

The observations remain strictly descriptive. What has been constructed so far is not an interpretation of the spectrum, but a vocabulary with which to describe it.

---

## Point of rest

Up to this point, the operator has been constructed and its spectral decomposition has been formally defined. The relevant statistical measures have been introduced, but the experimental protocol is not yet complete.

The minimal set of tools required to confront the observed behaviour with known spectral classes is now in place.

The reading and interpretation of these results will be addressed separately, only after the systematic execution of the measurements.

---

[$\gets$ Previous Chapter](./05_spectral_mechanics.md) | [Contents](../../index.md) | [Next Chapter $\to$](./07_eigenvalues_recognition_of_goe.md)
