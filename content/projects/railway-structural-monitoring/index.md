---
title: "Railway Structural Health Monitoring System"
description: "Low-cost railway structural monitoring prototype using sensors, Python data processing, an interpretable damage function and a Streamlit dashboard."
date: 2026-06-12
draft: false
tags: ["Python", "Streamlit", "Sensors", "ESP32", "Data Processing", "Machine Learning", "Structural Health Monitoring"]
summary: "Low-cost railway monitoring prototype that turns physical sensor data into interpretable damage indicators and an interactive dashboard."
featuredImage: "/images/projects/railway-monitoring/railway-hero.png"
mathjax: true
---

## Overview

This project develops a first functional version of a **railway structural health monitoring system**. Rather than only connecting sensors, the team built an end-to-end pipeline that transforms physical measurements into interpretable information for predictive maintenance.

The prototype measures acceleration, vibration, temperature and piezoelectric signals with an ESP32-based device. The readings are stored in CSV files, cleaned and normalized in Python, combined through an interpretable damage function, and presented in an interactive Streamlit dashboard.

<figure style="margin: 1.5rem auto 2rem; max-width: 900px;">
  <img src="/images/projects/railway-monitoring/railway-hero.png"
       alt="Railway structural monitoring project overview"
       loading="eager"
       style="width: 100%; display: block; border-radius: 14px;">
  <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
    End-to-end prototype for railway structural health monitoring.
  </figcaption>
</figure>

<div style="display: flex; flex-wrap: wrap; gap: 0.75rem; margin: 1.25rem 0 2rem;">
  <a class="btn btn-primary" href="https://github.com/javiergonzalvez07-star/Proyecto1" target="_blank" rel="noopener noreferrer">View repository</a>
  <a class="btn btn-outline-primary" href="/#projects">Back to projects</a>
</div>

This was a group project for **Proyecto I** in the Double Degree in Mathematical Engineering and Physics at Universidad CEU San Pablo, developed by Javier Gonzalvez, Pablo Prada, Miguel Rodriguez, Santiago Hernandez and Ricardo Mazariegos.

---

## Problem

Railway tracks are exposed to repeated dynamic loads, vibrations, temperature changes, fatigue and mechanical events. Frequent inspections can be costly, while raw measurements alone do not provide the clear information required to support predictive maintenance.

The challenge was to design a low-cost prototype capable of collecting physical data and converting it into simple indicators that could help describe the condition of a monitored track section.

---

## Solution

The solution is a modular monitoring pipeline:

- sensor-based acquisition of acceleration, temperature and piezoelectric signals
- CSV storage for raw and processed measurements
- cleaning, filtering, interpolation and normalization in Python
- an interpretable weighted damage function
- an interactive Streamlit dashboard for condition monitoring and alerts

Its central purpose is to move from raw signals to understandable outputs such as **instantaneous damage, accumulated damage, remaining life and track condition**.

---

## System Architecture

<figure style="margin: 1.5rem auto; max-width: 900px;">
  <img src="/images/projects/railway-monitoring/railway-architecture.png"
       alt="System architecture from sensors to dashboard"
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
  <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
    Complete pipeline from physical measurements to interpretable dashboard indicators.
  </figcaption>
</figure>

<div style="overflow-x: auto; margin: 1.25rem 0;">
  <div style="min-width: 760px; display: flex; align-items: stretch; gap: 0.5rem; text-align: center;">
    <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Sensors</strong><br><small>Physical signals</small></div>
    <div style="align-self: center;">&rarr;</div>
    <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>ESP32</strong><br><small>Acquisition</small></div>
    <div style="align-self: center;">&rarr;</div>
    <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Raw CSV</strong><br><small>Storage</small></div>
    <div style="align-self: center;">&rarr;</div>
    <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Python</strong><br><small>Processing</small></div>
    <div style="align-self: center;">&rarr;</div>
    <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Damage</strong><br><small>Model</small></div>
    <div style="align-self: center;">&rarr;</div>
    <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Dashboard</strong><br><small>Insights</small></div>
  </div>
</div>

1. **Sensors:** measure acceleration, temperature and piezoelectric response.
2. **ESP32:** collects measurements from the physical device.
3. **Raw CSV:** provides simple, portable initial storage.
4. **Python processing:** cleans, filters, interpolates and normalizes the data.
5. **Final dataset:** stores consistent features ready for analysis.
6. **Damage function:** combines the relevant variables in a weighted model.
7. **Streamlit dashboard:** displays signals, condition indicators and alerts.

---

## Hardware

The hardware was intentionally based on accessible, low-cost components. The objective was not to build an industrial device, but to validate a complete prototype connecting real measurements with mathematical and visual monitoring.

<figure style="margin: 1.5rem auto; max-width: 800px;">
  <img src="/images/projects/railway-monitoring/railway-hardware-prototype.jpg"
       alt="Physical prototype with ESP32 and sensors"
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
  <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
    Low-cost prototype based on ESP32, vibration, temperature and piezoelectric sensing.
  </figcaption>
</figure>

| Component | Role |
|---|---|
| **ESP32** | Main microcontroller and acquisition device |
| **MPU6050** | Acceleration and vibration measurements |
| **MAX6675 + K-type thermocouple** | Temperature measurement |
| **Piezoelectric sensor** | Detection of impacts and mechanical events |
| **Breadboard and wiring** | Prototype connections |
| **3D-printed enclosure** | Physical protection and mounting concept |

