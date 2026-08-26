# Phase assignment for the CuWO4 / CuSe hydrothermal series

Working notes, 7 August 2026. Analysis migrated to the revised figure
(3099 x 2484 px, 2theta axis 10 to 80 degrees, sample labels at the right).

> **Superseded in part.** Raw XY data were supplied later and refined directly.
> For phase quantification, refined lattice parameters and structural model
> parameters, use `Rietveld_analysis_CuWO4_CuSe.docx`, which is based on the
> raw patterns rather than on the digitised figure. This file remains the
> record of the peak indexing, the phase identification logic and the phases
> that were excluded.

Source figure: `CuWO4-CuSe xrd.png`.
Indexed figure: `CuWO4-CuSe_xrd_indexed.png`.
Peak lists: `xrd_peaks_digitized.csv`, `CuWO4_indexed.csv`.
Reference structures: `cif/`.

## Method and its limits

No raw XY data were available, so peak positions and full profiles were
digitised from the plotted image. The 2theta scale was fixed on the axis tick
marks: frame from x = 511 to x = 2789 px spanning 10 to 80 degrees, giving
32.543 px per degree. Each trace was isolated as a wide connected component of
its own colour, so the black sample labels cannot contaminate the black CuWO4
curve. Column coverage is 100 percent for all five traces.

Reference patterns were computed from published crystal structures in the
Crystallography Open Database using Cromer-Mann atomic scattering factors,
isotropic displacement parameters and a Lorentz-polarisation correction, at
Cu K-alpha1 = 1.54056 A.

Calibration check: refining the triclinic CuWO4 cell against the digitised
black trace reproduces the reference cell to about 0.05 percent with an RMS
residual of 0.085 degrees in 2theta, so no significant zero offset is present
and digitised positions are reliable to roughly plus or minus 0.05 to
0.1 degrees. Intensities read off a plotted figure are far less reliable than
positions.

## Summary of phases

| Trace | Label | Phases identified |
|---|---|---|
| black | CuWO4 | CuWO4, triclinic P-1, single phase |
| red | 4:1 | CuO tenorite (major) + cubic Cu2-xSe + Cu3Se2 umangite |
| blue | 1:1 | Cu3Se2 umangite (major) + cubic Cu2-xSe + minor CuSe and CuO |
| teal | 1:4 | CuSe klockmannite (major) + cubic Cu2-xSe + minor CuO |
| magenta | CuSe | CuSe klockmannite, essentially single phase |

No CuWO4 reflection survives in any of the three intermediate samples. The
strongest CuWO4 lines at 19.03, 25.98, 30.13, 31.63 and 32.16 degrees are all
absent, consistent with the reported absence of tungsten in XPS and EDX for the
4:1 sample.

## Refined cell parameters

| Phase | Space group | Refined cell (A) | Reference |
|---|---|---|---|
| CuWO4 | P-1 | a 4.7006, b 5.8422, c 4.8787, alpha 91.616, beta 92.434, gamma 82.673 | COD 4000809 |
| CuO tenorite | C2/c | a 4.689, b 3.429, c 5.113, beta 99.43 | COD 9014580 (298 K) |
| Cu3Se2 umangite | P-42(1)m | a 6.404, c 4.275 (1:1 sample) | COD 9009856 |
| CuSe klockmannite | P6_3/mmc | a 3.939, c 17.222 (CuSe reference) | COD 9000063 |
| Cu2-xSe berzelianite | Fm-3m | a 5.703 to 5.705 | COD 9009855 |

Note on the CuO reference: COD 9016057 is a 196 K determination in Cc, and
COD 4000806 is a high-pressure CuWO4 phase. Neither is appropriate for ambient
data. The ambient C2/c tenorite (COD 9014580) and the ambient triclinic CuWO4
(COD 4000809) were used instead. Substituting the 196 K CuO structure changes
no assignment.

## Semi-quantitative phase fractions

Weight fractions were obtained by fitting the digitised profile of each trace
with a sum of calculated phase profiles. The scale factor of phase alpha is
proportional to W_alpha divided by the product of unit-cell mass and unit-cell
volume, the standard Rietveld relation, so fitted scale factors convert to
weight fractions without an external standard. Pseudo-Voigt profiles with a
refined width per phase were used, together with a March-Dollase texture
parameter for the plate-like klockmannite.

| Sample | CuO | Cu3Se2 | CuSe | Cu2-xSe | fit Rwp |
|---|---|---|---|---|---|
| 4:1 | 55 | 6 | 0 | 38 | 16 % |
| 1:1 | 6 | 79 | 6 | 9 | 26 % |
| 1:4 | 5 | 1 | 65 | 29 | 28 % |
| CuSe reference | 0 | 0 | 90 | 10 | 32 % |

