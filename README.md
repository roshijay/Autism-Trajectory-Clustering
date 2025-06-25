# Autism Developmental Trajectory Clustering

> A longitudinal clustering project to model developmental heterogeneity in children with Autism Spectrum Disorder (ASD) using simulated cognitive trajectories across childhood.

---

## Overview

Autism Spectrum Disorder (ASD) presents wide variability in developmental patterns, making early intervention and precision support challenging. This project uses **unsupervised learning** to identify **trajectory-based subgroups** in simulated cognitive data from ages 3 to 15.

By applying clustering to longitudinal trends and evaluating both internal and external validity (Silhouette Score, Adjusted Rand Index), this pipeline demonstrates how interpretable subgroups like **stable**, **improving**, and **declining** can be modeled and validated for real-world use.

---

## Project Goals

- Group children by **longitudinal cognitive patterns**
- Evaluate unsupervised clusters against known developmental archetypes
- Assess **fairness across demographics** (e.g., gender, ethnicity)
- Lay groundwork for scalable clustering pipelines in pediatric health

---

## Dataset Summary

- **Type**: Simulated longitudinal pediatric dataset
- **Size**: 200 subjects × 5 timepoints (ages 3, 6, 9, 12, 15)
- **Features**:
  - `Age`: Timepoints (in years)
  - `Cognitive_Score`: Simulated cognitive metric
  - `Label`: Underlying trajectory type (ground truth, for ARI only)
  - `Demographics`: Gender, Ethnicity

> Dataset is synthetic, ethically generated, and balanced across demographic factors.

---

## Methodology

### 1. Data Simulation
- Generated 3 archetypal trajectories: **Stable**, **Improving**, and **Declining**
- Introduced Gaussian noise to simulate clinical data variance

### 2. Clustering Techniques
- K-Means and Agglomerative Clustering applied at `k=3, 4, 6`
- Compared cluster robustness and trajectory alignment

### 3. Evaluation Metrics
- **Silhouette Score**: Internal cluster cohesion
- **Adjusted Rand Index (ARI)**: External alignment with latent labels

### 4. Bias & Fairness
- Stratified demographic review
- No clustering bias observed by gender or ethnicity

---

##  Key Findings

- Optimal clusters at `k=3` captured core developmental profiles
- ARI ~0.65 indicates strong match to latent groupings
- No demographic skew detected, supporting fairness of unsupervised grouping
- Visuals showed clear separation between **Stable**, **Improving**, and **Declining** trajectories

---

##  Project Deliverables

- ✅ `clustering_analysis.ipynb`: Full notebook with simulation, clustering, validation
- ✅ Cluster plots and trajectory comparisons
- ✅ Demographic fairness assessment
- ✅ Clear documentation and metrics

---

## Tools & Libraries

- **Python 3.10**
- **Pandas**, **NumPy** – data handling
- **Scikit-learn** – clustering & metrics
- **Matplotlib**, **Seaborn** – visualization
- **Jupyter Notebook** – development and exploration


