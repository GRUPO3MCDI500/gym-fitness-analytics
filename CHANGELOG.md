# CHANGELOG - Proyecto ABP F1-F4

Proyecto: Análisis global de la industria fitness y gimnasios 2000-2026  
Curso: MCDI500 - Programación para la Ciencia de Datos  
Equipo: Grupo 3  
Integrantes: Wilson Arévalo, Luis Espinosa, Mauricio Ortega, Eduardo Garrido  

---

## Propósito del archivo

Este archivo registra la evolución técnica del proyecto ABP desde la Fase 1 hasta la Fase 4. Su objetivo es evidenciar trazabilidad, mejoras progresivas, decisiones técnicas, optimización del código, reproducibilidad y relación entre los cambios realizados y los requerimientos del proyecto final.

Debe mantenerse en la raíz del repositorio para que sea visible junto al `README.md`, los archivos de dependencias y la estructura general del proyecto.

Ruta recomendada:

```text
gym-fitness-analytics/CHANGELOG.md
```

---

## Resumen de evolución por fase

| Fase | Enfoque principal | Resultado técnico |
|---|---|---|
| F1 | Definición del problema y entorno reproducible | Problema, objetivos, repositorio, notebook inicial, README y CI/CD base |
| F2 | Limpieza y transformación de datos | Dataset procesado, variables derivadas, validaciones y pipeline reproducible |
| F3 | Núcleo algorítmico y POO | Algoritmos, mediciones de eficiencia, recursividad, grafos, clases y arquitectura modular |
| F4 | Integración y comunicación final | Visualizaciones finales, resultados, conclusiones, informe, presentación y repositorio final |

---

## Registro de cambios

