# 15. Confirmation at Stratospheric Heights

> *Wir müssen wissen. Wir werden wissen.*  
> *(We must know. We shall know.)*  
> — David Hilbert

## Historical context: Montgomery, Berry and Odlyzko

To appreciate the significance of what is examined in this final chapter, it is essential to situate it within the historical connection between prime numbers, the zeros of the zeta function, and quantum chaos.

The path followed throughout this work echoes one of the most remarkable convergences between mathematics and physics of the twentieth century.

### The initial spark: Montgomery and Dyson

In the 1970s, Hugh Montgomery investigated the correlation between the non-trivial zeros of the Riemann zeta function. In an informal conversation with Freeman Dyson, Montgomery presented the formula he had obtained for the pair correlation function of those zeros.

Dyson immediately recognised the underlying statistical structure: it was the same statistics that describes level repulsion in the energy spectra of heavy atomic nuclei, a domain modelled by Random Matrix Theory.

This observation inaugurated an unexpected bridge between analytic number theory and quantum physics.

### The physical framework: Berry and quantum chaos

The connection required an explanatory principle. Michael Berry, together with other physicists, provided this framework by establishing Random Matrix Theory as the appropriate language of quantum chaos.

The Bohigas–Giannoni–Schmit (BGS) conjecture asserts that quantum systems whose classical analogue is chaotic exhibit universal spectral statistics described by Random Matrix Theory (RMT). The specific ensemble (GOE or GUE) is determined by the symmetries of the system; **within the real and mirrored arithmetic domain explored here, the emergent class is the GOE**.

In this context, the zeros of the zeta function, and by extension the arithmetic of the primes, came to be interpreted as an abstract quantum chaotic system.

### Computational confirmation: Odlyzko

The conjecture received decisive empirical support through the work of Andrew Odlyzko. Using supercomputers and highly optimised algorithms, Odlyzko computed the locations of billions of zeros of the zeta function at extreme heights on the critical line, reaching orders such as $10^{22}$ and beyond.

The results were unequivocal: the observed statistics matched, with extraordinary precision, the predictions of the GUE (Gaussian Unitary Ensemble), the class expected for systems without time-reversal symmetry.

The laboratory presented in this chapter is a direct homage to this intellectual trajectory, but with a fundamental distinction: while the zeros in the complex plane reveal GUE rigidity, our analysis of the real arithmetic line, anchored in unity, reveals the emergence of the GOE — the signature of systems that preserve mirror symmetry.

These two regimes are neither in competition nor in contradiction, but belong to distinct observational domains: one associated with complex spectral flow and broken reversibility, the other with a real, symmetric and reflective arithmetic structure.

## The challenge of stratospheric heights

In previous chapters, we established that GOE-type statistics emerge stably from initial scales of order $10^5$.

The natural question that arises is whether this behaviour persists at genuinely extreme scales — those explored by Odlyzko in his analysis of the zeros of the zeta function.

A direct approach is impractical. Explicit prime counting rapidly becomes infeasible at stratospheric heights.

To circumvent this limitation, we resort to a theoretical bridge: Riemann’s $\mathrm{R}(x)$ function (also known as the smoothed prime-counting function), which provides an extremely accurate asymptotic approximation to $\pi(x)$, even in astronomical domains.

The substitution of $\pi(x)$ by $\mathrm{R}(x)$ is not intended to introduce new structure, but to preserve the asymptotic geometry of the arithmetic signal in regimes where direct enumeration of primes is no longer practical.

This substitution allows us to probe regions of the number line far beyond the reach of elementary algorithms, while preserving the relevant statistical structure.

## Analysis of stratospheric data

In this final experiment, no new raw data are generated. Instead, we analyse a set of results computed in real time, organised in a dataframe (a tabular numerical data structure) covering a sweep of $X_0$ from $10^8$ up to approximately $10^{28}$.

No external data or precomputed tables are used. All values analysed in this chapter are generated directly within **Notebook 15**, which implements the complete experiment at high precision, using Riemann’s $\mathrm{R}(x)$ function as an asymptotic approximation to $\pi(x)$ in order to enable probing at stratospheric heights.

Two central statistics are monitored throughout this sweep:

- the mean ratio of adjacent level spacings, $\langle r \rangle$;
- the normalised participation ratio, $\mathrm{PR}/N$.

Both serve as independent fingerprints of the GOE class.

## Final hypothesis

If the connection between the arithmetic of the primes and GOE statistics is structural **within the observational regime considered**, sustained by the mirror symmetry inherent to the real line, then these two quantities should remain stable, closely adhering to the theoretical GOE values,

> $\langle r \rangle_{\text{GOE}} \approx 0.536$  
> $\mathrm{PR}/N \approx 1/3$

even when the analysis is pushed to the most distant frontiers of the number line.

What this chapter therefore examines is no longer the emergence of chaos, but the **statistical persistence of this regime** under extreme shifts of scale.

## Computational reproducibility and the role of Notebook 15

It is important to emphasise that the results presented in this chapter are not merely expository or interpretative.

**Notebook 15** (`15_alturas_estratosfericas.ipynb`)  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/descobrindo_caos/blob/main/notebooks/15_alturas_estratosfericas.ipynb)  
explicitly implements the experiment described throughout this chapter and constitutes the complete computational laboratory for this final stage of the investigation.

In this notebook:

- stratospheric data are **generated in real time**, directly within the notebook, by numerical evaluation of the $\mathrm{R}(x)$ function, without recourse to precomputed tables, external databases or previously stored data;
- Riemann’s $\mathrm{R}(x)$ function is used as an asymptotic approximation to $\pi(x)$;
- the statistics $\langle r \rangle$ and $\mathrm{PR}/N$ are computed directly from the operator’s spectrum;
- the results are visualised and compared with the theoretical GOE values;
- the entire process can be **fully replicated** by the reader.

The notebook not only confirms numerically the persistence of GOE statistics at extreme heights, but also provides a transparent, auditable and re-executable protocol for independent verification of the results.

Accordingly, this chapter does not rest on historical authority or isolated theoretical extrapolation, but on an explicit computational experiment, aligned with contemporary standards of scientific reproducibility.

As emphasised by Berry, these statistics describe local properties of the spectrum and are not intended to capture the complete global behaviour across all scales.

---

## Point of rest

In this chapter, the historical connection between prime numbers, the zeros of the zeta function and quantum chaos has been contextualised, while the computational limitations inherent to direct exploration of extreme scales have been made explicit. To overcome this boundary, Riemann’s $\mathrm{R}(x)$ function was introduced as an asymptotic bridge, enabling the probing of stratospheric heights without direct enumeration of primes.

With this instrument, spectral statistics were analysed in domains extending up to $10^{28}$, and the final stability of the signatures associated with the GOE class was tested systematically.

The observed outcome is systematically consistent. The music of quantum chaos does not fade with height. It persists, intact, as a **robust and recurrent structural regularity** within the aligned arithmetic regime identified in this work.

Here, the journey does not end through computational exhaustion, but through conceptual saturation.  
Nothing higher needs to be climbed within the regime considered: the relevant structure has already revealed itself in full.

---

[$\gets$ Previous Chapter](./14_operadores_alternativos.md) | [Contents](../../index.md) | [Next Chapter $\to$](./16_visao_berry.md)
