---
title: "PeerScope — Plataforma de inteligencia competitiva"
description: "PeerScope es una plataforma validada de inteligencia competitiva que combina KPIs financieros, benchmarking por comparables, scoring interpretable, imports privados, análisis fundamentado con IA e informes ejecutivos versionados."
summary: "Plataforma analítica integral que convierte datos financieros en benchmarks, scores interpretables, diagnósticos con IA fundamentada e informes versionados."
date: 2026-07-23
draft: false
slug: "peerscope"
translationKey: "peerscope"
layout: "peerscope"
tags: ["Python", "FastAPI", "Supabase", "OpenAI API", "Analítica financiera", "Apoyo a decisiones"]
badges: ["Python", "FastAPI", "Supabase", "OpenAI API", "Analítica financiera"]
image: "/images/projects/peerscope/peerscope-landing.webp"
featuredImage: "/images/projects/peerscope/peerscope-landing.webp"
images: ["/images/projects/peerscope/peerscope-landing.webp"]
imageAlt: "Landing pública de PeerScope que presenta el producto de inteligencia competitiva"
status: "Beta privada funcional"
eyebrow: "Caso de estudio de ingeniería y producto"
subtitle: "Plataforma integral para transformar datos financieros empresariales en comparaciones justas, diagnósticos competitivos interpretables e informes ejecutivos."
liveLabel: "Abrir beta"
backLabel: "Volver a proyectos"
coldStart: "Alojada en Render; la beta puede tardar unos segundos en despertar tras un periodo de inactividad."
heroCaption: "Landing pública de PeerScope. Las vistas analíticas inferiores proceden de la demo pública estática del producto."
metricsLabel: "Métricas verificadas del proyecto"
metrics:
  - value: "1.777"
    label: "empresas en el pipeline de datos"
  - value: "1.164"
    label: "empresas con score competitivo válido"
  - value: "6"
    label: "dimensiones interpretables de scoring"
  - value: "194"
    label: "tests automatizados superados"
  - value: "11"
    label: "subtests adicionales superados"
  - value: "1"
    label: "Sector Pack real: industria química"
finalEyebrow: "Explorar el producto"
finalTitle: "De registros financieros a un diagnóstico revisable"
finalText: "El sitio público y la demo estática muestran el flujo del producto sin presentar sus resultados como asesoramiento financiero definitivo."
---

## De los registros financieros al apoyo a decisiones

PeerScope está pensado para consultoras boutique, analistas, equipos de estrategia y proyectos de diagnóstico empresarial que necesitan transformar datos financieros en una lectura estructurada y presentable. Conecta ingesta, normalización, KPIs, selección de comparables, percentiles, scoring determinista, diagnósticos, IA fundamentada y reporting en un flujo trazable.

> La parte difícil no es mostrar datos financieros, sino decidir qué significa cada valor frente a empresas comparables, comunicar las limitaciones y convertir el resultado en una recomendación trazable.

La plataforma apoya el criterio profesional; no sustituye una revisión financiera experta ni garantiza decisiones correctas.

## El problema

<div class="ps-grid">
<section class="ps-card"><h3>Datos sin contexto</h3><p>Un ratio aislado no determina si una empresa está bien posicionada. Su lectura depende de escala, deuda, productividad, cobertura y contexto sectorial.</p></section>
<section class="ps-card"><h3>Comparaciones injustas</h3><p>Comparar directamente empresas incompatibles puede engañar. Los peer groups consideran tamaño, empleados, ingresos y sector, y muestran cuándo la muestra es limitada.</p></section>
<section class="ps-card"><h3>Reporting manual</h3><p>Convertir el análisis en un documento ejecutivo exige trabajo repetitivo, consistencia metodológica, revisión y distinguir evidencia de interpretación.</p></section>
</div>

PeerScope no predice el mercado bursátil ni promete decisiones acertadas. Estructura evidencia para un analista humano.

## Flujo end-to-end

