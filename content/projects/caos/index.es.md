---
title: "Azar frente a caos: mapa logístico y péndulo doble"
date: 2026-01-20
draft: false
tags: ["Python", "Physics", "Chaos Theory", "Nonlinear Dynamics", "Simulation"]
summary: "Un estudio comparativo entre procesos aleatorios y caos determinista utilizando el mapa logístico y una simulación de doble péndulo."
featuredImage: "/images/projects/caos.png"
---

## Descripción general
Este proyecto explora la **diferencia entre aleatoriedad y caos determinista** a través de dos sistemas clásicos:
- el **mapa logístico**, un modelo discreto no lineal simple,
- y el **doble péndulo**, un sistema mecánico determinista con comportamiento caótico.

Aunque ambos sistemas pueden producir resultados impredecibles, su **origen y estructura son fundamentalmente diferentes**.

<img src="/images/projects/caos.png"
     alt="Visualización de la simulación sobre azar y caos"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">

---

## Lo que construí
- Una exploración numérica del **mapa logístico**, analizando cómo pequeños cambios en las condiciones iniciales afectan el comportamiento a largo plazo.
- Una **simulación de doble péndulo**, mostrando extrema sensibilidad a las condiciones iniciales a pesar de estar regido por ecuaciones deterministas.
- Comparaciones visuales (series de tiempo y trayectorias) para resaltar similitudes y diferencias entre caos y aleatoriedad.

---

## Idea clave
El proyecto muestra que:
- **La aleatoriedad** proviene de procesos estocásticos sin determinismo subyacente.
- **El caos** surge de sistemas deterministas muy sensibles a las condiciones iniciales.

Esta distinción es crucial en física, ingeniería y análisis de datos, donde los sistemas caóticos pueden parecer aleatorios pese a ser completamente deterministas.

---

## Por qué es importante
Comprender la diferencia entre caos y aleatoriedad es esencial cuando:
- se interpretan datos ruidosos,
- se modelizan sistemas físicos,
- se decide si la imprevisibilidad puede reducirse con mejores modelos o mediciones.

Este proyecto se centra en **claridad e interpretación conceptual**, no solo en la simulación.

---

## Tecnologías
- Python
- NumPy
- matplotlib
- Jupyter Notebook

---

## Archivos
- `mapa_logistico.ipynb` — análisis de mapas logísticos
- `pendulo_doble.ipynb` — simulación de doble péndulo

---

## Enlaces
- GitHub: https://github.com/javiergonzalvez07-star/Aleatoriedad-vs-Caos
