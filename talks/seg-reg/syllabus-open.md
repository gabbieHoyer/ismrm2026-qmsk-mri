# MSK MRI Segmentation & Registration Approaches — Open Syllabus

**Speaker:** Gabrielle Hoyer (UCSF)  
**Contact:** Gabbie.Hoyer@ucsf.edu  
**Course:** Fundamentals of MSK MRI — Quantitative MSK MRI: From Acquisition to Analysis  
**Session:** Sunrise Course | 11 May 2026, 07:00–08:00 SAST

*This is an open-access companion to the official ISMRM syllabus. The official version is available to registered conference attendees.*

---

## Take-home messages

1. **Segmentation** defines anatomy-specific regions of interest for quantitative MSK MRI endpoints (morphometry, composition, relaxometry, and shape).
2. **Registration** supports comparable measurements across sequences, time points, and subjects, but requires care in articulated anatomy where rigid bones and deformable soft tissues coexist.
3. **Report performance in units that match the scientific question** (e.g., thickness error and longitudinal sensitivity), not only overlap scores.
4. **Recent work** has expanded beyond single-task models toward multi-structure, sequence-tolerant segmentation and promptable workflows; these approaches still require domain adaptation and explicit quality assurance.

## Scope and motivation

This syllabus accompanies an invited educational lecture on segmentation and registration approaches for musculoskeletal MRI. The focus is methodological: practical families of algorithms, common failure modes in MSK anatomy, and evaluation strategies that preserve quantitative endpoints. While segmentation and registration are analysis steps, their reliability depends on acquisition choices (contrast, resolution, artifact profile, and acceleration), so validation should be repeated when protocols, scanners, reconstruction methods, or field strength change.

Quantitative MSK MRI commonly aims to measure cartilage thickness and volume, meniscus morphology, muscle volume and composition, or spatially localized relaxometry (e.g., T2, T1ρ). Segmentation defines the anatomical support over which measurements are computed, and registration defines how those measurements are compared across time, contrasts, or subjects.

## I. Segmentation approaches

### I.A Classical baselines and anatomical priors
Manual contouring remains a reference standard, but it is time intensive and variable across readers. Atlas-based segmentation propagates labels by deformably registering labeled examples to the target scan and has been used for muscle labeling and label propagation for augmentation. Shape priors address anatomically implausible predictions by combining statistical shape knowledge with CNN inference.

### I.B Deep learning baselines and benchmarking
Modern MSK segmentation is dominated by encoder-decoder CNNs (U-Net family) and their 3D variants. The IWOAI knee MRI segmentation challenge is a commonly cited benchmark, and nnU-Net remains a strong baseline due to its self-configuring strategy. For quantitative imaging, overlap metrics alone are insufficient — generalization should be assessed using both morphology and relaxometry agreement, and longitudinal sensitivity should be reported.

### I.C Recent directions (2024–2026)
- **Sequence-tolerant multi-structure segmentation:** TotalSegmentator MRI illustrates a direction toward fewer task-specific models.
- **General bone segmentation:** SegmentAnyBone targets bone seg across multiple anatomic locations.
- **Promptable segmentation:** Memory-based promptable models for 3D knee MRI offer interactivity as a structured correction mechanism.
- **Geometry-aware morphometrics:** CartiMorph and CartiSurface combine segmentation with mapping for standardized thickness fields.

## II. Registration approaches

### II.A MSK-specific issues
Articulated anatomy and mixed rigidity make alignment nontrivial. Staged workflows are common: rigid or affine alignment (bone-focused) followed by deformable refinement in soft tissue regions.

### II.B Learning-based registration and plausibility
VoxelMorph and similar frameworks predict deformation fields from image pairs. MSK-specific safeguards include Bone Rigidity Error (BRE) for quantifying non-rigid deformation inside bones, and local rigidity constraints to reduce implausible bone warping.

## III. Validation and reporting

A minimal quality assurance set:
- Visual overlay review in multiple planes
- Boundary-sensitive metrics (surface distance, Hausdorff percentile) alongside Dice
- Biomarker agreement in physical units (mm, ms)
- Deformation plausibility checks (Jacobian, BRE)

## Key references

See the [full annotated reference list](../talks/seg-reg/) for complete citations with links.

---

*Licensed under [CC BY 4.0](../LICENSE). Please cite the session if you use these materials.*