<div class="ps-workflow">
<section class="ps-step"><span class="ps-step-number">1</span><h3>Buscar o importar una empresa</h3><p>Búsqueda en el dataset base o carga opcional de CSV/XLSX asociados a una cuenta u organización.</p></section>
<section class="ps-step"><span class="ps-step-number">2</span><h3>Normalizar y validar</h3><p>Conversión de formatos y campos a una estructura canónica, validación previa y exportación normalizada cuando corresponde.</p></section>
<section class="ps-step"><span class="ps-step-number">3</span><h3>Construir un peer group relevante</h3><p>Escala, ingresos y contexto evitan comparaciones incompatibles; el sistema comunica cuándo la muestra es limitada.</p></section>
<section class="ps-step"><span class="ps-step-number">4</span><h3>Calcular KPIs y percentiles</h3><p>Ratios financieros y operativos, posición relativa y señales fuertes, débiles o de datos ausentes.</p></section>
<section class="ps-step"><span class="ps-step-number">5</span><h3>Generar el score competitivo</h3><p>Seis bloques ponderados producen un tier interpretable. El método es determinista, no un algoritmo de IA ni una caja negra.</p></section>
<section class="ps-step"><span class="ps-step-number">6</span><h3>Producir diagnóstico y palancas</h3><p>Fortalezas, alertas, brechas, próximos focos y palancas de mejora trazables a valores concretos.</p></section>
<section class="ps-step"><span class="ps-step-number">7</span><h3>Usar AI Analyst</h3><p>Preguntas fundamentadas, explicaciones para públicos financieros o no financieros, síntesis de riesgos y priorización de KPIs.</p></section>
<section class="ps-step"><span class="ps-step-number">8</span><h3>Crear y versionar el informe</h3><p>Preview, revisión y versiones sucesivas HTML/PDF, separando contenido interno y destinado al cliente.</p></section>
</div>

La IA aparece después de una cadena analítica definida; no sustituye ingesta, comparabilidad, scoring o revisión profesional.

<figure class="ps-demo-figure">
  <img src="/images/projects/peerscope/peerscope-benchmark.webp" alt="Demo pública estática de PeerScope con benchmark empresarial y resultados de scoring competitivo" loading="lazy" width="1065" height="720">
  <figcaption>Demo pública estática: benchmark por peer group y scoring interpretable con datos de demostración.</figcaption>
</figure>

## Metodología de scoring interpretable

| Dimensión | Peso |
|---|---:|
| Rentabilidad | 25% |
| Solidez financiera | 25% |
| Productividad | 20% |
| Crecimiento | 15% |
| Operaciones | 10% |
| Eficiencia | 5% |

Cada bloque agrupa KPIs relacionados y los interpreta dentro del peer group. Los percentiles expresan la posición relativa; el score global resume la evidencia sin sustituir el detalle. Fortalezas y alertas siguen siendo trazables a valores. Un dato ausente se distingue de un resultado negativo, y los grupos pequeños o con baja cobertura no deben presentarse con falsa precisión.

Los pesos son metodología de producto, no una verdad financiera universal. Se hacen explícitos para poder discutirlos, validarlos y evolucionarlos.

> **Por qué importa:** dos empresas pueden presentar el mismo margen y, aun así, tener una lectura competitiva distinta cuando se consideran escala, deuda, productividad y contexto sectorial.

## Sector Packs: profundidad controlada

Cada sector puede requerir KPIs, reglas, umbrales y prioridades diferentes. PeerScope mantiene un núcleo común de scoring y extensiones controladas para evitar copias dispersas de lógica. El primer pack real se centra en **industria química**. Añadir y validar más packs es un próximo paso; el producto no afirma dominar hoy todos los sectores industriales.

## AI Analyst: qué hace realmente

### Preguntas sobre una empresa

El usuario puede preguntar por situación general, riesgos, KPIs prioritarios, comparación con empresas similares, fortalezas, palancas o una explicación para un cliente no financiero. El contexto permitido se limita a datos visibles y autorizados, KPIs calculados, benchmark disponible, imports permitidos y metodología aprobada.

Las claves de OpenAI permanecen en backend. Las respuestas se fundamentan en valores del sistema, separan afirmaciones verificadas de hipótesis, no inventan cifras ausentes y comunican las limitaciones. El uso puede limitarse según el plan.

### Asistencia durante la preparación de informes

El analista puede pedir una observación concreta, otro enfoque, explicar una anomalía, adaptar el tono o incorporar su propio razonamiento. La IA no sobrescribe ciegamente el documento: se conservan preview, control humano, trazabilidad, estructura aprobada, versionado y separación cliente/interno. Es una capa de interacción y redacción sobre un sistema analítico real, no la fuente de verdad.

## Reporting como entregable

El flujo cubre ficha de empresa, KPIs principales, benchmark por bloques, fortalezas, alertas, palancas, conclusiones y próximos focos. Admite HTML/PDF, preview antes de compartir, versiones sucesivas por empresa, plantillas y comentarios estándar reutilizables, metodología interna y separación entre informe de cliente y observaciones internas.

