# Análisis global de la industria fitness y gimnasios 2000-2026

## Integrantes

- Wilson Arévalo
- Luis Espinosa
- Mauricio Ortega
- Eduardo Garrido

---

## Descripción del proyecto

Este proyecto corresponde al ABP del curso **MCDI500 — Programación para la Ciencia de Datos** y tiene como propósito iniciar un flujo de trabajo reproducible para analizar la evolución global de la industria fitness y gimnasios entre los años 2000 y 2026.

El análisis se basa en el dataset **World Gym & Fitness Trends 2000-2026**, disponible en formato CSV bajo el archivo `clean_gym_data.csv`. Este conjunto de datos contiene información sobre membresías de gimnasio, participación fitness, ingresos del sector, cantidad de gimnasios, tasa de penetración, PIB per cápita, urbanización, obesidad e inactividad física en distintos países y regiones.

En la Fase 1 se define la problemática, se formulan los objetivos, se organiza el repositorio, se configura el entorno inicial de trabajo, se crea el notebook base, se documentan las primeras decisiones técnicas y se implementan validaciones automáticas mediante GitHub Actions.

Además, se incorpora GitHub Models para apoyar la documentación automática de Pull Requests y una Wiki técnica para profundizar las decisiones metodológicas, la trazabilidad del dataset, el flujo reproducible y la gestión de evidencias.

En la Fase 2 se incorpora el notebook de obtención, limpieza, depuración, transformación y validación técnica del dataset. Esta fase complementa el trabajo realizado en la Fase 1, avanzando desde la definición y exploración inicial hacia la preparación técnica de los datos para análisis posteriores.

El proceso de Fase 2 mantiene la trazabilidad entre el archivo original ubicado en `data/raw/clean_gym_data.csv` y el archivo procesado generado en `data/processed/gym_data_processed.csv`, asegurando que las transformaciones aplicadas sean reproducibles, documentadas y verificables.

En la Fase 3 se incorpora el núcleo algorítmico del proyecto mediante notebooks ubicados en `src/fase3/`. Esta fase implementa programación estructurada, recursividad, estrategias divide and conquer, exploración de grafos mediante DFS recursivo, mediciones de tiempo y memoria, y un núcleo de Programación Orientada a Objetos con encapsulamiento, herencia y polimorfismo.

En la Fase 4 se consolida el proyecto final mediante notebooks ubicados en `src/fase4/`. Esta fase integra los resultados F1-F4, construye visualizaciones analíticas finales, sintetiza hallazgos, limitaciones, riesgos, recomendaciones y conclusiones, y entrega insumos para el informe técnico final y la presentación audiovisual en Canvas Studio.

---

## Problemática

La industria fitness y de gimnasios ha crecido de manera desigual a nivel mundial entre 2000 y 2026. Existen diferencias importantes entre países y regiones en cuanto a membresías, número de gimnasios, ingresos del sector, acceso a servicios fitness y participación de la población en actividades físicas.

A partir de esta situación, el proyecto busca comprender qué factores económicos, de acceso y de salud pública se relacionan con el crecimiento y adopción de la industria fitness a nivel global.

Esta problemática requiere un análisis reproducible, ya que el estudio involucra múltiples variables, países, regiones y años. Por ello, el proyecto no solo se enfoca en analizar datos, sino también en documentar cómo se organizan, validan, versionan y reproducen los procesos técnicos asociados al análisis.

---

## Objetivo general

Analizar la evolución global de la industria fitness y gimnasios entre 2000 y 2026, identificando la relación entre el crecimiento del sector, el acceso a gimnasios, las condiciones económicas de los países y los indicadores de salud pública, mediante un flujo de trabajo reproducible apoyado en herramientas científicas colaborativas.

---

## Objetivos específicos

- Identificar las variables principales del dataset y su relación con la problemática del proyecto.
- Organizar una estructura inicial de repositorio que permita mantener trazabilidad y reproducibilidad.
- Implementar un notebook inicial de Fase 1 con carga, exploración y revisión preliminar del dataset.
- Implementar un notebook de Fase 2 para la obtención, limpieza, depuración, transformación y validación técnica del dataset.
- Documentar el proceso técnico mediante README, notebook, Wiki y archivos de apoyo.
- Utilizar Git y GitHub para registrar avances mediante commits descriptivos.
- Configurar validaciones automáticas mediante GitHub Actions.
- Ejecutar automáticamente el notebook en CI para comprobar su reproducibilidad.
- Ejecutar automáticamente el notebook de Fase 2 mediante GitHub Actions para comprobar la reproducibilidad del pipeline de datos.
- Incorporar GitHub Models para generar resúmenes automáticos de Pull Requests.
- Definir criterios iniciales para limpieza, validación y trazabilidad de datos.
- Preparar la base técnica para las siguientes fases del proyecto ABP.
- Implementar notebooks de Fase 3 con algoritmos estructurados, recursivos, mediciones de complejidad y Programación Orientada a Objetos.
- Comparar implementaciones algorítmicas mediante mediciones reproducibles de tiempo y memoria.
- Implementar notebooks de Fase 4 para integrar resultados, construir visualizaciones finales y sintetizar hallazgos.
- Mantener trazabilidad de mejoras mediante `CHANGELOG.md`, evidencias y commits descriptivos.

---

## Preguntas de análisis

- ¿Cómo ha evolucionado la cantidad de membresías de gimnasio entre 2000 y 2026?
- ¿Qué países o regiones presentan mayor penetración de gimnasios?
- ¿Existe relación entre PIB per cápita y tasa de penetración de gimnasios?
- ¿Cómo se relacionan la obesidad y la inactividad física con la participación fitness?
- ¿Qué cambios se observan en la industria fitness antes, durante y después del periodo COVID-19?
- ¿Qué variables podrían ser útiles para predecir la penetración de gimnasios en fases posteriores?

---

## Dataset utilizado

