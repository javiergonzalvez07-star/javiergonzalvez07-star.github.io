---
title: "F1 Pit-Stop Strategy: Simulation + Real-Data Validation"
date: 2026-02-04
draft: false
tags: ["Python", "Simulation", "NumPy", "pandas", "Matplotlib", "F1 Strategy"]
summary: "A simplified race simulator to reason about pit-stop strategy (tire degradation vs pit-loss), plus a validation notebook using real modern F1 race data."
featuredImage: "/images/projects/f1.png"
---

## Overview
This project studies **pit-stop strategy in Formula 1** by combining:
1) a **simplified physics-based race simulator**, and  
2) a **data validation step** using historical F1 race data.

The focus is **interpretability and reasoning**: understanding why an “optimal” number of stops emerges in theory, and why real racing often favors more conservative strategies.
<img src="/images/projects/f1.png"
     alt="Mapa de calor"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">
---

## Goals
Build an interpretable model to reason about the trade-off between:
- **tire degradation** (loss of grip across a stint)
- **pit-stop time loss**
- the **optimal number of stops** for a given race

…and then **validate** the conclusions against real-world data.

---

## What I built

### 1) Physics-based simulation (`simulación_f1.ipynb`)
- A simple 1D lap + race model with acceleration/braking/curves
- Simplified circuit representation
- Explicit tire degradation modeled as a reduction in **grip (μ)** across the stint
- Sensitivity analysis + search for the stop count that minimizes total race time

> The goal is to understand strategy trends, not to replicate full telemetry.

### 2) Data validation (`validación_datos.ipynb`)
- Cleaning and unifying historical F1 datasets
- Filtering to a **modern era** for comparability
- Estimating average pit-stop time empirically
- Comparing observed strategies (e.g., top-3) vs model expectations
- Explaining discrepancies between simulation and reality with clear reasoning

---

## Key takeaway
Even if the model shows a clear theoretical optimum, real competition introduces constraints (traffic, safety cars, risk, track position, etc.) that often push teams toward more conservative strategies.

This project demonstrates how combining **modeling + validation** gives a more realistic view than either one alone.

---

## Tech stack
- Python
- NumPy, pandas, matplotlib
- Jupyter Notebook

---

## Repo
- GitHub: https://github.com/javiergonzalvez07-star/f1