---

## Data Processing

Real sensor measurements introduced noise, offsets, missing values and invalid readings. A robust processing pipeline therefore became essential:

- temporal sorting
- duplicate removal
- physical range filtering
- missing-value interpolation
- acceleration filtering using the Fourier transform
- derived feature creation
- min-max normalization

The main derived variables were:

- **Dynamic acceleration:** difference from baseline acceleration.
- **Piezo proxy:** difference from the baseline piezoelectric or strain signal.
- **Temperature deviation:** difference from a reference temperature.

---

## Interpretable Damage Function

The dashboard does more than display raw signals. It calculates an aggregated damage metric:

<div style="padding: 1.5rem; margin: 1.25rem auto; max-width: 620px; text-align: center; border: 1px solid rgba(127,127,127,.3); border-radius: 14px; font-size: 1.6rem;">
  <strong>D = 0.45P + 0.10T + 0.45A</strong>
</div>

<figure style="margin: 1.5rem auto; max-width: 800px;">
  <img src="/images/projects/railway-monitoring/railway-damage-function.png"
       alt="Interpretable damage function with piezoelectric temperature and acceleration weights"
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
  <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
    Interpretable weighted model combining piezoelectric response, temperature deviation and dynamic acceleration.
  </figcaption>
</figure>

- **P:** normalized piezoelectric contribution
- **T:** normalized temperature deviation
- **A:** normalized dynamic acceleration

Logistic regression and random forest models were applied to an external structural-monitoring dataset to compare the relative importance of the variables. The final weights were then adjusted according to the physical meaning of each signal in the railway context.

The goal of machine learning was not to create a black-box predictor, but to guide the construction of a function that remained understandable and easy to communicate.

---

## Streamlit Dashboard

The dashboard turns the mathematical model into an understandable monitoring interface. It includes:

- individual device and general track views
- instantaneous and accumulated damage
- estimated remaining life
- **Normal**, **Attention** and **Alert** states
- temporal signal charts
- data updates during the demonstration
- a train-passage simulator

It allows a user to inspect the current device state, follow the evolution of the signals and understand the estimated condition of the monitored section.

<figure style="margin: 1.5rem auto 2rem; max-width: 900px;">
  <img src="/images/projects/railway-monitoring/railway-dashboard-individual.png"
       alt="Individual Streamlit dashboard for the monitored device"
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
  <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
    Individual device view showing live indicators, damage and remaining life.
  </figcaption>
</figure>

---

## Demo Simulator

Because validation on a real railway track was not possible during the project, the team created a synthetic demonstration simulator. It generates train-passage events, increases vibration and piezoelectric activity, and updates the CSV file so the Streamlit dashboard can react during the presentation.

The simulator demonstrates the complete data flow and interface behavior. It does **not** validate real structural damage.

---

## Tech Stack

- **Data and modeling:** Python, pandas, NumPy, SciPy, `scipy.fft`, scikit-learn
- **Dashboard:** Streamlit, Plotly
- **Hardware:** ESP32, MPU6050, MAX6675, K-type thermocouple, piezoelectric sensor
- **Storage and collaboration:** CSV, GitHub

---

## Challenges and Lessons

- The original scope was reduced to one modular prototype.
- No labeled dataset of real railway deterioration was available.
- Low-cost sensors introduced noise, offsets and erroneous readings.
- A reliable cleaning pipeline was required before meaningful visualization.
- The live demonstration needed a continuous data source.
- Working with physical hardware proved very different from using clean datasets.

One of the main lessons was that **real sensor data is messy**. Data cleaning and normalization became as important as the dashboard itself because the quality of every final indicator depends on the quality of the processed measurements.

---

## Limitations

- This is not an industrially validated monitoring system.
- The damage function has not been calibrated with measurements from deteriorated railway tracks.
- The external dataset does not perfectly reproduce the railway use case.
- Low-cost sensors can introduce significant measurement noise.
- Physical mounting influences signal quality.
- The simulator demonstrates the pipeline rather than validating real damage.

---

## Future Work

- validate the system with real track data or a controlled experimental test bench
- distribute multiple devices across different track sections
- add wireless communication and a central server
- improve the enclosure and mechanical attachment
- calibrate the damage function experimentally
- reduce consumption with ESP32 deep sleep
- explore piezoelectric energy harvesting and solar assistance
- train more advanced models once sufficient project-specific data is available

---

## Results and Impact

The final result is a working prototype integrating hardware, data processing, mathematical modeling and visualization. Its main value is the complete end-to-end pipeline: from physical sensor readings to interpretable indicators for railway structural monitoring.

---

## My Contribution

My work focused on connecting the mathematical and software parts of the group project: data cleaning, feature engineering, damage-function design, model interpretation, dashboard development and demo preparation.

I also worked on making the system understandable to a non-technical user by turning raw measurements into visual indicators such as accumulated damage, remaining life and alert states.

---

## Links

- **Repository:** https://github.com/javiergonzalvez07-star/Proyecto1
- **Back to portfolio projects:** [Projects](/#projects)
