# Region-Based Image Segmentation Techniques

**DCIT407 - Image Processing Semester Project**  
**Group 19**

## Project Overview

This project explores various techniques used in region-based image segmentation, a fundamental component of computer vision and image processing. Region-based segmentation divides an image into multiple regions or segments based on characteristics such as color, intensity, texture, or other visual properties.

## Project Topic

**Techniques used in region-based image segmentation**

Region-based segmentation methods group pixels into regions that share similar characteristics. This project implements and compares several key techniques including:
- Region Growing
- Region Splitting and Merging
- Watershed Segmentation
- Mean Shift Segmentation
- Graph-Based Segmentation
- TODO: Pending update after teams conclusion on 8th Feb

## Team Members

| Name | Student ID | Role |
|------|-----------|------|
| Ryan Nii Akwei Brown | 11357610 | Group Leader |
| Cyril Ashong | 11253767 | Member |
| Prince Henry Kissi | 11063475 | Member |
| Martey Kelvin Mamah | 11237476 | Member |
| Ebenezer Nii Nai Badger | 11290659 | Member |
| Harriet Esinam Kale | 11357530 | Member |
| Delina Awash Welday | 11358725 | Member |
| Owusu Emmanuel Takyi | 11264083 | Member |


## Project Structure

```
19/
├── README.md                          # Project documentation
├── region_segmentation_project.ipynb  # Main Jupyter notebook
├── requirements.txt                   # Python dependencies
├── images/                            # Input images directory
│   ├── sample/                        # Sample test images
│   └── README.md                      # Image guidelines
├── results/                           # Output/processed images
└── LICENSE                            # Project license
```
> Collaborating: Working in the main notebook, you can work in a section or your own colab nb, and when ready, you compile and include your cells.

## Requirements

- Python 3.8+
- OpenCV (cv2)
- NumPy
- Matplotlib
- scikit-image
- Jupyter Notebook

Install all dependencies using:
```bash
pip install -r requirements.txt
```

## Running the Project

1. Clone the repository(or use a github codespace):
```bash
git clone https://github.com/DCIT407-IMAGE-PROCESSING/19.git
cd 19
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook(or your usual):
```bash
jupyter notebook region_segmentation_project.ipynb
```

4. Run all cells to see the implementations and results

## Project Sections

### 1. Theory
- Introduction to image segmentation
- Region-based segmentation concepts
- Mathematical foundations
- Comparison with edge-based and threshold-based methods

### 2. Implementation
- Region Growing algorithm
- Split and Merge techniques
- Watershed transformation
- Mean Shift clustering
- Graph-based segmentation methods

### 3. Results
- Original vs. segmented images
- Comparative analysis of different techniques
- Performance metrics
- Visual quality assessment

### 4. Discussion
- Strengths and limitations of each technique
- Computational complexity analysis
- Real-world applications
- Best use cases for each method

## Real-World Applications

- **Medical Imaging**: Tumor detection, organ segmentation
- **Autonomous Vehicles**: Road and object detection
- **Agriculture**: Crop analysis, disease detection
- **Satellite Imagery**: Land use classification, urban planning
- **Manufacturing**: Quality control, defect detection

## Assessment Criteria

This project will be evaluated based on:
- ✓ Understanding of image processing concepts
- ✓ Correctness of implementation
- ✓ Quality of results and analysis
- ✓ Code organization and documentation
- ✓ Presentation and teamwork

## References

1. Gonzalez, R. C., & Woods, R. E. (2018). *Digital Image Processing* (4th ed.). Pearson.
2. Szeliski, R. (2022). *Computer Vision: Algorithms and Applications* (2nd ed.).
3. OpenCV Documentation: https://docs.opencv.org/
4. scikit-image Documentation: https://scikit-image.org/

## License

This project is part of the DCIT407 course at the University of Ghana.

## Contact

For questions or collaboration, please contact the group leader via the university email system @blip-cmd, rnabrown001@st.ug.edu.gh

---

**Last Updated**: February 6, 2026 Evening
