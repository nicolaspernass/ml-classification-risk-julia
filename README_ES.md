# Clasificación con Aprendizaje Automático bajo Riesgo (Julia)

## Descripción del Proyecto
Proyecto de clasificación con aprendizaje automático centrado en la toma de decisiones bajo riesgo asimétrico.
El objetivo fue comparar distintos modelos supervisados y seleccionar aquellos más adecuados priorizando la reducción de errores de alto coste, en lugar de basarse únicamente en la precisión global.

## Conjunto de Datos
- Conjunto de datos real de clasificación binaria (UCI Sonar)
- Tarea: distinguir entre dos clases a partir de características numéricas
- Los costes de error son asimétricos:
  - Los falsos negativos son más críticos que los falsos positivos
- Las características del dataset influyeron en la selección de modelos y métricas

## Metodología

### Exploración y Preprocesado
- Análisis exploratorio para estudiar la distribución de variables y clases
- Normalización mediante escalado Min-Max
- Preprocesado uniforme aplicado a todos los modelos para garantizar comparabilidad

### Entrenamiento de Modelos
Todos los modelos se implementaron y evaluaron en Julia:

- Redes Neuronales
- Máquinas de Vectores de Soporte (SVM)
- k-Vecinos más Cercanos (kNN)
- Árboles de Decisión
- DoME (algoritmo simbólico personalizado)

Se ajustaron hiperparámetros para analizar los compromisos entre rendimiento y complejidad.

### Estrategia de Evaluación
Los modelos se evaluaron utilizando:
- F1-score
- Sensibilidad (Recall)

Estas métricas se priorizaron debido al coste asimétrico de los errores, donde no detectar casos críticos resulta más grave que generar falsas alarmas.

Se utilizó validación cruzada para mejorar la robustez y evitar sobreajuste.

## Selección del Modelo
Varios modelos obtuvieron resultados similares.
La selección final se basó en:
- Sensibilidad frente a errores de alto coste
- Estabilidad entre particiones de validación
- Equilibrio entre rendimiento predictivo y riesgo

El proyecto enfatiza la toma de decisiones basada en métricas alineadas con restricciones reales.

## Resultados
- F1-scores similares entre distintos modelos
- Preferencia por modelos con mayor sensibilidad
- Análisis explícito de compromisos entre complejidad, interpretabilidad y rendimiento

## Herramientas
- Julia
- Librerías de aprendizaje automático
- Herramientas de análisis estadístico y visualización

## Conclusiones Clave
- La selección de modelos debe reflejar el riesgo operativo o de negocio
- La precisión global no es suficiente cuando los costes de error son asimétricos
- Comparar modelos diversos mejora la calidad de la decisión

## Nota
Este proyecto fue desarrollado en el contexto de una asignatura de aprendizaje automático y se presenta como ejemplo de razonamiento aplicado y evaluación orientada a la toma de decisiones.
