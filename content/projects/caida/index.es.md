---
title: "Caída libre con rozamiento lineal (velocidad terminal)"
date: 2026-01-18
draft: false
tags: ["Python", "Physics", "Numerical Simulation", "ODEs", "Matplotlib"]
summary: "Una simulación física simple de caída libre vertical con resistencia lineal, que muestra cómo surge la velocidad terminal y la compara con el valor teórico."
featuredImage: "/images/projects/Caida.png"
---

## Descripción general
Este proyecto es una simulación física en Python de la **caída libre vertical bajo la gravedad** que incluye un **modelo de rozamiento lineal**.
El objetivo es estudiar cómo aparece la **velocidad terminal** y comparar la velocidad terminal **teórica** con el resultado **numérico** de una simulación de integración temporal.

<img src="/images/projects/Caida.png"
     alt="Simulación de caída libre con rozamiento lineal"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">

## Lo que construí
- Una **integración temporal paso a paso** (simulación discreta con un `dt` pequeño) de la ecuación de movimiento con rozamiento lineal.
- Una comparación entre:
 - **velocidad terminal teórica**
 - **velocidad terminal estimada mediante la simulación**
- Pequeños estudios de parámetros para ver el efecto de:
 - **altura inicial**
 - **coeficiente de arrastre**

## Por qué es importante
Incluso con un modelo simple, este proyecto demuestra el flujo de trabajo completo para **convertir la física en código**:
- definir supuestos (rozamiento lineal),
- simular la dinámica numéricamente,
- validar los resultados frente a la teoría,
- interpretar el comportamiento y cuándo y por qué se alcanza la velocidad terminal.

## Tecnologías
- Python
- Jupyter Notebook
- matplotlib

## Archivos
- `caída_libre_con_rozamiento.ipynb` — cuaderno de proyecto completo (modelo + simulación + gráficos)

## Enlaces
- Repositorio GitHub: https://github.com/javiergonzalvez07-star/
