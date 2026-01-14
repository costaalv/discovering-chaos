# 9. The Logarithmic Scale — The Lens for Chaos

> *Measure what is measurable,*  
> *and make measurable what is not.*  
> — Galileo Galilei

One of the central results of this work is the observation that the emergence of GOE-type statistics in the spectrum of the operator $M$ is **not invariant under changes of scale**.

On the contrary, it manifests robustly only when the system is observed through a specific lens: the **logarithmic scale**.

This chapter investigates the reason for this selectivity.  
The question is no longer *whether* the statistics change with scale — that has already been established — but *why* only the logarithmic scale creates the conditions required for the emergence of a correlated regime.

The answer lies in the very geometry of the distribution of prime numbers.

## The topography of the primes

The prime counting function $ \pi(x) $ describes the number of primes less than or equal to $ x $.  
The Prime Number Theorem establishes that, asymptotically,

$$
\pi(x) \sim \frac{x}{\ln(x)},
$$

which implies that the local density of primes along the linear number line satisfies

$$
\frac{d\pi}{dx} \approx \frac{1}{\ln(x)}.
$$

This expression contains a fundamental piece of information:  
**the density of primes decays continuously as $ x $ increases**.

Therefore, any observation carried out directly on the linear scale takes place on a terrain whose dominant structural feature is a progressive structural degeneracy of density.

## Empirical verification

The geometric structure described above is not merely asymptotic or conceptual.  
It is verified directly in **Notebook 09** (`09_logarithmic_scale.ipynb`)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/09_logarithmic_scale.ipynb),
where the empirical density of primes is measured and compared in both linear and logarithmic scales.

The plots produced in this experiment show explicitly:

* the continuous decay of $d\pi/dx$ on the linear scale;
* the transformation of this collapse into a smooth growth law when passing to $d\pi/d(\ln\,x)$.

These visualisations provide the geometric background necessary to interpret the spectral regimes observed in the previous chapters.

## The linear lens: an unstable stage

When the system is observed under a linear parametrisation, the density of states associated with the primes decreases continuously.
There is no stable local scale: each successive interval contains less structure than the previous one.

In this regime, the more subtle statistical fluctuations — those responsible for long-range spectral correlations — are submerged beneath a dominant trend of rarefaction.

The observational outcome is straightforward:

> on a stage whose geometry collapses continuously, only uncorrelated statistics survive.

This is why, even after local normalisation of spacings, the spectrum of the operator $ M $, when observed linearly, exhibits Poisson-type statistics.

This is not due to a lack of structure in the operator, but to the absence of geometric conditions allowing that structure to manifest.

## Change of variable and logarithmic density

Let us now consider the change of variable

$$
y = \ln(x).
$$

The density of primes with respect to the new variable is obtained by the chain rule:

$$
\frac{d\pi}{dy} = \frac{d\pi}{dx} \cdot \frac{dx}{dy}.
$$

Since $ dx/dy = x $, it follows that

$$
\frac{d\pi}{d(\ln x)} = x \cdot \frac{d\pi}{dx}.
$$

Substituting the asymptotic approximation for the linear density,

$$
\frac{d\pi}{dx} \approx \frac{1}{\ln(x)},
$$

we obtain

$$
\frac{d\pi}{d(\ln x)} \approx \frac{x}{\ln(x)}.
$$

This expression is fundamental:  
the function $ x/\ln(x) $ is **strictly increasing**.

What was previously a continuous degeneracy of the linear geometry is now transformed into a smooth and predictable growth law.

## The logarithmic lens: stabilising the stage

The logarithmic scale does not render the density of primes constant.  
It does something subtler and more important: it transforms a structural degeneracy into a regular geometry.

Instead of a density that tends to zero, we obtain a density that grows in a controlled manner, without violent oscillations.  
This creates a stable background against which fluctuations can be analysed meaningfully.

It is in this regime that:

* the function $ \Delta_\pi(x) $ exhibits structural fluctuations across multiple scales;
* the operator $ M $ becomes highly variable;
* the spectrum begins to display local correlations and global rigidity.

GOE-type statistics are not created by the logarithmic scale.  
They are **revealed** by it.

## The condition for emergence

Numerical experiments show that the transition from an uncorrelated regime to the GOE regime occurs systematically from initial scales of order

$$
X_0 \approx 10^4\text{–}10^5.
$$

This observation now admits a clear geometric interpretation.

Below this region, the distribution of primes is still dominated by discrete irregularities and finite-size effects.
Above it, the asymptotic law $ x/\ln(x) $ governs the density robustly.

At this point, the “stage” stabilises.  
From then on, fluctuations — rather than the mean trend — dominate the spectral statistics.

## Synthesis

The role of the logarithmic scale can now be summarised precisely:

* it does not introduce randomness;
* it does not impose universality;
* it corrects the geometry of the observation space.

By aligning observation with the natural scale of the primes, the logarithmic lens creates the minimal conditions under which deep spectral correlations become visible.

The music of chaos does not arise by chance.  
It can only be heard when the stage is properly constructed.

---

## Point of rest

Up to this point, the distinction between linear and logarithmic observation has been reformulated as a geometric problem of density.

On the linear scale, prime density decays as  
$d\pi/dx \approx 1/\ln(x)$, producing a structurally unstable background in which fluctuations are continuously damped by the rarefaction of the system.

On the logarithmic scale, the corresponding density,  
$d\pi/d(\ln x) \approx x/\ln(x)$, transforms this collapse into a law of smooth growth. What was previously suppressed by structural degeneracy becomes observable.

It thus becomes clear that the logarithmic lens does not “create” universality. It merely stabilises the observation regime in which fluctuations can dominate the statistical behaviour of the operator.

The empirically observed critical scale ($X_0 \approx 10^4\text{–}10^5$) therefore appears not as an arbitrary parameter, but as the point at which the asymptotic regime consolidates.

The role of scale is thus isolated: it determines whether the operator is observed over collapsing terrain or over stabilised ground.

In the next chapter, we move from geometric diagnosis to operational analysis. We will investigate which perturbations preserve the observed regime and which destroy it, explicitly delineating the minimal conditions required for the persistence of universality.


---

[$\gets$ Previous Chapter](./08_the_discovery_lens.md) | [Contents](../../index.md) | [Next Chapter $\to$](./10_conditions_for_chaos.md)

---