**These are estimates, not Rietveld results.** They come from a figure, not
from counts, so they carry no counting statistics and the Rwp values are not
comparable with those from a real refinement. Independent fitting schemes
(single shared width; per-phase widths with texture) and the two renders of the
figure agree to within about 5 weight percent for the major phases and about 8
for the minor ones. Treat the values as plus or minus 10 weight percent
absolute, and treat any phase below about 10 percent as "present, amount not
determined". Microabsorption is not corrected, which biases the strongly
absorbing selenides relative to CuO.

### Internal consistency check

Converting the fitted phase fractions to an overall selenium to copper atomic
ratio, taking the cubic phase as Cu1.7Se:

| Sample | nominal CuWO4:CuSe | Se:Cu from phase fractions |
|---|---|---|
| 4:1 | 4:1 | 0.22 |
| 1:1 | 1:1 | 0.61 |
| 1:4 | 1:4 | 0.78 |
| CuSe reference | selenide only | 0.95 |

The ratio rises monotonically with the selenium loading and the CuSe reference
lands near unity, as it should. This is an independent check that the phase set
and fractions are self-consistent. It is not proof of accuracy; an EDX or ICP
bulk Cu:Se ratio would test it directly.

## CuWO4 indexing

Indexed against COD 4000809, triclinic P-1. 52 of 53 observed reflections
index, 87 calculated lines matched, RMS residual 0.085 degrees. Refined cell
a = 4.7006, b = 5.8422, c = 4.8787 A, alpha = 91.616, beta = 92.434,
gamma = 82.673 degrees, against 4.7080, 5.8400, 4.8840 A and 91.77, 92.47,
82.81 degrees for the reference. Full table in `CuWO4_indexed.csv`.

| 2theta obs | d obs (A) | I obs | h k l | 2theta calc | I calc |
|---|---|---|---|---|---|
| 15.29 | 5.7918 | 29 | 0 1 0 | 15.28 | 21 |
| 19.03 | 4.6587 | 82 | 1 0 0 | 19.03 | 66 |
| 22.94 | 3.8741 | 42 | 1 1 0 | 22.91 | 37 |
| 23.58 | 3.7695 | 43 | 0 1 -1 | 23.57 | 33 |
| 24.14 | 3.6844 | 42 | 0 1 1 | 24.11 | 34 |
| 25.98 | 3.4269 | 58 | 1 -1 0 | 25.99 | 51 |
| 28.71 | 3.1065 | 100 | 1 1 -1 | 28.70 | 100 |
| 30.13 | 2.9638 | 86 | 1 1 1 | 30.11 | 83 |
| 30.83 | 2.8975 | 28 | 0 2 0 | 30.85 | 26 |
| 31.63 | 2.8261 | 68 | 1 -1 -1 | 31.68 | 60 |
| 32.16 | 2.7814 | 57 | 1 -1 1 | 32.15 | 55 |
| 35.66 | 2.5158 | 38 | 0 2 -1 | 35.66 | 40 |
| 36.43 | 2.4645 | 28 | 0 2 1 | 36.42 | 29 |
| 36.83 | 2.4386 | 46 | 0 0 2 | 36.86 | 43 |
| 38.55 | 2.3336 | 27 | 1 -2 0 | 38.59 | 30 |
| 41.04 | 2.1977 | 19 | 1 0 -2 | 41.09 | 18 |

Calculated and observed intensities track closely, including the 100 percent
(1 1 -1) line at 28.71 degrees and the 86 percent (1 1 1) at 30.13, supporting
the assignment as untextured single-phase CuWO4. The only unindexed feature is
a 2.4 percent line at 20.54 degrees (d = 4.32 A), at the noise level of a
digitised trace.

## Notes on individual assignments

**Cu3Se2, umangite.** Dominant phase of the 1:1 sample, accounting for
essentially every line including the weak 20.79 degree (001).

**Cu2-xSe, berzelianite.** A face-centred cubic phase present in all three
intermediate samples and the origin of the strong line near 44.9 degrees, which
belongs to no other phase here. In the 1:4 sample four reflections resolve and
give a consistent cell: (111) 27.02 gives a = 5.712, (220) 44.97 gives 5.697,
(311) 53.2 and (400) 65.4 agree. Mean a = 5.703 A. This sits below the range
usually quoted for berzelianite, about 5.74 A for Cu1.8Se up to 5.86 A for
Cu2Se, implying pronounced copper deficiency. Confirm before claiming a
stoichiometry.

**CuSe, klockmannite.** Lines at 26.13, 41.04 and 47.33 degrees index as (100),
(106) and (112) to better than 0.03 degrees, but the idealised hexagonal
P6_3/mmc average structure predicts them below 1 percent relative intensity
whereas 26.13 is observed near 22 percent. The d value of 3.41 A for (100) is a
listed klockmannite spacing, and the three lines track the CuSe phase across
both the magenta and teal traces, so they belong to it. The likely explanation
is the orthorhombic Cmcm distortion of room-temperature klockmannite, which
lifts the near-extinction, possibly with some preferred orientation of the
plates.

