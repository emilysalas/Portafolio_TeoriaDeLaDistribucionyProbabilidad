# 📚 Bitácora de Autoevaluación — Unidad 3: Inferencia, Regresión y Modelado Predictivo

**Estudiante:** Emily Salas

**Asignatura:** Teoría de la Distribución y Probabilidad — Ciclo 2do "A"

---

## APE 11 - Inferencia Estadística Multigrupo (ANOVA y Tukey)
Aprendí a comparar las medias de tres o más grupos simultáneamente usando ANOVA de un factor (`scipy.stats.f_oneway`). Como reto principal, primero validé la igualdad de varianzas con la prueba de Levene y, dado que el ANOVA solo indica si al menos un grupo es diferente pero no cuál, utilicé la prueba Post-Hoc de Tukey (`pairwise_tukeyhsd`) para identificar con exactitud los pares que presentaban diferencias significativas.

---

## APE 12 - Análisis Bivariado y Predicción (Pearson y OLS)
Evalué la fuerza y dirección de la relación entre dos variables continuas con el Coeficiente de Correlación de Pearson ($r$) y ajusté un modelo de Regresión Lineal Simple por Mínimos Cuadrados Ordinarios (OLS)[cite: 2]. El desafío clave fue auditar el modelo analizando los residuos para confirmar que cumplieran los supuestos de normalidad y homocedasticidad, garantizando así predicciones confiables.

---

## APE 13 - Análisis Predictivo Multivariado (Regresión Múltiple y VIF)
Extendí el análisis a múltiples variables independientes para predecir un resultado continuo mediante Regresión Lineal Múltiple. Durante este proceso, aprendí a detectar la multicolinealidad (cuando las variables explicativas están fuertemente correlacionadas entre sí) calculando el Factor de Inflación de la Varianza (VIF), asegurando que los coeficientes del modelo fueran estables e interpretables.

---

## APE 14 - Modelado Probabilístico Avanzado (Regresión Logística y Matriz de Confusión)
Pasé de predecir valores continuos a clasificar eventos binarios (sí/no) mediante la implementación de algoritmos de Regresión Logística. Para evaluar el rendimiento del clasificador, construí e interpreté la Matriz de Confusión, analizando métricas clave como exactitud, precisión, sensibilidad (*recall*) y los errores de tipo I y II.

---

## APE 15 - Evaluación Avanzada de Modelos (Curvas ROC, AUC y K-Fold)
Implementé técnicas avanzadas para validar el rendimiento global de los modelos de clasificación y su capacidad de generalización. Grafiqué curvas ROC y calculé el Área Bajo la Curva (AUC) para medir la separación entre clases, además de aplicar Validación Cruzada ($K$-Fold) para probar el modelo en distintas divisiones de datos y evitar el sobreajuste (*overfitting*).

---

### 💡 Reflexión General
A lo largo de estas prácticas, la clave fue avanzar desde la comparación básica de grupos hasta la creación y evaluación rigurosa de modelos predictivos. Comprendí que no basta con entrenar un algoritmo; la verdadera validez radica en diagnosticar sus supuestos (Levene, VIF, análisis de residuos) y evaluar su rendimiento real en datos no vistos mediante validación cruzada y métricas robustas (ROC/AUC).