> Los informes se tratan como entregables analíticos versionados, no como respuestas desechables de una IA.

El objetivo no es exportar una tabla, sino crear un documento consistente que pueda revisarse y presentarse.

## Imports privados y separación de datos

<div class="ps-grid">
<section class="ps-card"><h3>Dataset base</h3><p>Datos empresariales para búsqueda general, comparación, cálculo de KPIs y scoring.</p></section>
<section class="ps-card"><h3>Datos importados</h3><p>CSV/XLSX de usuarios vinculados a su cuenta u organización y almacenados aparte con historial persistente.</p></section>
</div>

Los imports se normalizan, pueden exportarse normalizados y alimentar módulos secundarios como el radar de oportunidades. **No** modifican SABI silenciosamente y **no** entran automáticamente en scoring o benchmark mientras esa integración no esté habilitada. Cualquier integración futura debe ser explícita, autorizada y controlada.

<figure class="ps-architecture">
  <img src="/images/projects/peerscope/peerscope-architecture.es.svg" alt="Diagrama con los datos SABI fluyendo hacia el scoring determinista y los informes, mientras los imports privados permanecen aislados tras un límite de integración explícito" loading="lazy" width="1200" height="760">
</figure>

## Arquitectura técnica

<div class="ps-grid">
<section class="ps-card"><h3>Interfaz de producto</h3><p>Landing HTML/CSS/JavaScript, autenticación y workspace para búsqueda, diagnóstico, KPIs, benchmark, palancas, imports, informes, AI Analyst y configuración.</p></section>
<section class="ps-card"><h3>API y lógica de negocio</h3><p>Python y FastAPI para endpoints, validación, autorización, peer groups, scoring, diagnósticos, informes y control del uso de IA.</p></section>
<section class="ps-card"><h3>Capa de datos</h3><p>Supabase, PostgreSQL y Supabase Auth para datos base, tablas de aplicación, imports privados, análisis guardados, plantillas, versiones y configuración.</p></section>
<section class="ps-card"><h3>Capa de IA</h3><p>OpenAI API con prompts controlados, contexto permitido, grounding en resultados calculados y distinción entre afirmaciones e hipótesis.</p></section>
<section class="ps-card"><h3>Despliegue y validación</h3><p>Render, configuración mediante entorno, pytest, imports de Python, builds y checklist de seguridad. Procesado CSV/XLSX y generación HTML/PDF completan el flujo.</p></section>
</div>

No se inventan microservicios, colas, Kubernetes o modelos propios entrenados: la arquitectura refleja la beta implementada.

## Seguridad y privacidad

Autenticación, sesiones y endpoints sensibles protegidos, claves OpenAI solo en backend, imports asociados a cuenta u organización, controles de acceso, límites de IA por plan y ausencia de secretos en frontend forman la base. Las políticas Row Level Security de Supabase son obligatorias en las tablas relevantes; la última validación conocida cubre específicamente **14 tablas**.

RLS no se trata como una casilla de configuración. Los tests verifican el comportamiento seguro esperado y detectan configuraciones RLS inseguras. Un checklist pre-demo apoya el uso controlado y la beta muestra planes de precios sin pagos reales.

<div class="ps-note"><strong>Alcance de la afirmación:</strong> es una beta funcional con controles reales y hardening en curso, no un sistema certificado o auditado externamente ni un entorno de producción sin restricciones para información financiera altamente sensible.</div>

## Testing y fiabilidad

La última suite verificada completó **194 tests automatizados y 11 subtests adicionales**. Cubre endpoints, configuración, scoring, seguridad, detección de RLS insegura, preview de informes y comportamiento seguro cuando falta configuración. La validación incluyó imports de Python, `py_compile` y la comprobación de que la aplicación FastAPI puede importarse.

La demo pública estática no crea datos, no ejecuta IA y no modifica imports. Permite inspeccionar de forma segura los conceptos de benchmark/scoring, imports, AI Analyst y reporting.

> La suite no protege únicamente funciones aisladas, sino también supuestos de producto como el aislamiento de datos, el control de acceso y la consistencia del scoring.

**Preparación actual:** preparada para una demo controlada y para validar el producto, pero todavía no para un uso en producción sin restricciones.

## Decisiones de producto e ingeniería

