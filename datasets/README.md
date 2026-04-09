# Open MSK MRI Datasets

Publicly available datasets for musculoskeletal MRI research, organized by anatomy. Datasets with segmentation labels are marked with 🏷️.

*Know a dataset that's missing? [Open an issue](../../issues) or submit a PR.*

---

## Knee

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| **OAI** | 3T MRI (DESS, T2w, T1ρ, etc.) | ~5,000 subjects, longitudinal (up to 10 yr) | Various subsets have cartilage/bone labels | [nda.nih.gov/oai](https://nda.nih.gov/oai/) |
| **IWOAI Challenge** | DESS | Standardized multi-team benchmark | 🏷️ Cartilage (femoral, tibial, patellar), meniscus | [github](https://github.com/IWOAI/data-challenge) |
| **SKM-TEA** | qDESS (3T) | Quantitative maps + raw k-space | 🏷️ Cartilage, meniscus, bones | [github](https://github.com/StanfordMIMI/skm-tea) |
| **SKI10** | MRI | Historical benchmark | 🏷️ Bone, cartilage surfaces | [grand-challenge](https://ski10.grand-challenge.org/) |
| **fastMRI Knee** | Multi-coil k-space | Raw k-space for reconstruction research | No seg labels | [fastmri.med.nyu.edu](https://fastmri.med.nyu.edu/) |
| **Mendeley trajectory data** | OAI-derived | Thickness trajectory subgroup data | Derived measurements | [Mendeley](https://data.mendeley.com/datasets/7jx8rhkcdz/1) |
| **CartiMorph data** | OAI-derived | Processed for cartilage morphometrics | 🏷️ Cartilage | [github](https://github.com/YongchengYAO/CartiMorph) |

## Muscle (thigh, lower limb, whole body)

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| **UK Biobank imaging** | Dixon MRI (1.5T) | ~100K subjects, whole-body composition | Community-derived labels available | [ukbiobank.ac.uk](https://www.ukbiobank.ac.uk/) (application required) |
| **Dafne training data** | Thigh MRI | Multi-site collaborative dataset | 🏷️ Thigh muscles | [dafne-imaging](https://github.com/dafne-imaging/dafne) |

## Spine

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| **SpineWeb** | Multi-modal (MRI, CT) | Collection of spine imaging challenges | Varies by sub-challenge | [spineWeb](https://spider.grand-challenge.org/) |
| **SPIDER** | Lumbar MRI (T1, T2) | 447 studies with expert annotations | 🏷️ Vertebrae, discs, canal | [grand-challenge](https://spider.grand-challenge.org/) |

## Hip

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| *Contributions welcome* | | | | |

## Shoulder

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| *Contributions welcome* | | | | |

## Wrist / Hand

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| *Contributions welcome* | | | | |

## Ankle / Foot

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| *Contributions welcome* | | | | |

## Multi-anatomy / whole-body

| Dataset | Modality | What's included | Labels | Link |
|---------|----------|-----------------|--------|------|
| **TotalSegmentator (MRI subset)** | Multi-sequence MRI | 298 MRI exams, 80 structures | 🏷️ Bones, muscles, organs | [github](https://github.com/wasserth/TotalSegmentator) |
| **AMOS** | CT + MRI | Abdominal multi-organ (some MSK overlap) | 🏷️ Multiple organs | [grand-challenge](https://amos22.grand-challenge.org/) |

---

*See also: [Tools](../tools/), [Papers](../papers/), [Session overview](../)*
