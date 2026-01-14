# 5. The Mechanics of the Spectrum

> *Eigenvalues are not properties of numbers,*
> *but of operators.*
> — John von Neumann

## Operational recap

In the previous chapters, a deterministic operator $M$ was constructed from the arithmetic signal $\Delta_\pi(x)$ and an explicit change to logarithmic scale.

This operator was introduced as a **geometric and visual object**, without any spectral analysis.

The purpose of this chapter is to **formally describe** the basic elements of spectral analysis as applied to the operator $M$, within a fully controlled regime.

Nothing new will be introduced.
Only the necessary tools will be defined.

## A finite and controlled domain

Before moving to large scales, it is instructive to work within a small domain, where all objects can be directly inspected.

In this chapter, we fix:

$$
N = 32,
$$

and consider the discrete domain $x \in {1, 2, \cdots, 32}$.

This choice has no theoretical significance.
It merely allows all components of the operator to be explicitly computed and examined.

## Preparation of the input data

**Notebook 05** (`05_spectral_mechanics.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/05_spectral_mechanics.ipynb) begins by generating, for each $x \leq 32$:

* the value of the arithmetic signal $\Delta_\pi(x)$;
* the corresponding value of $\ln(x)$.

These data constitute the **only inputs** to the operator.
No filtering, smoothing, or additional normalisation is applied.

## Explicit construction of the operator

With the vectors $\Delta_\pi(x)$ and $\ln(x)$ defined, the operator $M$ is constructed directly via the formula:

$$
M_{ij}
=
\cos\!\big(\Delta_\pi(x_i)\,\ln(x_j)\big)
+
\cos\!\big(\Delta_\pi(x_j)\,\ln(x_i)\big).
$$

For $N = 32$, this yields a real, symmetric matrix of dimension $32 \times 32$.

The heatmap shown in **Notebook 05** allows the internal organisation of the operator to be visualised within this finite regime.

No interpretation is attached to this visualisation.
It merely confirms that the operator is well defined and structurally non-trivial.

## Eigenvalues and eigenvectors: minimal definitions

Let $M$ be a real symmetric matrix.

A real number $\lambda$ is called an eigenvalue of $M$ if there exists a non-zero vector $v$ such that:

$$
Mv = \lambda v.
$$

The corresponding vector $v$ is called an eigenvector.

These objects are not introduced as physical analogies.
They constitute the canonical decomposition of symmetric operators in real vector spaces.

## The spectrum of the operator in finite dimension

**Notebook 05** explicitly computes:

* the complete set of eigenvalues of $M$;
* the associated eigenvectors.

For $N* = 32$, the spectrum is discrete and finite.
All eigenvalues are real, as guaranteed by the symmetry of the operator.

Ordering these eigenvalues and inspecting the eigenvectors makes it possible to verify that:

* the operator admits a complete spectral basis;
* different spectral modes correspond to distinct patterns of distribution across the indices $i$.

At this stage, **no statistics are computed**.
No regularity is postulated.

## Limits of the finite regime

The analysis at $N = 32$ is not intended to reveal universal laws.
Its purpose is to:

* fix definitions;
* validate the construction of the operator;
* establish the spectral vocabulary to be used later.

The behaviour of interest does not fully manifest at such small scales.

To observe it, we will need to study:

* how the spectrum varies with the size of the domain;
* how it depends on the initial scale $X_0$.

## Scope delimitation

In this chapter:

* the operator $M$ was explicitly diagonalised;
* eigenvalues and eigenvectors were defined and computed;
* no spectral statistics were analysed;
* no universal hypothesis was formulated.

The operator remains unchanged.
Only the regime of observation will change.

---

## Point of Rest

Up to this point, spectral analysis has been introduced in its formal sense. The operator has been examined in finite dimension. All necessary tools are now defined.

In the next chapter, these tools will be applied systematically to growing domains, allowing us to observe how the operator’s spectrum responds to changes of scale.

*Nothing will be assumed. Everything will be measured*.

---

[$\gets$ Previous Chapter](./04_operator_M.md) | [Contents](../../index.md) | [Next Chapter $\to$](./06_scale_regimes_and_spectral_statistics.md)