| Elemento | Descripción |
|---|---|
| Nombre del dataset | World Gym & Fitness Trends 2000-2026 |
| Archivo utilizado | `clean_gym_data.csv` |
| Archivo procesado | `gym_data_processed.csv` |
| Fuente | Kaggle |
| Periodo de análisis | 2000-2026 |
| Unidad de análisis | Países y regiones |
| Ubicación original | `data/raw/clean_gym_data.csv` |
| Ubicación procesada | `data/processed/gym_data_processed.csv` |

El archivo ubicado en `data/raw/` se conserva como fuente original sin modificaciones. Las transformaciones realizadas durante la Fase 2 se exportan a `data/processed/`, manteniendo trazabilidad entre los datos originales y los datos procesados.

El archivo se mantiene en `data/raw/` para conservar una copia original sin modificaciones. En fases posteriores, cualquier versión transformada o procesada deberá almacenarse en `data/processed/`, manteniendo la trazabilidad entre el dato original y las versiones derivadas.

---

## Variables principales

El dataset contiene variables relacionadas con industria fitness, economía, territorio y salud pública:

| Variable | Descripción general |
|---|---|
| `country` | País registrado en el dataset. |
| `region` | Región geográfica asociada al país. |
| `year` | Año del registro. |
| `gym_memberships` | Cantidad de membresías de gimnasio. |
| `fitness_participation_rate` | Tasa de participación en actividades fitness. |
| `total_health_club_revenue_usd` | Ingresos totales de la industria fitness en USD. |
| `number_of_gyms` | Número de gimnasios registrados. |
| `gym_penetration_rate` | Tasa de penetración de gimnasios. |
| `urban_population_percentage` | Porcentaje de población urbana. |
| `obesity_rate` | Tasa de obesidad. |
| `gdp_per_capita_usd` | PIB per cápita en USD. |
| `population_total` | Población total del país. |
| `average_membership_cost_usd` | Costo promedio de membresía en USD. |
| `insufficient_physical_activity_pct` | Porcentaje de actividad física insuficiente. |

---

## Variables derivadas de Fase 2

Durante la Fase 2 se generan nuevas variables para apoyar análisis posteriores:

| Variable | Descripción general |
|---|---|
| `memberships_per_100k` | Cantidad de membresías por cada 100.000 habitantes. |
| `gyms_per_100k` | Cantidad de gimnasios por cada 100.000 habitantes. |
| `revenue_per_membership_usd` | Ingreso estimado por membresía. |
| `periodo` | Clasificación temporal del registro: `pre_covid`, `covid` o `post_covid`. |

Además, se crean variables normalizadas con sufijo `_norm`, aplicando normalización min-max sobre variables numéricas seleccionadas. Estas columnas permiten comparar variables con escalas diferentes sin reemplazar los valores originales.

---

## Herramientas utilizadas

| Herramienta | Uso dentro del proyecto |
|---|---|
| Python | Lenguaje principal para análisis de datos. |
| Pandas | Carga, manipulación, limpieza, transformación y exploración de datos. |
| NumPy | Apoyo en operaciones numéricas y creación de variables derivadas. |
| Matplotlib | Visualización inicial de datos. |
| Jupyter Notebook | Desarrollo del análisis reproducible mediante código y celdas narrativas. |
| Git | Control de versiones local. |
| GitHub | Repositorio remoto y colaboración grupal. |
| GitHub Desktop | Gestión visual de commits, cambios y sincronización con GitHub. |
| GitHub Actions | Validación automática de estructura, dependencias, dataset y notebooks. |
| GitHub Models | Generación automática de resúmenes técnicos en Pull Requests. |
| GitHub Wiki | Documentación técnica ampliada del proyecto. |

---

## Justificación técnica de herramientas

El uso de estas herramientas responde a la necesidad de construir un flujo reproducible, trazable y colaborativo.

- **Python y Pandas** permiten cargar, revisar y transformar el dataset de forma programática, evitando procesos manuales difíciles de replicar.
- **Jupyter Notebook** permite integrar código, resultados, visualizaciones y explicación metodológica en un mismo documento ejecutable.
- **Git y GitHub** permiten registrar la evolución del proyecto mediante commits, ramas y Pull Requests.
- **requirements.txt** permite reconstruir el entorno de ejecución con las dependencias necesarias.
- **GitHub Actions** permite validar automáticamente que la estructura, dependencias, dataset y notebook funcionen correctamente.
- **GitHub Models** permite documentar automáticamente el impacto técnico de los cambios realizados en Pull Requests.
- **GitHub Wiki** permite ampliar la documentación técnica sin sobrecargar el README.

Esta combinación de herramientas permite que el proyecto no dependa exclusivamente del computador local de un integrante, sino que pueda ejecutarse, revisarse y validarse desde un entorno común.

---

## Estructura del repositorio

```text
gym-fitness-analytics/
│
├── README.md
├── requirements.txt
├── .gitignore
├── .gitattributes
│
├── .github/
│   └── workflows/
│       ├── main.yml
│       └── ai-pr-summary.yml
│
├── data/
│   ├── raw/
│   │   └── clean_gym_data.csv
│   └── processed/
│       ├── .gitkeep
│       └── gym_data_processed.csv
│
├── notebooks/
│   ├── F1_Definicion.ipynb
│   ├── F1_Definicion_v2.ipynb
│   └── F2_Limpieza_Transformacion.ipynb
│
├── src/
│   └── .gitkeep
│
├── outputs/
│   ├── figures/
│   │   └── .gitkeep
│   └── tables/
│       └── .gitkeep
│
├── docs/
│   └── mapa_conceptual.pdf
│
└── reports/
    ├── fase1/
    │   ├── informe_tecnico_fase1.pdf
    │   └── evidencias/
    │
    └── fase2/
        ├── informe_tecnico_fase2.pdf
        └── evidencias/
```

---

## Estructura actualizada para F1-F4

La estructura base anterior se mantiene, pero para la entrega final se complementa con las carpetas de Fase 3 y Fase 4:

