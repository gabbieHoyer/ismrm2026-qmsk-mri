# Open-Source Tools for MSK MRI

*Know a tool that's missing? [Open an issue](../../issues) or submit a PR.*

---

## Segmentation

| Tool | Description | Language | Link |
|------|-------------|----------|------|
| **nnU-Net** | Self-configuring segmentation baseline — strong default for new tasks | Python | [github](https://github.com/MIC-DKFZ/nnUNet) |
| **MONAI** | PyTorch framework for medical image analysis (includes seg, transforms, metrics) | Python | [github](https://github.com/Project-MONAI/MONAI) |
| **MONAI Label** | Interactive annotation with AI-in-the-loop (works with 3D Slicer) | Python | [github](https://github.com/Project-MONAI/MONAILabel) |
| **TotalSegmentator** | Multi-structure seg for CT and MRI | Python | [github](https://github.com/wasserth/TotalSegmentator) |
| **Dafne** | Federated / collaborative muscle segmentation with incremental learning | Python | [github](https://github.com/dafne-imaging/dafne) |
| **MedSAM** | SAM fine-tuned for medical images | Python | [github](https://github.com/bowang-lab/MedSAM) |

## Registration

| Tool | Description | Language | Link |
|------|-------------|----------|------|
| **ANTs** | Advanced Normalization Tools — diffeomorphic registration, template building | C++ / Python (ANTsPy) | [github](https://github.com/ANTsX/ANTs) |
| **Elastix** | Parametric registration (rigid, affine, B-spline, etc.) | C++ / Python (SimpleElastix) | [github](https://github.com/SuperElastix/elastix) |
| **SimpleITK** | Python/C++ interface for ITK-based registration and filtering | Python / C++ | [simpleitk.org](https://simpleitk.org/) |
| **VoxelMorph** | Learning-based deformable registration | Python (PyTorch) | [github](https://github.com/voxelmorph/voxelmorph) |

## Morphometrics & quantitative analysis

| Tool | Description | Language | Link |
|------|-------------|----------|------|
| **pyKNEEr** | Knee MRI analysis (cartilage thickness, registration) | Python | [github](https://github.com/sbonaretti/pyKNEEr) |
| **CartiMorph** | Cartilage seg + template mapping + morphometrics | Python | [github](https://github.com/YongchengYAO/CartiMorph) |
| **DOSMA** | Musculoskeletal image analysis (quantitative mapping, seg) | Python | [github](https://github.com/ad12/DOSMA) |

## Visualization & annotation

| Tool | Description | Link |
|------|-------------|------|
| **3D Slicer** | Medical image visualization, segmentation, registration | [slicer.org](https://www.slicer.org/) |
| **ITK-SNAP** | Segmentation and annotation | [itksnap.org](http://www.itksnap.org/) |
| **MITK** | Medical Imaging Interaction Toolkit | [mitk.org](https://www.mitk.org/) |

## Reconstruction (relevant to upstream quality)

| Tool | Description | Link |
|------|-------------|------|
| **BART** | Berkeley Advanced Reconstruction Toolbox | [github](https://github.com/mrirecon/bart) |
| **fastMRI** | Facebook AI Research MRI reconstruction | [github](https://github.com/facebookresearch/fastMRI) |
| **MIRTORCH** | MRI reconstruction in PyTorch | [github](https://github.com/guanhuaw/MIRTorch) |

---

*See also: [Datasets](../datasets/), [Papers](../papers/), [Session overview](../)*
