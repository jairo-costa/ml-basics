# Project 01 — Data Visualization & Exploratory Analysis

This project introduces fundamental data manipulation and visualization techniques using Python. It serves as the foundation for building analytical intuition and preparing structured datasets for Machine Learning workflows. The notebook included in this project demonstrates a complete exploratory pipeline, from loading the dataset to generating clear, meaningful visual insights.

This project follows VisionRail’s standardized documentation format:
- contextual introduction at the top,
- structured cell-by-cell workflow,
- line-by-line explanations,
- rationales for each transformation,
- visual analysis aligned with real-world analytical practices.


---

## Dataset Overview

This project uses a tabular dataset suitable for initial exploratory analysis.  
The dataset includes numerical and categorical features commonly found in business or operational environments.

### Typical Characteristics
- Mixed data types (numeric + categorical)  
- No missing labels in target column  
- Sufficient variability for exploration  
- Applicable to both statistical and visualization techniques  

The dataset allows us to practice:
- data loading,
- missing value inspection,
- outlier checks,
- relational analysis,
- and visualization patterns.


---

## Objectives of the Project

This project is designed to:

### ✔ Build familiarity with foundational data analysis operations:
- loading structured data with Pandas,  
- inspecting shape, types, and column characteristics,  
- handling missing values and basic cleaning.

### ✔ Develop visualization intuition:
- distributions,  
- relationships between variables,  
- categorical comparisons,  
- correlation structures.

### ✔ Introduce reproducible analytical workflows:
- clear explanations,
- execution order,
- narrative-driven analysis,
- consistent documentation.

This forms the analytical base required for more advanced ML pipelines.


---

## Techniques Used

### 1. Data Loading & Inspection
- `pandas.read_csv()`  
- `.info()`, `.describe()`, `.head()`

### 2. Data Cleaning
- Handling missing values  
- Type correction  
- Basic transformations  

### 3. Visualization Techniques
Using **Matplotlib** and **Seaborn**:
- histograms  
- boxplots  
- countplots  
- bar charts  
- scatterplots  
- correlation heatmaps  

### 4. Statistical Insights
- summary statistics  
- correlation checks  
- distribution patterns  
- comparative categorical analysis  


---

## Key Insights from the Notebook

The notebook highlights:
- overall distribution structure,  
- presence (or absence) of outliers,  
- relationships between key variables,  
- categorical trends,  
- high-level numerical patterns.

These insights demonstrate the value of visualization in building intuition before modeling.


---

## How to Run

### 1. Open the Repository
Access via GitHub or Codespaces:
https://github.com/jairo-costa/project-01-data-visualization


### 2. Open the Notebook
Navigate to:
notebooks/01-data-visualization.ipynb


### 3. Install Dependencies
Run once per environment:

```python
%pip install pandas matplotlib seaborn

### 4. Run All Cells
Execute the notebook sequentially to reproduce:

- data loading  
- inspection and cleaning  
- exploratory visualizations  
- statistical insights  

The notebook follows a structured, commented, and line-by-line format to support clarity and reproducibility.

## Requirements

To run this project, ensure the following packages and tools are available:

- **Python 3.9+**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Jupyter / VS Code Notebook support**

These requirements ensure full compatibility and reproducibility of the notebook.

## Next Steps

Recommended improvements and extensions for Project 01:

### 1. Add Interactive Visualizations
Introduce more expressive and interactive visual exploration using:
- Plotly  
- Altair  
- Dash  

### 2. Build Feature Engineering Notebook
Design transformations and feature creation steps to prepare the dataset for ML pipelines.

### 3. Apply Data Cleaning Automation
Convert cleaning logic into reusable functions or scripts for consistent preprocessing.

### 4. Introduce Statistical Testing
Explore:
- ANOVA  
- Chi-square tests  
- Correlation diagnostics  
- Normality checks  

Useful for deeper analytical validation.

### 5. Prepare Comparative Analysis
Compare multiple visualization methods to evaluate expressive power and interpretability.

## Author

**Jairo Costa**  
AI Engineering Intern  
VisionRail Analytics (2025)

