---
title: "Sistema de monitorización de la integridad estructural ferroviaria"
description: "Prototipo de bajo coste para monitorizar la integridad estructural ferroviaria mediante sensores, procesamiento de datos con Python, una función de daño interpretable y un panel de Streamlit."
date: 2026-06-12
draft: false
tags: ["Python", "Streamlit", "Sensors", "ESP32", "Data Processing", "Machine Learning", "Structural Health Monitoring"]
summary: "Prototipo ferroviario de bajo coste que transforma los datos de sensores físicos en indicadores de daño interpretables y un panel interactivo."
featuredImage: "/images/projects/railway-monitoring/railway-hero.png"
mathjax: true
---

## Descripción general

Este proyecto desarrolla una primera versión funcional de un **sistema de monitorización de la integridad estructural ferroviaria**. En lugar de limitarse a conectar sensores, el equipo construyó un sistema de principio a fin que transforma las mediciones físicas en información interpretable para el mantenimiento predictivo.

El prototipo mide aceleración, vibración, temperatura y señales piezoeléctricas con un dispositivo basado en ESP32. Las lecturas se almacenan en archivos CSV, se limpian y normalizan con Python, se combinan mediante una función de daño interpretable y se presentan en un panel interactivo de Streamlit.

<figure style="margin: 1.5rem auto 2rem; max-width: 900px;">
 <img src="/images/projects/railway-monitoring/railway-hero.png"
       alt="Descripción general del proyecto de monitorización estructural ferroviaria"
       loading="eager"
       style="width: 100%; display: block; border-radius: 14px;">
 <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
 Prototipo integral para monitorizar la integridad estructural ferroviaria.
 </figcaption>
</figure>

<div style="display: flex; flex-wrap: wrap; gap: 0.75rem; margin: 1.25rem 0 2rem;">
 <a class="btn btn-primary" href="https://github.com/javiergonzalvez07-star/Proyecto1" target="_blank" rel="noopener noreferrer">Ver repositorio</a>
 <a class="btn btn-outline-primary" href="/es/#projects">Volver a proyectos</a>
</div>

Este fue un proyecto en grupo para la asignatura **Proyecto I** del Doble Grado en Ingeniería Matemática y Física de la Universidad CEU San Pablo, desarrollado por Javier Gonzálvez, Pablo Prada, Miguel Rodríguez, Santiago Hernández y Ricardo Mazariegos.

---

## Problema

Las vías del ferrocarril están expuestas a cargas dinámicas repetidas, vibraciones, cambios de temperatura, fatiga y eventos mecánicos. Las inspecciones frecuentes pueden ser costosas, mientras que las mediciones brutas por sí solas no proporcionan la información clara necesaria para respaldar el mantenimiento predictivo.

El reto consistía en diseñar un prototipo de bajo coste capaz de recopilar datos físicos y convertirlos en indicadores sencillos que ayudaran a describir el estado de una sección de vía monitorizada.

---

## Solución

La solución es un flujo modular de monitorización:

- adquisición basada en sensores de aceleración, temperatura y señales piezoeléctricas
- almacenamiento en CSV para mediciones sin procesar y procesadas
- limpieza, filtrado, interpolación y normalización en Python
- una función de daño ponderada e interpretable
- un panel interactivo de Streamlit para monitorizar el estado y las alertas

Su propósito central es convertir señales sin procesar en resultados comprensibles como **daño instantáneo, daño acumulado, vida útil restante y estado de la vía**.

---

## Arquitectura del sistema

<figure style="margin: 1.5rem auto; max-width: 900px;">
 <img src="/images/projects/railway-monitoring/railway-architecture.png"
       alt="Arquitectura del sistema desde los sensores hasta el panel"
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
 <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
 Flujo completo desde las mediciones físicas hasta indicadores interpretables en el panel.
 </figcaption>
</figure>

<div style="overflow-x: auto; margin: 1.25rem 0;">
 <div style="min-width: 760px; display: flex; align-items: stretch; gap: 0.5rem; text-align: center;">
 <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Sensores</strong><br><small>Señales físicas</small></div>
 <div style="align-self: center;">→</div>
 <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>ESP32</strong><br><small>Adquisición</small></div>
 <div style="align-self: center;">→</div>
 <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>CSV sin procesar</strong><br><small>Almacenamiento</small></div>
 <div style="align-self: center;">→</div>
 <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Python</strong><br><small>Procesamiento</small></div>
 <div style="align-self: center;">→</div>
 <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Daño</strong><br><small>Modelo</small></div>
 <div style="align-self: center;">→</div>
 <div style="flex: 1; padding: 1rem 0.65rem; border: 1px solid rgba(127,127,127,.3); border-radius: 12px;"><strong>Panel</strong><br><small>Información</small></div>
 </div>
