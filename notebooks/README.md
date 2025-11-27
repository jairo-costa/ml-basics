# CIFAR-10 Baseline Classifier (Fully Connected)

This notebook implements a fully documented baseline image classifier using the CIFAR-10 dataset, following our internal simulation of real corporate workflows (technical e-mails, requirements, and decision-oriented reporting).

### 🔹 What this notebook includes
- Dataset loading and visual exploration  
- Preprocessing (normalization + label formatting)  
- Fully connected baseline model (Flatten → Dense → Dense → Softmax)  
- Training with validation split  
- Loss/accuracy curves  
- Final evaluation on the test set  
- Decision-oriented insights for the UrbanSense V2 project  

### 🔹 About our methodology
All notebooks in this repository follow a structured format:
- clear context at the top,  
- organized cells,  
- complete explanations,  
- line-by-line breakdowns,  
- and sections highlighting why each step matters (recruiter, interview, real ML workflow).  

This approach simulates the expectations of an actual ML engineering environment.

### 🔹 Objective
Provide a fast, reproducible baseline to support the next architectural decisions:
- evaluate feasibility of lightweight models,  
- measure baseline accuracy,  
- identify limitations of dense networks for image tasks,  
- guide the transition toward CNN-based pipelines.

---

**Author:** Jairo Costa  
AI Engineering Intern — VisionRail Analytics