| Fecha | Fase | Cambio realizado | Archivos o carpetas involucradas | Justificación técnica | Evidencia / Commit |
|---|---|---|---|---|---|
| 2026-06-05 | F1 | Creación de la estructura inicial del repositorio | `README.md`, `data/`, `notebooks/`, `docs/`, `reports/`, `.github/` | Organizar el proyecto bajo una estructura reproducible, separando datos, notebooks, documentación, reportes y automatizaciones. | Completar con hash o enlace del commit |
| 2026-06-05 | F1 | Incorporación del dataset original | `data/raw/clean_gym_data.csv` | Mantener el archivo fuente sin modificaciones para asegurar trazabilidad entre datos originales y transformados. | Completar con hash o enlace del commit |
| 2026-06-05 | F1 | Desarrollo del notebook inicial de definición | `notebooks/F1_Definicion.ipynb` | Documentar la problemática, objetivos, preguntas de análisis, carga inicial del dataset y exploración preliminar. | Completar con hash o enlace del commit |
| 2026-06-05 | F1 | Complemento del notebook de definición | `notebooks/F1_Definicion_v2.ipynb` | Reforzar la documentación metodológica, la validación de estructura y la conexión con el flujo reproducible del proyecto. | Completar con hash o enlace del commit |
| 2026-06-05 | F1 | Configuración inicial de dependencias | `requirements.txt` | Declarar librerías necesarias para ejecutar el proyecto en distintos equipos. | Completar con hash o enlace del commit |
| 2026-06-05 | F1 | Configuración de GitHub Actions | `.github/workflows/main.yml` | Automatizar validaciones de estructura, dependencias, dataset y notebooks para mejorar reproducibilidad. | Completar con hash o enlace del commit |
| 2026-06-05 | F1 | Incorporación de resumen automático de Pull Requests | `.github/workflows/ai-pr-summary.yml` | Apoyar la documentación colaborativa de cambios mediante GitHub Models. | Completar con hash o enlace del commit |
| 2026-06-05 | F1 | Documentación técnica inicial del proyecto | `README.md`, `docs/`, `reports/fase1/` | Registrar decisiones técnicas, estructura del repositorio, herramientas, problemática y evidencias de Fase 1. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Implementación del notebook de limpieza y transformación | `notebooks/F2_Limpieza_Transformacion.ipynb` | Construir un pipeline reproducible para obtener, limpiar, depurar, transformar y validar el dataset. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Estandarización de nombres de columnas | `notebooks/F2_Limpieza_Transformacion.ipynb` | Evitar errores por espacios, mayúsculas, caracteres inconsistentes o nombres poco manejables en Python. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Conversión de tipos de datos | `notebooks/F2_Limpieza_Transformacion.ipynb` | Asegurar que variables numéricas, temporales y categóricas puedan ser procesadas correctamente. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Tratamiento de valores nulos | `notebooks/F2_Limpieza_Transformacion.ipynb` | Mejorar integridad del dataset mediante imputación o sustitución controlada, evitando errores en análisis posteriores. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Revisión y eliminación de duplicados | `notebooks/F2_Limpieza_Transformacion.ipynb` | Evitar conteos o promedios distorsionados por registros repetidos. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Creación de variables derivadas | `data/processed/gym_data_processed.csv`, `notebooks/F2_Limpieza_Transformacion.ipynb` | Generar métricas comparables entre países: membresías por 100.000 habitantes, gimnasios por 100.000 habitantes, ingreso por membresía y periodo temporal. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Normalización de variables numéricas | `notebooks/F2_Limpieza_Transformacion.ipynb` | Permitir comparación entre variables de distinta escala sin reemplazar los valores originales. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Exportación del dataset procesado | `data/processed/gym_data_processed.csv` | Generar una versión limpia y validada del dataset para alimentar Fase 3 y Fase 4. | Completar con hash o enlace del commit |
| 2026-06-08 | F2 | Actualización del README con Fase 2 | `README.md` | Documentar el pipeline de limpieza, criterios de transformación, dataset procesado y reproducibilidad. | Completar con hash o enlace del commit |
| 2026-06-17 | F3 | Creación de carpeta modular para Fase 3 | `src/fase3/` | Separar los notebooks de desarrollo algorítmico de los notebooks iniciales F1-F2, manteniendo una organización escalable. | Completar con hash o enlace del commit |
| 2026-06-17 | F3 | Implementación del notebook de preprocesamiento F3 | `src/fase3/F3_01_Preprocesamiento.ipynb` | Reforzar validaciones del dataset procesado, asegurar columnas necesarias y dejar una base robusta para algoritmos y mediciones. | Completar con hash o enlace del commit |
| 2026-06-17 | F3 | Implementación de algoritmos estructurados | `src/fase3/F3_02_Algoritmos.ipynb` | Aplicar funciones con parámetros claros para ranking, máximo iterativo, promedio por región, búsqueda lineal y filtros. | Completar con hash o enlace del commit |
| 2026-06-17 | F3 | Implementación de algoritmos recursivos | `src/fase3/F3_02_Algoritmos.ipynb` | Aplicar recursividad y divide and conquer mediante máximo recursivo con slicing y versión optimizada por índices. | Completar con hash o enlace del commit |
| 2026-06-17 | F3 | Incorporación de grafo y DFS recursivo | `src/fase3/F3_02_Algoritmos.ipynb` | Demostrar una estrategia algorítmica adicional para relacionar regiones según similitud de indicadores. | Completar con hash o enlace del commit |
| 2026-06-17 | F3 | Validaciones de casos normales, límite y excepciones | `src/fase3/F3_02_Algoritmos.ipynb` | Comprobar robustez del código ante listas válidas, listas vacías, columnas inexistentes y escenarios extremos. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Implementación del notebook de mediciones | `src/fase3/F3_03_Mediciones.ipynb` | Medir tiempo y memoria de distintas implementaciones para justificar decisiones algorítmicas. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Comparación de algoritmos por complejidad | `src/fase3/F3_03_Mediciones.ipynb` | Comparar máximo iterativo, máximo recursivo con slicing, máximo recursivo optimizado, ranking y promedios regionales. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Generación de gráficos de eficiencia | `reports/fase3/figures/`, `src/fase3/F3_03_Mediciones.ipynb` | Guardar figuras de tiempo promedio y memoria pico como evidencia visual de eficiencia algorítmica. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Creación de carpeta de evidencias F3 | `reports/fase3/evidencias/` | Centralizar capturas de ejecución, validaciones, resultados y revisión del núcleo algorítmico. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Implementación del núcleo POO | `src/fase3/F3_04_Nucleo_POO.ipynb` | Incorporar clases con alta cohesión, bajo acoplamiento, encapsulamiento, herencia y polimorfismo. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Implementación de clases analíticas | `src/fase3/F3_04_Nucleo_POO.ipynb` | Encapsular responsabilidades mediante `DatasetFitness`, `AlgoritmoBase`, `RankingFitness`, `MaximoFitness`, `PromedioRegionalFitness`, `MedidorComplejidad` y `ExperimentoAlgoritmico`. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Integración de resultados de Fase 3 | `src/fase3/F3_05_Integrador_Resultados.ipynb` | Consolidar evidencias, decisiones técnicas, cumplimiento de requerimientos y síntesis de resultados F3. | Completar con hash o enlace del commit |
| 2026-06-18 | F3 | Documentación técnica F3 | `src/fase3/README_F3.md`, `requirements_f3.txt` | Explicar notebooks, orden de ejecución, dependencias, algoritmos, POO y evidencias esperadas. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Creación de carpeta modular para Fase 4 | `src/fase4/` | Separar la integración final, visualizaciones y conclusiones del núcleo algorítmico F3. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Implementación del notebook de integración final | `src/fase4/F4_01_Integracion_Final.ipynb` | Integrar F1-F4, validar dataset procesado y generar tablas de trazabilidad del proyecto final. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Implementación del notebook de visualizaciones finales | `src/fase4/F4_02_Visualizaciones_Finales.ipynb` | Construir visualizaciones analíticas para comunicar hallazgos del proyecto final. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Generación de visualización de evolución anual | `reports/fase4/figures/figura_1_evolucion_membresias.png` | Comunicar la evolución temporal de membresías fitness por cada 100.000 habitantes. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Generación de visualización de penetración regional | `reports/fase4/figures/figura_2_penetracion_region.png` | Comparar diferencias regionales en la penetración promedio de gimnasios. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Generación de visualización PIB-participación | `reports/fase4/figures/figura_3_pib_participacion.png` | Explorar la relación entre PIB per cápita y participación fitness. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Generación de visualización por periodo | `reports/fase4/figures/figura_4_comparacion_periodo.png` | Comparar indicadores entre periodos `pre_covid`, `covid` y `post_covid`. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Implementación del notebook de resultados y conclusiones | `src/fase4/F4_03_Resultados_Conclusiones.ipynb` | Sintetizar hallazgos, limitaciones, riesgos, recomendaciones y conclusiones para informe final. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Creación de carpeta de evidencias F4 | `reports/fase4/evidencias/` | Centralizar capturas de visualizaciones, ejecución de notebooks, README, changelog, commits y presentación. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Documentación técnica F4 | `src/fase4/README_F4.md`, `requirements_f4.txt` | Explicar notebooks F4, orden de ejecución, dependencias, visualizaciones y evidencias esperadas. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Creación del guion de presentación audiovisual | `docs/fase4/guion_presentacion_f4.md` | Preparar estructura de exposición de 5 a 8 minutos para Canvas Studio. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Creación de checklist de entrega final | `docs/fase4/checklist_f4.md` | Verificar informe, notebooks, repositorio, evidencias, presentación y bibliografía antes de entregar. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Creación de estructura del informe final | `docs/fase4/informe_f4_estructura.md` | Organizar el informe final en máximo 10 páginas de acuerdo con los requerimientos institucionales. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Actualización final del README | `README.md` | Integrar F1-F4, corregir conflictos de merge, documentar estructura actualizada, orden de ejecución, notebooks, figuras y evidencias. | Completar con hash o enlace del commit |
| 2026-06-19 | F4 | Consolidación del changelog final | `CHANGELOG.md` | Evidenciar trazabilidad de mejoras, decisiones técnicas y evolución del proyecto ABP completo. | Completar con hash o enlace del commit |