</div>

1. **Sensores:** miden la aceleración, la temperatura y la respuesta piezoeléctrica.
2. **ESP32:** recopila mediciones del dispositivo físico.
3. **CSV sin procesar:** proporciona un almacenamiento inicial sencillo y portátil.
4. **Procesamiento con Python:** limpia, filtra, interpola y normaliza los datos.
5. **Conjunto de datos final:** almacena características consistentes listas para el análisis.
6. **Función de daño:** combina las variables relevantes en un modelo ponderado.
7. **Panel de Streamlit:** muestra señales, indicadores de estado y alertas.

---

## Hardware

El hardware se basó deliberadamente en componentes accesibles y de bajo coste. El objetivo no era construir un dispositivo industrial, sino validar un prototipo completo que conectara mediciones reales con una monitorización matemática y visual.

<figure style="margin: 1.5rem auto; max-width: 800px;">
 <img src="/images/projects/railway-monitoring/railway-hardware-prototype.jpg"
       alt="Prototipo físico con ESP32 y sensores."
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
 <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
 Prototipo de bajo coste basado en ESP32 y sensores de vibración, temperatura y respuesta piezoeléctrica.
 </figcaption>
</figure>

| Componente | Rol |
|---|---|
| **ESP32** | Microcontrolador principal y dispositivo de adquisición |
| **MPU6050** | Mediciones de aceleración y vibración |
| **MAX6675 + termopar tipo K** | Medición de temperatura |
| **Sensor piezoeléctrico** | Detección de impactos y eventos mecánicos |
| **Placa de prueba y cableado** | Conexiones prototipo |
| **Recinto impreso en 3D** | Concepto de protección física y montaje |

---

## Procesamiento de datos

Las mediciones de sensores reales introdujeron ruido, desviaciones, valores ausentes y lecturas no válidas. Por ello, resultó esencial disponer de un flujo de procesamiento sólido:

- clasificación temporal
- eliminación de duplicados
- filtrado de rango físico
- interpolación de valores perdidos
- filtrado de aceleración usando la transformada de Fourier
- creación de características derivadas
- normalización min-max

Las principales variables derivadas fueron:

- **Aceleración dinámica:** diferencia con respecto a la aceleración inicial.
- **Variable piezoeléctrica aproximada:** diferencia respecto a la señal piezoeléctrica o tensión de referencia.
- **Desviación de temperatura:** diferencia con respecto a una temperatura de referencia.

---

## Función de daño interpretable

El panel no se limita a mostrar señales sin procesar: calcula una métrica de daño agregada:

<div style="padding: 1.5rem; margin: 1.25rem auto; max-width: 620px; text-align: center; border: 1px solid rgba(127,127,127,.3); border-radius: 14px; font-size: 1.6rem;">
 <strong>D = 0.45P + 0.10T + 0.45A</strong>
</div>

<figure style="margin: 1.5rem auto; max-width: 800px;">
 <img src="/images/projects/railway-monitoring/railway-damage-function.png"
       alt="Función de daño interpretable con temperatura piezoeléctrica y pesos de aceleración."
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
 <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
 Modelo ponderado interpretable que combina respuesta piezoeléctrica, desviación de temperatura y aceleración dinámica.
 </figcaption>
</figure>

- **P:** contribución piezoeléctrica normalizada
- **T:** desviación de temperatura normalizada
- **A:** aceleración dinámica normalizada

Se aplicaron modelos de regresión logística y bosque aleatorio a un conjunto de datos externo de monitorización estructural para comparar la importancia relativa de las variables. Después se ajustaron los pesos finales de acuerdo con el significado físico de cada señal en el contexto ferroviario.

El objetivo del aprendizaje automático no era crear un predictor de caja negra, sino guiar la construcción de una función que siguiera siendo comprensible y fácil de comunicar.

---

## Panel de Streamlit

El panel convierte el modelo matemático en una interfaz de monitorización comprensible. Incluye:

