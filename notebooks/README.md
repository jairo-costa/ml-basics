# CIFAR-10 Baseline Classifier (Fully Connected Model)

This project implements a fully documented baseline image classifier using the CIFAR-10 dataset as part of the UrbanSense V2 exploratory phase. The goal is to establish a fast, lightweight reference model to support early architectural decisions, estimate feasibility, and understand initial performance boundaries before transitioning to convolutional neural networks (CNNs).

This notebook follows VisionRail’s internal documentation standard, including:
- clear project context at the top,
- structured cell-by-cell workflow,
- line-by-line explanations,
- rationale for each design choice,
- and insights aligned with real ML engineering practices.

It serves as the foundational baseline against which future models—such as small CNN architectures with augmentation and normalization techniques—will be compared.

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
- Its small resolution (32×32) allows for **fast experimentation**, especially with lightweight models such as fully connected networks.  
- The 10 classes provide enough variability to highlight the **limitations of dense architectures**, making it ideal for demonstrating why CNNs are needed in real-world computer vision projects.  
- Its structured format allows us to create clear reproducible baselines before scaling to **UrbanSense’s proprietary urban imagery dataset**.

This dataset establishes a solid foundation for evaluating training time, generalization behavior, and the feasibility of early-stage models.

## Architecture Used

This project implements a **fully connected (dense) neural network** as the initial baseline for CIFAR-10 classification. The goal is not to maximize accuracy, but to establish a **lightweight and fast reference model** that helps the team evaluate feasibility, training cost, and initial performance boundaries before moving to more complex architectures.

### Model Structure
The model follows this sequence:

1. **Flatten**  
   Converts each 32×32×3 image into a 1-dimensional vector of 3,072 values.  
   This step removes spatial structure, which is intentional for this baseline.

2. **Dense (256 units, ReLU)**  
   First fully connected layer, responsible for learning initial abstract representations.

3. **Dense (128 units, ReLU)**  
   Additional non-linear layer to increase representational capacity.

4. **Dense (10 units, Softmax)**  
   Output layer mapping predictions to the 10 CIFAR-10 classes.

### Rationale Behind This Architecture
- **Speed:** Dense networks train quickly, enabling rapid iteration and early feedback.  
- **Low computational cost:** Ideal for assessing feasibility in environments with limited resources.  
- **Baseline comparison:** Establishes a lower bound against which CNN-based models will be evaluated.  
- **Simplicity:** Useful for dem

## Training Setup

The baseline model was trained using a simple and efficient configuration aligned with lightweight experimentation. The focus is to keep training time low while generating enough signal to evaluate feasibility before moving to CNN-based architectures.

### Configuration Details
- **Loss function:** `sparse_categorical_crossentropy`  
  Used because the labels are integer-encoded (not one-hot). Efficient and appropriate for multi-class classification.

- **Optimizer:** `adam`  
  Provides fast convergence and good stability, ideal for baseline experiments.

- **Batch size:** 64  
  Balanced choice between computational efficiency and gradient stability.

- **Epochs:** 10  
  Sufficient to reveal the strengths and weaknesses of the architecture.

- **Validation split:** 0.1  
  Automatically allocates 10% of the training data for validation, enabling monitoring of generalization during training.

### Purpose of This Setup
- Keep training time low for rapid iteration  
- Provide stable metrics for comparison  
- Establish a reproducible baseline  
- Highlight early signs of overfitting or underfitting  

These hyperparameters are intentionally simple to maintain clarity and reproducibility throughout the experiment.

## Results & Evaluation

The baseline fully connected model provides a fast and interpretable first look at CIFAR-10 performance. While not expected to achieve high accuracy due to its lack of spatial understanding, it establishes an essential lower bound for the UrbanSense V2 model roadmap.

### Final Test Metrics
- **Test Accuracy:** *reported by the notebook execution*  
- **Test Loss:** *reported by the notebook execution*

(CIFAR-10 typically yields ~45–55% accuracy with dense baselines, depending on seed and configuration.)

### Training Curves
The notebook includes:
- **Loss curve** (training vs validation)  
- **Accuracy curve** (training vs validation)

These curves help identify:
- underfitting or overfitting trends,  
- gradient stability,  
- how quickly the model converges,  
- and whether training longer epochs would be beneficial.

### Key Insights
- Dense architectures struggle to capture spatial hierarchies present in image data.  
- Training is fast, confirming suitability for rapid early-stage experiments.  
- Validation accuracy typically stabilizes early, indicating limited expressive power.  
- The baseline is **useful** for feasibility studies but **insufficient** for production-level performance.

These observations guide the next steps toward more suitable architectures.

## How to Run

Follow the steps below to execute the CIFAR-10 baseline notebook in a reproducible environment.

### 1. Open the Repository
Clone or access the repository via GitHub Codespaces:

https://github.com/jairo-costa/ml-basics


### 2. Open the Notebook
Navigate to:


### 3. Install Dependencies
Run the following cell at the top of the notebook (only needed once per Codespace or environment):

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


```markdown
## Next Steps

This baseline experiment provides the foundation for more advanced modeling phases in the UrbanSense V2 project. Recommended next steps include:

### 1. Implement a Small CNN Baseline
Introduce spatial awareness with layers such as:
- Conv2D  
- MaxPooling2D  
- Dropout  
- Batch Normalization  

This will immediately improve accuracy and generalization.

### 2. Apply Data Augmentation
Increase dataset variability with transformations like:
- random flips  
- random rotations  
- shifts and crops  

Useful for reducing overfitting and improving robustness.

### 3. Add Batch Normalization
Stabilizes training, speeds convergence, and improves final accuracy.

### 4. Evaluate Training Time vs. Accuracy Trade-offs
Part of the UrbanSense V2 architectural roadmap involves analyzing:
- computational cost  
- memory usage  
- inference speed  
- generalization performance  

### 5. Prepare Comparative Report
Compare:
- Dense baseline  
- Small CNN  
- Augmented CNN  
- Potential transfer learning baselines (future phases)

This comparison will support the committee’s decision regarding the next architectural milestone.