<div class="ps-decisions">
<section class="ps-card"><h3>Peer groups antes del scoring</h3><p>Un score sin comparables adecuados puede ser engañoso.</p></section>
<section class="ps-card"><h3>Scoring interpretable antes que IA generativa</h3><p>La IA explica cálculos; no inventa la metodología.</p></section>
<section class="ps-card"><h3>Imports privados aislados</h3><p>Los datos de usuario no se mezclan con el dataset base por comodidad.</p></section>
<section class="ps-card"><h3>Informes versionados</h3><p>Un entregable importante debe poder revisarse y evolucionar.</p></section>
<section class="ps-card"><h3>Contenido interno distinto del cliente</h3><p>Las observaciones de consultoría pueden quedar fuera del informe final.</p></section>
<section class="ps-card"><h3>Afirmaciones distintas de hipótesis</h3><p>La incertidumbre y los límites de datos deben comunicarse.</p></section>
<section class="ps-card"><h3>Seguridad exigida mediante tests</h3><p>La seguridad de Supabase se verifica, no se supone.</p></section>
<section class="ps-card"><h3>Pricing beta sin pagos</h3><p>Los planes prueban posicionamiento y límites antes de cobrar prematuramente.</p></section>
<section class="ps-card"><h3>Profundidad sectorial antes que amplitud falsa</h3><p>Un pack químico real es más honesto que un soporte multisector superficial.</p></section>
</div>

## Mi papel y proceso de desarrollo

PeerScope nació como proyecto propio y alcanzó esta beta en menos de un mes. Definí el problema y usuario objetivo, diseñé el benchmarking, elegí dimensiones y pesos, especifiqué el flujo de producto, decidí la separación de datos base e imports y diseñé el papel de la IA. Revisé auditorías, prioricé seguridad, validé iteraciones y dirigí arquitectura y evolución.

Utilicé Codex intensivamente para acelerar implementación, revisión, tests y refactors, evaluando los resultados y tomando las decisiones finales de producto e ingeniería.

> Diseñé el producto, la metodología analítica y los requisitos de ingeniería, y utilicé Codex como agente de implementación y revisión. El desarrollo siguió ciclos repetidos de auditoría, implementación, testing y corrección, no la generación de un único prototipo.

## Resultados y estado actual

La beta funcional incluye landing pública, autenticación y workspace protegido; búsqueda; pipeline de 1.777 empresas y 1.164 scores válidos; peer groups, KPIs, percentiles y seis bloques de scoring; diagnóstico, fortalezas, alertas y palancas; AI Analyst; imports CSV/XLSX, normalización, historial aislado y exportación; radar de oportunidades; análisis recientes o guardados; plantillas, comentarios estándar y metodología interna; separación cliente/interno, preview e informes HTML/PDF versionados; planes y límites beta; controles de seguridad; despliegue público en Render; y la suite automatizada.

## Limitaciones actuales

- Sigue siendo una beta privada cuya profundidad metodológica se concentra en industria química.
- Faltan nuevos Sector Packs y validación con más sectores y empresas.
- Cobertura y calidad dependen del dataset; peer groups pequeños reducen la solidez.
- Los imports privados no alteran automáticamente el scoring sin integración explícita.
- La IA depende de datos autorizados disponibles y no sustituye el criterio financiero experto.
- Los resultados apoyan el análisis; no son asesoramiento financiero definitivo.
- El pricing no procesa pagos reales, falta hardening completo y se necesita más validación con usuarios.

## Próximos pasos

- Añadir Sector Packs a partir de KPIs ya diseñados y validarlos con más empresas.
- Mejorar la evaluación de peer groups e integrar imports solo bajo reglas explícitas.
- Ampliar organizaciones y colaboración, reforzando permisos y seguridad.
- Mejorar personalización de plantillas, trazabilidad, observabilidad y seguimiento de errores.
- Medir utilidad con usuarios reales y preparar el producto para un uso controlado en producción.

Son prioridades de desarrollo, no promesas comerciales.

## Qué demuestra este proyecto

PeerScope combina diseño de producto técnico, data engineering, analítica financiera, modelización de KPIs, sistemas interpretables, APIs, bases de datos, autenticación y permisos, IA fundamentada, testing, seguridad, despliegue y comunicación técnica. También refleja un desarrollo iterativo dirigido con agentes, manteniendo la responsabilidad sobre metodología y resultado.

> PeerScope demuestra mi capacidad para transformar un problema empresarial ambiguo en una metodología analítica estructurada, una arquitectura de software validada y un producto utilizable de apoyo a decisiones.