- dispositivo individual y vistas generales de seguimiento
- daño instantáneo y acumulado
- vida restante estimada
- estados **Normal**, **Atención** y **Alerta**
- gráficos de señales temporales
- actualizaciones de datos durante la demostración
- un simulador del paso de un tren

Permite inspeccionar el estado actual del dispositivo, seguir la evolución de las señales y comprender el estado estimado de la sección monitorizada.

<figure style="margin: 1.5rem auto 2rem; max-width: 900px;">
 <img src="/images/projects/railway-monitoring/railway-dashboard-individual.png"
       alt="Panel individual de Streamlit para el dispositivo monitorizado"
       loading="lazy"
       style="width: 100%; display: block; border-radius: 14px;">
 <figcaption style="margin-top: 0.65rem; text-align: center; color: var(--text-secondary-color); font-size: 0.92rem;">
 Vista individual del dispositivo con indicadores en tiempo real, daño y vida útil restante.
 </figcaption>
</figure>

---

## Simulador de demostración

Como durante el proyecto no fue posible validar el sistema en una vía real, el equipo creó un simulador sintético de demostración. Este genera eventos de paso de trenes, aumenta la vibración y la actividad piezoeléctrica y actualiza el archivo CSV para que el panel de Streamlit pueda reaccionar durante la presentación.

El simulador demuestra el flujo de datos completo y el comportamiento de la interfaz. **No** valida daños estructurales reales.

---

## Tecnologías

- **Datos y modelado:** Python, pandas, NumPy, SciPy, `scipy.fft`, scikit-learn
- **Panel de control:** Streamlit, Plotly
- **Hardware:** ESP32, MPU6050, MAX6675, termopar tipo K, sensor piezoeléctrico
- **Almacenamiento y colaboración:** CSV, GitHub

---

## Desafíos y lecciones

- El alcance original se redujo a un prototipo modular.
- No estaba disponible ningún conjunto de datos etiquetados sobre el deterioro ferroviario real.
- Los sensores de bajo coste introdujeron ruido, desviaciones y lecturas erróneas.
- Se necesitó un flujo de limpieza fiable antes de poder obtener una visualización significativa.
- La demostración en vivo necesitaba una fuente de datos continua.
- Trabajar con hardware físico resultó muy diferente a usar conjuntos de datos limpios.

Una de las principales lecciones fue que **los datos reales de sensores son imperfectos**. La limpieza y la normalización adquirieron tanta importancia como el propio panel, porque la calidad de cada indicador final depende de la calidad de las mediciones procesadas.

---

## Limitaciones

- No es un sistema de monitorización validado industrialmente.
- La función de daño no se ha calibrado con mediciones de vías ferroviarias deterioradas.
- El conjunto de datos externo no reproduce perfectamente el caso de uso ferroviario.
- Los sensores de bajo coste pueden introducir un ruido de medida significativo.
- El montaje físico influye en la calidad de la señal.
- El simulador demuestra el flujo del sistema, pero no valida daños reales.

---

## Trabajo futuro

- validar el sistema con datos de vía reales o un banco de pruebas experimental controlado
- distribuir múltiples dispositivos en diferentes secciones de vía
- agregar comunicación inalámbrica y un servidor central
- mejorar la carcasa y la fijación mecánica
- calibrar la función de daño experimentalmente
- reducir el consumo mediante el modo de sueño profundo del ESP32
- explorar la recolección de energía piezoeléctrica y la asistencia solar
- entrenar modelos más avanzados una vez que haya suficientes datos específicos del proyecto disponibles

---

## Resultados e impacto

El resultado final es un prototipo funcional que integra hardware, procesamiento de datos, modelización matemática y visualización. Su principal valor reside en el proceso completo: desde las lecturas de sensores físicos hasta indicadores interpretables para monitorizar la integridad estructural ferroviaria.

---

## Mi contribución

Mi trabajo se centró en conectar las partes matemáticas y de software del proyecto grupal: limpieza de datos, ingeniería de características, diseño de la función de daño, interpretación de modelos, desarrollo del panel y preparación de la demostración.

También trabajé para que un usuario no técnico pudiera comprender el sistema, convirtiendo mediciones sin procesar en indicadores visuales como daño acumulado, vida útil restante y estados de alerta.

---

## Enlaces

- **Repositorio:** https://github.com/javiergonzalvez07-star/Proyecto1
- **Volver a los proyectos del portfolio:** [Proyectos](/es/#projects)