---

## Cambios destacados por dimensión técnica

### Reproducibilidad

- Se mantuvo el dataset original sin modificaciones en `data/raw/`.
- Se generó un dataset procesado en `data/processed/`.
- Se definieron rutas relativas para evitar dependencia de rutas locales.
- Se documentó el orden de ejecución de notebooks.
- Se incorporaron archivos de dependencias (`requirements.txt`, `requirements_f3.txt`, `requirements_f4.txt`).
- Se configuró GitHub Actions para validaciones automáticas.

### Calidad de datos

- Se estandarizaron nombres de columnas.
- Se revisaron valores nulos, duplicados y tipos de datos.
- Se aplicaron transformaciones e imputaciones controladas.
- Se crearon variables derivadas comparables entre países.
- Se validó el dataset procesado antes de usarlo en algoritmos y visualizaciones.

### Eficiencia algorítmica

- Se implementaron algoritmos iterativos y recursivos.
- Se compararon implementaciones de búsqueda de máximo.
- Se incorporó análisis de complejidad temporal y espacial.
- Se midió tiempo de ejecución y memoria pico.
- Se justificó la selección de enfoques más eficientes.

### Programación Orientada a Objetos

- Se implementó una estructura modular basada en clases.
- Se aplicó encapsulamiento mediante atributos internos y copias controladas del dataset.
- Se utilizó herencia a partir de una clase base común.
- Se demostró polimorfismo mediante ejecución uniforme de distintos algoritmos.
- Se favoreció alta cohesión y bajo acoplamiento.

