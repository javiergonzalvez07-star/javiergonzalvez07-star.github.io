---
title: "Respuesta térmica transitoria de un ladrillo modificado con parafina: comparación experimental y modelado de orden reducido"
shortTitle: "Ladrillo modificado con parafina"
date: 2026-05-04
draft: false
description: "Una comparación experimental de ladrillos convencionales y rellenos de parafina, respaldada por un modelo de orden reducido de amortiguación térmica transitoria."
summary: "Un experimento de calentamiento controlado y un modelo de dos nodos mostraron un aumento retardado de la temperatura de la cara superior con parafina, mientras que los incrementos de temperatura finales permanecieron similares."
area: "Física experimental · Modelización térmica"
image: "/images/research/thermal/aligned-temperature.png"
imageAlt: "Curvas experimentales de temperatura de la superficie superior para los ladrillos de referencia y modificados con parafina."
badges: ["Física térmica", "Termopares tipo K", "Limpieza de datos", "Modelización de orden reducido"]
glance:
  - label: "Sistema experimental"
    value: "Dos ladrillos cerámicos huecos"
  - label: "Instrumentación"
    value: "Termopares tipo K + MAX6675"
  - label: "Datos de calentamiento"
    value: "1.858 muestras de referencia · 1.276 PCM"
  - label: "Comparación alineada"
    value: "1.150 s desde 36,25 °C"
---

## El problema

Los materiales de cambio de fase pueden absorber energía como calor latente y retrasar así los picos de temperatura sin aporte activo de energía. Este estudio planteó una pregunta precisa: **¿rellenar un ladrillo cerámico hueco con parafina modifica la escala temporal característica del calor que alcanza la cara opuesta?** El material no se trató como un aislante permanente ni se intentaron inferir propiedades que no se hubieran medido.

## Enfoque de investigación

<div class="process-grid" aria-label="Flujo de trabajo de investigación">
 <div class="process-step"><b>01 · Preparar</b>Rellenar un ladrillo con 1 kg de parafina comercial y sellar ambas muestras.</div>
 <div class="process-step"><b>02 · Medir</b>Calentar desde abajo y registrar las temperaturas de las caras superior e inferior.</div>
 <div class="process-step"><b>03 · Alinear</b>Limpiar errores de adquisición y comparar a partir de una temperatura inicial común.</div>
 <div class="process-step"><b>04 · Modelizar</b>Comprobar la interpretación de la inercia térmica con un modelo de dos nodos.</div>
</div>

### Configuración experimental

Los ladrillos de referencia y modificado con PCM se calentaron desde una cara en condiciones similares. Se cubrieron los laterales y las aberturas con poliestireno expandido para reducir las pérdidas y favorecer un flujo de calor predominantemente vertical. Dos termopares tipo K conectados a módulos MAX6675 midieron la zona calentada y la respuesta transmitida a la superficie superior.

El proveedor especificaba para la parafina un intervalo de fusión aproximado de **56–58 °C**. No se disponía de una medición DSC independiente, por lo que se trata de una referencia comercial y no de una propiedad medida en la muestra.

## Modelado y análisis de datos

El preprocesamiento detectó la cabecera real del CSV, eliminó las líneas iniciales, corrigió los reinicios temporales y los problemas con las etiquetas de los sensores, seleccionó la fase de calentamiento y alineó ambos experimentos a una temperatura de la superficie superior de aproximadamente **36,25 °C**. Se utilizó la siguiente comparación:

<div class="equation"><strong>ΔT<sub>upper</sub>(t) = T<sub>upper</sub>(t) − T<sub>upper</sub>(0)</strong></div>

El modelo fenomenológico de dos nodos representó el estado interno del ladrillo y midió la cara superior. Para el caso PCM, un factor de inercia dependiente de la temperatura se aproximó al efecto de cambio de fase:

