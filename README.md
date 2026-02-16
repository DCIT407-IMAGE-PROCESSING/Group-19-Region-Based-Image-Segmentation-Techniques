# Region-Based Image Segmentation Techniques

**University Of Ghana**

**Department Of Computer Science**

**DCIT407 - Image Processing Semester Project**  

**Group 19**

---

## Project Overview

This project explores **9 segmentation techniques** - from classical algorithms to modern deep learning approaches - applied to region-based image segmentation. Each technique is implemented in its own Jupyter notebook by a team member, and a master notebook ties together the theory, mathematics, and comparative analysis.

## Team Members

| Name | Student ID | Role | Technique(s) |
|------|-----------|------|--------------|
| Ryan Nii Akwei Brown | 11357610 | Group Leader | CNN + Transformer Hybrid (Deep Learning) |
| Cyril Ashong | 11253767 | Member | Watershed Segmentation |
| Prince Henry Kissi | 11063475 | Member | Diffusion-Based Segmentation |
| Martey Kelvin Mamah | 11237476 | Member | Mean Shift Segmentation |
| Ebenezer Nii Nai Badger | 11290659 | Member | Active Contours / Snakes |
| Harriet Esinam Kale | 11357530 | Member | Split and Merge |
| Delina Awash Welday | 11358725 | Member | Region Growing & Self-Supervised Segmentation |
| Owusu Emmanuel Takyi | 11264083 | Member | Graph-Based Segmentation (Felzenszwalb) |

## Project Structure

```
19/
├── README.md                                                   # This file
├── REGION_SEGMENTATION_PROJECT.ipynb                           # Master notebook (theory, math, comparison)
├── requirements.txt                                            # Python dependencies
├── LICENSE                                                     # Project license
│
│   # ── Individual technique notebooks ──
├── Cyril_Ashong_Watershed_Segmentation.ipynb
├── Delina_Region Growing_ Self-Supervised Segmentation.ipynb
├── Eben_ActiveContours.ipynb
├── Harriet _split_merge_segmentation.ipynb
├── HenryKissi_DiffusionBasedSegmentation.ipynb
├── Ryan_CNN_Transformer_Hybrid.ipynb
├── Takyi_GraphBasedSegmentation(Felzenszwalb).ipynb
│
│   # ── Supporting directories ──
├── images/
│   └── sample/                         # Shared test images (007.jpg, Circle.jpg)
├── results/                            # Output visualizations (TODO)
├── docs/                               # Guides & supplementary material
│   ├── NOTEBOOK_STYLE_GUIDE.md         # Standard notebook structure for all members
│   ├── SegFormer_B0_Explained.md
│   └── STUDY_GUIDE_CNN_Transformer.md
└── original individual notebooks/      # Archive of earlier drafts
```

## Techniques Covered

**Classical Methods (1980s–2000s):**

1. Region Growing
2. Watershed Segmentation
3. Mean Shift Segmentation
4. Split and Merge
5. Active Contours (Snakes)
6. Graph-Based Segmentation (Felzenszwalb)

**Modern Deep Learning Methods (2020s):**

7. CNN + Transformer Hybrid (SegFormer)
8. Self-Supervised Segmentation
9. Diffusion-Based Segmentation

## Master Notebook Sections

The master notebook (`REGION_SEGMENTATION_PROJECT.ipynb`) contains:

1. **Introduction** - Project scope, classical vs. deep learning overview
2. **Theory** - Descriptions of all 9 techniques
3. **Mathematical Foundations** - Key equations for each method
4. **Individual Technique Implementations** - Links & summaries for each notebook
5. **Comparative Analysis** - Side-by-side evaluation of methods
6. **Conclusion** - Findings and takeaways
7. **References** - Papers, textbooks, and library documentation

## Requirements

- Python 3.8+
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- scikit-image
- SciPy
- pandas
- Jupyter

Additional libraries for deep learning notebooks:
- `torch`, `torchvision`
- `transformers` (Hugging Face)
- `Pillow`

Install core dependencies:
```bash
pip install -r requirements.txt
```

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/DCIT407-IMAGE-PROCESSING/19.git
cd 19
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open the master notebook for the full project overview:
```bash
jupyter notebook REGION_SEGMENTATION_PROJECT.ipynb
```

4. Or open any individual technique notebook directly (e.g., `Ryan_CNN_Transformer_Hybrid.ipynb`).

## Notebook Style Guide

All individual notebooks follow a standardized 8-section structure defined in [`docs/NOTEBOOK_STYLE_GUIDE.md`](docs/NOTEBOOK_STYLE_GUIDE.md):

> Title & Info → Introduction → Theoretical Foundation → Methodology → Implementation → Results → Discussion → Conclusion → References

## Real-World Applications

- **Autonomous Driving** - Road, vehicle, and pedestrian detection
- **Medical Imaging** - Tumor detection, organ segmentation
- **Satellite Imagery** - Land use classification, urban planning
- **Agriculture** - Crop analysis, disease detection
- **Manufacturing** - Quality control, defect detection

## References

1. Gonzalez, R. C., & Woods, R. E. (2018). *Digital Image Processing* (4th ed.). Pearson.
2. Szeliski, R. (2022). *Computer Vision: Algorithms and Applications* (2nd ed.). Springer.
3. Xie, E., et al. (2021). *SegFormer: Simple and Efficient Design for Semantic Segmentation with Transformers*. NeurIPS 2021.
4. OpenCV Documentation: https://docs.opencv.org/
5. scikit-image Documentation: https://scikit-image.org/
6. Hugging Face Transformers: https://huggingface.co/docs/transformers

## License

This project is part of the DCIT407 course at the University of Ghana.

## Contact

For questions or collaboration, contact the group leader: rnabrown001@st.ug.edu.gh

---

**Last Updated**: February 16, 2026