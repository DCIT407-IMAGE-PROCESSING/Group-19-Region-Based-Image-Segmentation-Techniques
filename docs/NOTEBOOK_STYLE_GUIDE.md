# Notebook Style Guide  Group 19

**DCIT407 - Image Processing Semester Project**

This guide defines the standard structure every teammate's notebook should follow. Use Ryan's CNN + Transformer Hybrid notebook as the reference implementation.

---

## Overall Structure (8 Sections)

Every notebook must have these sections **in this order**:

| # | Section | Purpose |
|---|---------|---------|
| 1 | **Introduction** | What the method is, why it matters, what the notebook covers |
| 2 | **Theoretical Foundation** | Math, diagrams, and concepts behind your method |
| 3 | **Methodology** | Pipeline overview, libraries, dataset description |
| 4 | **Implementation** | All code  setup, model/algorithm, helpers, running it |
| 5 | **Results** | Visualizations, metrics, class/region analysis |
| 6 | **Discussion** | Interpretation, strengths/limitations, applications, comparison |
| 7 | **Conclusion** | Summary of findings, practical implications, future work |
| 8 | **References** | Papers, textbooks, software libraries used |

---

## Section-by-Section Guide

### Cell 1  Title & Project Info (Markdown)

Start with a top-level heading, the course/project line, and a metadata table:

```markdown
# [Your Method Name] for Image Segmentation

**DCIT407 - Image Processing Semester Project**  
**Group 19 | Section [X.X]**

---

## Project Information

| Field | Details |
|-------|--------|
| **Author** | [Your Full Name] |
| **Student ID** | [Your ID] |
| **Topic** | [Method Name] Segmentation |
| **Libraries** | `lib1`, `lib2`, `lib3`, ... |
| **Model/Algorithm** | [Model or algorithm name + variant] |
| **Date** | February 2026 |

---

## Table of Contents

1. [Introduction](#introduction)
2. [Theoretical Foundation](#theory)
3. [Methodology](#methodology)
4. [Implementation](#implementation)
5. [Results](#results)
6. [Discussion](#discussion)
7. [Conclusion](#conclusion)
8. [References](#references)
```

> **Note:** Keep the anchor IDs (`#introduction`, `#theory`, etc.) consistent so the Table of Contents links work.

---

### Section 1  Introduction (Markdown)

Add the anchor tag, then cover:

```markdown
<a id="introduction"></a>
## 1. Introduction
```

**Must include:**
- What image segmentation is (1–2 sentences  keep brief, we all share this context)
- What your specific method is and the core idea behind it
- Why it's relevant / what problem it solves
- A numbered list of what the notebook will do, e.g.:

```markdown
**In this notebook we:**
1. Explain the theory behind [method]
2. Implement [method] on sample images
3. Analyze and visualize the results
4. Discuss strengths, limitations, and applications
```

---

### Section 2  Theoretical Foundation (Markdown)

```markdown
<a id="theory"></a>
## 2. Theoretical Foundation
```

**Must include:**
- Use **subsections** (`### 2.1`, `### 2.2`, …) to organize concepts
- Key equations in **LaTeX** (use `$$...$$` for display math, `$...$` for inline)
- At least one comparison table if your method involves contrasting approaches
- Bold key terms on first mention
- Explain jargon in plain language (use analogies where helpful)

**Example equation format:**
```markdown
$$\text{Attention}(Q, K, V) = \text{softmax}\!\left(\frac{QK^\top}{\sqrt{d_k}}\right) V$$
```

---

### Section 3  Methodology (Markdown)

```markdown
<a id="methodology"></a>
## 3. Methodology
```

**Must include 3 subsections:**

#### 3.1 Implementation Approach
- Describe your pipeline in words, then as an ASCII flow:
```
Input Image → Step A → Step B → Step C → Segmented Output
```
- Mention if you use a pretrained model or implement from scratch

#### 3.2 Libraries and Tools
- Bullet list of every library and its role, e.g.:
```markdown
- **opencv-python**: Image I/O and preprocessing
- **numpy**: Numerical operations
```

#### 3.3 Dataset
- What images you test on
- If using a pretrained model, describe the training dataset and what classes it recognizes

---

### Section 4  Implementation (Code + Markdown)

```markdown
<a id="implementation"></a>
## 4. Implementation
```

**Organize code into subsections  each subsection gets a markdown header cell followed by a code cell:**

