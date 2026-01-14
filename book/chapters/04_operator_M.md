# 4. The Harmonic Spectrometer

> *Structure reveals itself when*  
> *we choose the correct representation.*  
> — Hermann Weyl

## From signal to structure

In the previous chapters, we identified a central object: the arithmetic signal $\Delta_\pi(x)$.

Point by point, it measures the imbalance between two functional roles of the primes — **structuring** and **stabilising** — as observed in Chapter 2 along the number line. This signal exhibits a persistent oscillatory behaviour, which we called the *pulse*.

However, there is an intrinsic limitation to what a one-dimensional signal can reveal.

A pulse indicates that something happens.  
It does not describe the full shape of what happens.

If we wish to understand internal correlations and global patterns, we must abandon a purely sequential reading and project the signal into a structure where interference can occur.

In mathematical terms: **a one-dimensional signal can be measured; a structure requires projection**.

This change of regime marks the beginning of this part of the book.

## The need for an operator

Eigenvalues, collective modes, and spectral regularities do not belong to isolated functions.  
They belong to **operators**.

To extract structural information from the pulse $\Delta_\pi(x)$, it is not sufficient to smooth it, accumulate it, or rescale it. The signal must be placed into interaction with itself — we must construct a two-dimensional object capable of registering cross-correlations between different points on the number line.

That object will be a matrix.

Not a statistical matrix, nor a random one, but a deterministic operator constructed exclusively from:
- exact prime counting;
- an explicit change of scale;
- structural symmetrisation.

What we seek is not prediction, but observability.

## Definition of the harmonic operator

We define the operator $M$ by its elements:

$$
M_{ij}
=
\cos\!\big(\Delta_\pi(x_i)\,\ln(x_j)\big)
+
\cos\!\big(\Delta_\pi(x_j)\,\ln(x_i)\big).
$$

Each term in this expression has a precise role:
- $\Delta_\pi(x)$ provides the arithmetic signal;
- $\ln(x)$ adjusts the observational scale;
- the cosine converts the product into harmonic phase;
- the sum enforces explicit symmetry.

Nothing is tuned, filtered, or normalised at this stage beyond what is structurally required.

The operator is **defined**, not calibrated.

## The proper scale

Prime numbers are inherently multiplicative entities.  
Their density decays according to a logarithmic law, as established by the Prime Number Theorem.

Observing arithmetic on a linear scale is convenient, but it is not neutral.  
The linear scale distorts relations that are naturally multiplicative.

The use of the logarithm is not an aesthetic choice.  
It is a requirement of structural compatibility.

The factor $\ln(x)$ acts as a lens: it re-expresses the number line on a scale where the internal relations of the primes become comparable and stable across the observed domain.

Without this lens, the operator loses coherence.  
With it, the operator becomes stably observable.

## The harmonic kernel

The cosine plays a dual role.

First, it transforms the product $\Delta_\pi(x)\,\ln(x)$ into a bounded oscillation, translating arithmetic tension into phase.

Second, being an even function, it removes the distinction between opposite signs. The operator does not measure direction — it measures **intensity of correlation**.

Positive and negative values contribute equally.

The aim here is not to track local fluctuations, but to enable the observation of global patterns.

## Symmetry and observability

The operator is constructed to be explicitly symmetric:

$$
M_{ij} = M_{ji}.
$$

This choice is not technical, but conceptual.

In mathematics, symmetric operators possess a fundamental property:  
**all of their eigenvalues are real**.

This condition ensures that the spectrum of the operator lies entirely on the real line, making it suitable for rigorous spectral analysis.

We are therefore constructing an arithmetic operator whose spectral structure can be investigated in a mathematically controlled way.

The operator $M$ is not fed by a normalised version of $\Delta_\pi$, but by the absolute signal of its accumulated divergence.

It is the discrete steps of $\pi(x) - 2\pi(x/2)$, as global arithmetic events, that generate spectral coherence under projection.

The emerging statistics do not arise from relative fluctuations, but from the discontinuous geometry of prime counting.

Nothing more is claimed.

## The visual laboratory

**Notebook 04** (`04_operator_M.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/04_operator_M.ipynb) implements the operator $M$ directly and allows its structure to be visualised as a heat map, for different initial scales $X_0$.

When executing it, observe carefully:
- At small scales, the operator appears irregular, fragmented, and noisy.
- As $X_0$ increases, geometric patterns begin to emerge.
- The initial fragmented appearance gives way to visually organised regions.

No additional transformation is applied.  
The only variable is scale.

The visualisation proves nothing.  
It merely indicates that a non-trivial organisation is present.

## Delimitation of scope

In this chapter, we performed a fundamental transition:
- from signal to operator;
- from sequence to geometry;
- from counting to structure.

The spectrometer has been built.

In the following chapters, we will abandon visual inspection and apply formal tools of spectral analysis — eigenvalues, level spacings, and eigenmodes — to quantify spectral regularities, if present.

Nothing will be added to the system.

---

## Point of Rest

Up to this point, only what is essential has been established. A deterministic operator has been constructed directly from the arithmetic signal $\Delta_\pi(x)$, without statistical assumptions or spectral hypotheses.

No analysis has yet been performed. Only the geometric structure of the operator has been exposed to observation.

The spectrometer is defined.  
The analysis has not yet begun.

---

[$\gets$ Previous Chapter](./03_the_search_for_balance.md) | [Contents](../../index.md) | [Next Chapter $\to$](./05_mecanica_espectro.md)
