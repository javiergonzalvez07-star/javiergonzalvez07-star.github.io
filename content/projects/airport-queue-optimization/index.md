---
title: "Airport Queue Optimization System"
date: 2026-05-19
draft: false
tags: ["Python", "pandas", "NumPy", "Streamlit", "Queueing", "Simulation", "YOLO", "Operations Research", "Data Analysis"]
summary: "Prototype for airport passenger flow simulation and decision support, combining queueing theory, simulated CSV data and operational recommendations."
featuredImage: "/images/projects/airport_queue_architecture.png"
---

## Overview
This project prototyped a **decision-support system for airport queue management** using simulated passenger flow data, simplified queueing models and an interactive Streamlit dashboard.

I developed the analytical workflow as part of the Applied Technical Projects Club, contributing to the simulation design, queueing modeling, CSV data pipeline, technical documentation and the project presentation.

<img src="/images/projects/airport_queue_architecture.png"
     alt="Airport Queue Optimization System architecture"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Problem
Airports face variable passenger arrivals, distributed service capacity and multiple service zones. The prototype focuses on estimating key operational metrics for:

- **check-in**
- **bag drop**
- **security**
- **passport control**
- **boarding**

The goal was to support operational decisions with a **simulation-based validation** of how queueing and capacity choices affect wait time and bottleneck events.

---

## Approach
The solution combines:

- **CSV-based data processing** to ingest synthetic passenger flow and zone measurements
- **queueing theory** models for service zones and saturation estimation
- **scenario comparison** between a base case without recommendations and a controlled case with operational guidance
- **YOLO / YOLOv8 proof of concept** for synthetic video-based people counting
- **Streamlit dashboard** to summarize metrics and support decisions

In the prototype, I built the core Python pipeline with `pandas` and `NumPy`, then translated model outputs into readable operational indicators.

<img src="/images/projects/airport_queue_yolo.png"
     alt="YOLO detection proof of concept for airport passenger counting"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## System Architecture
The model is intentionally modular:

1. **Synthetic data generation** for passenger arrivals and service times
2. **CSV ingestion** and preprocessing with Python
3. **Queueing model** for each airport zone
4. **Saturation and wait time estimation** for the current and recommended scenarios
5. **Streamlit dashboard** for operational visualization and decision support

This architecture was designed to keep the proof of concept practical while retaining clear separation between simulation, analysis and visualization.

<img src="/images/projects/airport_queue_system.png"
     alt="Conceptual system architecture for airport queue optimization"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Results
The simulation highlighted a meaningful difference between the baseline and the recommendation-enabled scenario.

- **Total accumulated wait** decreased from **19.09 min to 5.32 min**
- **Relative improvement** in aggregate wait: **approximately 72.1%**
- **Peak aggregated wait** dropped from **1.70 min to 0.75 min**
- **Estimated bottleneck events** went from **56 to 52**

These results come from the prototype simulation and should be understood as a **proof of concept**, not an industrial validation.

<img src="/images/projects/airport_queue_results.png"
     alt="Result comparison for airport queue optimization simulation"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Dashboard
A Streamlit dashboard was used to present the main operational indicators, compare base vs recommendation scenarios, and make the simulation outputs accessible for decision makers.

<img src="/images/projects/airport_queue_dashboard.png"
     alt="Streamlit dashboard for airport queue optimization"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Technologies
- Python
- pandas, NumPy
- CSV processing
- Streamlit
- Queueing theory and operations research concepts
- YOLO / YOLOv8
- OpenCV
- Data analysis and visualization

---

## Limitations
- The project is a **simulation prototype** and does not represent a fully validated airport deployment.
- Results are based on **synthetic or simulated inputs**, not live operational data.
- The YOLO/YOLOv8 element is a **proof of concept** for passenger counting from synthetic footage.

---

## Future Work
Potential next steps include:

- validating the model with real airport throughput data
- refining the service-zone model with variable service distributions
- adding a live data ingestion layer for real-time decision support
- extending the prototype to support alternative staffing and queue routing policies

---

## Links
- Club project page: https://club-proyectos-tecnicos.github.io/projects/airport-queue-optimization/
- Repository: TODO (add GitHub repo link when available)
- Documentation/memory PDF: TODO