**Weak unassigned features.** Five weak lines remain: 21.34 degrees in the 4:1
sample (4 percent), 29.70 and 29.76 degrees in the 1:1 and CuSe traces (4 and
7 percent), and 63.38 and 66.91 degrees in the CuSe trace (3 percent each). The
29.7 degree position coincides with the (101) of trigonal selenium, the
strongest line of that phase, which would be a plausible unreacted reagent.
This was tested and **not** confirmed: the companion lines Se (100) at 23.50
and Se (102) at 43.62 degrees, which should carry 44 and 32 percent of the
(101) intensity, are absent above the noise floor. The features are recorded as
unassigned rather than forced onto a phase.

**Phases excluded.** CuSe2 krutaite (no strong (200) at 29.2), Cu2O cuprite
(no (111) at 36.4 or (200) at 42.3), Cu(OH)2 spertiniite (no (020) at 16.7 or
(021) at 23.8), metallic Cu (no (111) at 43.3), CuSeO3.2H2O chalcomenite (none
of its four strongest lines below 30 degrees), trigonal Se (see above).

## On the tungsten loss, and what can actually be cited

A literature search did not find a study of CuWO4 dissolution or tungsten
leaching in NaOH, hydrothermal or otherwise. **The alkaline-leaching
explanation should therefore be presented as an inference, not as a cited
fact.** Two points matter:

1. The photoelectrochemical literature generally describes CuWO4 as reasonably
   stable at neutral to moderately basic pH. Yourey and co-workers examined
   CuWO4 stability in phosphate and borate buffers but only over pH 3 to 7, so
   that work neither supports nor refutes behaviour in concentrated NaOH at
   hydrothermal temperature. It should not be cited as evidence for leaching.
2. What is well established is that wolframite-type tungstates are decomposed
   by caustic alkali to soluble sodium tungstate, the basis of industrial
   tungsten extraction. CuWO4 is a wolframite-type (triclinically distorted)
   tungstate, so the analogous reaction is chemically reasonable. The analogy
   is ours; the cited work does not state it about CuWO4.

A second driving force does not require CuWO4 to be intrinsically
alkali-soluble. Selenide generated in situ from selenium, hydrazine and
hydroxide forms copper selenides of very low solubility. Sequestering copper
into those phases releases tungstate into a solution in which it is already the
stable and highly soluble species, so decomposition is pulled forward by the
selenide sink. Both routes act in the same direction and cannot be separated by
XRD alone.

**The decisive experiment is to analyse the filtrate for tungsten by ICP-OES.**
A mass balance closing on dissolved W turns the inference into a measurement,
and it is a single analysis.

### Verified references

All checked against Crossref on 7 August 2026.

- Martins, J. I. Leaching Systems of Wolframite and Scheelite: A Thermodynamic
  Approach. *Mineral Processing and Extractive Metallurgy Review* **2013**,
  *35* (1), 23-43. DOI: 10.1080/08827508.2012.757095
- Li, X.; Xu, X.; Liu, Y.; Zhou, Q.; Shen, L. Thermodynamic Modeling of
  Scheelite and Wolframite Leaching in Caustic Soda and Soda Solutions by
  Pitzer Equation for Near-Equilibrium Tungsten Extractive Metallurgy.
  *Mineral Processing and Extractive Metallurgy Review* **2025**, 1-12.
  DOI: 10.1080/08827508.2025.2587044
- Zheng, Y.; Zhang, L.; Bai, H.; Xi, X. Optimization of Efficient Tungsten
  Extraction Process from Wolframite by Na2CO3 Alkaline Melting. *Minerals*
  **2026**, *16* (2), 126. DOI: 10.3390/min16020126
- Yourey, J. E.; Pyper, K. J.; Kurtz, J. B.; Bartlett, B. M. Chemical Stability
  of CuWO4 for Photoelectrochemical Water Oxidation. *The Journal of Physical
  Chemistry C* **2013**, *117* (17), 8708-8718. DOI: 10.1021/jp402048b
  (pH 3 to 7 only; cite for what it measures, not for alkaline leaching)

## Suggested confirmation

1. Rietveld refinement on raw XY data for defensible phase fractions and a
   defensible Cu2-xSe cell parameter.
2. EDX or ICP bulk Cu:Se ratio per sample, to test the Se:Cu trend above and
   the copper deficiency of the cubic phase.
3. ICP-OES of the filtrate for tungsten, to establish the leaching route.
4. Cu 2p and Se 3d XPS with Auger parameter analysis to separate Cu(I) from
   Cu(II) and confirm selenide rather than selenite.
