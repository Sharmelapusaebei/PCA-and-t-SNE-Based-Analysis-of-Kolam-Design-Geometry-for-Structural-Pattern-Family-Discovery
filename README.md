# Kolam Design Geometry Analysis Workbench

An interactive web-based unsupervised machine learning workbench and exploratory simulator designed to analyze and cluster geometric patterns in traditional South Indian kolam designs.

This repository accompanies the IEEE technical report titled "PCA and t-SNE-Based Analysis of Kolam Design Geometry for Structural Pattern-Family Discovery" (SIH26044).

---

## 🔬 Methodology & Pipeline Architecture

* Dataset & Preprocessing (N = 50): Curated corpus of 50 digital pattern images split evenly across two structural families (n = 25 each):
  * Family A: Pulli Kolam (grid-matrix based).
  * Family B: Sikku Kolam (continuous closed-loop weave).
* Pipeline: Grayscale conversion, adaptive binarization, morphological thinning, and canonical bounding-box centering.
* Geometric Feature Extraction : Computes multi-dimensional structural descriptors including Pulli Density (ρ_p), Euler Number (χ = C - H), Mean Stroke Curvature (κ̄), Rotational/Reflectional Symmetry (Sᵣ, S_θ), and Stroke Tortuosity (τ), followed by z-score standardization.
* Dimensionality Reduction:
  * PCA (Linear Projection): Captures global variance across leading principal components (PC₁, PC₂).
  * t-SNE (Non-Linear Manifold Learning): Preserves local neighborhood topology via Kullback–Leibler divergence minimization.
* Quantitative Validation: Internal cluster validation evaluated via Silhouette Score (s) and Davies–Bouldin Index (DBI).

---
