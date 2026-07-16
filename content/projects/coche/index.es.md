---
title: "Análisis de seguridad vial mediante simulación de fricción y frenado"
date: 2026-01-29
draft: false
tags: ["Python", "Physics", "Simulation", "Road Safety", "Numerical Modeling"]
summary: "Un estudio de simulación basado en la física que analiza cómo la fricción en la carretera afecta la distancia de frenado y el riesgo de colisión en escenarios de conducción reales."
featuredImage: "/images/projects/seguridad_vial.png"
---

## Descripción general
Este proyecto utiliza **simulación numérica basada en la física** para estudiar el impacto de la **fricción de la carretera** en la distancia de frenado y la seguridad del vehículo.
Al modelar la dinámica de frenado en diferentes condiciones de la superficie, el proyecto conecta **la física teórica** con **implicaciones para la seguridad vial en el mundo real**.

<img src="/images/projects/seguridad_vial.png"
     alt="Visualización de la simulación de frenado y seguridad vial"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">

---

## Problema
Las condiciones de la carretera (asfalto mojado, superficies desgastadas, materiales de baja fricción) afectan significativamente el rendimiento de frenado.
Sin embargo, estos efectos a menudo se subestiman en la conducción diaria.

El objetivo de este proyecto es **cuantificar** cómo influyen directamente los cambios en el coeficiente de fricción:
- distancia de frenado,
- tiempo de frenado,
- probabilidad de colisión.

---

## Lo que construí
- Un modelo físico simplificado de frenado de vehículos basado en la mecánica newtoniana.
- Simulaciones numéricas que comparan la distancia de frenado para diferentes coeficientes de fricción.
- Análisis por escenarios para estudiar los márgenes de seguridad en distintas condiciones de la carretera.
- Visualizaciones claras que vinculan los valores de fricción con resultados de seguridad reales.

---

## Ideas clave
- La distancia de frenado se escala **no linealmente** con pérdidas por fricción.
- Pequeñas reducciones en la fricción pueden reducir drásticamente los márgenes de seguridad.
- La calidad de la infraestructura y el estado del vehículo son igualmente importantes para la seguridad.

---

## Por qué es importante
Este proyecto destaca cómo **las decisiones de ingeniería y las condiciones materiales** afectan directamente la seguridad pública.
Demuestra el valor de la simulación como herramienta para:
- análisis de seguridad,
- evaluación de infraestructura,
- y comunicación de riesgos.

El trabajo se centra en la **interpretabilidad y el razonamiento**, no en modelos innecesariamente complejos.

---

## Tecnologías
- Python
- NumPy
- matplotlib
- Jupyter Notebook

---

## Archivos
- Cuadernos de simulación que modelan la dinámica de frenado y escenarios de fricción.

---

## Enlaces
- Repositorio GitHub: https://github.com/javiergonzalvez07-star/modelado-friccion-seguridad-vial
