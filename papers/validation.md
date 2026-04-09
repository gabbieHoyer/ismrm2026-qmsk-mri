# Validation & Evaluation

## Biomarker-oriented evaluation
- Schmidt et al. (2023) — Generalizability assessed via morphology AND relaxometry agreement. [JMRI](https://doi.org/10.1002/jmri.28365)
- Eckstein et al. (2022) — Longitudinal sensitivity: automated seg detects cartilage thickness loss. [Arthritis Care Res](https://doi.org/10.1002/acr.24539)
- Desai et al. (2021) — IWOAI challenge: Dice, surface distance, AND thickness error. [Rad:AI](https://doi.org/10.1148/ryai.2021200078) *(open access via PMC)*

## Registration validation
- Smolders et al. (2025) — Bone Rigidity Error for deformable registration QC. [PHIRO](https://doi.org/10.1016/j.phro.2025.100767) *(open access)*

## Domain shift & generalization
- Hostin et al. (2023) — Pathology (fatty infiltration) degrades seg → downstream measurement unreliable. [JMRI](https://doi.org/10.1002/jmri.28708)

## Recommended QC checklist
1. Visual overlay in multiple planes (include severe disease + artifact cases)
2. Boundary-sensitive metrics: mean surface distance, 95th-percentile Hausdorff (not just Dice)
3. Biomarker agreement in physical units (mm for thickness, ms for relaxometry)
4. Registration plausibility: Jacobian stats + BRE where applicable
5. Longitudinal endpoint: test-retest precision and sensitivity to known change
6. Outlier screening: flag out-of-range volumes/thicknesses → route to manual review
