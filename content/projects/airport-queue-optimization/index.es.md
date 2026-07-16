---
title: "Sistema de optimización de colas en el aeropuerto"
date: 2026-05-19
draft: false
tags: ["Python", "pandas", "NumPy", "Streamlit", "Queueing", "Simulation", "YOLO", "Operations Research", "Data Analysis"]
summary: "Prototipo para simulación de flujo de pasajeros en aeropuertos y soporte de decisiones, combinando teoría de colas, datos CSV simulados y recomendaciones operativas."
featuredImage: "/images/projects/airport_hero.jpg"
---

## Descripción general
Este proyecto creó un prototipo de **sistema de soporte de decisiones para la gestión de colas en aeropuertos** utilizando datos de flujo de pasajeros simulados, modelos de colas simplificados y un panel interactivo Streamlit.

Desarrollé el flujo de análisis como parte del Club de Proyectos Técnicos Aplicados y contribuí al diseño de la simulación, la modelización de colas, el flujo de datos CSV, la documentación técnica y la presentación del proyecto.

<img src="/images/projects/airport_hero.jpg"
     alt="Descripción general del aeropuerto"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Problema
Los aeropuertos afrontan llegadas variables de pasajeros, una capacidad de servicio distribuida y múltiples zonas de atención. El prototipo se centra en estimar métricas operativas clave para:

- **check-in**
- **depósito de equipaje**
- **seguridad**
- **control de pasaportes**
- **embarque**

El objetivo era apoyar las decisiones operativas mediante una **evaluación basada en simulación** de cómo la configuración de las colas y la capacidad afectan al tiempo de espera y a los cuellos de botella.

---

## Enfoque
La solución combina:

- **Procesamiento de datos basado en CSV** para ingerir mediciones sintéticas de zona y flujo de pasajeros
- **modelos de teoría de colas** para las zonas de servicio y la estimación de la saturación
- **comparación de escenarios** entre un caso base sin recomendaciones y un caso controlado con guía operativa
- **prueba de concepto con YOLO / YOLOv8** para contar personas en vídeo sintético
- **panel de Streamlit** para resumir métricas y apoyar las decisiones

En el prototipo construí el flujo principal de procesamiento con `pandas` y `NumPy` y convertí los resultados del modelo en indicadores operativos comprensibles.

<img src="/images/projects/aeropuerto_esquema.png"
     alt="Cuadro comparativo de resultados"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Arquitectura del sistema
El modelo es intencionalmente modular:

1. **Generación de datos sintéticos** de llegadas de pasajeros y tiempos de servicio
2. **Ingestión de CSV** y preprocesamiento con Python
3. **Modelo de cola** para cada zona del aeropuerto
4. **Estimación de saturación y tiempo de espera** para los escenarios actuales y recomendados
5. **Panel de control Streamlit** para visualización operativa y soporte de decisiones

La arquitectura mantiene una separación clara entre simulación, análisis y visualización sin complicar la prueba de concepto.

<img src="/images/projects/aeropuerto_cuellos_de_botella.png"
     alt="Eventos de cuello de botella por zona"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Resultados
La simulación destacó una diferencia significativa entre el escenario de referencia y el escenario habilitado para recomendaciones.

- **La espera acumulada total** disminuyó de **19,09 min a 5,32 min**
- **Mejora relativa** en la espera agregada: **aproximadamente 72,1%**
- **Espera máxima agregada** cayó de **1,70 min a 0,75 min**
- **Los eventos de cuello de botella estimados** pasaron de **56 a 52**

Estos resultados provienen de la simulación del prototipo y deben entenderse como una **prueba de concepto**, no como una validación industrial.

<img src="/images/projects/aeropuerto_mejora.png"
 alt="Evolución de la espera agregada a lo largo del tiempo"
style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Panel de control
Se utilizó Streamlit para presentar los principales indicadores operativos, comparar los escenarios base y recomendado y facilitar la interpretación de la simulación por parte de quienes toman decisiones.

<img src="/images/projects/aeropuerto_dashboard.png"
     alt="Captura de pantalla del panel Streamlit"
     style="width: 100%; max-width: 900px; display: block; margin: 1rem auto; border-radius: 14px;">

---

## Tecnologías
- Python
- pandas, NumPy
- Procesamiento de CSV
- Streamlit
- Teoría de colas y conceptos de investigación de operaciones
- YOLO / YOLOv8
- OpenCV
- Análisis y visualización de datos

---

## Limitaciones
- El proyecto es un **prototipo de simulación** y no representa una implementación aeroportuaria completamente validada.
- Los resultados se basan en **entradas sintéticas o simuladas**, no en datos operativos en vivo.
- El componente YOLO/YOLOv8 es una **prueba de concepto** para contar pasajeros a partir de secuencias de vídeo sintéticas.

---

## Trabajo futuro
Los posibles próximos pasos incluyen:

- validar el modelo con datos reales de rendimiento del aeropuerto
- refinar el modelo de zona de servicio con distribuciones de servicio variables
- agregar una capa de ingesta de datos en vivo para soporte de decisiones en tiempo real
- ampliar el prototipo para admitir políticas alternativas de personal y encaminamiento de colas

---

## Enlaces
- Página del proyecto del club: https://club-proyectos-tecnicos.github.io/projects/airport-queue-optimization/
- Repositorio: https://github.com/javiergonzalvez07-star/Optimizacion-Inteligente-Colas-Aeropuertos
