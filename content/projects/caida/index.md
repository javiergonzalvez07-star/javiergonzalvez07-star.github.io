---
title: "Free Fall with Linear Drag (Terminal Velocity)"
date: 2026-01-18
draft: false
tags: ["Python", "Physics", "Numerical Simulation", "ODEs", "Matplotlib"]
summary: "A simple physics simulation of vertical free fall with linear drag, showing how terminal velocity emerges and matching it against the theoretical value."
featuredImage: "/images/projects/Caida.png"
---

## Overview
This project is a small, physics-driven Python simulation of **vertical free fall under gravity** including a **linear drag model**.  
The goal is to study how **terminal velocity** appears and to compare the **theoretical** terminal velocity with the **numerical** result from a time-integration simulation. 

<img src="/images/projects/Caida.png"
     alt="Mapa de calor"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">

## What I built
- A **step-by-step time integration** (discrete simulation over small `dt`) of the motion equation with linear drag.
- A comparison between:
  - **theoretical terminal velocity**
  - **terminal velocity estimated from the simulation**
- Small parameter studies to see the effect of:
  - **initial height**
  - **drag coefficient** 

## Why it matters
Even with a simple model, this project demonstrates the full workflow of **turning physics into code**:
- define assumptions (linear drag),
- simulate dynamics numerically,
- validate results against theory,
- and interpret the behavior (why/when terminal velocity is reached). 

## Tech stack
- Python
- Jupyter Notebook
- matplotlib 

## Files
- `caída_libre_con_rozamiento.ipynb` — full project notebook (model + simulation + plots) 

## Links
- GitHub repository: https://github.com/javiergonzalvez07-star/
