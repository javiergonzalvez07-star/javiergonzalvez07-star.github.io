---
title: "Estrategia de parada en boxes de F1: simulación + validación de datos reales"
date: 2026-02-04
draft: false
tags: ["Python", "Simulation", "NumPy", "pandas", "Matplotlib", "F1 Strategy"]
summary: "Un simulador de carreras simplificado para razonar sobre la estrategia de parada en boxes (degradación de neumáticos frente a pérdida en boxes), además de un cuaderno de validación que utiliza datos reales y modernos de las carreras de F1."
featuredImage: "/images/projects/f1.png"
---

## Descripción general
Este proyecto estudia **la estrategia de paradas en boxes en la Fórmula 1** combinando:
1) un **simulador de carreras basado en física simplificada** y
2) un **paso de validación de datos** utilizando datos históricos de carreras de F1.

El enfoque es **interpretabilidad y razonamiento**: comprender por qué surge un número "óptimo" de paradas en teoría, y por qué las carreras reales a menudo favorecen estrategias más conservadoras.
<img src="/images/projects/f1.png"
     alt="Simulación de estrategias de paradas en boxes de Fórmula 1"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">

---

## Objetivos
Construir un modelo interpretable para razonar sobre la compensación entre:
- **degradación de los neumáticos** (pérdida de agarre durante un stint)
- **tiempo perdido en la parada en boxes**
- el **número óptimo de paradas** para una carrera determinada

...y luego **validar** las conclusiones con datos del mundo real.

---

## Lo que construí

### 1) Simulación basada en la física (`simulación_f1.ipynb`)
- un modelo sencillo unidimensional de vuelta y carrera con curvas de aceleración y frenado
- Representación de circuito simplificada.
- degradación explícita de los neumáticos modelizada como una reducción del **agarre (μ)** a lo largo de cada stint
- análisis de sensibilidad y búsqueda del número de paradas que minimiza el tiempo total de carrera

> El objetivo es comprender las tendencias estratégicas, no replicar la telemetría completa.

### 2) Validación de datos (`validación_datos.ipynb`)
- Limpieza y unificación de conjuntos de datos históricos F1
- Filtrado a una **era moderna** para comparabilidad
- Estimación empírica del tiempo medio de parada en boxes
- Comparación de las estrategias observadas (por ejemplo, las tres primeras) con las expectativas del modelo
- Explicación razonada de las discrepancias entre la simulación y la realidad

---

## Conclusión clave
Incluso si el modelo muestra un óptimo teórico claro, la competencia real introduce limitaciones (tráfico, coches de seguridad, riesgo, posición en la pista, etc.) que a menudo empujan a los equipos hacia estrategias más conservadoras.

Este proyecto demuestra cómo la combinación de **modelado + validación** proporciona una visión más realista que cualquiera de los dos por separado.

---

## Tecnologías
- Python
- NumPy, pandas, matplotlib
- Jupyter Notebook

---

## Repositorio
- GitHub: https://github.com/javiergonzalvez07-star/f1