<div class="equation"><strong>F<sub>PCM</sub>(T) = 1 + A exp[−½((T − T<sub>m</sub>)/σ)²]</strong></div>

Aquí, la temperatura de transición ajustada es un **parámetro efectivo del modelo concentrado**, no una medida del punto de fusión de la parafina.

## Resultados principales

<div class="result-callout"><div><strong>Respuesta retardada</strong>La cara superior del ladrillo con PCM permaneció más tiempo cerca de su temperatura inicial.</div><div><strong>7,75 °C frente a 8,25 °C</strong>Los incrementos finales de la cara superior durante la misma ventana de 1.150 s fueron similares.</div><div><strong>Transitorio, no permanente</strong>La evidencia respalda un retraso en la transmisión, no un mejor aislamiento en estado estacionario.</div></div>

<figure class="research-figure">
 <img src="/images/research/thermal/aligned-temperature.png" alt="Temperaturas alineadas de la superficie superior que muestran un aumento más temprano para el ladrillo de referencia y un aumento retrasado para el ladrillo PCM" loading="lazy">
<figcaption>La cara superior del ladrillo modificado con PCM permaneció más tiempo cerca de su temperatura inicial antes de converger hacia la respuesta de referencia.</figcaption>
</figure>

- El ladrillo convencional transmitió el aumento de temperatura antes; el ladrillo PCM mostró un claro retraso inicial e intermedio.
- Los incrementos finales sobre la ventana común fueron similares: **7,75 °C** para la referencia y **8,25 °C** para el ladrillo PCM. Por lo tanto, la evidencia respalda la amortiguación en el tiempo, no el aislamiento permanente.
- Los incrementos finales modelizados fueron **7,98 °C** para la referencia y **6,42 °C** para el ladrillo PCM. Sus respectivos valores de RMSE de la curva fueron **2,69 °C** y **0,64 °C**. El mayor error de la referencia refleja su rápido aumento inicial, que el modelo de dos nodos no reprodujo bien; estos errores evalúan el ajuste de la curva, no las propiedades del material.

<figure class="research-figure">
 <img src="/images/research/thermal/model-comparison.png" alt="Comparación de los incrementos de temperatura del modelo experimental y de orden reducido para ambos ladrillos" loading="lazy">
 <figcaption> El modelo de orden reducido respalda la interpretación de la inercia térmica; no es una simulación tridimensional calibrada.</figcaption>
</figure>

## Conclusiones y limitaciones

El experimento es consistente con que la parafina actúa como un **amortiguador térmico transitorio**: redistribuye la transmisión de calor a lo largo del tiempo en lugar de impedirla. La geometría del ladrillo hueco, el relleno no uniforme, el contacto del sensor, la potencia de calentamiento finita y las pérdidas residuales limitan la inferencia cuantitativa. El trabajo no cuantificó de forma independiente el calor latente, no resolvió la ecuación de calor tridimensional completa ni validó otras geometrías y condiciones de contorno.

El trabajo futuro debería incorporar caracterización mediante DSC, ensayos repetidos con estimaciones de incertidumbre, potencia de calentamiento controlada, sensores de temperatura internos y un modelo que resuelva explícitamente la geometría.

## Habilidades demostradas

<div class="skills-grid"><div class="skill-chip">Diseño experimental</div><div class="skill-chip">Instrumentación con sensores</div><div class="skill-chip">Preprocesamiento de datos</div><div class="skill-chip">Modelización térmica</div><div class="skill-chip">Interpretación de modelos</div><div class="skill-chip">Tratamiento de la incertidumbre</div><div class="skill-chip">Visualización científica</div><div class="skill-chip">Redacción técnica</div></div>

## Trabajo relacionado

La adquisición de datos mediante sensores y el flujo de modelización interpretable conectan directamente con el [sistema de monitorización de la integridad estructural ferroviaria](/es/projects/railway-structural-monitoring/), donde las mediciones físicas también se convierten en indicadores orientados a la toma de decisiones.
