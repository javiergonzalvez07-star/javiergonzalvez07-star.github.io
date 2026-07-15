---
title: "Análisis de datos de clientes bancarios y predicción de abandono"
date: 2026-02-01
draft: false
tags: ["Python", "pandas", "EDA", "Machine Learning"]
summary: "Un análisis exploratorio de los datos de los clientes bancarios y un modelo predictivo de la pérdida de clientes."
featuredImage: "/images/projects/Banco.png"
---


## 🧠 Resumen del proyecto

Este proyecto combina **análisis de datos exploratorios (EDA)** con una **extensión de modelado predictivo básico** aplicada a un conjunto de datos de clientes bancarios del mundo real.
El EDA original se desarrolló como una tarea académica grupal y luego se amplió individualmente para enmarcar y resolver un **problema de clasificación binaria** centrado en predecir la pérdida de clientes (si un cliente abandonará el banco)
<img src="/images/projects/Banco.png"
     alt="Visualización del análisis de clientes bancarios"
     style="width: 450px; max-width: 100%; display: block; margin: 1rem auto; border-radius: 12px;">


---

## 📊 Conjunto de datos y problema

- **Conjunto de datos:** conjunto público de Kaggle sobre clientes bancarios, con 10.127 clientes × 23 variables.
- **Objetivo:** Comprender el comportamiento del cliente a través de la exploración de datos y crear un modelo simple e interpretable para predecir la pérdida de clientes.
- **Reto:** equilibrar un preprocesamiento riguroso y una modelización interpretable sin añadir complejidad innecesaria.

---

## 🔧 Herramientas y tecnologías

Este proyecto se creó utilizando:

- **Python**
- **pandas** / **NumPy**
- **matplotlib**
- **scikit-learn**

Todo el análisis y la modelización se encuentran en el cuaderno de Jupyter incluido en el repositorio.

---

## 📋 Enfoque

1. **Limpieza y preprocesamiento de datos**
 - inspección de la forma, los tipos y los valores ausentes
 - tratamiento de valores atípicos y conversión de rangos de ingresos categóricos a numéricos
 - cambio de nombre de características y eliminación de variables redundantes
2. **Análisis exploratorio de datos (EDA)**
 - Estadística descriptiva
 - Exploración visual de distribuciones y correlaciones
3. **Modelado predictivo**
- planteamiento del abandono como un problema de clasificación binaria
- entrenamiento de un **modelo de regresión logística** por su interpretabilidad
- evaluación y mejora del modelo mediante balanceo y ajuste del umbral
4. **Interpretación**
- interpretación de los coeficientes del modelo para comprender los factores de abandono

---

## 📈 Información clave

- **Multicolinealidad** entre el límite de crédito y el importe medio disponible para compras
- **Actividad de transacción** diferencia los perfiles de clientes
- **Indicadores de abandono:** La menor actividad y la inactividad prolongada aumentan la probabilidad de abandono.

---

## 🧪 Lo que aprendí

- Cómo formular un problema empresarial en una tarea de aprendizaje automático
- Aplicación de razonamiento estadístico y estrategias de preprocesamiento
- Transición del análisis descriptivo al modelado predictivo
- Interpretación de coeficientes de regresión en un contexto empresarial.

---

## 🔗 Enlaces

- **Repositorio:** https://github.com/javiergonzalvez07-star/estudio-de-csv-banco
- **Linkedin:** https://www.linkedin.com/in/javier-gonzalvez-sempere-b526552b0/