```text
gym-fitness-analytics/
│
├── README.md
├── CHANGELOG.md
├── requirements.txt
├── requirements_f3.txt
├── requirements_f4.txt
│
├── data/
│   ├── raw/
│   │   └── clean_gym_data.csv
│   └── processed/
│       └── gym_data_processed.csv
│
├── notebooks/
│   ├── F1_Definicion.ipynb
│   ├── F1_Definicion_v2.ipynb
│   └── F2_Limpieza_Transformacion.ipynb
│
├── src/
│   ├── fase3/
│   │   ├── F3_01_Preprocesamiento.ipynb
│   │   ├── F3_02_Algoritmos.ipynb
│   │   ├── F3_03_Mediciones.ipynb
│   │   ├── F3_04_Nucleo_POO.ipynb
│   │   ├── F3_05_Integrador_Resultados.ipynb
│   │   └── README_F3.md
│   │
│   └── fase4/
│       ├── F4_01_Integracion_Final.ipynb
│       ├── F4_02_Visualizaciones_Finales.ipynb
│       ├── F4_03_Resultados_Conclusiones.ipynb
│       └── README_F4.md
│
├── docs/
│   ├── mapa_conceptual.pdf
│   └── fase4/
│       ├── informe_f4_estructura.md
│       ├── guion_presentacion_f4.md
│       └── checklist_f4.md
│
└── reports/
    ├── fase1/evidencias/
    ├── fase2/evidencias/
    ├── fase3/
    │   ├── figures/
    │   └── evidencias/
    └── fase4/
        ├── figures/
        └── evidencias/
```

---

## Función de las carpetas principales

| Carpeta | Uso |
|---|---|
| `data/raw/` | Contiene el dataset original sin modificaciones. |
| `data/processed/` | Contiene versiones procesadas o limpias del dataset generadas durante la Fase 2. |
| `notebooks/` | Contiene notebooks reproducibles del análisis. |
| `src/` | Guardará scripts reutilizables en fases futuras. |
| `outputs/figures/` | Guardará gráficos generados durante el análisis. |
| `outputs/tables/` | Guardará tablas derivadas del análisis. |
| `docs/` | Contiene documentación de apoyo, mapa conceptual y referencias técnicas. |
| `reports/fase1/` | Contiene informe técnico y evidencias de la Fase 1. |
| `reports/fase2/` | Contiene informe técnico y evidencias asociadas a la Fase 2. |
| `.github/workflows/` | Contiene workflows de GitHub Actions. |
| `src/fase3/` | Contiene notebooks de núcleo algorítmico, mediciones de complejidad y Programación Orientada a Objetos. |
| `src/fase4/` | Contiene notebooks de integración final, visualizaciones, resultados y conclusiones. |
| `reports/fase3/figures/` | Contiene gráficos de mediciones de algoritmos generados en Fase 3. |
| `reports/fase3/evidencias/` | Contiene capturas y evidencias de ejecución de notebooks Fase 3. |
| `reports/fase4/figures/` | Contiene las visualizaciones finales del proyecto. |
| `reports/fase4/evidencias/` | Contiene capturas y evidencias para informe final y presentación audiovisual. |

---

## Reproducibilidad técnica

Para reproducir este proyecto, se recomienda clonar el repositorio, instalar las dependencias declaradas en `requirements.txt` y ejecutar los notebooks correspondientes a cada fase.

### Instalación de dependencias

Desde la carpeta raíz del repositorio:

```bash
pip install -r requirements.txt
```

### Dependencias principales

El archivo `requirements.txt` contiene:

```text
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
jupyter>=1.0.0
notebook>=7.0.0
ipykernel>=6.0.0
nbconvert>=7.0.0
```

### Orden general de ejecución F1-F4

```text
1. notebooks/F1_Definicion.ipynb
2. notebooks/F1_Definicion_v2.ipynb
3. notebooks/F2_Limpieza_Transformacion.ipynb
4. src/fase3/F3_01_Preprocesamiento.ipynb
5. src/fase3/F3_02_Algoritmos.ipynb
6. src/fase3/F3_03_Mediciones.ipynb
7. src/fase3/F3_04_Nucleo_POO.ipynb
8. src/fase3/F3_05_Integrador_Resultados.ipynb
9. src/fase4/F4_01_Integracion_Final.ipynb
10. src/fase4/F4_02_Visualizaciones_Finales.ipynb
11. src/fase4/F4_03_Resultados_Conclusiones.ipynb
```

El archivo `data/processed/gym_data_processed.csv` debe existir antes de ejecutar los notebooks de Fase 3 y Fase 4. Si no existe, se debe ejecutar primero `notebooks/F2_Limpieza_Transformacion.ipynb` o `src/fase3/F3_01_Preprocesamiento.ipynb`.

### Ejecución del notebook Fase 1

El notebook principal de Fase 1 se encuentra en:

```text
notebooks/F1_Definicion.ipynb
```

También se mantiene una versión actualizada o complementaria:

```text
notebooks/F1_Definicion_v2.ipynb
```

Para ejecutarlo localmente:

1. Abrir Jupyter Notebook o JupyterLab.
2. Entrar a la carpeta del repositorio.
3. Abrir la carpeta `notebooks`.
4. Ejecutar el archivo `F1_Definicion.ipynb` o `F1_Definicion_v2.ipynb`.
5. Ejecutar las celdas en orden.

El notebook carga el dataset desde la ruta relativa:

```python
from pathlib import Path

DATA_PATH = Path("../data/raw/clean_gym_data.csv")
```

Esta ruta permite que el notebook funcione correctamente siempre que se respete la estructura del repositorio.

### Ejecución del notebook Fase 2

El notebook principal de Fase 2 se encuentra en:

```text
notebooks/F2_Limpieza_Transformacion.ipynb
```

Para ejecutarlo localmente:

1. Abrir Jupyter Notebook o JupyterLab.
2. Entrar a la carpeta del repositorio `gym-fitness-analytics`.
3. Abrir la carpeta `notebooks`.
4. Ejecutar el archivo `F2_Limpieza_Transformacion.ipynb`.
5. Ejecutar las celdas en orden.

El notebook toma como entrada el dataset original:

```text
data/raw/clean_gym_data.csv
```

