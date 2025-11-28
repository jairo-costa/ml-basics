# CIFAR-10 Baseline Classifier (Fully Connected Model)

This project implements a fully documented baseline image classifier using the CIFAR-10 dataset as part of the UrbanSense V2 exploratory phase. The goal is to establish a fast, lightweight reference model to support early architectural decisions, estimate feasibility, and understand initial performance boundaries before transitioning to convolutional neural networks (CNNs).

This notebook follows VisionRail’s internal documentation standard, including:
- clear project context at the top,
- structured cell-by-cell workflow,
- line-by-line explanations,
- rationale behind each design choice,
- and insights aligned with real ML engineering practices.

It serves as the foundational baseline against which future models—such as small CNN architectures with augmentation and normalization techniques—will be compared.


---

## Dataset Overview

The CIFAR-10 dataset is a widely used benchmark for image classification tasks and serves as an appropriate starting point for establishing baseline performance in the UrbanSense V2 project.

### Key Characteristics
- **Total images:** 60,000  
- **Training set:** 50,000 images  
- **Test set:** 10,000 images  
- **Image dimensions:** 32 × 32 pixels  
- **Color channels:** 3 (RGB)  
- **Number of classes:** 10  

### Class Labels
- airplane  
- automobile  
- bird  
- cat  
- deer  
- dog  
- frog  
- horse  
- ship  
- truck  

### Why CIFAR-10 for this baseline?
- It provides a **consistent and well-known benchmark** for rapid prototyping.  
- Its small resolution (32×32) allows for **fast experimentation**, especially with lightweight models.  
- It exposes the **limitations of dense architectures**, making it ideal for demonstrating the need for CNNs in real computer vision tasks.  
- It allows for reproducible benchmarking before transitioning to **UrbanSense’s proprietary urban imagery dataset**.

This dataset establishes a solid foundation for evaluating training time, generalization behavior, and feasibility.


---

## Architecture Used

This project implements a **fully connected (dense) neural network** as the initial baseline for CIFAR-10 classification. The goal is not to maximize accuracy, but to establish a **lightweight and fast reference model** that helps the team evaluate feasibility before moving to more complex architectures.

### Model Structure
1. **Flatten** – Converts each 32×32×3 image into a 1D vector (3,072 values).  
2. **Dense (256 units, ReLU)** – First non-linear layer for abstract representation learning.  
3. **Dense (128 units, ReLU)** – Secondary representation layer.  
4. **Dense (10 units, Softmax)** – Output layer mapping predictions to the 10 CIFAR-10 classes.

### Rationale Behind This Architecture
- **Speed:** Excellent for rapid iteration.  
- **Low computational cost:** Ideal for feasibility checks in early project phases.  
- **Baseline comparison:** Establishes the lower bound of performance.  
- **Intentional simplicity:** Highlights why CNNs are necessary later.

### Expected Behavior
- Fast training  
- Limited generalization  
- Early plateau in accuracy  
- Strong demonstration of dense-network constraints


---

## Training Setup

The baseline model was trained using a simple and efficient configuration aligned with lightweight experimentation.

### Configuration Details
- **Loss function:** `sparse_categorical_crossentropy`
- **Optimizer:** `adam`
- **Batch size:** 64
- **Epochs:** 10
- **Validation split:** 0.1

### Purpose of This Setup
- Maintain fast iteration cycles  
- Provide clear and stable metrics  
- Support reproducible baselines  
- Reveal early generalization patterns  


---

## Results & Evaluation

The baseline fully connected model provides a fast and interpretable first look at CIFAR-10 performance. While not expected to achieve high accuracy, it serves as the **reference minimum** for future models.

### Final Test Metrics
- **Test Accuracy:** *(from notebook execution)*  
- **Test Loss:** *(from notebook execution)*  

Dense baselines typically achieve ~45–55% accuracy on CIFAR-10.

### Training Curves
Included in the notebook:
- Training vs. Validation Loss  
- Training vs. Validation Accuracy  

These graphs help detect:
- underfitting,  
- overfitting,  
- convergence behavior,  
- need for architectural changes.

### Key Insights
- The model trains quickly but lacks spatial awareness.  
- Validation accuracy plateaus early, exposing expressive limitations.  
- This confirms the need for CNN-based baselines for UrbanSense V2.

This baseline establishes the **reference point** for architectural decisions.


---

## How to Run

Follow the steps below to execute the CIFAR-10 baseline notebook in a reproducible environment.

### 1. Open the Repository
https://github.com/jairo-costa/ml-basics


### 2. Open the Notebook
ml-basics/project-02-cifar-10-classifier.ipynb


### 3. Install Dependencies
Run this once in the Codespace / environment:
```python
%pip install tensorflow

### 4. Run All Cells
Execute the notebook sequentially to reproduce:

- dataset loading  
- preprocessing  
- model creation  
- training  
- evaluation  
- insights  

The notebook is fully documented with line-by-line explanations and output visualizations.

## Requirements

To run this project, ensure the following packages and tools are available:

- **Python 3.9+**
- **TensorFlow 2.x**
- **Matplotlib**
- **NumPy**
- **Jupyter / VS Code Notebook support**

These requirements guarantee full compatibility and reproducibility of the experiment.

## Next Steps

Recommended next steps for UrbanSense V2:

### 1. Implement a Small CNN Baseline
Introduce spatial awareness with:
- Convolutional layers  
- MaxPooling2D  
- Dropout  
- Batch Normalization  

This will significantly improve accuracy and generalization.

### 2. Add Data Augmentation
Increase dataset variability using:
- random horizontal flips  
- rotations  
- crops  
- shifts  

Useful to reduce overfitting and improve robustness.

### 3. Apply Batch Normalization
Stabilizes training, reduces internal covariate shift, and accelerates convergence.

### 4. Evaluate Training Cost vs. Accuracy Trade-offs
Analyze:
- computational cost  
- memory usage  
- training time  
- inference speed  
- generalization performance  

This aligns with UrbanSense’s architectural planning requirements.

### 5. Prepare Comparative Report
Compare performance between:
- Dense baseline  
- Small CNN  
- Augmented CNN  
- (future) transfer learning baselines  

This will support data-driven decisions for the next architectural phase.

## Author

**Jairo Costa**  
AI Engineering Intern  
VisionRail Analytics (2025)

