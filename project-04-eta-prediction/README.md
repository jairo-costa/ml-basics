# Project 04 — ETA Prediction (Regression Model)

This project implements a regression-based ETA (Estimated Time of Arrival) prediction model using logistics and delivery operational data.  
It follows the IA/ML Decision Framework (PPI) and simulates a real corporate environment, including internal requests, technical reports, and decision-oriented analysis.

---

## 1. Project Overview

- **Goal:** Predict the delivery ETA (in minutes/hours) based on operational features (route, distance, time window, traffic profile, etc.).  
- **Type:** Supervised learning — Regression.  
- **Context:** Logistics / last-mile delivery / shipping ETA.  
- **Business Stakeholders:** Operations, Planning, Customer Experience.

The main objective is not only to train models, but to support decision-making with interpretable metrics and clear performance baselines.

---

## 2. Business Context

This project is part of the internal portfolio for Applied Machine Learning in logistics.  
The ETA prediction model aims to:

- improve delivery time estimation,  
- reduce SLA violations,  
- enhance customer communication,  
- provide realistic expectations for internal planning.

The project is framed as a response to a corporate request from the manager **Mariana**, simulating an internal e-mail that starts the initiative.

---

## 3. Dataset Overview (ETA / Shipping Data)

**Note:** The dataset will be defined and documented in detail as soon as the final source is selected.

Expected characteristics:

- Historical delivery records  
- Pickup and drop-off locations (or zones)  
- Distance or route features  
- Timestamps (pickup time, delivery time, day of week, etc.)  
- Operational constraints (time windows, service type, etc.)  
- Target: **ETA** (or actual delivery duration)

A dedicated “Dataset Card” can be added later to document fields, quality, and limitations.

---

## 4. Modeling Approach

This project will compare multiple regression models to estimate ETA:

- **Linear Regression**  
- **Random Forest Regressor**  
- **Gradient Boosting Regressor / XGBoost**  

The goal is to:

- start from a simple interpretable baseline,  
- incrementally add non-linear models,  
- evaluate trade-offs between accuracy, robustness, and complexity.

Feature engineering, scaling, and encoding strategies will be documented as part of the modeling pipeline.

---

## 5. Evaluation Metrics

Models will be evaluated using:

- **MAE (Mean Absolute Error)** — average absolute error in time units  
- **RMSE (Root Mean Squared Error)** — penalizes larger errors more strongly  
- **R² (Coefficient of Determination)** — proportion of variance explained  

Visual evaluation:

- Residual plots  
- Predicted vs Actual ETA plots  
- Error distribution plots  

These metrics will be interpreted from a business perspective (impact on SLA, customer perception, etc.).

---

## 6. Repository Structure (for this project)

```text
project-04-eta-prediction/
  project-04-eta-prediction.ipynb   # main regression notebook
  README.md                         # this file
  requirements.txt                  # dependencies for this project
  (future) environment.yml          # optional - full environment spec