y genera como salida el archivo procesado:

```text
data/processed/gym_data_processed.csv
```

---

## Flujo reproducible del proyecto

El flujo reproducible se organiza en la siguiente secuencia:

```text
Definición del problema
        ↓
Adquisición y organización del dataset
        ↓
Exploración inicial
        ↓
Limpieza y preparación de datos
        ↓
Análisis exploratorio
        ↓
Visualización de resultados
        ↓
Interpretación y documentación
        ↓
Versionamiento y validación automática
```

Cada etapa cumple una función específica:

| Etapa | Propósito |
|---|---|
| Definición | Delimitar problemática, objetivos y preguntas de análisis. |
| Adquisición | Incorporar el dataset en `data/raw/`. |
| Exploración | Revisar dimensiones, columnas, tipos, nulos y duplicados. |
| Limpieza | Definir criterios para tratar datos faltantes, duplicados y valores atípicos. |
| Análisis | Comparar países, regiones, años y relaciones entre variables. |
| Visualización | Generar gráficos y tablas interpretables. |
| Documentación | Registrar decisiones, hallazgos y configuraciones. |
| Validación | Verificar estructura, dataset y notebook mediante GitHub Actions. |

---

## Notebook Fase 1

El archivo `F1_Definicion.ipynb` contiene:

- Contexto del proyecto.
- Problemática.
- Objetivo general y objetivos específicos.
- Preguntas centrales de análisis.
- Descripción del dataset.
- Herramientas utilizadas.
- Carga inicial de librerías.
- Carga del dataset desde `data/raw`.
- Revisión de dimensiones del dataset.
- Revisión de columnas.
- Revisión de tipos de datos.
- Revisión de valores nulos.
- Revisión de duplicados.
- Resumen estadístico inicial.
- Función simple de exploración.
- Primeras visualizaciones.
- Decisiones técnicas iniciales.
- Vinculación con el mapa conceptual.
- Proyección para fases posteriores.

La versión `F1_Definicion_v2.ipynb` complementa el trabajo inicial de Fase 1 con mayor documentación metodológica, validaciones adicionales, relación con CI/CD, GitHub Models y proyección hacia fases posteriores.

---

## Notebook Fase 2

El archivo `F2_Limpieza_Transformacion.ipynb` contiene el pipeline de obtención, limpieza, depuración, transformación y validación técnica del dataset.

Este notebook implementa:

- Carga reproducible del dataset original.
- Validación de existencia del archivo fuente.
- Validación de columnas esperadas.
- Diagnóstico inicial de calidad de datos.
- Revisión de tipos de datos.
- Revisión de valores nulos.
- Revisión de registros duplicados.
- Limpieza de nombres de columnas.
- Conversión de variables numéricas y categóricas.
- Validación de rangos para tasas, porcentajes y variables no negativas.
- Revisión de consistencia temporal.
- Revisión de consistencia país-región.
- Creación de variables derivadas.
- Normalización min-max de variables seleccionadas.
- Comparación antes/después del procesamiento.
- Exportación del dataset procesado.
- Verificación de existencia y carga del archivo generado.
- Bitácora de transformaciones aplicadas.
- Documentación técnica integrada mediante Markdown y comentarios.

### Pipeline de Fase 2

```text
Carga del dataset original
        ↓
Copia de trabajo
        ↓
Diagnóstico inicial
        ↓
Validación de columnas esperadas
        ↓
Limpieza y estandarización
        ↓
Casting de tipos de datos
        ↓
Tratamiento de duplicados
        ↓
Tratamiento de valores nulos
        ↓
Validación de rangos
        ↓
Transformación de variables
        ↓
Creación de variables derivadas
        ↓
Normalización
        ↓
Validación del dataset procesado
        ↓
Exportación a data/processed/
```

### Criterios de limpieza aplicados en Fase 2

Los criterios de limpieza definidos para esta fase son:

- No modificar directamente el archivo original ubicado en `data/raw/`.
- Trabajar sobre una copia del DataFrame original.
- Estandarizar nombres de columnas.
- Convertir variables numéricas mediante `pd.to_numeric`.
- Convertir variables categóricas a texto y eliminar espacios laterales.
- Eliminar duplicados exactos si existen.
- Reemplazar valores nulos categóricos por `No especificado`.
- Reemplazar valores nulos numéricos por la mediana de cada variable.
- No imputar la variable `year`, ya que define la estructura temporal del dataset.
- Validar tasas y porcentajes dentro del rango 0 a 1.
- Validar variables de conteo o monto como valores no negativos.
- Documentar cada transformación aplicada.

---

## Notebook Fase 3

La Fase 3 implementa el núcleo algorítmico, las mediciones de eficiencia y la Programación Orientada a Objetos del proyecto. Los notebooks se ubican en:

```text
src/fase3/
```

| Notebook | Propósito |
|---|---|
| `F3_01_Preprocesamiento.ipynb` | Reutiliza y refuerza el pipeline de limpieza, transformación, validación y exportación del dataset procesado. |
| `F3_02_Algoritmos.ipynb` | Implementa algoritmos estructurados, recursivos, divide and conquer, búsqueda lineal, filtros y grafo con DFS recursivo. |
| `F3_03_Mediciones.ipynb` | Mide tiempo y memoria de los algoritmos, genera gráficos comparativos y justifica la elección algorítmica. |
| `F3_04_Nucleo_POO.ipynb` | Implementa el núcleo orientado a objetos con clases, encapsulamiento, herencia, polimorfismo, mediciones y validaciones. |
| `F3_05_Integrador_Resultados.ipynb` | Integra resultados de Fase 3, evidencia cumplimiento técnico y apoya la redacción del informe. |

### Algoritmos implementados en Fase 3

