---
title: "Randomness vs Chaos: Logistic Map & Double Pendulum"
date: 2026-01-20
draft: false
tags: ["Python", "Physics", "Chaos Theory", "Nonlinear Dynamics", "Simulation"]
summary: "A comparative study between random processes and deterministic chaos using the logistic map and a double pendulum simulation."
featuredImage: "/images/projects/caos.png"
---

## Overview
This project explores the **difference between randomness and deterministic chaos** through two classical systems:
- the **logistic map**, a simple nonlinear discrete model,
- and the **double pendulum**, a deterministic mechanical system with chaotic behavior.

Although both systems can produce unpredictable results, their **origin and structure are fundamentally different**.

<img src="/images/projects/caos.png"
     alt="Mapa de calor"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">
---

## What I built
- A numerical exploration of the **logistic map**, analyzing how small changes in initial conditions affect long-term behavior.
- A **double pendulum simulation**, showing extreme sensitivity to initial conditions despite being governed by deterministic equations.
- Visual comparisons (time series and trajectories) to highlight similarities and differences between chaos and randomness.

---

## Key idea
The project shows that:
- **Randomness** comes from stochastic processes with no underlying determinism.
- **Chaos** arises from deterministic systems that are highly sensitive to initial conditions.

This distinction is crucial in physics, engineering, and data analysis, where chaotic systems can appear random despite being fully deterministic.

---

## Why it matters
Understanding the difference between chaos and randomness is essential when:
- interpreting noisy data,
- modeling physical systems,
- or deciding whether unpredictability can be reduced with better models or measurements.

This project focuses on **conceptual clarity and interpretation**, not just simulation.  

---

## Tech stack
- Python
- NumPy
- matplotlib
- Jupyter Notebook

---

## Files
- `mapa_logistico.ipynb` — logistic map analysis  
- `pendulo_doble.ipynb` — double pendulum simulation  

---

## Links
- GitHub repository: https://github.com/javiergonzalvez07-star/Aleatoriedad-vs-Caos