### Visualización y comunicación

- Se generaron visualizaciones finales para comunicar tendencias temporales, diferencias regionales, relaciones socioeconómicas y comparación por periodos.
- Se organizaron figuras en `reports/fase4/figures/`.
- Se prepararon insumos para informe técnico y presentación audiovisual.
- Se documentaron hallazgos, limitaciones, riesgos y recomendaciones.

---

## Evidencias esperadas por fase

| Fase | Carpeta recomendada | Evidencias |
|---|---|---|
| F1 | `reports/fase1/evidencias/` | README inicial, notebook F1, CI/CD, dataset, estructura del repo |
| F2 | `reports/fase2/evidencias/` | Notebook F2, pipeline de limpieza, dataset procesado, validaciones |
| F3 | `reports/fase3/evidencias/` | Algoritmos, pruebas, mediciones, POO, integración |
| F3 | `reports/fase3/figures/` | Gráficos de tiempo y memoria |
| F4 | `reports/fase4/evidencias/` | Integración, visualizaciones, conclusiones, README, commits, presentación |
| F4 | `reports/fase4/figures/` | Figuras finales del proyecto |

---

## Commits sugeridos para dejar trazabilidad final

Los siguientes mensajes pueden usarse para los commits finales si aún no han sido registrados:

```bash
git add README.md CHANGELOG.md requirements_f3.txt requirements_f4.txt
git commit -m "Actualizar documentacion final del proyecto ABP F1-F4"
```

```bash
git add src/fase3 reports/fase3
git commit -m "Agregar nucleo algoritmico mediciones y POO Fase 3"
```

```bash
git add src/fase4 reports/fase4 docs/fase4
git commit -m "Agregar integracion visualizaciones y conclusiones Fase 4"
```

```bash
git add reports/fase4/evidencias reports/fase3/evidencias
git commit -m "Agregar evidencias de ejecucion Fase 3 y Fase 4"
```

---

## Pendientes antes de entrega final

- Completar la columna `Evidencia / Commit` con hash o enlace real de GitHub.
- Confirmar que todos los notebooks ejecutan sin errores.
- Confirmar que las figuras F3 y F4 fueron generadas correctamente.
- Guardar capturas de evidencia en las carpetas correspondientes.
- Actualizar `README.md` con la versión final.
- Verificar que `requirements.txt` incluya todas las dependencias necesarias.
- Exportar el informe final a PDF.
- Grabar y subir la presentación audiovisual a Canvas Studio.
- Completar autoevaluación y coevaluación en Canvas.

---

## Criterio de cierre

El proyecto se considera listo para entrega cuando el repositorio permite:

1. Comprender el problema y los objetivos del análisis.
2. Ejecutar el flujo completo desde datos crudos hasta visualizaciones finales.
3. Revisar el código, las mediciones y la arquitectura POO.
4. Identificar evidencias, figuras, informes y documentación.
5. Reconstruir la evolución técnica mediante commits, README y CHANGELOG.