---
title: "Transient Thermal Response of a Paraffin-Modified Brick: Experimental Comparison and Reduced-Order Modelling"
shortTitle: "Paraffin-modified brick"
date: 2026-05-04
draft: false
description: "An experimental comparison of conventional and paraffin-filled bricks, supported by a reduced-order model of transient thermal buffering."
summary: "A controlled heating experiment and two-node model showed a delayed upper-face temperature rise with paraffin, while final temperature increments remained similar."
area: "Experimental Physics · Thermal Modelling"
image: "/images/research/thermal/aligned-temperature.png"
imageAlt: "Experimental upper-surface temperature curves for the reference and paraffin-modified bricks"
badges: ["Thermal Physics", "K-type Thermocouples", "Data Cleaning", "Reduced-order Modelling"]
glance:
  - label: "Experimental system"
    value: "Two hollow ceramic bricks"
  - label: "Instrumentation"
    value: "K-type thermocouples + MAX6675"
  - label: "Heating data"
    value: "1,858 reference · 1,276 PCM samples"
  - label: "Aligned comparison"
    value: "1,150 s from 36.25 °C"
---

## The problem

Phase change materials can absorb energy as latent heat, potentially delaying temperature peaks without active power. This study asked a precise question: **does filling a hollow ceramic brick with paraffin change the characteristic time scale of heat reaching its opposite face?** It did not treat the material as a permanent insulator or attempt to infer unmeasured material properties.

## Research approach

<div class="process-grid" aria-label="Research workflow">
  <div class="process-step"><b>01 · Prepare</b>Fill one brick with 1 kg of commercial paraffin and seal both samples.</div>
  <div class="process-step"><b>02 · Measure</b>Heat from below and record lower- and upper-face temperatures.</div>
  <div class="process-step"><b>03 · Align</b>Clean acquisition errors and compare from a common initial temperature.</div>
  <div class="process-step"><b>04 · Model</b>Test the thermal-inertia interpretation with a two-node model.</div>
</div>

### Experimental setup

The reference and PCM-modified bricks were heated from one side under similar conditions. Expanded polystyrene covered the lateral sides and openings to reduce lateral losses and encourage a predominantly vertical heat path. Two K-type thermocouples connected to MAX6675 modules measured the heated region and transmitted upper-surface response.

The paraffin had a supplier-specified melting range of approximately **56–58 °C**; no independent DSC measurement was available, so that value is a commercial reference rather than a measured property of the sample.

## Modelling and data analysis

Preprocessing detected the real CSV header, removed startup lines, corrected time resets and sensor-label issues, selected the heating stage and aligned both experiments at an upper-surface temperature of approximately **36.25 °C**. The comparison used:

<div class="equation"><strong>ΔT<sub>upper</sub>(t) = T<sub>upper</sub>(t) − T<sub>upper</sub>(0)</strong></div>

The phenomenological two-node model represented the brick's internal state and measured upper face. For the PCM case, a temperature-dependent inertia factor approximated the phase-change effect:

<div class="equation"><strong>F<sub>PCM</sub>(T) = 1 + A exp[−½((T − T<sub>m</sub>)/σ)²]</strong></div>

Here, the fitted transition temperature is an **effective lumped-model parameter**, not a measurement of paraffin's melting point.

## Key results

<div class="result-callout"><div><strong>Delayed response</strong>The PCM upper face remained near its initial temperature for longer.</div><div><strong>7.75 °C vs 8.25 °C</strong>Final upper-face increments over the same 1,150 s window were similar.</div><div><strong>Transient, not permanent</strong>The evidence supports delayed transmission, not improved steady-state insulation.</div></div>

<figure class="research-figure">
  <img src="/images/research/thermal/aligned-temperature.png" alt="Aligned upper-surface temperatures showing an earlier rise for the reference brick and a delayed rise for the PCM brick" loading="lazy">
  <figcaption>The PCM-modified brick stayed near its initial upper-face temperature longer before converging toward the reference response.</figcaption>
</figure>

- The conventional brick transmitted the temperature rise earlier; the PCM brick showed a clear initial and intermediate delay.
- Final increments over the common window were similar: **7.75 °C** for the reference and **8.25 °C** for the PCM brick. The evidence therefore supports buffering in time, not permanent insulation.
- Modelled final increments were **7.98 °C** for the reference and **6.42 °C** for the PCM brick. Their respective curve RMSE values were **2.69 °C** and **0.64 °C**. The larger reference error reflects its rapid early rise, which the two-node model did not reproduce well; these errors assess curve agreement, not material properties.

<figure class="research-figure">
  <img src="/images/research/thermal/model-comparison.png" alt="Comparison of experimental and reduced-order model temperature increments for both bricks" loading="lazy">
  <figcaption>The reduced-order model supports the thermal-inertia interpretation; it is not a calibrated three-dimensional simulation.</figcaption>
</figure>

## Conclusions and limitations

The experiment is consistent with paraffin acting as a **transient thermal buffer**: it redistributes heat transmission over time rather than preventing it. Hollow-brick geometry, non-uniform filling, sensor contact, finite heating power and residual losses limit quantitative inference. The work did not independently quantify latent heat, solve the complete three-dimensional heat equation or validate other geometries and boundary conditions.

Future work should add DSC characterization, repeated trials with uncertainty estimates, controlled heating power, internal temperature sensing and a geometry-resolved model.

## Skills demonstrated

<div class="skills-grid"><div class="skill-chip">Experimental design</div><div class="skill-chip">Sensor instrumentation</div><div class="skill-chip">Data preprocessing</div><div class="skill-chip">Thermal modelling</div><div class="skill-chip">Model interpretation</div><div class="skill-chip">Uncertainty awareness</div><div class="skill-chip">Scientific visualization</div><div class="skill-chip">Technical writing</div></div>

## Related work

The sensor acquisition and interpretable modelling workflow connects directly with the [Railway Structural Health Monitoring System](/projects/railway-structural-monitoring/), where physical measurements are also transformed into decision-oriented indicators.