| Algoritmo | Tipo | Complejidad temporal | Complejidad espacial |
|---|---|---|---|
| Ranking iterativo | Estructurado | O(n log n) | O(n) |
| Máximo iterativo | Estructurado | O(n) | O(1) |
| Máximo recursivo con slicing | Recursivo | O(n) | O(n) |
| Máximo recursivo optimizado | Recursivo optimizado | O(n) | O(log n) |
| Promedio manual por región | Estructurado | O(n) | O(k) |
| Promedio Pandas por región | Pandas groupby | O(n) aprox. | O(k) |
| DFS recursivo sobre grafo regional | Recursivo / grafos | O(V + E) | O(V) |

### Programación Orientada a Objetos en Fase 3

El notebook `F3_04_Nucleo_POO.ipynb` implementa:

- `DatasetFitness`
- `AlgoritmoBase`
- `RankingFitness`
- `MaximoFitness`
- `PromedioRegionalFitness`
- `MedidorComplejidad`
- `ExperimentoAlgoritmico`

Se aplican principios de encapsulamiento, herencia, polimorfismo, alta cohesión, bajo acoplamiento y métodos documentados.

### Figuras y evidencias de Fase 3

```text
reports/fase3/figures/grafico_tiempo_algoritmos.png
reports/fase3/figures/grafico_memoria_algoritmos.png
reports/fase3/evidencias/
```

---

## Notebook Fase 4

La Fase 4 integra los resultados finales del proyecto, construye visualizaciones analíticas y genera insumos para el informe final y la presentación audiovisual. Los notebooks se ubican en:

```text
src/fase4/
```

| Notebook | Propósito |
|---|---|
| `F4_01_Integracion_Final.ipynb` | Integra las fases F1-F4, valida el dataset procesado y genera tablas de trazabilidad. |
| `F4_02_Visualizaciones_Finales.ipynb` | Construye visualizaciones finales y las guarda en `reports/fase4/figures/`. |
| `F4_03_Resultados_Conclusiones.ipynb` | Sintetiza hallazgos, limitaciones, riesgos, recomendaciones y conclusiones. |

### Visualizaciones finales Fase 4

| Figura | Descripción |
|---|---|
| `figura_1_evolucion_membresias.png` | Evolución anual de membresías fitness por cada 100.000 habitantes. |
| `figura_2_penetracion_region.png` | Penetración promedio de gimnasios por región. |
| `figura_3_pib_participacion.png` | Relación entre PIB per cápita y participación fitness. |
| `figura_4_comparacion_periodo.png` | Comparación de indicadores fitness por periodo. |

Estas figuras se guardan en:

```text
reports/fase4/figures/
```

### Evidencias Fase 4

```text
reports/fase4/evidencias/
```

Evidencias recomendadas:

```text
01_f4_integracion_dataset.png
02_f4_visualizacion_1.png
03_f4_visualizacion_2.png
04_f4_visualizacion_3.png
05_f4_visualizacion_4.png
06_f4_resultados_conclusiones.png
07_readme_actualizado.png
08_changelog.png
09_commits_f4.png
10_presentacion_canvas.png
```

---

## Ejecución automática de notebooks en CI

Como mejora de reproducibilidad, los notebooks se ejecutan automáticamente mediante GitHub Actions usando `nbconvert`.

El workflow ejecuta los notebooks desde la carpeta `notebooks/` para que la ruta relativa al dataset funcione correctamente.

Comando utilizado para Fase 1:

```bash
jupyter nbconvert --to notebook --execute F1_Definicion_v2.ipynb --output F1_Definicion_v2_ejecutado.ipynb --ExecutePreprocessor.timeout=300 --ExecutePreprocessor.kernel_name=python3
```

Comando utilizado para Fase 2:

```bash
jupyter nbconvert --to notebook --execute F2_Limpieza_Transformacion.ipynb --output F2_Limpieza_Transformacion_ejecutado.ipynb --ExecutePreprocessor.timeout=300 --ExecutePreprocessor.kernel_name=python3
```

Esta validación permite comprobar que:

- Los notebooks existen.
- Las dependencias están instaladas.
- El dataset se encuentra en la ruta esperada.
- Las rutas relativas funcionan.
- Las celdas se ejecutan sin errores.
- El notebook de Fase 2 genera el dataset procesado.
- El análisis no depende de un entorno local específico.

El kernel se fuerza a `python3` para evitar errores asociados a kernels locales de Anaconda u otros entornos.

---

## Control de versiones

El proyecto utiliza Git y GitHub para mantener trazabilidad de los avances. Los commits deben ser descriptivos y representar cambios específicos.

### Ejemplos de commits

```text
Crear estructura inicial del repositorio
Agregar dataset original de gimnasios
Crear notebook inicial de Fase 1
Actualizar README del proyecto
Agregar archivo de dependencias iniciales
Agregar mapa conceptual técnico
Agregar workflow de CI para Fase 1
Ejecutar notebook en CI
Corregir kernel de ejecucion del notebook en CI
Agregar resumen automatico de PR con GitHub Models
Agregar informe tecnico de Fase 1
Documentar Wiki del proyecto
Agregar notebook de limpieza y transformacion Fase 2
Actualizar CI para validar Fase 2
Actualizar README con documentacion de Fase 2
```

---

## Estrategia de ramas

La rama `main` se mantiene como la versión estable del proyecto. Los cambios se trabajan primero en ramas secundarias tipo `feature/`, luego se validan mediante GitHub Actions y finalmente se integran a `main` mediante Pull Request.

### Rama principal

| Rama | Uso |
|---|---|
| `main` | Contiene la versión estable del proyecto. Solo debe recibir cambios revisados y validados. |

### Ramas implementadas

