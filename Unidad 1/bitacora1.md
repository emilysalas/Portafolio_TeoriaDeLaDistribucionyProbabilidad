# 📚 Bitácora de Autoevaluación — Unidad 1: Fundamentos de Probabilidad

**Estudiante:** Emily Salas


**Asignatura:** Teoría de la Distribución y Probabilidad — Ciclo 2do "A"


**Prácticas cubiertas:** APE 00 – APE 05
 
---
 
## APE 00 — Fundamentos de Probabilidad y Espacios Muestrales
 
Aprendí a construir espacios muestrales con `itertools` en vez de listarlos a mano. Lo más difícil fue traducir un evento descrito en palabras a una condición de filtrado correcta sobre ese espacio, sin dejar casos fuera ni contar de más.
 
## APE 01 — Variables Aleatorias y Distribuciones de Probabilidad
 
Entendí la diferencia entre una variable aleatoria y su distribución de probabilidad. El reto fue distinguir con seguridad variables discretas de continuas en casos límite, como conteos con rangos muy amplios que a simple vista parecían continuos.
 
## APE 02 — Distribuciones Muestrales y Teorema del Límite Central
 
Mi primer contacto con el TLC, simulando muestreo repetido para ver cómo las medias muestrales tienden a la normalidad. Al inicio confundía la población original con la distribución muestral, hasta que ordené bien el bucle de simulación.
 
## APE 03 — Variables Aleatorias Discretas y Continuas
 
Clasifiqué variables reales del dataset en discretas o continuas. Lo difícil fue justificar esa clasificación con criterios claros, en vez de decidir "a ojo".
 
## APE 004 — Momentos Estadísticos y Análisis de Tendencia Central
 
Calculé esperanza, varianza y tendencia central primero con bucles `for` y luego contrastando con NumPy. Mis resultados no coincidían al inicio porque usaba la fórmula de varianza poblacional cuando el caso pedía la muestral (`ddof=1`).
 
## APE 05 — Distribuciones Discretas Notables
 
Trabajé con Binomial y Poisson aplicadas a conteo de eventos. Lo más difícil fue reconocer, según el enunciado, qué distribución correspondía (ensayos fijos vs. eventos en un intervalo), ya que confundirlas daba resultados parecidos pero conceptualmente incorrectos.
 
---
 
## Reflexión General
 
El hilo conductor de la unidad fue aprender a **modelar** antes de calcular: identificar bien el espacio muestral, clasificar la variable y elegir la distribución correcta. La mayoría de mis errores fueron de interpretación previa al código, no de sintaxis en Python.
