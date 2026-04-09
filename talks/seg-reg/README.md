# MSK MRI Segmentation & Registration Approaches

**Speaker:** Gabrielle Hoyer (UCSF) — [Gabbie.Hoyer@ucsf.edu](mailto:Gabbie.Hoyer@ucsf.edu)  
**Time:** 07:15–07:30 SAST, Monday 11 May 2026

---

## Overview

This talk covers segmentation and registration methods for quantitative musculoskeletal MRI — from classical atlas-based and shape-model approaches through modern deep learning, foundation models (SAM family), and self-supervised / weak-label strategies. Emphasis is on what breaks in MSK anatomy (articulated joints, thin cartilage, pathology-driven appearance shifts) and how to validate methods for downstream biomarkers rather than overlap alone.

## Slides

| Version | Link |
|---------|------|
| Preliminary | [slides.com/gabbiehoyer/ismrm2026-seg-reg](https://slides.com/gabbiehoyer/ismrm2026-seg-reg) |
| Final | *Available after the conference* |

> Slides are provided for educational use. Please cite the session if reusing figures.

## Interactive notebooks

Jupyter notebooks demonstrating key concepts from the talk using open-source data and tools. These are meant as hands-on companions — run them locally or in Google Colab.

| Notebook | Topic | Data | Colab |
|----------|-------|------|-------|
| [01_knee_seg_nnunet.ipynb](notebooks/01_knee_seg_nnunet.ipynb) | Knee cartilage segmentation with nnU-Net | OAI / IWOAI | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gabbieHoyer/ismrm2026-qmsk-mri/blob/main/talks/seg-reg/notebooks/01_knee_seg_nnunet.ipynb) |
| [02_registration_basics.ipynb](notebooks/02_registration_basics.ipynb) | Rigid + deformable registration with SimpleITK | Synthetic / OAI | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gabbieHoyer/ismrm2026-qmsk-mri/blob/main/talks/seg-reg/notebooks/02_registration_basics.ipynb) |
| [03_sam_knee_mri.ipynb](notebooks/03_sam_knee_mri.ipynb) | Promptable segmentation with SAM/MedSAM on knee MRI | OAI | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gabbieHoyer/ismrm2026-qmsk-mri/blob/main/talks/seg-reg/notebooks/03_sam_knee_mri.ipynb) |
| [04_thickness_morphometry.ipynb](notebooks/04_thickness_morphometry.ipynb) | Cartilage thickness mapping from segmentation masks | OAI-derived | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gabbieHoyer/ismrm2026-qmsk-mri/blob/main/talks/seg-reg/notebooks/04_thickness_morphometry.ipynb) |

> **Status:** *Notebooks are in development. Check back closer to the conference.*

### Running locally

```bash
git clone https://github.com/gabbieHoyer/ismrm2026-qmsk-mri.git
cd ismrm2026-qmsk-mri/talks/seg-reg/notebooks
pip install -r requirements.txt
jupyter lab
```

## Learning objectives

1. Explain where segmentation and registration sit in quantitative MSK MRI pipelines
2. Compare classical pipelines (manual, atlas, shape priors) with deep learning and promptable foundation models
3. Choose registration models (rigid/affine vs deformable) that match the anatomy and study question
4. Apply practical quality checks that protect downstream biomarkers (thickness, volume, fat fraction)
5. Point to datasets, benchmarks, and open software that support reproducible research

---

## Key references