| Rama | Propósito | Archivos o carpetas asociadas |
|---|---|---|
| `feature/actualizar-notebook-f1` | Actualizar y mejorar el notebook principal de la Fase 1. | `notebooks/F1_Definicion.ipynb`, `notebooks/F1_Definicion_v2.ipynb` |
| `feature/actualizar-readme` | Mejorar la documentación principal del repositorio. | `README.md` |
| `feature/documentacion-fase1` | Incorporar documentos, evidencias, anexos y material de apoyo de la Fase 1. | `docs/`, `reports/fase1/` |
| `feature/ci-cd` | Ajustar y probar la configuración de integración continua. | `.github/workflows/main.yml` |
| `feature/dataset-validacion` | Revisar la ubicación, estructura y validación inicial del dataset. | `data/`, `data/raw/clean_gym_data.csv` |
| `feature/github-models-pr-summary` | Implementar resumen automático de Pull Requests con GitHub Models. | `.github/workflows/ai-pr-summary.yml` |
| `feature/fase2-limpieza-transformacion` | Implementar el notebook, pipeline, validaciones y documentación de Fase 2. | `notebooks/F2_Limpieza_Transformacion.ipynb`, `data/processed/`, `reports/fase2/` |
| `feature/fase3-algoritmos-poo` | Implementar algoritmos, mediciones, núcleo POO y documentación de Fase 3. | `src/fase3/`, `reports/fase3/`, `requirements_f3.txt` |
| `feature/fase4-integracion-visualizaciones` | Implementar integración final, visualizaciones, resultados, conclusiones y documentación Fase 4. | `src/fase4/`, `reports/fase4/`, `docs/fase4/`, `requirements_f4.txt`, `CHANGELOG.md` |

### Flujo de trabajo con ramas

```text
main
│
├── feature/actualizar-notebook-f1
├── feature/actualizar-readme
├── feature/documentacion-fase1
├── feature/ci-cd
├── feature/dataset-validacion
├── feature/github-models-pr-summary
└── feature/fase2-limpieza-transformacion
```

Procedimiento recomendado:

1. Actualizar `main`.
2. Crear una rama `feature/` según el tipo de cambio.
3. Realizar modificaciones.
4. Hacer commit con mensaje descriptivo.
5. Hacer push de la rama.
6. Crear Pull Request hacia `main`.
7. Esperar validaciones de GitHub Actions.
8. Revisar el resumen automático generado por GitHub Models.
9. Integrar a `main` solo si las validaciones pasan.

---

## CI/CD con GitHub Actions

Se implementó un workflow de integración continua mediante GitHub Actions, ubicado en:

```text
.github/workflows/main.yml
```

Nombre del workflow:

```text
CI - Validacion Fases 1 y 2
```

El workflow se ejecuta automáticamente en:

- Push a `main`.
- Push a ramas `feature/**`.
- Pull Requests hacia `main`.

### Validaciones realizadas

El workflow principal realiza las siguientes comprobaciones:

- Descarga el repositorio.
- Muestra la estructura inicial del proyecto.
- Configura Python 3.11.
- Instala las dependencias desde `requirements.txt`.
- Verifica la existencia de `README.md`.
- Verifica la existencia de `requirements.txt`.
- Verifica la existencia de `data/raw/clean_gym_data.csv`.
- Verifica la existencia de `notebooks/F1_Definicion.ipynb`.
- Verifica la existencia de `notebooks/F1_Definicion_v2.ipynb`.
- Verifica la existencia de `notebooks/F2_Limpieza_Transformacion.ipynb`.
- Verifica la existencia de carpetas principales.
- Carga el dataset original mediante Pandas.
- Verifica que el dataset original tenga filas y columnas.
- Valida la presencia de las columnas principales esperadas.
- Ejecuta el notebook `F1_Definicion_v2.ipynb` mediante `nbconvert`.
- Ejecuta el notebook `F2_Limpieza_Transformacion.ipynb` mediante `nbconvert`.
- Verifica la generación de `data/processed/gym_data_processed.csv`.
- Carga el dataset procesado mediante Pandas.
- Verifica que el dataset procesado tenga filas y columnas.
- Valida la presencia de columnas derivadas creadas en Fase 2.

### Columnas principales validadas

```text
country
region
year
gym_memberships
fitness_participation_rate
total_health_club_revenue_usd
number_of_gyms
gym_penetration_rate
urban_population_percentage
obesity_rate
gdp_per_capita_usd
population_total
average_membership_cost_usd
insufficient_physical_activity_pct
```

### Columnas derivadas validadas en Fase 2

```text
memberships_per_100k
gyms_per_100k
revenue_per_membership_usd
periodo
```

### Evidencia CI/CD

| Elemento | Detalle |
|---|---|
| Workflow | CI - Validacion Fases 1 y 2 |
| Job | validar-proyecto |
| Archivo | `.github/workflows/main.yml` |
| Eventos | push a `main`, push a ramas `feature/**` y Pull Requests hacia `main` |
| Estado esperado | exitoso |

---

## Resumen automático de Pull Requests con GitHub Models

Además del workflow principal de CI/CD, se implementó un workflow complementario basado en GitHub Models para apoyar la documentación automática de los cambios realizados mediante Pull Requests.

El workflow se encuentra en:

```text
.github/workflows/ai-pr-summary.yml
```

Nombre del workflow:

```text
AI - Resumen de Pull Request
```

### Funcionamiento general

```text
Pull Request hacia main
        ↓
GitHub Actions ejecuta AI - Resumen de Pull Request
        ↓
Se identifican los archivos modificados
        ↓
Se clasifica el tipo de cambio
        ↓
GitHub Models genera un resumen técnico automático
        ↓
El resumen se publica como comentario en el Pull Request
        ↓
El resumen también se guarda como artifact descargable
```

### Qué analiza el workflow

| Tipo de cambio | Archivos o carpetas relacionadas |
|---|---|
| Notebook | `notebooks/` |
| Documentación | `README.md` |
| Dataset | `data/` |
| CI/CD | `.github/workflows/` |
| Documentación técnica | `docs/` |
| Informe o evidencias | `reports/` |

### Contenido del resumen generado

El resumen automático generado por GitHub Models incluye:

- Tipo de cambio detectado.
- Archivos modificados.
- Impacto técnico del cambio.
- Relación del cambio con la fase correspondiente del proyecto.
- Riesgos o puntos de atención.
- Validaciones recomendadas.
- Observación final.
- Checklist automático de revisión.

### Dónde se puede ver el resumen

