---
title: "Instrucciones orientadas a la honestidad y equilibrio entre fiabilidad y utilidad: evaluación controlada de las alucinaciones de los LLM"
shortTitle: "Equilibrio entre fiabilidad y utilidad en los LLM"
date: 2026-07-06
draft: false
description: "Evaluación controlada de 600 respuestas que mide cómo las instrucciones orientadas a la honestidad modifican las alucinaciones, la precisión y la abstención en tres LLM ligeros."
summary: "En 600 respuestas, la instrucción de honestidad redujo las alucinaciones observadas del 21,3 % al 7,3 %, pero aumentó la abstención total e innecesaria."
area: "Evaluación de IA · Investigación sobre fiabilidad"
image: "/images/research/hallucination/provider-hallucination.png"
imageAlt: "Tasas de alucinaciones por proveedor con instrucciones normales y orientadas a la honestidad"
badges: ["Evaluación de LLM", "Diseño de bancos de pruebas", "IC bootstrap", "Pruebas emparejadas"]
glance:
  - label: "Banco de pruebas"
    value: "100 preguntas · 8 categorías"
  - label: "Modelos"
    value: "3 modelos ligeros mediante API"
  - label: "Resultados evaluados"
    value: "600 respuestas"
  - label: "Compromiso principal"
    value: "Menos invenciones · más abstenciones"
---

## El problema

La fiabilidad real no se mide únicamente mediante la precisión. Un modelo útil debe evitar afirmaciones sin fundamento, abstenerse cuando faltan pruebas y, al mismo tiempo, responder preguntas sencillas. Este estudio controlado evaluó si una breve instrucción orientada a la honestidad mejora esa calibración o se limita a volver más cautelosos a los modelos.

## Enfoque de investigación

<div class="process-grid" aria-label="Flujo de trabajo de investigación"><div class="process-step"><b>01 · Diseñar</b>Crear un banco de 100 preguntas adversariales en ocho modos de fallo.</div><div class="process-step"><b>02 · Generar</b>Consultar tres modelos en condiciones normal y de honestidad, con temperatura 0.</div><div class="process-step"><b>03 · Anotar</b>Etiquetar manualmente la corrección, la alucinación, la gravedad y el exceso de confianza.</div><div class="process-step"><b>04 · Comparar</b>Aplicar pruebas emparejadas e intervalos de confianza bootstrap por pregunta.</div></div>

### Banco de pruebas y modelos

El banco de pruebas abarcó hechos claros, errores conceptuales comunes, hechos propensos a error, artículos o citas inventados, casos de abstención correcta, falta de contexto, hechos sensibles al tiempo y presuposiciones falsas. Cada uno de los tres modelos ligeros accesibles mediante API (`gpt-4o-mini`, `gemini-2.5-flash-lite` y `claude-haiku-4-5-20251001`) respondió dos veces a cada elemento, lo que produjo **300 respuestas por condición**.

<figure class="research-figure"><img src="/images/research/hallucination/category-rate.png" alt="Tasa de alucinaciones en ocho categorías de referencia, con el máximo en las citas inventadas" loading="lazy"><figcaption>Las citas inventadas, las consultas sensibles al tiempo y la falta de contexto fueron las categorías más propensas a fallos en esta prueba de estrés.</figcaption></figure>

## Modelado y análisis de datos

Las respuestas se etiquetaron manualmente conforme a una referencia predefinida. La abstención se reconstruyó mediante detección determinista de frases, manteniendo una trazabilidad de auditoría por fila. Se comprobó que el conjunto final contenía seis respuestas válidas por pregunta. Como cada modelo respondió la misma pregunta con ambas instrucciones, los resultados pudieron compararse como **observaciones emparejadas** en vez de muestras independientes. Las pruebas binomiales exactas de tipo McNemar evaluaron las respuestas cuyo resultado cambió, mientras que el remuestreo bootstrap por pregunta estimó intervalos de confianza del 95 %.

Al tratarse de un banco adversarial de 100 preguntas, los resultados son exploratorios y no deben generalizarse al rendimiento global de cada proveedor.

## Resultados principales

<div class="result-callout"><div><strong>21,3 % → 7,3 %</strong>La tasa de alucinaciones observada disminuyó 14,0 puntos porcentuales.</div><div><strong>79,7 % → 88,3 %</strong>La precisión aumentó dentro de esta evaluación controlada.</div><div><strong>10,3 % → 25,0 %</strong>La abstención total aumentó, mostrando el coste en utilidad.</div></div>

| Métrica | Instrucción normal | Instrucción de honestidad | Diferencia |
|---|---:|---:|---:|
| Tasa de alucinaciones | 21,3% | 7,3% | −14,0 puntos |
| Tasa de abstención | 10,3% | 25,0% | +14,7 puntos |
| Tasa de precisión | 79,7% | 88,3% | +8,6 puntos |

<figure class="research-figure"><img src="/images/research/hallucination/provider-hallucination.png" alt="Tasas de alucinaciones por proveedor, reducidas con la instrucción de honestidad en los tres modelos evaluados" loading="lazy"><figcaption>Las alucinaciones observadas disminuyeron en los tres proveedores de modelos con la instrucción orientada a la honestidad.</figcaption></figure>

Por tanto, el cambio no supuso una mejora universal. En los elementos donde rechazar la respuesta era apropiado, la abstención correcta aumentó del **46,7 % al 73,3 %**. Sin embargo, en los elementos que sí debían responderse, la abstención innecesaria aumentó del **1,7 % al 14,2 %**.

<figure class="research-figure"><img src="/images/research/hallucination/provider-abstention.png" alt="Aumento de las tasas de abstención por proveedor con la instrucción de honestidad" loading="lazy"><figcaption>Una mayor cautela factual también aumentó las abstenciones, incluso ante preguntas que sí podían responderse.</figcaption></figure>

## Interpretación de los resultados

En este banco de pruebas, las instrucciones orientadas a la honestidad redujeron las invenciones, pero actuaron como una herramienta de calibración poco precisa: elevaron el umbral aparente de respuesta e indujeron una cautela excesiva. Una intervención más eficaz distinguiría las afirmaciones no verificables de los hechos estables mediante mecanismos de verificación o confianza más granulares.

### Limitaciones

El estudio utilizó solo 100 preguntas adversariales, tres modelos ligeros y un único anotador manual. No se midió el acuerdo entre evaluadores; además, la detección de abstenciones basada en frases puede pasar por alto formas sutiles de incertidumbre y los resultados no representan la distribución de consultas cotidianas.

## Habilidades demostradas

<div class="skills-grid"><div class="skill-chip">Diseño de bancos de pruebas</div><div class="skill-chip">Experimentación mediante API</div><div class="skill-chip">Anotación manual</div><div class="skill-chip">Contrastes de hipótesis emparejados</div><div class="skill-chip">Intervalos bootstrap</div><div class="skill-chip">Auditoría de datos</div><div class="skill-chip">Análisis de errores</div><div class="skill-chip">Comunicación científica</div></div>