### Classical & atlas-based segmentation
- Ambellan et al. (2019) — CNN + statistical shape models for knee bone/cartilage. [MedIA](https://doi.org/10.1016/j.media.2018.11.009)
- Henson et al. (2023) — Multi-atlas muscle segmentation via deformable registration. [PLOS ONE](https://doi.org/10.1371/journal.pone.0273446) *(open access)*

### Deep learning segmentation & benchmarks
- Isensee et al. (2021) — nnU-Net: self-configuring baseline. [Nat Methods](https://doi.org/10.1038/s41592-020-01008-z)
- Desai et al. (2021) — IWOAI knee MRI segmentation challenge. [Rad:AI](https://doi.org/10.1148/ryai.2021200078) *(open access via PMC)*
- Schmidt et al. (2023) — Cross-dataset generalizability (morphology + relaxometry). [JMRI](https://doi.org/10.1002/jmri.28365)
- Eckstein et al. (2022) — Longitudinal cartilage thickness loss detection. [Arthritis Care Res](https://doi.org/10.1002/acr.24539)

### Muscle segmentation & pathology
- Hostin et al. (2023) — Fatty infiltration impact on muscle seg accuracy. [JMRI](https://doi.org/10.1002/jmri.28708)
- Riem et al. (2025) — Hamstring musculotendon injury segmentation. [Sci Rep](https://doi.org/10.1038/s41598-025-16926-1) *(open access)*

### Foundation models & promptable segmentation
- Kirillov et al. (2023) — Segment Anything Model (SAM). [ICCV](https://arxiv.org/abs/2304.02643)
- Ma et al. (2024) — MedSAM: Segment Anything in medical images. [Nat Commun](https://doi.org/10.1038/s41467-024-44824-z) *(open access)*
- Hoyer et al. (2025) — SAM-family evaluation on knee MRI. [arXiv](https://arxiv.org/abs/2501.13376) *(open access)*
- Ferreira et al. (2026) — Memory-based promptable model for 3D knee cartilage/meniscus. [Sci Rep](https://doi.org/10.1038/s41598-025-31503-2) *(open access)*
- Wahd et al. (2025) — Sam2Rad: learnable prompts for medical images. [Comput Biol Med](https://doi.org/10.1016/j.compbiomed.2025.109725)
- Chukwujindu et al. (2025) — SAM2 impact analysis on multi-planar datasets. [EJRAI](https://doi.org/10.1016/j.ejrai.2025.100034)

### Multi-structure & generalist segmentation
- D'Antonoli et al. (2025) — TotalSegmentator MRI. [Radiology](https://doi.org/10.1148/radiol.241613)
- Gu et al. (2025) — SegmentAnyBone: universal bone seg on MRI. [MedIA](https://doi.org/10.1016/j.media.2025.103469)

### Geometry-aware morphometrics
- Yao et al. (2024) — CartiMorph: cartilage morphometrics framework. [MedIA](https://doi.org/10.1016/j.media.2023.103035)
- Wang et al. (2025) — CartiSurface: implicit surface thickness mapping. [npj Digit Med](https://doi.org/10.1038/s41746-025-02040-z) *(open access)*

### Registration
- Balakrishnan et al. (2019) — VoxelMorph: learning-based deformable registration. [IEEE TMI](https://doi.org/10.1109/TMI.2019.2897538)
- Smolders et al. (2025) — Bone Rigidity Error metric. [PHIRO](https://doi.org/10.1016/j.phro.2025.100767) *(open access)*
- Draper et al. (2025) — Local rigidity constraints for deformable registration. [Med Phys](https://doi.org/10.1002/mp.70109)

### Longitudinal & cohort-scale analysis
- Iriondo et al. (2021) — 8-year cartilage thickness trajectories. [J Orthop Res](https://doi.org/10.1002/jor.24849)
- Esrafilian et al. (2025) — Automated knee FE modeling from MRI. [IEEE TBME](https://doi.org/10.1109/TBME.2024.3438272)

### Additional
- Chaudhari et al. (2020) — Super-resolution and OA biomarker stability. [JMRI](https://doi.org/10.1002/jmri.26872)
- Panfilov et al. (2022) — Subregional cartilage morphology from DL. [J Orthop Res](https://doi.org/10.1002/jor.25150)
- Hu et al. (2025) — Vision foundation model for MRI seg (ISMRM 2025 #0012). [Abstract](https://archive.ismrm.org/2025/0012_MtiJEjRKZ.html)
- Dam et al. (2015) — High/low-field knee seg. [JMI](https://doi.org/10.1117/1.JMI.2.2.024001) *(open access via PMC)*
- Listone et al. (2025) — Bone seg in low-field knee MRI. [BDCC](https://doi.org/10.3390/bdcc9060146) *(open access)*
- Yao et al. (2026) — DL knee cartilage seg: multi-model validation. [The Knee](https://doi.org/10.1016/j.knee.2025.10.024)
- Yoo (2025) — DL-based image reconstruction in MSK MRI (review). [JKSR](https://doi.org/10.3348/jksr.2025.0015)
- Nikolova et al. (2025) — DL-reconstructed 3D MRI for knee assessment. [Eur J Radiol](https://doi.org/10.1016/j.ejrad.2025.112458)

---

*See also: [Open syllabus](syllabus-open.md) · [Datasets](../../datasets/) · [Tools](../../tools/) · [Session overview](../../)*