| Ubicación | Descripción |
|---|---|
| Comentario en el Pull Request | El workflow publica o actualiza automáticamente un comentario dentro del Pull Request. |
| Logs de GitHub Actions | El resumen se imprime en el paso `Mostrar resumen en logs`. |
| Artifact descargable | El archivo `resumen_ai.md` se guarda como artifact bajo el nombre `resumen-ai-pr`. |

---

## Wiki del proyecto

Además del README, el proyecto cuenta con una Wiki técnica para documentar de forma más detallada las decisiones metodológicas y técnicas del flujo reproducible.

Páginas implementadas o sugeridas:

- `Home`
- `Contexto del proyecto`
- `Dataset y variables`
- `Flujo reproducible`
- `Estructura del repositorio`
- `Notebook Fase 1`
- `Notebook Fase 2`
- `Control de versiones y ramas`
- `CI/CD con GitHub Actions`
- `GitHub Models`
- `Evidencias y anexos`
- `Riesgos, limitaciones y decisiones técnicas`
- `Referencias`

La Wiki permite profundizar en aspectos que en el README se presentan de forma resumida, tales como criterios de limpieza, justificación de herramientas, trazabilidad del dataset, funcionamiento del CI/CD, pipeline de datos y gestión de evidencias.

---

## Criterios iniciales de revisión del dataset

Durante la exploración inicial se revisarán:

- Posible presencia de datos estimados o modelados para años recientes.
- Diferencias en la calidad de datos entre países.
- Variables económicas o de salud pública provenientes de distintas fuentes.
- Posibles valores atípicos asociados al periodo COVID-19.
- Comparaciones afectadas por diferencias demográficas entre países.
- Riesgo de interpretar correlaciones como causalidad.
- Posibles registros incompletos o inconsistentes.
- Diferencias de escala entre variables como población, ingresos, membresías y cantidad de gimnasios.

Estos riesgos serán abordados mediante exploración inicial, documentación de decisiones, limpieza reproducible, transformación de variables y validaciones técnicas.

---

## Criterios de limpieza y transformación

Durante la Fase 2, la limpieza y transformación del dataset considera:

- No modificar directamente el archivo original ubicado en `data/raw/`.
- Guardar versiones procesadas en `data/processed/`.
- Documentar cada transformación aplicada en el notebook.
- Justificar cualquier eliminación de filas o columnas.
- Revisar valores nulos antes de imputar o excluir.
- Identificar valores atípicos antes de decidir su tratamiento.
- Validar rangos razonables de variables numéricas.
- Revisar consistencia temporal por país y año.
- Mantener trazabilidad entre dataset original y dataset procesado.
- Crear variables derivadas para mejorar la comparabilidad entre países.
- Normalizar variables seleccionadas sin reemplazar las variables originales.

---

## Riesgos y limitaciones iniciales

El dataset y el proceso de análisis pueden presentar desafíos metodológicos que serán considerados en fases posteriores:

- Posible presencia de datos estimados o modelados para años recientes.
- Diferencias en la calidad de datos entre países.
- Variables económicas o de salud pública provenientes de distintas fuentes.
- Posibles valores atípicos asociados al periodo COVID-19.
- Comparaciones afectadas por diferencias demográficas entre países.
- Riesgo de interpretar correlaciones como causalidad.
- Posibles registros incompletos o inconsistentes.

Estos riesgos serán abordados mediante exploración inicial, documentación de decisiones, limpieza reproducible y validaciones técnicas.

---

## Evidencias y anexos

Las evidencias del proyecto deben organizarse preferentemente en:

```text
reports/fase1/evidencias/
reports/fase2/evidencias/
```

Evidencias recomendadas para Fase 1:

| Evidencia | Descripción |
|---|---|
| Mapa conceptual | Evidencia visual del flujo reproducible planificado. |
| Repositorio GitHub | Captura de estructura del repositorio. |
| README actualizado | Evidencia de documentación principal. |
| Notebook ejecutado | Evidencia de carga y exploración inicial. |
| GitHub Actions exitoso | Evidencia de validación automática. |
| Ejecución del notebook en CI | Evidencia del paso `Ejecutar notebook Fase 1`. |
| Pull Requests | Evidencia del proceso de revisión. |
| GitHub Models | Evidencia del resumen automático generado. |
| Historial de commits | Evidencia de trazabilidad. |
| Ramas `feature/` | Evidencia de estrategia colaborativa. |

Evidencias recomendadas para Fase 2:

| Evidencia | Descripción |
|---|---|
| Notebook Fase 2 ejecutado | Evidencia de obtención, limpieza y transformación del dataset. |
| Diagnóstico inicial | Evidencia de tipos de datos, nulos, duplicados y columnas esperadas. |
| Pipeline de limpieza | Evidencia de funciones y transformaciones aplicadas. |
| Dataset procesado | Evidencia de generación de `data/processed/gym_data_processed.csv`. |
| Variables derivadas | Evidencia de creación de métricas por 100.000 habitantes y periodo temporal. |
| Validaciones finales | Evidencia de dataset procesado no vacío, sin duplicados y con columnas derivadas. |
| GitHub Actions Fase 2 | Evidencia de ejecución automática del notebook F2. |
| Pull Request Fase 2 | Evidencia del proceso de integración a `main`. |
| GitHub Models | Evidencia del resumen automático del Pull Request de Fase 2. |

---

### Evidencias recomendadas para Fase 3

| Evidencia | Descripción |
|---|---|
| `01_preprocesamiento_validado.png` | Evidencia del pipeline de preprocesamiento y validación final. |
| `02_algoritmos_ejecutados.png` | Evidencia de algoritmos estructurados y recursivos. |
| `03_pruebas_casos_limite.png` | Evidencia de validaciones normales, límite y excepciones. |
| `04_tabla_mediciones.png` | Evidencia de mediciones de tiempo y memoria. |
| `grafico_tiempo_algoritmos.png` | Figura comparativa de tiempo promedio. |
| `grafico_memoria_algoritmos.png` | Figura comparativa de memoria pico. |
| `05_nucleo_poo.png` | Evidencia de clases, herencia, polimorfismo y encapsulamiento. |
| `06_integrador_resultados.png` | Evidencia de integración de resultados F3. |

