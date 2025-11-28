# ml-basics — Machine Learning Fundamentals & Applied Projects

This repository consolidates the core foundations of Machine Learning through fully documented, structured, and realistic hands-on projects.  
It is part of a professional training pipeline designed to simulate real ML Engineering environments, using internal communication, technical requests, reproducible experiments, and documentation standards aligned with enterprise-level workflows.

Each notebook follows a rigorous methodology focused on clarity, reproducibility, and engineering mindset.


---

## Vision & Purpose of This Repository

The goal of *ml-basics* is to build a strong practical foundation in:

- data manipulation  
- exploratory analysis  
- machine learning pipelines  
- baseline modeling  
- reproducible notebooks  
- technical communication skills  

This repository serves as an evolving portfolio and a training ground where every project simulates a real workflow—receiving internal requests, producing deliverables, writing insights for decision-making, and maintaining documentation standards.

It is developed as part of the AI Engineering Internship training under the **VisionRail Analytics** learning framework.


---

## Documentation & Methodology

This repository adopts a standardized structure across all notebooks:

### ✔ Context at the top  
Each notebook starts with a clear description of:
- objective  
- environment  
- scope  
- dataset used  
- expected outcomes  

### ✔ Structured cell-by-cell workflow  
Clear logical sequencing from data → preprocessing → modeling → evaluation → insights.

### ✔ Line-by-line explanations  
Every code block includes:
- full-cell explanation  
- detailed line-by-line breakdown  
- why the line exists  
- typical errors  
- how it appears in interviews  
- how it is used in real ML pipelines  

### ✔ Professional communication  
Projects follow corporate-style internal communication:
- technical requests from leadership  
- internal memos  
- delivery notes  
- decision-oriented insights  

This enhances communication skills while reinforcing real-world ML engineering practices.

### ✔ Reproducibility first  
All experiments include:
- seed fixing  
- environment notes  
- clear dependencies  
- how to run  
- versioned READMEs  


---

## Repository Structure

ml-basics/
│
├── notebooks/
│ ├── project-01-data-visualization/
│ │ ├── 01-data-visualization.ipynb
│ │ └── README.md
│ │
│ ├── project-02-cifar10-classifier/
│ │ ├── 01-cifar10-baseline-fully-connected.ipynb
│ │ └── README.md
│ │
│ └── (future projects)
│
└── notes/
├── notes-day1.md
├── notes-day2.md
└── README.md


### Folder Roles

- **project-01-data-visualization/**  
  Exploratory data analysis project focusing on data inspection, cleaning, and visualization.

- **project-02-cifar10-classifier/**  
  Fully connected baseline classifier for CIFAR-10, created to support early-phase architectural decisions for UrbanSense V2.

- **notes/**  
  Daily technical notes, summaries, and reflections documenting the learning path.


---

## Project Summaries

### 🔹 **Project 01 — Data Visualization & Exploratory Analysis**
A complete exploratory data analysis pipeline covering:
- loading and inspecting tabular data  
- cleaning procedures  
- distribution plots  
- categorical comparisons  
- correlation heatmaps  
- insights extracted from visual patterns  

📄 *Full README:*  
`notebooks/project-01-data-visualization/README.md`

---

### 🔹 **Project 02 — CIFAR-10 Baseline Classifier (Fully Connected Model)**
Implements a dense-network baseline to establish:
- initial model performance  
- feasibility of lightweight architectures  
- training cost vs. accuracy  
- the need for CNN-based pipelines  

Includes full documentation, visualizations, and insights for decision-making.

📄 *Full README:*  
`notebooks/project-02-cifar10-classifier/README.md`


---

## How to Run the Notebooks

1. Open the repository in GitHub Codespaces or VS Code.
2. Navigate to the desired project folder inside `notebooks/`.
3. Install dependencies (example):
   ```python
   %pip install pandas matplotlib seaborn tensorflow

### 4. Run All Cells
Execute the notebook sequentially to reproduce:

- dataset loading  
- preprocessing  
- model creation  
- training  
- evaluation  
- insights  

The notebook is fully documented with line-by-line explanations and output visualizations.

---

## Requirements

To run this project, ensure the following packages and tools are available:

- **Python 3.9+**
- **TensorFlow 2.x**
- **Matplotlib**
- **NumPy**
- **Jupyter / VS Code Notebook support**

These requirements guarantee full compatibility and reproducibility of the experiment.

---

## Next Steps

Recommended next steps for UrbanSense V2:

### 1. Implement a Small CNN Baseline
Introduce spatial awareness with:
- Convolutional layers  
- MaxPooling2D  
- Dropout  
- Batch Normalization  

### 2. Add Data Augmentation
Use transformations such as:
- random flips  
- rotations  
- shifts  
- crops  

### 3. Apply Batch Normalization
Stabilizes training, speeds convergence, and improves generalization.

### 4. Evaluate Training Cost vs Accuracy
Analyze:
- compute cost  
- inference time  
- memory usage  
- generalization behavior  

### 5. Prepare Comparative Report
Compare:
- Dense baseline  
- Small CNN  
- Augmented CNN  
- Future transfer learning baselines  

---

## Author

**Jairo Costa**  
🔗 LinkedIn: https://www.linkedin.com/in/jairo-costa-0472b839a/  
🔗 Hugging Face: https://huggingface.co/Jairo-Costa


