# 📚 Bitácora de Autoevaluación — Unidad 2: Inferencia Estadística

**Estudiante:** Emily Salas

**Asignatura:** Teoría de la Distribución y Probabilidad — Ciclo 2do "A"

**Prácticas cubiertas:** APE 06 – APE 10
 
---
 
## Introducción
 
A lo largo de esta unidad trabajé sobre el mismo dataset regional de Global Forest Watch (pérdida de cobertura forestal en las provincias del Ecuador, con foco en Loja), aplicando herramientas cada vez más avanzadas.
 
---
 
## APE 06 — Distribuciones Continuas Notables
 
Aprendí a trabajar con la distribución Normal de forma aplicada, entendiendo cómo la media y la desviación estándar definen su forma. La dificultad principal fue distinguir cuándo usar la PDF (`scipy.stats.norm`) y cuándo la CDF: al inicio confundía ambas, hasta que entendí que para calcular probabilidades de intervalos siempre necesito la CDF, no la PDF.
 
## APE 07 — Distribuciones Muestrales y TLC mediante Simulación Estocástica
 
Fue la práctica más reveladora: simular miles de muestras y ver cómo la distribución de sus medias se aproxima a una Normal me hizo entender *por qué* podemos usar pruebas basadas en la Normal más adelante. El reto algorítmico fue estructurar bien el bucle de simulación —guardar la media de cada muestra en una lista aparte, no la muestra completa—, ya que al principio terminaba graficando los datos originales en vez de la distribución de las medias.
 
## APE 08 — Intervalos de Confianza (Z y T de Student)
 
Aprendí a construir intervalos de confianza y a decidir entre Z o T según si conocía o no la desviación poblacional. Me costó manejar bien el valor crítico (`stats.t.ppf()`, dividiendo alfa entre 2 para dos colas). También aprendí a filtrar por `threshold=30` antes de calcular, porque cada provincia aparece 8 veces en el dataset (una por cada umbral de densidad de dosel) y mezclarlas inflaba mis resultados.
 
## APE 09 — Pruebas de Hipótesis Paramétricas (Z y T) y Valor-p
 
Aquí interioricé la lógica de plantear H0/H1 y usar el valor-p como criterio objetivo. El error conceptual que más me costó desterrar fue pensar que el valor-p es "la probabilidad de que H0 sea verdadera", en vez de la probabilidad de un resultado tan extremo como el mío *asumiendo que H0 es cierta*. A nivel de código, tuve que aprender a usar bien el argumento `alternative` de `ttest_1samp` según cómo planteaba mi H1.
 
## APE 10 — ANOVA de 1 Factor y Prueba Post-Hoc de Tukey
 
Di el salto de comparar dos grupos a comparar varios a la vez, entendiendo por qué el ANOVA evita inflar el error tipo I frente a hacer varias pruebas T por pares. El mayor reto fue transformar mi dataset de formato ancho a largo con `pandas.melt()` para poder agrupar por provincia; también me costó interpretar bien la tabla de Tukey, entendiendo que un ANOVA significativo no implica que *todos* los pares difieran (en mi caso, Azuay y El Oro fueron la única pareja sin diferencia significativa).
 
---
 
## Reflexión General
 
El hilo conductor de la unidad fue aprender a **justificar** cada decisión estadística en vez de aplicar fórmulas de memoria: por qué Z o T, por qué una cola o dos, por qué T o ANOVA, y qué me obliga el valor-p a concluir. Lo más difícil no fue el código, sino leer mis propios resultados con sentido crítico —como cuando mi prueba unimuestral no rechazó H0 porque Loja tuvo *menos* pérdida forestal que el benchmark nacional, algo que no esperaba. Eso me enseñó que una H0 "no rechazada" también es un resultado válido, no un fracaso del análisis.