### Evidencias recomendadas para Fase 4

| Evidencia | Descripción |
|---|---|
| `01_f4_integracion_dataset.png` | Evidencia de integración F1-F4 y carga del dataset procesado. |
| `02_f4_visualizacion_1.png` | Evidencia de evolución anual de membresías. |
| `03_f4_visualizacion_2.png` | Evidencia de penetración promedio por región. |
| `04_f4_visualizacion_3.png` | Evidencia de relación PIB per cápita y participación fitness. |
| `05_f4_visualizacion_4.png` | Evidencia de comparación por periodo. |
| `06_f4_resultados_conclusiones.png` | Evidencia de hallazgos, limitaciones, riesgos y conclusiones. |
| `07_readme_actualizado.png` | Evidencia del README final. |
| `08_changelog.png` | Evidencia de trazabilidad de mejoras. |
| `09_commits_f4.png` | Evidencia de commits de Fase 4. |
| `10_presentacion_canvas.png` | Evidencia de presentación audiovisual en Canvas Studio. |

---

## Vinculación con el mapa conceptual

El mapa conceptual permitió planificar la relación entre problemática, dataset, herramientas científicas, flujo reproducible, documentación técnica y control de versiones.

En esta Fase 1 se materializan los siguientes componentes del mapa:

- Definición de la problemática del proyecto.
- Formulación del objetivo general y objetivos específicos.
- Identificación del dataset y variables principales.
- Organización inicial del repositorio.
- Creación del notebook `F1_Definicion.ipynb`.
- Documentación inicial mediante `README.md`.
- Documentación ampliada mediante Wiki.
- Registro de dependencias en `requirements.txt`.
- Uso de Git/GitHub para trazabilidad.
- Implementación de validación automática mediante GitHub Actions.
- Ejecución automática del notebook mediante `nbconvert`.
- Organización de ramas de trabajo.
- Implementación de resumen automático de Pull Requests mediante GitHub Models.

En la Fase 2 se materializan los siguientes componentes:

- Obtención y carga reproducible del dataset.
- Limpieza y estandarización de datos.
- Tratamiento de duplicados y valores nulos.
- Transformación de variables.
- Creación de variables derivadas.
- Normalización de variables seleccionadas.
- Validación del dataset procesado.
- Exportación de datos procesados.
- Trazabilidad entre datos originales y datos transformados.
- Validación automática del notebook de Fase 2 mediante CI/CD.

Quedan proyectados para fases posteriores:

- Análisis exploratorio más profundo.
- Visualizaciones comparativas entre países y regiones.
- Análisis del periodo pre y post COVID-19.
- Interpretación de resultados.
- Posible modelación predictiva de la tasa de penetración de gimnasios.

---

## Articulación con fases F1-F4

| Fase | Propósito | Evidencia principal |
|---|---|---|
| F1 | Definir problemática, organizar entorno reproducible, crear notebook inicial y documentar decisiones técnicas. | `notebooks/F1_Definicion.ipynb`, `notebooks/F1_Definicion_v2.ipynb`, README, CI/CD. |
| F2 | Realizar obtención, limpieza, depuración, transformación, validación y exportación del dataset procesado. | `notebooks/F2_Limpieza_Transformacion.ipynb`, `data/processed/gym_data_processed.csv`. |
| F3 | Implementar soluciones algorítmicas eficientes, mediciones de complejidad y Programación Orientada a Objetos. | `src/fase3/`, `reports/fase3/figures/`, `reports/fase3/evidencias/`. |
| F4 | Integrar resultados, construir visualizaciones finales, discutir hallazgos y preparar informe/presentación final. | `src/fase4/`, `reports/fase4/figures/`, `docs/fase4/`. |

---

## Estado del proyecto

**Fase actual:** Fase 4 - Proyecto final ABP.

El proyecto cuenta con una base reproducible de Fase 1, un pipeline de limpieza y transformación de Fase 2, un núcleo algorítmico y POO de Fase 3, y notebooks de Fase 4 orientados a integración final, visualizaciones, resultados, conclusiones e insumos para la presentación audiovisual.

La entrega final consolida informe técnico, notebooks ejecutables, repositorio reproducible, visualizaciones finales, evidencias, changelog y presentación audiovisual.

---

## Documentación final Fase 4

La Fase 4 incorpora documentación de apoyo ubicada en:

```text
docs/fase4/
```

| Archivo | Propósito |
|---|---|
| `informe_f4_estructura.md` | Propone la estructura del informe final en máximo 10 páginas. |
| `guion_presentacion_f4.md` | Entrega un guion base para la presentación audiovisual en Canvas Studio. |
| `checklist_f4.md` | Lista de verificación para informe, notebooks, repositorio y presentación. |

Además, el archivo `CHANGELOG.md` registra las mejoras aplicadas entre F1 y F4, permitiendo demostrar trazabilidad técnica, decisiones de optimización y evolución del proyecto.

---

## Referencias iniciales

Mishra, A. (2026). *World Gym & Fitness Trends 2000-2026* [Conjunto de datos]. Kaggle.

pandas development team. (2024). *pandas documentation*. https://pandas.pydata.org/docs/

Python Software Foundation. (2024). *Python documentation*. https://docs.python.org/3/

Project Jupyter. (2024). *Jupyter documentation*. https://docs.jupyter.org/

GitHub Docs. (2024). *GitHub Docs*. https://docs.github.com/

GitHub Docs. (2024). *GitHub Actions documentation*. https://docs.github.com/actions

GitHub Docs. (2024). *GitHub Models documentation*. https://docs.github.com/github-models

McKinney, W. (2022). *Python for Data Analysis: Data Wrangling with pandas, NumPy, and Jupyter* (3rd ed.). O'Reilly Media.

Makridakis, S., Spiliotis, E., & Assimakopoulos, V. (2018). Statistical and machine learning forecasting methods: Concerns and ways forward. *PLoS ONE, 13*(3), e0194889. https://doi.org/10.1371/journal.pone.0194889