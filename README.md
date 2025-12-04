# 📘 ML-Basics — Machine Learning Portfolio Repository

This repository contains a structured collection of introductory and intermediate Machine Learning projects, developed following professional documentation standards and a simulation of real-world Applied ML workflows.

Each project in this repository is organized to reflect:

- clear technical objectives  
- corporate-style communication (internal e-mails, requirements, decision reports)  
- fully documented notebooks with line-by-line explanations  
- reproducible environments  
- incremental learning across different ML tasks  

---

## 🗂️ Repository Structure

ml-basics/
│
├── notebooks/
│ ├── project-01-data-visualization/
│ │ ├── project-01-data-visualization.ipynb
│ │ └── README.md
│ │
│ ├── project-02-cifar10-classifier/
│ │ ├── 01-cifar10-baseline-fully-connected.ipynb
│ │ └── README.md
│ │
│ ├── project-04-eta-prediction/
│ │ ├── data/
│ │ │ └── eta_dataset.csv
│ │ ├── project-04-eta-prediction.ipynb
│ │ ├── README.md
│ │ └── requirements.txt
│ │
│ └── notes/
│ ├── notes-day1.md
│ ├── notes-day2.md
│ └── README.md
│
└── README.md ← (you are here)


---

## 📚 Project Summaries

### **Project 01 — Data Visualization**
Exploratory Data Analysis using Seaborn/Matplotlib with a structured interpretation workflow.  
Focus: clarity, EDA pipeline, and communication of insights.

---

### **Project 02 — CIFAR-10 Baseline Classifier**
Image classification using a fully connected neural network as a baseline.  
Focus: model interpretation, baseline creation, training curves, and corporate-style reporting.

---

### **Project 04 — ETA Prediction (Regression Model)**
Delivery ETA prediction using a synthetic logistics-like dataset stored in `data/eta_dataset.csv`.  
Implements a regression pipeline comparing:

- Linear Regression  
- Random Forest  
- Gradient Boosting  
- optional XGBoost  

Includes business-oriented interpretation and model diagnostics.

---

## 📝 Notes Section

The `notes/` folder contains conceptual notes, study diaries, and technical reflections produced during development.  
It serves as supplementary learning material and knowledge consolidation.

---

## ▶️ How to Run the Projects

### Using Codespaces (recommended)

%pip install -r requirements.txt


Then open each notebook inside `notebooks/project-XX/...` and run the cells sequentially.

### Local environment

pip install pandas numpy matplotlib seaborn scikit-learn xgboost


---

## 👤 Author

**Jairo Costa**  
🔗 LinkedIn: https://www.linkedin.com/in/jairo-costa-0472b839a/  
🔗 Hugging Face: https://huggingface.co/Jairo-Costa

---

## 📄 License

This repository is for educational and portfolio purposes.
