# 14. Where Does Chaos Reside? — Testing Alternative Operators

> *If you drag a net with a five-centimetre mesh through the sea,*  
> *your conclusion will be that no fish smaller than five centimetres exist.*  
> *But is that a fact about the fish in the sea, or about your net?*  
> — Arthur Eddington

## The final doubt

The preceding chapters established a strong result: when the arithmetical signal of the primes is observed on the logarithmic scale, the spectrum of the constructed operator robustly exhibits statistics compatible with the universal GOE class, whereas linear observation systematically leads to the Poisson regime.

Nevertheless, a legitimate doubt remains.

Up to this point, the central operator of this work has been defined through a *cosine kernel*, of the form

$$
M_{ij} \propto \cos(f_i \cdot \log x_j) + \cos(f_j \cdot \log x_i),
$$

where $f_i = \Delta_\pi(x_i)$.

It is natural to ask whether the observed duality — Poisson on the linear scale and GOE on the logarithmic scale — is an intrinsic property of the arithmetical system, or whether it could be an artefact of the specific functional choice of the kernel.

In other words:

*does chaos reside in the primes, or in the operator we chose to observe them?*

This chapter is devoted to confronting this question directly.

## Changing the instrument

The cosine is not an arbitrary function. It arises naturally as the real part of a complex phase:

$$
\cos(\theta) = \mathrm{Re}(e^{i\theta}).
$$

An immediate generalisation therefore consists in abandoning the real projection and working directly with the full complex phase.

We thus introduce an alternative operator, defined through a *phase kernel*:

$$
M'_{ij} = e^{i \cdot f_i \cdot \log x_j}.
$$

This operator is not real-symmetric, but it carries the same fundamental structural information: the interaction between the arithmetical signal $f_i$ and the logarithmic scale of $x_j$.

The motivation for this test is simple and rigorous: if the GOE statistics observed previously arise from the deep interaction between the prime signal and the scale of observation — and not from the particular form of the cosine — then replacing the kernel should not destroy the phenomenon.

## Operational hypothesis

The hypothesis tested in this chapter can be stated objectively:

> If the Poisson/GOE duality is structural, then alternative operators, constructed from the same arithmetical information and observed at the same scales, should exhibit the same statistical behaviour.

In particular, we expect to observe:

* Poisson statistics on the linear scale;
* statistics compatible with GOE on the logarithmic scale;
* stability of these results under changes of kernel.

## The operator laboratory

**Notebook 14** (`14_alternative_operators.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/14_alternative_operators.ipynb) implements this test in a controlled manner.

A selector was introduced allowing one to switch between the *cosine kernel* and the *phase kernel*, while keeping unchanged:

* the arithmetical signal $\Delta_\pi(x)$;
* the observation regimes (linear and logarithmic);
* the statistical protocol applied to the spectrum.

This approach guarantees that any observed difference can be attributed exclusively to the form of the operator — and not to collateral changes in the method.

## Result: statistical invariance

The outcome of the experiment is unambiguous.

Replacing the cosine kernel with the phase kernel **does not alter** the statistical diagnosis:

* on the linear scale, the spectrum remains compatible with Poisson;
* on the logarithmic scale, the spectrum continues to exhibit level repulsion, global rigidity, and reference values compatible with GOE.

This invariance is non-trivial. It demonstrates that the observed statistical duality is not a functional artefact, but a robust property of the underlying system.

## Where chaos truly resides

The test with alternative operators now allows us to locate precisely the origin of the phenomenon.

The observed chaos:

* does not reside in the specific form of the kernel;
* is not created by the operator;
* does not depend on a delicate functional choice.

It emerges from the combination of two fundamental elements:

1. the intrinsic arithmetical structure of the signal $\Delta_\pi(x)$;
2. the observation of this signal on the logarithmic scale natural to the primes.

The operator acts merely as a reading instrument. Changing the instrument does not change the music.

---

## Point of rest

Up to this point, the dependence of the phenomenon on the specific form of the operator has been examined systematically. It has been verified that functionally distinct kernels lead to the same statistical diagnosis, and that the duality between Poisson-type and GOE-type regimes remains invariant under this substitution.

As a result, the origin of the observed behaviour can be isolated with clarity: it does not reside in formal details of the construction, but in the interaction between the arithmetical signal of the primes and the adopted scale of observation.

This chapter therefore closes the investigation into possible operational artefacts.

In the chapters that follow, the focus shifts from causes to consequences. We shall investigate what is genuinely universal, which perturbations can be introduced without destroying the observed regime, and which natural limits emerge from the very structure that has been identified.

---

[$\gets$ Previous Chapter](./13_varreduras_escala.md) | [Contents](../../index.md) | [Next Chapter $\to$](./15_stratospheric_heights.md)