| Subsection | Content |
|------------|---------|
| **4.1 Environment Setup** | Imports, device setup, config, matplotlib defaults |
| **4.2 Load Model / Define Algorithm** | Load pretrained model OR define your algorithm's core logic |
| **4.3 Helper Functions** | All utility functions (loading images, running inference, colorizing masks, overlays). Each function needs a **docstring** with Args/Returns |
| **4.4 Load Test Image** | Load image, print shape, display it with `plt.imshow` |
| **4.5 Run Segmentation** | Execute your method, print summary stats (mask shape, # classes/regions, etc.) |

**Code standards:**
- Every function must have a docstring:
  ```python
  def my_function(image, param):
      """
      Brief description.
      
      Args:
          image: RGB image as numpy array
          param: Description of parameter
      Returns:
          Description of return value
      """
  ```
- Print a confirmation after major steps (e.g., `print("✓ Model loaded")`)
- Use `warnings.filterwarnings('ignore')` to suppress noisy warnings
- Comment blocks of logic, not every line

---

### Section 5  Results (Code + Markdown)

```markdown
<a id="results"></a>
## 5. Results
```

**Must include at minimum:**

#### 5.1 Visualization
- A **1×3 subplot figure** showing:
  - (a) Original Image
  - (b) Segmentation Output
  - (c) Overlay (original + segmentation blended)
- Use `figsize=(18, 6)`, bold titles with `fontweight='bold'`
- Add a `suptitle` with your method name

#### 5.2 Quantitative Analysis
- Print a formatted table of detected classes/regions with pixel counts and percentages
- Use separator lines (`"="*60`) for readability

#### 5.3 Legend (if applicable)
- Color legend mapping colors to class/region names

---

### Section 6  Discussion (Markdown)

```markdown
<a id="discussion"></a>
## 6. Discussion
```

**Must include 4 subsections:**

#### 6.1 Interpretation of Results
- Explain **why** your method produced these results
- Connect back to theory (e.g., "The Transformer's self-attention is why sky was correctly segmented")

#### 6.2 Strengths and Limitations
- Use ✓ / ✗ bullet formatting:
```markdown
**Strengths:**
- ✓ Good at X because Y

**Limitations:**
- ✗ Struggles with X because Y
```

#### 6.3 Real-World Applications
- At least 3 applications with brief descriptions
- Mention when your method is **not** the best choice

#### 6.4 Comparison with Other Methods
- A markdown table comparing your method against at least one other approach:
```markdown
| Aspect | Your Method | Other Method |
|--------|-------------|-------------|
| ... | ... | ... |
```

---

### Section 7  Conclusion (Markdown)

```markdown
<a id="conclusion"></a>
## 7. Conclusion
```

**Must include:**
- **Key Findings**  numbered list (3–4 points)
- **Practical Implications**  when/why to use this method
- **Future Directions**  bullet list of extensions or improvements

---

### Section 8  References (Markdown)

```markdown
<a id="references"></a>
## 8. References
```

**Organize into categories:**
- **Core Papers**  numbered, full citation with arXiv/DOI links
- **Datasets**  if applicable
- **Textbooks**  Gonzalez & Woods (required), plus any others
- **Software Libraries**  links to docs

**Required references (everyone should cite):**
```
Gonzalez, R. C., & Woods, R. E. (2018). Digital Image Processing (4th ed.). Pearson.
```

**End the notebook with:**
```markdown
---
*End of Notebook - [Your Name] | Student ID: [Your ID] | Group 19, DCIT407*
```

---

## Formatting Checklist

Before submitting, verify:

- [ ] All 8 sections present in correct order
- [ ] Project Info table filled in completely
- [ ] Table of Contents links work (anchor IDs match)
- [ ] Equations rendered in LaTeX
- [ ] All functions have docstrings (Args + Returns)
- [ ] 1×3 visualization subplot included
- [ ] Quantitative stats printed (pixel counts, percentages, or metrics)
- [ ] Strengths/limitations listed with ✓/✗ markers
- [ ] Comparison table with at least one other method
- [ ] References section has papers, textbook, and library links
- [ ] Closing line with name, student ID, group number
- [ ] Code cells run top-to-bottom without errors
- [ ] No hardcoded absolute paths (use relative paths like `images/sample/...`)
- [ ] Test images are in the shared `images/sample/` folder

---

## Quick Reference: Cell Order

```
 1. [MD]  Title + Info Table + TOC
 2. [MD]  1. Introduction
 3. [MD]  2. Theoretical Foundation (with subsections)
 4. [MD]  3. Methodology
 5. [MD]  4. Implementation header
 6. [PY]  4.1 Environment Setup (imports, config)
 7. [MD]  4.2 header
 8. [PY]  4.2 Load Model / Algorithm
 9. [MD]  4.3 header
10. [PY]  4.3 Helper Functions
11. [MD]  4.4 header
12. [PY]  4.4 Load Test Image
13. [MD]  4.5 header
14. [PY]  4.5 Run Segmentation
15. [MD]  5. Results header
16. [PY]  5.1 Visualization (1×3 subplot)
17. [MD]  5.2 header
18. [PY]  5.2 Quantitative Analysis
19. [MD]  5.3 header
20. [PY]  5.3 Legend
21. [MD]  6. Discussion (all subsections in one cell)
22. [MD]  7. Conclusion
23. [MD]  8. References + closing line
```

`[MD]` = Markdown cell, `[PY]` = Python code cell

---

*Guide created from Ryan's CNN + Transformer Hybrid notebook  Group 19, DCIT407*
