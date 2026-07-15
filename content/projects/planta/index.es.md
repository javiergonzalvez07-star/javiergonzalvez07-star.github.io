---
title: "Monitorización inteligente de plantas: recopilación de datos IoT en condiciones reales"
date: 2026-01-31
draft: false
tags: ["IoT", "ESP32", "Sensors", "Data Collection", "Python", "Real-World Data"]
summary: "Proyecto IoT para monitorizar las condiciones de plantas domésticas, centrado en las dificultades de recopilar datos reales de sensores en entornos no controlados."
featuredImage: "/images/projects/planta.png"
---

## Descripción general
Este proyecto es un **sistema de monitorización de plantas basado en IoT** diseñado para abordar un problema sencillo pero real:
**comprender y mejorar el cuidado de las plantas domésticas**.

En lugar de trabajar con conjuntos de datos limpios y preparados, el reto principal fue **recopilar datos de hardware real en condiciones no controladas**.

---
<img src="/images/projects/planta.png"
     alt="Visualización de datos de la monitorización inteligente de plantas"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">

## Problema
El cuidado de las plantas domésticas a menudo se basa en la intuición más que en los datos:
- ¿Hasta qué punto está seco el suelo?
- ¿Cómo afectan la temperatura y la humedad a las necesidades de riego?
- ¿Podemos detectar patrones a lo largo del tiempo en lugar de reaccionar demasiado tarde?

El objetivo de este proyecto era **medir y registrar variables relevantes** para comenzar a responder estas preguntas con datos.

---

## Sistema y recopilación de datos
- **Microcontrolador ESP32**
- **Sensor de humedad del suelo**
- **Sensores ambientales** (temperatura/humedad)
- Registro periódico de datos del sensor en CSV

El sistema se instaló en un entorno doméstico real, no en un montaje de laboratorio.

---

## Qué salió mal (y qué aprendí)
No todo funcionó perfectamente, y ese era el punto.

- Las lecturas del sensor fueron **ruidosas y a veces inconsistentes**
- Los problemas de hardware (conexiones, humedad y estabilidad de la alimentación) afectaron a la calidad de los datos
- Las condiciones del mundo real son confusas e impredecibles

Este proyecto se convirtió en una lección práctica en:
- depuración de las interacciones entre hardware y software,
- validación de los datos de sensores en vez de confiar ciegamente en ellos,
- adaptación del flujo de trabajo cuando las condiciones no están controladas.

---

## Análisis de datos
Utilizando Python, los datos recopilados fueron:
- limpiados y explorados,
- visualizados para identificar tendencias y anomalías,
- analizados para comprender la evolución temporal de la humedad del suelo.

El trabajo se centró en la **interpretación**, no solo en representar cifras.

---

## Extensiones futuras
Este proyecto es intencionalmente una **primera iteración**. Las extensiones planificadas incluyen:
- sensores adicionales,
- recopilación de datos a más largo plazo,
- y un **modelo predictivo** para recomendar programas de riego óptimos.

La idea es pasar progresivamente de **monitorización → comprensión → predicción**.

---

## Por qué es importante este proyecto
Este proyecto refleja cómo se ve a menudo el trabajo de ingeniería real:
- datos imperfectos,
- problemas inesperados,
- necesidad de adaptar las soluciones en tiempo real.

El objetivo principal no era la perfección técnica, sino **resolver un problema del mundo real con restricciones prácticas**.

---

## Tecnologías
- ESP32 (Arduino)
- Python
- pandas, matplotlib
- Registro de datos basado en CSV

---

## Enlaces
- Repositorio GitHub: https://github.com/javiergonzalvez07-star/Planta
