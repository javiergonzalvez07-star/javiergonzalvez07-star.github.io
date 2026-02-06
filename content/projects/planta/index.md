---
title: "Smart Plant Monitoring: IoT Data Collection in Real Conditions"
date: 2026-01-31
draft: false
tags: ["IoT", "ESP32", "Sensors", "Data Collection", "Python", "Real-World Data"]
summary: "An IoT project to monitor domestic plant conditions, focused on the challenges of collecting real sensor data in non-controlled environments."
featuredImage: "/images/projects/planta.png"
---

## Overview
This project is an **IoT-based plant monitoring system** designed to address a simple but real problem:  
**understanding and improving the care of domestic plants**.

Instead of working with clean, ready-made datasets, the core challenge here was **collecting data from real hardware under non-controlled conditions**.

---
<img src="/images/projects/planta.png"
     alt="Mapa de calor"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">

## Problem
Domestic plant care is often based on intuition rather than data:
- How dry is the soil, really?
- How do temperature and humidity affect watering needs?
- Can we detect patterns over time instead of reacting too late?

The goal of this project was to **measure and record relevant variables** to start answering these questions with data.

---

## System & Data Collection
- **ESP32 microcontroller**
- **Soil moisture sensor**
- **Environmental sensors** (temperature / humidity)
- Periodic logging of sensor data to CSV

The system was deployed in a real domestic environment, not a lab setup.

---

## What went wrong (and what I learned)
Not everything worked perfectly — and that was the point.

- Sensor readings were **noisy and sometimes inconsistent**
- Hardware issues (connections, moisture, power stability) affected data quality
- Real-world conditions are messy and unpredictable

This project became a hands-on lesson in:
- debugging hardware-software interactions,
- validating sensor data instead of blindly trusting it,
- and adapting the workflow when conditions are not controlled.

---

## Data analysis
Using Python, the collected data was:
- cleaned and explored,
- visualized to identify trends and anomalies,
- analyzed to understand soil moisture dynamics over time.

The focus was on **interpretation**, not just plotting numbers.

---

## Future extensions
This project is intentionally a **first iteration**. Planned extensions include:
- additional sensors,
- longer-term data collection,
- and a **predictive model** to recommend optimal watering schedules.

The idea is to progressively move from **monitoring → understanding → prediction**.

---

## Why this project matters
This project reflects how real engineering work often looks:
- imperfect data,
- unexpected problems,
- and the need to adapt solutions in real time.

The main objective was not technical perfection, but **solving a real-world problem with practical constraints**.

---

## Tech stack
- ESP32 (Arduino)
- Python
- pandas, matplotlib
- CSV-based data logging

---

## Links
- GitHub repository: https://github.com/javiergonzalvez07-star/Planta
