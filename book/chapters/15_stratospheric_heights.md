# 15. Confirmation at Stratospheric Heights

> *Wir müssen wissen. Wir werden wissen.*  
> *(We must know. We shall know.)*  
> — David Hilbert

## Historical context: Montgomery, Berry, and Odlyzko

To appreciate the significance of what is observed in this final chapter, it is essential to place historically the connection between prime numbers, the zeros of the zeta function, and quantum chaos.

The path followed throughout this work echoes one of the most remarkable convergences between mathematics and physics in the twentieth century.

### The initial spark: Montgomery and Dyson

In the 1970s, Hugh Montgomery was investigating correlations between the non-trivial zeros of the Riemann zeta function. In an informal conversation with Freeman Dyson, Montgomery presented the formula he had obtained for the pair correlation function of these zeros.

Dyson immediately recognised the underlying statistical structure: it was the very same statistic that describes level repulsion in the energy spectra of heavy atomic nuclei — a domain modelled by Random Matrix Theory.

This observation opened an unexpected bridge between analytic number theory and quantum physics.

### The physical framework: Berry and quantum chaos

The connection required an explanatory principle. Michael Berry, together with other physicists, provided this framework by establishing Random Matrix Theory as the universal language of quantum chaos.

Berry’s conjecture states that quantum systems whose classical counterparts are chaotic exhibit universal spectral statistics, described by the Gaussian Orthogonal Ensemble (GOE).

Within this framework, the zeros of the zeta function — and, by extension, the arithmetic of the primes — came to be interpreted as an abstract quantum chaotic system.

### Computational confirmation: Odlyzko

The conjecture gained decisive empirical support through the work of Andrew Odlyzko. Using supercomputers and highly optimised algorithms, Odlyzko computed the positions of billions of zeta zeros at extreme heights along the critical line, reaching scales of order (10^{22}) and beyond.

The results were unequivocal: the observed statistics matched, with extraordinary precision, the predictions of the **GUE** (Gaussian Unitary Ensemble).

The laboratory presented in this chapter is a direct homage to this intellectual trajectory, but with a fundamental distinction: while the zeros in the complex plane reveal GUE rigidity, our analysis of the real arithmetic line, anchored in unity, reveals the emergence of the **GOE** class — the signature of systems that preserve mirror symmetry.

## The challenge of stratospheric heights

In the preceding chapters, we established that GOE-type statistics emerge stably from initial scales of order $10^{5}$.

The natural question that follows is whether this law persists at truly extreme scales — those explored by Odlyzko in the study of zeta zeros.

A direct approach is impractical. Explicit prime counting rapidly becomes infeasible at stratospheric heights.

To circumvent this limitation, we turn to a theoretical bridge: Riemann’s function $\mathrm{R}(x)$ (also known as the smoothed prime counting function), which provides an extremely accurate asymptotic approximation to $\pi(x)$, even in astronomical regimes.

This substitution allows us to probe regions of the number line far beyond the reach of elementary algorithms, while preserving the relevant statistical structure.

## Analysis of stratospheric data

In this final experiment, no new raw data are generated. Instead, we analyse a set of results computed in real time, organised into a \textit{dataframe} (a tabular structure of numerical data) that spans a sweep of $X_0$ from $10^8$ to approximately $10^{28}$.

No external data nor precomputed tables are used. All values analysed in this chapter are generated directly within \textbf{Notebook 15}, which implements the full experiment at high precision, resorting to Riemann’s $\mathrm{R}(x)$ function as an asymptotic approximation to $\pi(x)$ in order to enable probing at stratospheric heights.

Two central statistics are monitored throughout this sweep:

* the mean ratio of adjacent spacings, $\langle r \rangle$;
* the normalised *Participation Ratio*, $\mathrm{PR}/N$.

Both act as independent fingerprints of the GOE class.

## Final hypothesis

If the connection between prime arithmetic and GOE statistics is structural and truly universal, **supported by the mirror symmetry inherent to the real line**, then these two quantities should remain stable, tightly clustered around their theoretical GOE values,

> $\langle r \rangle_{\text{GOE}} \approx 0.536$  
> $\mathrm{PR}/N \approx 1/3$

even as the analysis is pushed to the most distant frontiers of the number line.

What this chapter examines, therefore, is no longer the emergence of chaos, but its absolute persistence.

## Computational reproducibility and the role of Notebook 15

It is important to emphasise that the results presented in this chapter are not merely expository or interpretative.

**Notebook 15** (`15_stratospheric_heights.ipynb`) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/costaalv/discovering-chaos/blob/main/notebooks/15_stratospheric_heights.ipynb) explicitly implements the experiment described throughout this chapter and constitutes the complete computational laboratory for this final stage of the investigation.

In this notebook:

* stratospheric data are **generated in real time**, directly within the notebook, via numerical evaluation of Riemann’s $\mathrm{R}(x)$ function, without recourse to pre-computed tables, external databases, or stored data;
* Riemann’s $\mathrm{R}(x)$ function is used as an asymptotic approximation to $\pi(x)$;
* the statistics $\langle r \rangle$ and $\mathrm{PR}/N$ are computed directly from the spectrum of the operator;
* results are visualised and compared with theoretical GOE values;
* the entire process can be **fully replicated** by the reader.

The notebook not only confirms numerically the persistence of GOE statistics at extreme heights, but also provides a transparent, auditable, and re-executable protocol for independent verification of the results.

Thus, this chapter rests neither on historical authority nor on isolated theoretical extrapolation, but on an explicit computational experiment, aligned with contemporary standards of scientific reproducibility.

---

## Point of rest

In this chapter, the historical connection between prime numbers, the zeros of the zeta function, and quantum chaos was placed in context, while the inherent computational limitations of direct exploration at extreme scales were made explicit. To overcome this barrier, Riemann’s function $\mathrm{R}(x)$ was introduced as an asymptotic bridge, allowing stratospheric heights to be probed without recourse to explicit prime enumeration.

With this instrument in hand, spectral statistics were analysed in domains extending up to $10^{28}$, and the ultimate stability of the signatures associated with the GOE class was tested systematically.

The observed outcome is unequivocal. The music of quantum chaos does not dissipate with height. It persists, intact, as a **universal structural regularity** of arithmetic.

Here, the journey does not end through computational exhaustion, but through conceptual saturation. Nothing higher needs to be climbed: the structure has already revealed itself in full.

---

[$\gets$ Previous Chapter](./14_alternative_operators.md) | [Contents](../../index.md) | [Next Chapter $\to$](./16_berry_view.md)
